# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML/CSS "hello world" welcome page with a focus on security, accessibility, and responsive design. The project consists of three files without any build system or dependencies.

## Development Commands

### Running the Project

Open directly in browser:
```bash
open index.html
```

Or use a local server (recommended for testing security headers):
```bash
# Python
python -m http.server 8000

# Node.js
npx http-server
```

Then visit `http://localhost:8000`

## Architecture

### File Structure
- `index.html` - Main HTML with security meta tags (CSP, X-Frame-Options, etc.)
- `styles.css` - All styling with CSS variables for customization
- `README.md` - Project documentation in Japanese

### Design Principles

**CSS Variables**: All customizable values (colors, animation duration, font sizes) are defined as CSS variables in `:root` in styles.css:1-9. Modify these variables rather than hard-coded values throughout the CSS.

**Security First**: index.html:10-25 contains strict security headers:
- CSP disables all scripts (`script-src 'none'`)
- X-Frame-Options prevents embedding
- No external resources allowed

**Accessibility**:
- Semantic HTML (`<main>`, proper heading hierarchy)
- ARIA attributes for screen readers (index.html:39)
- `prefers-reduced-motion` support disables animations (styles.css:47-53)

**Responsive Design**: Breakpoints at 768px and 480px (styles.css:56-66) adjust font size for mobile/tablet devices.

## Language

All documentation and comments are in Japanese. The README is entirely in Japanese and should be maintained in that language.
