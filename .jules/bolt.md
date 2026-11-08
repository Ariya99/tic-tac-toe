## 2024-03-24 - Faster NumPy Boolean Evaluation
**Learning:** Checking for zeros in NumPy arrays using `np.where(arr == 0)` and checking the length of the result is significantly slower (by ~36% in a simple benchmark) than using the C-level `.all()` method (e.g., `arr.all()`), which evaluates if all elements evaluate to True (non-zero).
**Action:** Use `.all()` instead of `np.where()` or `np.any()` when checking if a NumPy array is fully populated (contains no zeros) to maximize performance.
