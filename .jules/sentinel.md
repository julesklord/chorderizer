## 2025-05-05 - Fix path traversal via symlink bypass
**Vulnerability:** Path traversal vulnerability in `_sanitize_path` (`src/chorderizer/chorderizer.py`) that could be bypassed using symbolic links.
**Learning:** `os.path.abspath` does not resolve symbolic links, allowing paths to pass string-based directory boundary checks (like `startswith`) if an attacker provides a path containing a symlink that points outside the allowed directory.
**Prevention:** Always use `os.path.realpath` to fully resolve paths (including symlinks) before performing security checks, and prefer `os.path.commonpath` over simple string prefix matching to verify that a path resides strictly within an expected base directory.
