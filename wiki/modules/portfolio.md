---
title: Portfolio Module
updated: 2026-04-24
sources: ["index.html"]
source_commit: b47b228
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
| **Projects** | Links to featured works with expandable "See More" functionality and GLightbox galleries. |
| **Contact** | Bilingual contact form with Web3Forms integration and social links. |
| **Back to Top** | Floating button for smooth navigation to the hero section. |

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
- **Animated Nordic Headers**: Section headers use a sophisticated "Nordic Gray" (Slate) gradient with a subtle shimmer animation for improved readability and a premium feel.
- **Dot-Grid Background**: A subtle, high-end dot-grid pattern is applied to the background to enhance the technical aesthetic.
- **Glassmorphism**: Accomplished via `backdrop-filter: blur(12px)` and semi-transparent backgrounds.
- **Animations**: Custom Tailwind animations for floating background blobs (`animate-blob`), section entry transitions, and thumbnail hover interactions.
- **Scroll Reveal**: Uses a dedicated Intersection Observer-based system (`.reveal` class) for smooth entry animations as the user scrolls.
- **Icons**: Dynamic SVG injection using Lucide Icons.

### 4. Interactive Project Galleries
- **Expandable List**: Projects list initially shows 4 top items, with the rest hidden behind a "Vaata veel" (View More) button.
- **Image Lightbox**: Clicking a project thumbnail opens a mobile-friendly, swipeable image gallery using `GLightbox`.

### 5. Contact Form Integration
- **Web3Forms**: Handles form submissions without a backend server.
- **User Experience**: Includes loading states, success messages, and bilingual placeholder support.

## Dependencies

- **Tailwind CSS**: Utility-first styling framework (via CDN).
- **Lucide Icons**: Open-source icon library.
- **Google Fonts (Inter)**: Modern sans-serif typography.
- **GLightbox**: Lightweight, pure JavaScript lightbox plugin for project image galleries.
