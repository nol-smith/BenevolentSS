# Editable Source Structure

## Quick Start

1. **Edit content**: Open `src/content/articles.json`
2. **Build site**: Run `node build.js`
3. **Deploy**: Push to GitHub

## Structure

```
src/
  content/
    articles.json    ← Edit your blog posts here
  templates/         ← HTML templates (future)
  styles/            ← Custom CSS (future)
```

## Edit Content

Open `src/content/articles.json` and edit:

```json
{
  "slug": "benefits-of-assisted-living",
  "title": "Benefits of Assisted Living",
  "content": "<p>Your content here...</p>"
}
```

## Build

```bash
node build.js
```

This generates HTML files in their respective folders.

## Next Steps

- Extract more content from existing HTML
- Create reusable templates
- Add markdown support
