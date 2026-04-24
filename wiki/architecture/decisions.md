---
title: Architectural Decisions
updated: 2026-04-24
source_commit: aae3c34
confidence: high
---

# Architectural Decisions (ADRs)

This page tracks significant design and technical decisions.

## ADR 1: Single-file Frontend
- **Status**: Accepted
- **Context**: The portfolio is a one-page site with relatively low complexity.
- **Decision**: Use a single `index.html` containing all HTML, CSS, and JS.
- **Consequences**: Easy deployment (GitHub Pages), fast loading (few requests), but can become harder to maintain if complexity grows significantly.

## ADR 2: Utility-First Styling (Tailwind CDN)
- **Status**: Accepted
- **Context**: Need for fast development and consistent design without a build step.
- **Decision**: Use Tailwind CSS via the runtime CDN.
- **Consequences**: No build step required; instant preview. Larger runtime payload compared to a compiled build, but acceptable for this scale.
