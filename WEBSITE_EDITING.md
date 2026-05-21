# Website Editing Guide

This site is a small Jekyll site. The main editable files are:

- `index.md` for the home page content.
- `papers.md` for the full papers page.
- `_config.yml` for profile metadata and links.
- `_includes/theme-style.html` for visual styling.
- `_layouts/home.html` and `_layouts/page.html` for page structure.

## Profile Information

Edit `_config.yml`.

Common fields:

```yml
title: Yuepeng Yang
title_cn: 杨粤鹏
position: Postdoc
affiliation: Yale University
department: Dept. of Stat&DS
email: first.last AT yale DOT edu
google_scholar: https://scholar.google.com/citations?user=9SITlKwAAAAJ&hl=en&oi=ao
cv_link: /assets/files/curriculum_vitae.pdf
avatar: /assets/img/profile2025.JPG
```

The profile sidebar is rendered by `_includes/profile.html`.

## Home Page

Edit `index.md`.

### Short Bio

Find:

```html
<p class="intro-copy">
...
</p>
```

Edit the paragraph text directly.

### News Entries

Find:

```html
<section id="news" aria-labelledby="news-title">
```

Each news item looks like:

```html
<li>
  <span class="date">Jul 2025</span>
  <span>I started as a postdoc at Yale University.</span>
</li>
```

To add news, copy one `<li>...</li>` block and edit the date/text.

### Selected Papers

Find:

```html
<section id="papers" class="home-publications" aria-labelledby="papers-title">
```

Each selected paper is an `<article class="publication">...</article>` block. Edit, remove, or copy these blocks to control which papers appear on the home page.

## Full Papers Page

Edit `papers.md`.

Each paper entry looks like:

```html
<article class="publication">
  <div class="venue">Preprint</div>
  <div>
    <h3>Paper title.</h3>
    <p class="authors">Author One, Author Two</p>
    <p class="meta">Venue, Year</p>
    <div class="links">
      <a href="https://arxiv.org/...">arXiv</a>
      <a href="/assets/slides/example.pdf">Slides</a>
    </div>
  </div>
</article>
```

To add a paper:

1. Copy an existing `<article class="publication">...</article>` block.
2. Paste it where the new paper should appear.
3. Edit the venue, title, authors, metadata, and links.

To remove a paper, delete its full `<article class="publication">...</article>` block.

## Navigation

Navigation is rendered by `_includes/nav.html`.

Current links:

```html
<a href="{{ '/' | relative_url }}">Home</a>
<a href="{{ '/papers' | relative_url }}">Papers</a>
```

Add future pages there after creating the corresponding Markdown file.

## Styling

Edit `_includes/theme-style.html`.

Useful values:

- Profile image width: `.hero { grid-template-columns: 180px minmax(0, 1fr); }`
- Bio/news spacing: `.intro #news { margin-top: 22px; }`
- News heading size: `.intro #news h2 { font-size: 18px; }`
- Main page width: `--max`
- Link color: `--blue`
- Accent color: `--green`

## Assets

Profile images live in:

```text
assets/img/
```

Slides live in:

```text
assets/slides/
```

The CV file is:

```text
assets/files/curriculum_vitae.pdf
```

