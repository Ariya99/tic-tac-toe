## 2024-05-18 - Out-of-bounds Array Access
**Vulnerability:** The GUI click handler does not validate coordinates mapped to the internal NumPy array, allowing negative and out-of-bounds indices.
**Learning:** Python lists and NumPy arrays allow negative indexing which wraps around, masking logical errors. Extreme coordinates cause IndexError crashes (Denial of Service).
**Prevention:** Always validate GUI-derived coordinates against array boundaries (e.g., 0 <= index < size) before using them as array indices.
