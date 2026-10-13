# Frontend Mentor - Recipe Page Solution

This is my solution to the [Recipe Page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm).

## Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Links](#links)
- [Built With](#built-with)
- [What I Learned](#what-i-learned)
- [Continued Learning](#continued-learning)

## Overview

A responsive recipe page built to closely match the provided design reference. The page includes a recipe introduction, preparation time, ingredients, step-by-step instructions, and nutritional information.

## Screenshots

![Recipe page screenshot - mobile](./screenshot1.png)

![Recipe page screenshot - desktop](./screenshot2.png)

## Links

- **Solution:** [GitHub Repository](https://github.com/promahmoud219/Recipe-Page)
- **Live Site:** [View the Recipe Page](https://promahmoud219.github.io/Recipe-Page/)
- **Challenge:** [Frontend Mentor - Recipe Page](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm)

## Built With

- Semantic HTML5
- CSS custom properties
- CSS Flexbox
- CSS media queries
- Responsive design principles
- Google Fonts: Young Serif and Outfit
- Git and GitHub

## What I Learned

### 1. CSS Selectors and Specificity

I learned how selectors such as element selectors, class selectors, ID selectors, and descendant combinators target elements differently.

For example, `.text-content h1` selects every `h1` descendant of an element with the `text-content` class. It does not require the `h1` itself to have a class.

I also learned that selector specificity affects how competing CSS rules are resolved. Using meaningful classes for reusable styling can make future overrides easier to manage.

### 2. CSS Custom Properties and Typography

I organized recurring colors and typography values using CSS custom properties.

I also explored using `rem` instead of `px` for typography. `rem` is relative to the root element's font size, while `px` represents a CSS pixel. The appropriate unit depends on the required behavior, precision, and accessibility considerations.

### 3. HTML Lists and the `::marker` Pseudo-Element

I learned how to style list markers independently from list text using `::marker`.

I used separate selectors for unordered-list bullets and ordered-list numbers so that their colors and supported text properties could be customized independently.

I also learned that browser support for marker styling is limited to a subset of CSS properties, so not every font or spacing property works on `::marker`.

### 4. Preserving Native List Behavior

I initially applied `display: flex` to every `li` element to experiment with spacing.

This changed the list item's display behavior from `list-item` to `flex`, affecting the browser's default marker rendering and the position of list markers.

Removing `display: flex` from `li` restored the native list behavior. I learned to apply `gap` to the list container when I need consistent vertical spacing between list items, rather than changing the display behavior of every item unnecessarily.

### 5. HTML Tables and Row Headers

I learned the semantic difference between `th` and `td`:

- `th` represents a table header cell.
- `td` represents a data cell.

In the nutrition table, each nutrient name describes the data in the same row. I used `scope="row"` to explicitly identify each `th` as a row header.

I also reviewed the roles of `caption`, `thead`, `tbody`, and `tfoot` in structuring tables.

### 6. Inspecting the DOM in DevTools

I discovered that the browser can automatically insert a `tbody` element into the DOM when parsing table markup that omits it.

Inspecting the DOM helped me understand the structure created by the browser and identify elements that I could target with CSS. I also learned the difference between the HTML source and the parsed DOM.

### 7. Table Borders

I experimented with applying borders to table rows and cells.

Applying borders to individual cells can produce separate borders or unexpected results depending on the table's border model. I learned how `border-collapse: collapse` affects adjacent cell borders and how to target rows with selectors such as `tr:not(:last-child)` when styling row separators.

### 8. Horizontal Rules

I used the `hr` element to represent thematic breaks between sections and styled it using CSS borders.

I learned that the HTML element's purpose, its dimensions, and its border styling are separate concerns. A rule can be styled with properties such as `width`, `height`, and `border-top`, but the computed dimensions and borders should be inspected when troubleshooting unexpected rendering.

### 9. Responsive Design

I used a media query to change the page layout for wider viewports.

I learned that responsive design requires more than adding a breakpoint: container widths, spacing, images, and layout behavior must all be considered across viewport sizes.

## Continued Learning

This project helped me identify areas for further practice:

- Accessibility and semantic HTML.
- Fine-grained control of list marker positioning and spacing.    very important
- Responsive typography and layout.
- Table accessibility and header relationships.
- Reducing unnecessary CSS overrides and improving selector maintainability.

## Author

GitHub: [@promahmoud219](https://github.com/promahmoud219)

