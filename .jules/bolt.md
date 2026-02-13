## 2026-02-13 - Layout Thrashing in Resize Handlers
**Learning:** The codebase uses synchronous JavaScript to calculate accordion content height (`scrollHeight`) on every resize event. This causes layout thrashing as the browser recalculates layout repeatedly.
**Action:** Always debounce resize event listeners that perform DOM measurements or manipulations.
