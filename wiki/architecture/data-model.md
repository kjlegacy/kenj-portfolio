---
title: Data Model
updated: 2026-04-24
source_commit: b47b228
confidence: high
---

# Data Model

The project is currently stateless and does not use a persistent database.

## Client-Side Persistence

### LocalStorage
We use browser `localStorage` to persist user preferences across sessions.

| Key | Value | Purpose |
|---|---|---|
| `theme` | `dark` \| `light` | User's preferred color scheme. |
| `language` | `en` \| `ee` | User's preferred display language. |
