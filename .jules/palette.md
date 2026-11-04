## 2023-11-20 - Interactive Affordance in Tkinter Canvas
**Learning:** The Tkinter `Canvas` component does not have an implicit interactive state, so clickable areas visually look the same as unclickable ones.
**Action:** Use `cursor='hand2'` when initializing the `Canvas` to provide a cursor visual affordance for clickable areas and improve UX.
