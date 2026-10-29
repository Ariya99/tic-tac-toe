## 2025-02-24 - Logical Out-of-bounds Array Access (DoS)
**Vulnerability:** GUI coordinates from user clicks were converted to logical array indices without boundary validation. In Python, negative indices wrap around to the end of the array, and indices out of bounds cause an `IndexError`, which crashes the application (Denial of Service).
**Learning:** Always validate that logically calculated indices mapped from raw UI inputs fall explicitly within the dimensions of the target data structure.
**Prevention:** Add explicit boundary checks (e.g., `0 <= index < max_size`) before performing state updates on arrays based on external inputs.
