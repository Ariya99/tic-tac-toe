## 2024-05-15 - Optimize empty cell check in numpy arrays
**Learning:** Using `np.where(array == 0)` to check for empty cells in a numpy array is significantly slower than using `.all()`, which leverages faster C-level boolean evaluation.
**Action:** When checking if a numpy array contains any zeros (or empty values), prefer `.all()` or `.any()` over `np.where()` for better performance.
