## 2026-10-19 - Clickable Tkinter Canvas Elements
**Learning:** Tkinter canvas elements, although interactive when bindings are applied, do not natively change the cursor on hover. This can lead to a lack of affordance for users.
**Action:** Always add `cursor='hand2'` when initializing interactive Tkinter elements like `Canvas` to provide visual feedback and improve user affordance.
