## 2024-10-17 - Numpy `.all()` vs `np.where()` for checking zeros
**Learning:** Checking for zeros in a small 2D array using `np.where(array == 0)` and checking its length creates intermediate arrays and is significantly slower than using `bool(array.all())`, which delegates to C-level loops and short-circuits. In testing, this improved performance by ~1.6x.
**Action:** When checking if a NumPy array contains any zeros, prefer using `.all()` over `np.where()` or `np.any()` for C-level boolean evaluation.
