---
title: Portfolio Module
updated: 2026-04-23
sources: ["index.html"]
source_commit: eee1db3
confidence: high
---

# Portfolio Module

The Portfolio module is the primary user-facing component of the repository. It is contained within a single `index.html` file to maximize portability and performance for a one-page site.

## Architecture

The page is built using a **Bento Grid** layout, which organizes information into rectangular tiles of varying sizes. This approach provides a clean, modular aesthetic that works well across different screen sizes.

### Key Components

| Component | Description |
|---|---|
| **Hero Section** | Displays name, senior-level hooks in two languages, and background blobs. |
| **Services** | Highlights core offerings (Web, Mobile, Backend). |
| **Skills** | Categorized list of technical proficiencies. |
| **Projects** | Links to featured works (e.g., digitalforall.eu). |
| **Contact** | Call-to-action buttons and social links. |

## Features & Implementation

### 1. Bilingual Engine
The page uses a simple data-attribute-based system for translations.
- Text elements contain both `.lang-en` and `.lang-ee` spans.
- CSS hides the inactive language based on the `lang` attribute on the `<html>` element.
- JavaScript toggles the `lang` attribute and persists the choice in `localStorage`.

### 2. Theme Management (Dark Mode)
Tailwind's `dark` class strategy is used.
- A toggle button switches the `.dark` class on the `<html>` element.
- Theme preference is persisted in `localStorage`.
- Glassmorphism effects (`glass-panel` class) adjust their opacity and borders based on the theme.

### 3. Visual Polish
- **Animated Gradient Headers**: Section headers use a dynamic multi-color gradient (`gradient-text`) with a continuous shimmer animation.
- **Dot-Grid Background**: A subtle, high-end dot-grid pattern is applied to the background to enhance the technical aesthetic.
- **Glassmorphism**: Accomplished via `backdrop-filter: blur(12px)` and semi-transparent backgrounds.
- **Animations**: Custom Tailwind animations for floating background blobs (`animate-blob`) and section entry transitions (`animate-fade-in-up`).
- **Icons**: Dynamic SVG injection using Lucide Icons.

## Dependencies

- **Tailwind CSS**: Utility-first styling framework (via CDN).
- **Lucide Icons**: Open-source icon library.
- **Google Fonts (Inter)**: Modern sans-serif typography.
