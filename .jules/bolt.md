## 2026-01-28 - [Vue List Rendering Anti-pattern]
**Learning:** The chat interface was using array indices as keys in `v-for` loops while prepending historical messages with `unshift`. This causes unnecessary re-renders of the entire list.
**Action:** When working with lists that change order (especially prepending), always ensure items have stable unique IDs and use them as keys. For local items, generate temporary IDs.
