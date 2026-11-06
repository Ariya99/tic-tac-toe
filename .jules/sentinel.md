## 2024-05-18 - Prevent Out-of-bounds Array Access in Click Handler
**Vulnerability:** GUI click events (coordinates mapped to logic) were not bounds-checked before indexing the `board_status` NumPy array. An out-of-bounds click could lead to an IndexError or negative wrapping access, potentially causing a Denial of Service.
**Learning:** GUI framework event inputs must be strictly validated at the boundaries before being used to index data structures, especially when negative indices in Python/NumPy are treated as valid wrap-around indexing rather than an exception.
**Prevention:** Always validate that logically converted coordinates are `>= 0` and `< array_dimension` before indexing.
