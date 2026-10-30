## 2026-10-30 - Faster empty cell checking in NumPy arrays
**Learning:** Checking for zeros in NumPy arrays using `np.where()` is significantly slower than using `.all()`. C-level boolean evaluation in `.all()` performs better than building index arrays.
**Action:** When checking for empty cells (zeros) in NumPy arrays, prefer using `.all()` over `np.where()` or `np.any()`.
