# Content Guide

This project is now maintained from the editable local copy:

```text
/Users/ac/Desktop/1/个人情况更新/leizhou.page.local
```

Public site:

```text
https://leizhou-ac.github.io/
```

Local preview after `./bin/serve`:

```text
http://127.0.0.1:4000/
```

If dependency installation hangs on RubyGems:

```bash
RUBYGEMS_MIRROR=https://gems.ruby-china.com ./bin/bootstrap
```

Run the preview server in the background:

```bash
DETACH=1 LIVERELOAD=0 ./bin/serve
```

If detached Jekyll exits under the macOS system Ruby, serve a built snapshot:

```bash
./bin/static
```

## Add

Add a normal page:

1. Create a Markdown file in `_pages/`, for example `_pages/research.md`.
2. Add front matter:

```markdown
---
title: "Research"
permalink: /research/
author_profile: true
---
```

3. Add the menu link in `_data/navigation.yml` if it should appear in the top navigation.

Add a publication:

1. Create a Markdown file in `_publications/`, for example `_publications/2026-paper-title.md`.
2. Use this structure:

```markdown
---
title: "Paper Title"
collection: publications
permalink: /publication/2026-paper-title
date: 2026-01-01
venue: "Conference or Journal Name"
paperurl: "/files/paper.pdf"
citation: "Lei Zhou, Coauthor. Paper Title. Conference or Journal, 2026."
---

Short optional note about the paper.
```

3. Put PDFs or supplements in `files/`.

Add an image:

1. Put the file in `images/`.
2. Reference it as `/images/file-name.png`.
3. To change the profile photo, update `author.avatar` in `_config.yml`.

## Delete

Delete content by removing its source file:

- Page: remove the matching file from `_pages/`.
- Publication: remove the matching file from `_publications/`.
- Attachment: remove the file from `files/`.
- Image: remove the file from `images/` only after checking it is not referenced.

If the deleted page was in the menu, also remove the link from `_data/navigation.yml`.

## Edit

Common edit locations:

- Home page text: `_pages/about.md`
- CV: `_pages/cv.md`
- Publications landing page: `_pages/publications.md`
- Site name, author bio, email, location, GitHub link: `_config.yml`
- Top menu: `_data/navigation.yml`
- Local preview settings: `_config.dev.yml`

After changing `_config.yml` or `_config.dev.yml`, restart `./bin/serve`.

## Search

Useful search commands:

```bash
rg "Lei Zhou"
rg "Waiting for|To be updated|Publications"
rg "permalink:" _pages _publications
rg "/images/" _pages _publications _includes
```

## Publish

After previewing locally, commit and push to GitHub:

```bash
git status
git add .
git commit -m "Update homepage content"
git push
```

GitHub Pages will rebuild the public site automatically.
