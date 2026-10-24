## 2024-10-24 - Avoid micro-optimizing Tkinter cold paths
**Learning:** Optimizing a 3x3 NumPy array evaluation inside a human-triggered Tkinter click event is a micro-optimization with zero measurable impact, directly violating instructions against premature optimization of cold paths.
**Action:** Before optimizing any array operations, ensure they are part of a hot loop or high-frequency event handler. Leave user-triggered event handlers (like GUI clicks) alone unless they perform significantly slow computations, as native speed is more than enough for human reaction times.
