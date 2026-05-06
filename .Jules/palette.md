
## 2024-05-18 - Discovering Accessibility Power in Textual TUIs
**Learning:** Textual TUI applications inherently lack standard web-like hover affordances for accessibility, making complex panels like the Chorderizer dashboard potentially difficult to parse for screen reader users or new users. However, we discovered that `tooltip` attributes are a powerful, universally supported prop across Textual interactive widgets (`Select`, `RadioSet`, `Button`, `DataTable`), providing vital contextual guidance.
**Action:** Always leverage `tooltip` attributes on interactive elements in TUI dashboard layouts to provide inline assistance, especially for domain-specific controls (like musical theory selections) where the UI layout must remain compact.

## 2026-05-05 - Double-Press Destructive Confirmations in TUIs
**Learning:** Terminal User Interfaces (TUIs) often lack modal dialogs common in web apps. When users hit shortcut keys (like `[X]` to clear a list), destructive actions can happen instantly without warning. Implementing a double-press pattern (with a 2-second timeout window) combined with a toast notification provides an elegant, non-blocking safety mechanism that feels natural in a keyboard-first terminal environment.
**Action:** Use a time-based double-press confirmation pattern (with `self.notify()` feedback) for destructive or significant actions in Textual TUIs instead of blocking the interface with modal popups.
