# Project Report: Thiranex Accessible Portfolio

This report explains what this project is, what features it includes, and the key concepts learned during Step 1.

---

## 1. What is in the Project?

We built a **4-page personal portfolio website** (Home, About, Projects, and Contact) designed from the ground up to be beautiful, clean, and 100% accessible to everyone (including people using screen readers or keyboard-only navigation).

### Key Features:
*   **Theme Switcher (Dark & Light Mode):** A button that toggles between dark and light themes, remembering your preference.
*   **Accessible Navigation Menu:** A mobile menu that can be opened and closed easily using a keyboard or mouse, keeping focus locked inside the menu while open.
*   **Live Contact Form Validation:** Real-time form checks that immediately show error messages if you type something wrong or leave a required field empty.
*   **Skip-to-Content Link:** A hidden link that appears only when using the keyboard tab key, allowing screen reader users to skip past the header straight to the main page content.
*   **SVG Graphics:** Built-in vector graphics for layouts and page favicons so they load instantly and look sharp on any screen.

---

## 2. What Did I Learn?

Here are the core web design principles learned during this project:

### 🌟 Semantic HTML5 (Clean Structure)
Instead of using generic `<div>` tags for everything, we used meaningful HTML5 tags:
*   `<header>` and `<footer>` for the top branding and bottom copyright sections.
*   `<nav>` for lists of navigation links.
*   `<main>` for the core content area.
*   `<section>` and `<article>` to group related information.
*   *Why this matters:* It helps search engines find your site easily (SEO) and allows assistive technologies (like screen readers) to understand the structure of your page.

### 🌟 WCAG 2.1 Guidelines (Accessibility Standards)
We followed the official Web Content Accessibility Guidelines (WCAG) to ensure the site is fully inclusive:
*   **Color Contrast:** All colors maintain a high contrast ratio (at least 4.5:1 for normal text and 7:1 for headers) so people with low vision can read everything easily.
*   **Focus Indicator outlines:** Visible blue rings outline buttons and links when using keyboard navigation, making it clear where you are on the page.
*   **Motion Control:** Added media queries that stop animations automatically if the user has requested "Reduced Motion" in their computer system settings.

### 🌟 WAI-ARIA (Screen Reader Support)
We used ARIA attributes to tell screen readers what is happening on the page in real-time:
*   `aria-expanded`: Tells the screen reader if the mobile menu is open or closed.
*   `aria-pressed`: Tells the screen reader which project filter button is active.
*   `aria-describedby` & `aria-invalid`: Links input fields to their respective error messages, so screen reader users hear the error immediately.
*   `aria-live="polite"`: A custom live region that reads out announcements (like "Theme changed to Light mode") without interrupting the user.

### 🌟 Secure & Resilient JavaScript
*   We wrapped `localStorage` calls inside `try-catch` blocks.
*   *Why this matters:* Some browsers or sandbox environments block access to storage for security reasons. By wrapping them in try-catch blocks, we prevent the website's JavaScript from crashing, keeping the site functional.
