## 2024-05-18 - Faster Boolean Array Evaluation
**Learning:** In NumPy, finding elements with `np.where()` creates a new array allocation which is computationally expensive. When only checking if any/all elements meet a condition (such as checking for empty cells in a grid), leveraging C-level boolean evaluations like `(array != 0).all()` or `.any()` is significantly faster.
**Action:** Always prefer `.all()` or `.any()` directly on the boolean mask array over `len(np.where(condition)[0])` when the positions themselves are not required, especially for array bounds and state checks.
