## 2026-01-26 - Vue List Rendering Performance
**Learning:** Using array index as `key` in `v-for` causes severe performance degradation when prepending items (like chat history) because Vue re-renders the entire list.
**Action:** Always verify that list items have stable unique IDs and use them as keys. For optimistic updates, generate a temporary unique ID.
