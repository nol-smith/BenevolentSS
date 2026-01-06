# Benevolent Senior Services - Source Code

## What Changed?

**Before:** Massive compiled HTML with 200KB+ of inline Tailwind CSS  
**After:** Clean, readable source code

## Structure

```
src/
  content/
    articles.json       ← Edit blog posts here
    home.json          ← Edit homepage content
  templates/
    article.html        ← Article template
    blog.html          ← Blog listing template
    home.html          ← Homepage template
  styles/
    main.css           ← Simple, readable CSS
build.js               ← Generates entire site
```

## Edit Content

Open `src/content/articles.json`:

```json
{
  "title": "Your Title",
  "author": "Author Name",
  "date": "Date",
  "content": "<p>Your content...</p>"
}
```

## Build Site

```bash
node build.js
```

This generates:
- `index.html` - Homepage
- `blog/index.html` - Blog listing
- `{slug}/index.html` - Each article

## What You Get

- ✅ **Clean HTML** - No CSS classes, just semantic markup
- ✅ **Simple CSS** - 50 lines vs 200KB of Tailwind
- ✅ **Editable** - Change content in JSON, not HTML
- ✅ **Fast** - Instant builds, no complex tooling

## File Sizes

| Before | After |
|--------|-------|
| 250KB HTML | 3KB HTML |
| Inline CSS | 2KB CSS file |
| Unreadable | Human-readable |

## Deploy

Just commit and push. The HTML files are ready to serve.
