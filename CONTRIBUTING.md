# Contributing to Retro Notes

## Front Matter Requirements

Each retro file must include:

- **title**: Descriptive title for the retro
- **date**: ISO format date (YYYY-MM-DD) - used for sorting and display
- **author**: Name of the person who facilitated/wrote the retro
- **good**: Array of positive points (at least one item required if change is empty)
- **change**: Array of improvement points (at least one item required if good is empty)

## Naming Convention

Files must follow: `YYYY-MM-DD-author-slug.md`

Examples:
- `2025-09-25-sarah-sprint-review.md`
- `2025-09-20-james-q3-platform.md`

## Example Entry

```yaml
---
title: "Sprint 23 Retrospective"
date: 2025-09-20
author: Sarah
good:
  - "Team velocity improved by 15%"
  - "New testing pipeline worked well"
change:
  - "Documentation needs updating"
  - "Code reviews taking too long"
---

Optional notes can go here using Markdown formatting.

## Action Items
- Update deployment docs by Friday
- Implement PR review time tracking
```

## Pull Request Process

1. Create a branch for your retro
2. Add your retro file with proper front matter
3. Test locally if possible (`bundle exec jekyll serve`)
4. Submit PR using the provided template
5. Address any feedback from reviewers
6. Merge to main triggers automatic site deployment

## Validation Rules

- Dates must be valid ISO format (YYYY-MM-DD)
- At least one item in either `good` or `change` arrays
- File names must match the date in front matter
- Author names should be consistent across retros

## Labels

Use these labels on PRs:
- `retro`: Standard retrospective entry
- `hotfix`: Urgent correction to existing retro
- `documentation`: Updates to guides or templates