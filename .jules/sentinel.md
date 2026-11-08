## 2024-05-15 - Unbounded Logical Array Indexing DoS
**Vulnerability:** The application calculates `logical_position` indices directly from GUI click coordinates. When user clicks outside the intended active canvas region, Python `numpy` array access allows wrapping around using negative indices or throws out-of-bounds index exceptions, which results in silent logical corruption or crash respectively.
**Learning:** In Python, arrays are vulnerable to negative array indices wrapping around, whereas standard indexing checks can crash the application completely resulting in a Denial of Service.
**Prevention:** Always explicitly validate that computed logical grid indices map firmly within expected bounding box ranges `>= 0` and `< size` prior to using them to access multi-dimensional arrays.
