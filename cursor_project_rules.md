## Project Overview

*   **Type:** cursor_project_rules
*   **Description:** An interactive web application featuring dynamic white string animations on a black background with a mouse-controlled force field and an adjustable control panel for real-time customization.
*   **Primary Goal:** Deliver a visually engaging and interactive experience where users can instantly adjust animation parameters such as field radius, field strength, string count, and reset speed, all while ensuring smooth, real-time performance on the Chrome browser.

## Project Structure

### Framework-Specific Routing

*   **Directory Rules:**

    *   **Next.js 14:** Enforce the App Router structure using the `app/` directory. Each main route such as the landing page, animation screen, and control panel uses nested folders following the `app/[route]/page.tsx` convention.

### Core Directories

*   **Versioned Structure:**

    *   **app/animation:** Contains components and pages responsible for rendering the interactive string animation.
    *   **app/control-panel:** Houses the modern control panel featuring sliders for real-time customization of animation properties.

### Key Files

*   **Stack-Versioned Patterns:**

    *   **app/layout.tsx:** Next.js 14 root layout for wrapping all pages and managing global providers.
    *   **app/page.tsx:** The landing page that introduces the interactive animation with default settings.
    *   **app/animation/page.tsx:** Implements the main interactive animation, handling real-time physics-based string movements.
    *   **app/control-panel/page.tsx:** Hosts the control panel responsible for updating animation parameters instantly.

## Tech Stack Rules

*   **Version Enforcement:**

    *   **next@14:** App Router is mandatory; avoid using legacy getInitialProps methods.
    *   **typescript:** Utilize strict typing and interfaces to maintain robust code quality.
    *   **tailwindcss:** Leverage utility-first classes for rapid style development and ensure purge settings are configured for production.
    *   **shadcn:** Adopt component-based design following the shadcn guidelines for consistency and modularity.

## PRD Compliance

*   **Non-Negotiable:**

    *   "Real-time responsiveness: adjustments made through the control panel update the animation immediately." This is a direct mandate to ensure that any customization instantly reflects in the animation, particularly on the Chrome browser.

## App Flow Integration

*   **Stack-Aligned Flow:**

    *   Next.js 14 Animation Flow → `app/animation/page.tsx` uses client-side interactions to deliver smooth, physics-inspired animations.
    *   Control Panel Integration → `app/control-panel/page.tsx` immediately communicates with the animation components to update the visual effects based on user input.

## Best Practices

*   **Next.js 14**

    *   Use file-based routing exclusively in the `app/` directory.
    *   Separate server and client components appropriately to enhance performance.
    *   Optimize image and asset delivery using Next.js built-in tools.

*   **TypeScript**

    *   Enforce strict typing and avoid using any implicit `any` types.
    *   Use interfaces and type definitions extensively for component props and state.
    *   Utilize TypeScript's latest features to improve code maintainability.

*   **Tailwind CSS**

    *   Leverage utility classes for rapid prototyping and responsive design.
    *   Configure PurgeCSS to remove unused styles in production builds.
    *   Use Tailwind’s customization features to maintain a consistent design system.

*   **shadcn**

    *   Follow the shadcn component guidelines to ensure design consistency across UI elements.
    *   Keep components modular and reusable.
    *   Integrate shadcn components with Tailwind CSS for rapid styling changes.

## Rules

*   Derive folder/file patterns **directly** from `techStackDoc` versions.
*   If Next.js 14 App Router: Enforce `app/` directory with nested route folders.
*   Never mix version patterns (e.g., no `pages/` in App Router projects).
