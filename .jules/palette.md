## 2025-05-18 - Improve Tkinter Canvas Clickability Affordance
**Learning:** In Tkinter, `Canvas` elements do not visually indicate that they are interactive/clickable by default, unlike buttons. This can lead to poor affordance for mouse users.
**Action:** Always add `cursor='hand2'` during the initialization of playable Tkinter `Canvas` elements to change the mouse cursor and explicitly signal to users that the area is clickable.
