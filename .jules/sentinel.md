## 2024-05-24 - Map GUI Coordinates to Arrays Safely
**Vulnerability:** Out-of-bounds indexing vulnerability when mapping GUI click coordinates to numpy array indices without explicit validation.
**Learning:** In Python/NumPy, negative array indices wrap around to the end of the structure rather than throwing an IndexError. GUI coordinates must be validated explicitly against calculated logical positions to prevent out-of-bounds `IndexError` exceptions and potential Denial of Service application crashes.
**Prevention:** Always explicitly validate that computed indices derived from GUI coordinates are within the expected bounds (e.g., >= 0 and < bounds) before accessing arrays or data structures.
