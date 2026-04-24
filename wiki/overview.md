---
title: Project Overview
updated: 2026-04-24
sources: [".agents/README.md", "index.html"]
source_commit: aae3c34
confidence: high
---

# Project Overview

This project is a high-end personal portfolio for **Ken Joela**, a Senior Developer from Estonia. It is designed to demonstrate both expert frontend engineering (via the portfolio itself) and modern AI-driven codebase maintenance (via the LLM Wiki pattern).

## Core Concepts

1. **The Portfolio**: A single-page, bilingual (EE/EN) web application built with Tailwind CSS, Lucide icons, and Inter typography. It uses a bento-grid layout to present professional experience, skills, and projects in a clean, modern aesthetic.
2. **The LLM Wiki**: An automated documentation layer located in the `wiki/` directory. It is maintained by AI agents using the conventions defined in `.agents/`.
3. **Graphify Integration**: The project is also integrated with the `graphify` tool to provide a navigable knowledge graph of the codebase structure and relationships.

## Tech Stack

- **Frontend**: HTML5, Tailwind CSS (via CDN), Vanilla JavaScript.
- **Iconography**: Lucide Icons.
- **Documentation**: Markdown, Mermaid.js (for diagrams).
- **Agent Tooling**: Antigravity (Skills, Workflows, Rules).

## Key Features

- **Bilingual Support**: Dynamic language switching between Estonian and English, including form placeholders.
- **Visual Excellence**: Bento-grid design, animated gradient headers, dot-grid background patterns, glassmorphism effects, and scroll-reveal animations.
- **Interactivity**: Mobile-friendly project galleries via GLightbox, smooth "Back to Top" navigation, and a functional contact form integrated with Web3Forms.
- **Living Wiki**: A documentation system that stays in sync with code changes via automated sync operations.
