---
name: durable-web-dev
description: Web development using web platform features and vanilla HTML, CSS, and JavaScript.
---

# Durable web development using the web platform

> Our plans are measured in centuries

Your goal is to build a web app that will stand the test of time by avoiding the use of external libraries, minimizing JavaScript, and maximizing the use web platform features.

## JavaScript

The app should be built with vanilla JavaScript.
Use modern JavaScript (ESM imports, await, fetch...). 
Do not use TypeScript, only JavaScript. 
You must add JSDoc.

### No build step

Do not use a build step.
When libraries are needed, install them in node_modules or use sdm.sh, and use import maps. 
The app be fully functionnal by just serving index.html using a basic static file service web server (like `npx serve` or `python3 -m http.server`).

### Frameworks and libraries

No Angular, no react, no Nextjs, no JS framework. 

Do not use any other library than what is strictly needed, for example a charting library, a mapping library, Three.js, or sql.js.

Optimize for using standard web APIs.
Avoid experimental APIs or APIs requiring a browser flag to be enabled.
Consider using web components and custom elements, but this isn't a hard requirement.

### Offline

If building an app, evaluate using a `manifest.json` and Service Workers to implement offline support by caching all of the app's files.

## UI elements

Work using HTML.
Minimize the use of JavaScript an prefer broswers' built-in APIs.
Prefer using native HTML elements rather than custom ones using JS.

For example:
- a dropdown should be a `<select>` menu
- a date picker should be a `<input type="date">`
- a file picker just a `<input type="file">`
- a expander should use `<summary>` and `<details>`

Use semantic HTML tags as much as possible, like `<main>`, `<nav>`, `<footer>`, `<header>`.
For user messages, use the dialog element, not `alert()`.

Use HTML templates to declare structure that is re-used accross the app.

Make sure the app is accessible, use ARIA labels and implement accessibility best practices.

## Styling

Use pure CSS, the way it was intended. No tailwind or shadcn/ui.
Use classes, no inline styles.
Pay attention to CSS class names (never use classes like "centered" but semantic names like "signup-form"), overall CSS cleanliness, and re-usability.
Use modern CSS features when possible, like CSS variables and color functions.

Add light and dark mode. Listen to system theme changes to change theme. 

The layout should work well on large screen, medium screen like tablet, and mobile screen.

Avoid pulling external fonts unless really necessary. 
