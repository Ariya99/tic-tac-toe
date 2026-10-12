## 2024-05-18 - Init
**Learning:** Initialized Bolt journal.
**Action:** Ready to document critical learnings.
## 2024-05-18 - Numpy Chained Indexing vs Tuple Indexing
**Learning:** Found that using chained indexing `arr[i][j]` with numpy arrays is significantly slower than tuple indexing `arr[i, j]` because chained indexing creates an intermediate array view before the second access. Also, `np.where(arr == 0)` allocates two new arrays to store indices, whereas `bool(arr.all())` is much faster when checking for the presence of 0s, provided 0 is the only falsy value.
**Action:** Always prefer tuple indexing for multidimensional numpy arrays and avoid `np.where` when a simple boolean check like `.all()` or `.any()` can suffice.
