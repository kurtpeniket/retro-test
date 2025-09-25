# Retro Notes

A minimal retrospective notes website built with Jekyll and GitHub Pages.

**Live Site**: https://kurtpeniket.github.io/retro-test

## Adding a New Retro

1. Create a new file in `_retros/` following the naming convention: `YYYY-MM-DD-author-slug.md`

2. Add the required front matter:
```yaml
---
title: "Your Retro Title"
date: YYYY-MM-DD
author: Your Name
good:
  - "Something that went well"
  - "Another positive point"
change:
  - "Something to improve"
  - "Another area for change"
---
```

3. Optionally add notes after the front matter using Markdown

4. Commit and push to main - the site updates automatically

## Local Development (Optional)

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Open http://localhost:4000
```

## How It Works

- **Jekyll Collections**: Retros are stored in `_retros/` and automatically processed
- **GitHub Pages**: Builds and deploys automatically from the main branch
- **Responsive Layout**: Two columns on desktop, stacked on mobile
- **Author Grouping**: Index page groups by author, sorts by date (newest first)