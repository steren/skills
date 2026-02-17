---
name: robust-web-dev
description: Web development using web platform features and vanilla HTML, CSS, and JavaScript.
---

# Web development using web platform features

> Our plans are measured in centuries

Your goal is to build a web app that will resist the test of time by avoiding the use of external libraries, minimizing JavaScript, and maximizing the use web platform features.

## Framework and libraries

The app should be built with vanilla JavaScript.
Do not use TypeScript, only JavaScript. 
Use modern JavaScript (ESM imports, await, fetch...). 
No Angular, no react, no Nextjs, no JS framework. 

Do not use any other library than what is strictly needed, for example a charting library, a mapping library, or a SQLite library.

Optimize for using standard web APIs that will survive the test of time.
Consider using web components and custom elements, but this isn't a hard requirement.

Prefer minimizing the use of JavaScript and instead use web platform features. 
Prefer using native HTML elements rather than custom ones using JS.  For example, a dropdown should be a `<select>` menu, same for date picker, just a `<input type="date">`, file picker, just a `<input type="file">`...  
Use semantic HTML tags as much as possible, like `<main>`, `<nav>`, `<footer>`, `<header>`.

## Styling

Use pure CSS, the way it was intended. No tailwind or shadcn/ui.
Use classes, no inline styles.
Pay attention to CSS class names (never use classes like "centered" but semantic names like "form-container"), overall CSS cleanliness, and re-usability.
Use modern CSS features when possible, like CSS variables and color functions.

## No build step

Do not use a build step.
When libraries are needed, install them in node_modules or use sdm.sh, and use import maps. 
The app be fully functionnal by just serving index.html using a basic static file service web server (like `npx serve` or `python3 -m http.server`).
