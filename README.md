# REPORT LAB 02

This document breaks down three different HTML/CSS exercises, explaining the "What, Why, and How" for each.

## Exercise 2: Bootstrap Survey Form

### What is it?
This is an HTML file that creates a survey form. It includes text fields (First Name, Last Name, etc.), radio buttons (How did you hear about us?), checkboxes (Would you like to receive announcements?), and a dropdown menu (Please contact me by:).

### Why was it built this way?
This code uses the **Bootstrap** CSS framework. The "why" is to build a clean, responsive, and professionally styled form **without writing complex custom CSS**. Bootstrap provides pre-made classes for layout (like grids) and form styling, which saves a lot of time.

### How does it work?
1.  **Bootstrap CDN:** The file links to the Bootstrap CSS library via a CDN (Content Delivery Network) in the `<head>`:
    ```html
    <link rel="stylesheet" href="[https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css](https://cdn.jsdelivr.net/npm/bootstrap@4.6.2/dist/css/bootstrap.min.css)">
    ```
2.  **Bootstrap Grid System:** It uses `<div class="row">` and `<div class="col">` to automatically align the labels and input fields side-by-side in a two-column grid.
3.  **Bootstrap Form Classes:**
    * `.form-control` is applied to `<input>` tags to make them styled and full-width.
    * `.form-check-inline` and `.form-check-input` are used to style the radio buttons and lay them out horizontally.
    * `.form-check` is used for the stacked checkboxes.
4.  **Custom Styling:** A small `<style>` tag is used to add custom styles not covered by Bootstrap, like setting the logo width and changing the heading colors to `#1e9690`.

# HTML/CSS Code Explanations

This document breaks down two HTML/CSS exercises, explaining the "What, Why, and How" for each.

---

## Exercise 3: 3-Column Fixed-Width Layout

### What is it?
This code creates a classic 3-column webpage layout. It features a full-width header at the top, a full-width footer at the bottom, and a middle section composed of a left sidebar (`Sidebar A`), a main content area, and a right sidebar (`Sidebar B`).

### Why was it built this way?
This code demonstrates how to create a fundamental webpage structure using modern CSS **Flexbox**. The goal is to have two **fixed-width** sidebars (200px each) and a central content area that is **fluid**, meaning it stretches to fill whatever space is left.

### How does it work?
1.  **Outer Flex Container:** The main `.container` is a **vertical** flexbox (`display: flex`, `flex-direction: column`). This stacks its children (header, content-wrapper, footer) on top of each other.
2.  **Inner Flex Container:** The `.content-wrapper` is a **horizontal** flexbox (`display: flex`, `flex-direction: row`). This arranges its children (the three columns) side-by-side.
3.  **Fixed-Width Sidebars:**
    * `.sidebar-a` and `.sidebar-b` use `flex: 0 0 200px;`.
    * This is shorthand for: `flex-grow: 0` (don't grow), `flex-shrink: 0` (don't shrink), `flex-basis: 200px` (start at this width). This locks them at 200px.
4.  **Fluid Main Content:**
    * `.main-content` uses `flex: 1;`.
    * This is shorthand for `flex-grow: 1`. It tells this element to "grow" and fill all remaining empty space in the flex container.

# HTML/CSS Code Explanation: Exercise 4

This document breaks down the provided HTML/CSS code, explaining its purpose and implementation.

---

## Exercise 4: Responsive 2-Column Page

### What is it?
This is a complete, styled webpage for a fictional "San Joaquin Valley Town Hall" event. It features a header (with a logo and tagline), a two-column main body (a wide content area on the left and a narrower sidebar on the right), and a footer. Most importantly, it is **responsive**, meaning its layout automatically adapts to different screen sizes, like mobile phones.

### Why was it built this way?
This code demonstrates a practical and modern approach to web layout using **CSS Flexbox** and **responsive design principles**. The goals are twofold:
1.  **Desktop View:** To create a visually appealing, proportional 2-column layout where the main content is wider than the sidebar, making it easy to read.
2.  **Mobile View:** To ensure the site is usable on small screens by "stacking" the two columns into a single vertical column, preventing users from having to zoom or scroll horizontally.

### How does it work?
1.  **Flexbox for Layout:** The `.main-content` element is set to `display: flex`. This turns it into a flex container, allowing its direct children (`.left-column` and `.right-column`) to be arranged side-by-side.

2.  **Proportional Columns:**
    * The `.left-column` has `flex: 2;`.
    * The `.right-column` has `flex: 1;`.
    * This is the core of the layout. It divides the available horizontal space into 3 "parts" (2 + 1). The left column is given 2 parts (two-thirds of the width), and the right column is given 1 part (one-third of the width). This creates a proportional

