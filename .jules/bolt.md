## 2024-05-22 - [Vue List Rendering Performance]
**Learning:** Using array index as 'key' in v-for is a performance anti-pattern, especially when using 'unshift' for history loading, as it forces re-renders of all elements.
**Action:** Always use unique, stable IDs for keys in lists. Generate temporary IDs for local optimistic updates.
