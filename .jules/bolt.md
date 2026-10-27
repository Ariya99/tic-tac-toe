## 2024-05-24 - Numpy array zero-check optimization
**Learning:** Checking for zeros in a small 3x3 Numpy array using `np.where(board_status == 0)` is ~30% slower than using the C-level boolean evaluation `board_status.all()`.
**Action:** When checking if a numpy array contains any zeros (empty cells in this case), prefer using `.all()` over `np.where()` for better performance.
