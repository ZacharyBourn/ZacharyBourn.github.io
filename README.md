# The American Retrospect — GitHub Pages starter

This is a Jekyll site for the `ZacharyBourn/ZacharyBourn.github.io` repository.

## Upload

Upload **the contents of this folder** to your repository's `main` branch (not the enclosing folder). Replace the existing `index.html`. In GitHub: **Add file → Upload files**, drag in the contents, **Commit changes**. If the web upload interface won't preserve folders, use GitHub Desktop or git instead.

The site will publish at https://zacharybourn.github.io if Pages is configured to deploy from `main` / `(root)`.

## Publish an article

Create a text file in `_posts` named `YYYY-MM-DD-your-article.md`, for example `2026-10-20-jared-bourne.md`.

Put this at the top (and your article below):

```yaml
---
layout: post
title: "Jared Bourne: Legacy and Lineage"
subtitle: "A historical study of early New England and Boston's Liberty Tree"
date: 2026-10-20
category: studies
pinned: true
---

Your text goes here, using Markdown.
```

Choose `category: studies`, `category: essays`, or `category: reflections`.

Only an article with `pinned: true` appears as the homepage feature. If more than one is pinned, the newest pinned article appears. To change the feature, set the old one to `pinned: false` and the new one to `true`.

To attach a PDF, put it in `assets/pdfs/` and link with `[Read the full study (PDF)]({{ '/assets/pdfs/filename.pdf' | relative_url }})`. Only do this once you are comfortable publishing the document and any personal details inside it.

## Edit the reading list

Open `_data/books.yml`. Each book needs `title`, `author`, `subject`, and `note`. Books automatically appear on `/reading/`. The three entries are **starter examples**, not final personal reviews.

## Customize

- Site name and description: `_config.yml`
- Homepage wording: `index.html`
- About content: `about.md`
- Colors and typography: `assets/css/style.css`
- Site header and footer: `_layouts/default.html`

This is a static site. There is no newsletter, subscription feature, tracking script, database, or paid dependency.
