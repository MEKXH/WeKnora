## 2026-01-30 - Chat List Performance
**Learning:** The chat interface (`frontend/src/views/chat/index.vue`) manages message history using `unshift`, but was using the array index as the `v-for` key. This caused full re-renders of the list whenever a message was added or history loaded, as all indices shifted.
**Action:** Always check `v-for` keys in list components, especially those with prepended items (history/chat logs). Ensure local optimistic UI updates generate temporary unique IDs to maintain key stability before backend confirmation.
