## 2024-05-18 - Faster empty cell checking in NumPy arrays
**Learning:** Using `np.where(array == 0)` to check for empty cells is computationally slower than using `.all()` (e.g., `(array != 0).all()`) due to C-level boolean evaluation efficiency.
**Action:** Prefer `.all()` over `np.where()` when checking for empty cells in NumPy arrays for faster C-level evaluation.
