## 2025-02-18 - Chat List Rendering Optimization
**Learning:** The chat interface used `unshift` to load history but used array indices as `v-for` keys. This forced Vue to re-render all message components whenever history was loaded. Standard `key` optimization was blocked because locally created user messages lacked unique IDs.
**Action:** Always ensure locally created optimistic UI updates (like new chat messages) generate a temporary unique ID so they can participate in stable keyed lists alongside server-provided items.
