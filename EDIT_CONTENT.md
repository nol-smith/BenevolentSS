# Content Editing Guide

## Current Situation
This is a **built/compiled** Gatsby site. You're editing HTML output, not source code.

## Quick Edits (Current Setup)
Edit these HTML files directly:
- `/index.html` - Homepage
- `/blog/index.html` - Blog listing
- `/benefits-of-assisted-living/index.html` - Article
- `/four-helpful-tips-to-reduce-fall-risks-for-seniors/index.html` - Article
- `/six-options-for-financing-senior-living/index.html` - Article

## Better Solution
Get the source code repository which should have:
```
src/
  pages/
  templates/
  components/
gatsby-config.js
```

This would let you edit in React/JSX instead of raw HTML.
