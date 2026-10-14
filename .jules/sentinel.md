## 2024-05-15 - Prevent Out-of-Bounds Indexing on Click Handler
**Vulnerability:** The application was vulnerable to state corruption or an IndexError crash (DoS risk) when users clicked out of bounds, because coordinate inputs were mapped to logical indices without validation.
**Learning:** Raw input coordinates must always be validated against boundary limits before being used as indices in multidimensional arrays like `board_status`.
**Prevention:** Implement validation checks (e.g., `0 <= x < width` and `0 <= y < height`) immediately after input parsing and before data structure access.
