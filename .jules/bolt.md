## 2024-10-16 - Fast Empty Cell Detection in NumPy
**Learning:** When checking for empty cells (zeros) in NumPy arrays, using `.all()` is significantly faster than using `np.where()` or `np.any()` due to C-level boolean evaluation.
**Action:** Always prefer `.all()` or `.any()` direct array methods over `np.where()` for simple boolean checks across the entire array in performance-critical code.
