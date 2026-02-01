# Project Structure & Architecture

This document provides a technical overview of the most important files and components in the portfolio.

## 📁 Core Directory Map

### `src/components/`
The heart of the UI logic. Components are written in Astro and often have an English counterpart in `src/components/en/`.

- **[About.astro](file:///d:/Github/Portafolio/src/components/About.astro)**: 
  - **Purpose**: Manages the "About Me" section, personal bio, and skills categorization.
  - **Logic**: Uses a central `iconMap` to pull SVG icons from external CDNs (Simple Icons, Devicon, Skill Icons) based on skill names.
  - **Structure**: Divided into a bio grid (with personal photo), a contribution grid mockup, and a categorized skills grid.

- **[SkillSphere.astro](file:///d:/Github/Portafolio/src/components/SkillSphere.astro)**:
  - **Purpose**: High-performance 3D interactive tag cloud.
  - **Logic**: 
    - Implemented with Vanilla JavaScript and HTML5 Canvas.
    - Uses the **Fibonacci Sphere algorithm** to distribute points evenly.
    - Features mouse-tracking for dynamic rotation and depth-based opacities/scaling.

- **[Projects.astro](file:///d:/Github/Portafolio/src/components/Projects.astro)**:
  - **Purpose**: Displays the portfolio showcase using a grid of interactive cards.

### `src/layouts/`
- **[Layout.astro](file:///d:/Github/Portafolio/src/layouts/Layout.astro)**:
  - **Purpose**: The base HTML template.
  - **Features**: 
    - Comprehensive SEO metadata (Open Graph, Twitter Cards).
    - Google Fonts integration (Aldrich & Roboto Condensed).
    - Global background effects (CSS Grid & Blurred Glow).
    - Selection styling.

### `src/pages/`
- **index.astro**: Standard home page (Spanish).
- **en.astro**: English version of the landing page.
- **og.png.ts**: A specialized TypeScript endpoint that generates dynamic social images using the Astro/Satori integration.

## 🌍 Localization System
The project follows a directory-based localization strategy. For every component in `src/components/`, a translated twin exists in `src/components/en/`. The `en.astro` page orchestrates the English components, ensuring a cohesive and independent experience for English-speaking visitors.

## 🎨 Asset Management
- **[public/Img/](file:///d:/Github/Portafolio/public/Img/)**: Contains all project mockups and branding assets.
- **[public/Img/Foto.jpeg](file:///d:/Github/Portafolio/public/Img/Foto.jpeg)**: The main profile photo used across the "About" section.
- **[src/fonts/](file:///d:/Github/Portafolio/src/fonts/)**: Local high-performance font files.
