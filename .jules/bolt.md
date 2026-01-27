# BOLT'S JOURNAL - CRITICAL LEARNINGS ONLY

## 2026-01-27 - [Vue List Rendering Anti-pattern]
**Learning:** The chat implementation uses `unshift` to add historical messages. Using array index as `key` caused full list re-renders.
**Action:** Always check `v-for` keys in lists that are modified with `unshift` or sorted.
