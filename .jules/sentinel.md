## 2026-05-04 - Insecure Directory Creation
**Vulnerability:** MIDI export directories were created with default permissions (`os.makedirs(..., exist_ok=True)`), which could allow other users on the system to access generated compositions.
**Learning:** Python's `os.makedirs` defaults to permissive modes, which can expose user data in shared environments.
**Prevention:** Always specify restrictive modes (e.g., `mode=0o700`) when creating directories intended to store private user data.
