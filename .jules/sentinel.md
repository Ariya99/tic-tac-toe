## 2023-10-26 - GUI Coordinate to Array Index Mapping
**Vulnerability:** Out-of-bounds Array Access / Denial of Service.
**Learning:** In Python/NumPy, mapping GUI coordinates directly to array indices without bounds checking can cause out-of-bounds access (leading to Denial of Service via IndexError) or unexpected logical behavior via negative indexing (which wraps around).
**Prevention:** When mapping GUI coordinates (like Tkinter user click events) to numpy array indices, always explicitly validate the calculated logical positions against array boundaries (e.g. `0 <= index < size`) to prevent out-of-bounds IndexError exceptions and negative wrap-around access.
