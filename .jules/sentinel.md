## 2025-02-12 - Missing Input Validation in Tkinter Grid Clicks
**Vulnerability:** A Denial of Service (DoS) vulnerability existed in `click(self, event)` because pixel coordinates were mapped to logical array indices without bounds checking, causing an `IndexError` on out-of-bounds clicks.
**Learning:** In UI applications relying on custom coordinate-to-grid mappings, user-triggered events (like clicks) can produce logical positions outside the allocated array dimensions if the window boundaries or event bounds are manipulated.
**Prevention:** Always validate mapped indices (`0 <= x < BOUND`) before using them to access multi-dimensional state arrays.
