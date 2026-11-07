---
name: web-development
description: Apply Fiascko's web development practices when writing, reviewing, or modifying web code, emphasizing vanilla technologies, simple architecture, reusable code, performance, accessibility, and security.
metadata:
  author: Fiascko
---

# Web Development

Apply these web-specific guidelines alongside `fiascko-philosophy` when working on web projects.

## Architecture

- Prefer simple, lightweight solutions using native web technologies.
- Prefer vanilla HTML, CSS, and JavaScript by default; introduce frameworks only when justified and approved.
- Use existing project technologies and frameworks when already established.
- Avoid unnecessary frameworks, libraries, build tools, and architectural layers.
- Keep frontend and backend responsibilities clearly separated when applicable.
- Reuse existing functions, modules, components, and utilities before creating new ones.
- Keep implementations proportional to actual project requirements.

## HTML

- Use semantic HTML elements and appropriate document structure.
- Prefer native HTML functionality over custom JavaScript implementations.
- Use accessible forms, labels, buttons, and navigation elements.
- Avoid unnecessary wrappers, attributes, and deeply nested structures.
- Maintain valid, readable, and consistent markup.
- Preserve existing element identifiers and JavaScript dependencies.

## CSS

- Prefer native CSS features over JavaScript-based styling solutions.
- Reuse existing classes, variables, and design patterns.
- Use CSS custom properties for shared colors, spacing, and other meaningful values.
- Avoid excessive specificity, unnecessary overrides, and duplicated declarations.
- Prefer simple, responsive layouts using Flexbox and Grid when appropriate.
- Avoid unnecessary animations, transitions, and expensive visual effects.
- Preserve existing responsive behavior and visual consistency.

## Design & Visual Consistency

- Respect the project's existing visual identity and design language.
- Reuse established colors, typography, spacing, components, and visual patterns.
- Keep layouts, animations, transitions, and interactions consistent across the project.
- Avoid generic AI-generated aesthetics, unnecessary gradients, excessive shadows, and decorative effects.
- Prefer intentional, simple, and cohesive designs over unnecessary visual complexity.
- Preserve existing design choices unless changes are explicitly requested.

## JavaScript

- Prefer modern vanilla JavaScript and built-in browser APIs.
- Use `const` by default and `let` when reassignment is necessary.
- Avoid unnecessary global variables and shared mutable state.
- Reuse existing functions and modules before introducing new abstractions.
- Prefer event-driven behavior over unnecessary polling.
- Cache frequently accessed DOM elements when beneficial.
- Avoid repeated DOM queries, unnecessary reflows, and redundant updates.
- Use `async`/`await` and handle asynchronous errors appropriately.
- Avoid unnecessary dependencies and browser compatibility polyfills.

## Performance

- Minimize unnecessary JavaScript execution and DOM manipulation.
- Avoid redundant network requests and excessive resource loading.
- Load scripts and assets efficiently using native browser capabilities.
- Optimize images, fonts, and other assets when appropriate.
- Avoid unnecessary animations and layout recalculations.
- Use browser caching and lazy loading when beneficial.
- Measure performance issues before introducing complex optimizations.

## Accessibility & Responsive Design

- Support keyboard navigation and visible focus states.
- Prefer semantic HTML over unnecessary ARIA attributes.
- Provide meaningful alternative text for informative images.
- Ensure sufficient contrast and readable text.
- Support different screen sizes without unnecessary device-specific implementations.
- Respect reduced-motion preferences when using significant animations.
- Avoid interactions that depend exclusively on hover.

## Security

- Validate untrusted input and use context-appropriate escaping, sanitization, or parameterized queries.
- Prevent injection vulnerabilities, including XSS and SQL injection when applicable.
- Prefer safe DOM APIs over inserting untrusted HTML.
- Avoid exposing secrets or sensitive information in client-side code.
- Use secure authentication, authorization, and session handling when applicable.
- Avoid unnecessary external scripts and third-party resources.
- Respect browser security policies and same-origin restrictions.

## Compatibility

- Respect the project's existing browser and platform requirements.
- Prefer widely supported web APIs when practical.
- Avoid introducing build steps or server requirements for static projects.
- Preserve existing URLs, navigation, localization, and data formats.
- Preserve direct file:// compatibility when required; avoid features that depend on a local server.
- Avoid unnecessary changes to existing deployment workflows.
