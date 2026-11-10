## 2023-11-10 - Logical Position Array Bounds Missing Validation
**Vulnerability:** The click handler in `first.py` does not validate if `logical_position` (calculated from raw UI coordinates) is within the bounds of `self.board_status` (a 3x3 NumPy array). Negative coordinates or out-of-bounds clicks cause an `IndexError` or logical out-of-bounds access.
**Learning:** Raw input coordinates must be verified before acting as index arrays, and negative indices in Python act as wrap-arounds, thus requiring an explicit `>= 0` check.
**Prevention:** Explicitly validate calculated array index boundaries against valid logical sizes before using them to access multi-dimensional arrays.
