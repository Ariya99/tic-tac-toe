## 2024-05-24 - NumPy Boolean Array Evaluation Speed
**Learning:** In NumPy, `.all()` is significantly faster than using `np.where()` or `np.any()` when evaluating boolean arrays, especially when checking for the presence of empty cells (zeros) on small grids like Tic-Tac-Toe.
**Action:** Use `.all()` over `np.where()` for faster C-level boolean evaluation when checking if all elements in a NumPy array meet a condition (e.g. non-zero).
