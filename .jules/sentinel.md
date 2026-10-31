## 2024-05-15 - Unvalidated GUI Click Mapping Causes DoS
**Vulnerability:** GUI coordinates mapping to array indices without bounds checking (e.g., in a `click` event handler).
**Learning:** Python array negative indexing and large coordinate clicks can cause silent logical errors or an out-of-bounds `IndexError`, which crashes the application (Denial of Service).
**Prevention:** Always validate that logically mapped index positions exist within the hard boundaries of the underlying data structures `(>= 0 and < MAX_LEN)` before data access.
