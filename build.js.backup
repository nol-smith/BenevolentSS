#!/usr/bin/env node
const fs = require('fs');
const path = require('path');

// Build articles
const articles = require('./src/content/articles.json');
const articleTemplate = fs.readFileSync('./src/templates/article.html', 'utf8');

articles.forEach(article => {
  const html = articleTemplate
    .replace(/\{\{title\}\}/g, article.title)
    .replace(/\{\{author\}\}/g, article.author)
    .replace(/\{\{date\}\}/g, article.date)
    .replace(/\{\{content\}\}/g, article.content);
  
  const dir = path.join(__dirname, article.slug);
  if (!fs.existsSync(dir)) fs.mkdirSync(dir, { recursive: true });
  
  fs.writeFileSync(path.join(dir, 'index.html'), html);
  console.log(`✓ Built article: ${article.slug}`);
});

// Build homepage
const homeContent = require('./src/content/home.json');
const homeTemplate = fs.readFileSync('./src/templates/home.html', 'utf8');

let homeHtml = homeTemplate;
Object.keys(homeContent).forEach(key => {
  homeHtml = homeHtml.replace(`{{${key}}}`, homeContent[key]);
});

fs.writeFileSync('index.html', homeHtml);
console.log('✓ Built homepage');

// Build blog listing
const blogTemplate = fs.readFileSync('./src/templates/blog.html', 'utf8');
const articlesList = articles.map(a => 
  `<article>
    <h2><a href="/${a.slug}">${a.title}</a></h2>
    <p class="meta">${a.author} • ${a.date}</p>
  </article>`
).join('\n');

const blogHtml = blogTemplate.replace('{{articles}}', articlesList);
const blogDir = path.join(__dirname, 'blog');
if (!fs.existsSync(blogDir)) fs.mkdirSync(blogDir);
fs.writeFileSync(path.join(blogDir, 'index.html'), blogHtml);
console.log('✓ Built blog listing');

console.log('\n✨ Build complete!');
