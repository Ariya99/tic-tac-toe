## 2026-10-13 - Avoid NumPy arrays for small coordinate math
**Learning:** Using NumPy arrays for simple 2D coordinate transformations (like screen to logical grid) is an anti-pattern in Python. The overhead of instantiating `np.array()` and performing vectorized math on just 2 elements is ~8x slower than native Python tuple/list math.
**Action:** Use native Python tuples and basic arithmetic for small (e.g., length-2) coordinate math instead of NumPy arrays.
