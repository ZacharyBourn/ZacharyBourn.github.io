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

## Add, remove, reorder, and change book covers

Your entire reading list lives in **[_data/books.yml](./_data/books.yml)**.

**From the GitHub website:**
1. Open the link above, then click the pencil icon (**Edit this file**).
2. **Add a book:** copy a complete book entry starting with `- order:`, paste it at the bottom, and change the fields.
3. **Remove a book:** delete the whole entry, including the `- order:` line.
4. **Reorder books:** edit the `order:` numbers. Lowest number is shown first. You don't need to physically move the entries.
5. Click **Commit changes**. GitHub Pages will update the public reading page automatically after the build.

Example book entry:

```yaml
- order: 4
  title: "Theodore Rex"
  author: "Edmund Morris"
  subject: "Presidential Biography"
  isbn: ""
  cover: ""
  note: "Write your own short assessment here."
```

**Cover images:** Add a valid 10- or 13-digit `isbn` (as a quoted string) and the site will attempt to show that edition's cover via Open Library. If you prefer your exact edition, upload a JPG/PNG/WebP cover image to the repository using **Add file → Upload files**, placing it in `assets/books/`, then set `cover: "/assets/books/your-filename.jpg"`. A full image URL can also be used in `cover`. If both `cover` and `isbn` are filled in, the custom cover takes priority.

If a cover cannot be found, a neutral placeholder appears. Make sure each entry starts with `- order:` and uses consistent indentation. Avoid using unescaped double quotes inside quoted text; apostrophes are fine.

The three included titles are examples, not finished personal endorsements or reviews. Change their notes however you like. A change to `_data/books.yml` updates the catalog without editing HTML or CSS.

## Customize

- Site name and description: `_config.yml`
- Homepage wording: `index.html`
- About content: `about.md`
- Colors and typography: `assets/css/style.css`
- Site header and footer: `_layouts/default.html`

This is a static site. There is no newsletter, subscription feature, tracking script, database, or paid dependency.
