## 2024-10-28 - Optimize Zero Check in NumPy Arrays
**Learning:** Using `np.where(array == 0)` to check for empty cells in NumPy arrays is slower than using `.all()`. C-level boolean evaluation in `.all()` performs significantly faster.
**Action:** When checking for empty cells (zeros) in NumPy arrays, prefer using `.all()` over `np.where()` or `np.any()` for better performance.
