1. **Fix `os.makedirs` security issues:**
   - Modify `src/chorderizer/chorderizer.py`, `src/chorderizer/tui_app.py`, and `src/chorderizer/generators.py` to create the export directory with restrictive permissions (`mode=0o700`) to prevent unauthorized access to user's generated compositions.

2. **Pre-commit Steps:**
   - Follow instructions from `pre_commit_instructions` to ensure code passes linting, tests, and formatting checks.

3. **Submit Change:**
   - Commit and submit the code as a single PR.
