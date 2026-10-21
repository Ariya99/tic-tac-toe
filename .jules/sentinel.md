## 2023-10-24 - Tkinter Out-Of-Bounds Click DoS
**Vulnerability:** User click coordinates on the Tkinter canvas were being directly mapped to numpy array indices without bounds validation, allowing a malicious or errant out-of-bounds click to crash the application via an `IndexError`.
**Learning:** GUI frameworks don't natively restrict event coordinates strictly to the drawn boundaries, particularly with custom layouts. Mapping pixel inputs to logical grid coordinates requires explicit bounds checking.
**Prevention:** Always validate that logically mapped coordinates from user inputs fall within the acceptable bounds before using them as indices for state arrays or matrices.
