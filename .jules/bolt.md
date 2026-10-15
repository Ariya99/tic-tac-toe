## 2024-05-24 - NumPy Boolean Checks vs Array Operations
**Learning:** Using `.all()` on a numpy array is significantly (~30-40%) faster than using `np.where()` or array-wide boolean comparisons like `np.any(board == 0)` when checking if all elements in an array are non-zero.
**Action:** When checking if a numpy array contains any zeros (e.g., in grid completion checks like `is_tie`), prefer `.all()` over `np.where()` or `0 not in board` for better performance.
