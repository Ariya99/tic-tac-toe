## 2024-11-03 - NumPy Empty Cell Evaluation
**Learning:** Using `np.where` to find zeros in an array and then checking length for emptiness requires unnecessary array allocation.
**Action:** Prefer `.all()` when checking if a NumPy array is fully non-zero as it evaluates much faster using C-level boolean logic.
