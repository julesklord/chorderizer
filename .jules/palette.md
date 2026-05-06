## 2025-02-28 - [Add Tooltip and Click Action to EXPORT MIDI Button]
**Learning:** Found an accessibility and UX issue where the `EXPORT MIDI` button lacked a tooltip showing the available shortcut key. Furthermore, the action was unlinked to the button press event, creating confusion for users who interact with the mouse.
**Action:** Always verify that TUI buttons have an `on_button_pressed` handler tied to the expected action, and use tooltips to reinforce keyboard shortcuts.
