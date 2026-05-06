## 2024-11-20 - Destructive Action Feedback
**Learning:** Implementing double-press confirmation for destructive actions (like clearing progress) prevents accidental data loss without adding cumbersome modal dialogs, which is a great pattern for keyboard-centric TUIs like Textual.
**Action:** Use time-deltas on consecutive keypresses for confirmations in keyboard-driven interfaces.
