# barbaracervone.com

Personal website for Barbara Cervone. Built with Jekyll and hosted on GitHub Pages.

**Live site:** https://ccerv1.github.io/barbara-cervone/

## How it works

The site is plain markdown files. When you push to `main`, GitHub Pages automatically rebuilds the site (takes 1-2 minutes). No build step, no dependencies to install.

## Site structure

```
index.md                              # Home page (bio + photo)
work/index.md                         # Work & Publications
personal-writing/index.md             # Personal Writing (blog selections + essays)
personal-writing/looking-outward.md   # "Looking Outward" (1965 Radcliffe speech)
progressive-education/index.md        # Progressive Education: A Personal Chronicle
_layouts/default.html                 # Page layout with nav bar
_config.yml                           # Site title and theme config
assets/css/custom.css                 # Custom stylesheet (Lora + Source Sans 3)
assets/img/barbara-cervone.JPG        # Profile photo
```

## Common updates

### Add a new blog post selection to Personal Writing

Edit `personal-writing/index.md`. Add a line under the appropriate category:

```markdown
- [Post Title](https://www.postcards-from-the-rogue-valley.blog/post-slug/) (2026)
```

### Add a new essay hosted on the site

1. Create a new markdown file in `personal-writing/`, e.g. `personal-writing/my-essay.md`
2. Add frontmatter at the top:
   ```markdown
   ---
   title: "My Essay Title"
   ---
   ```
3. Add a link to it from `personal-writing/index.md`:
   ```markdown
   - ["My Essay Title"](my-essay) — Brief description.
   ```

### Add a book, article, or press mention

Edit `work/index.md` and add an entry under the appropriate section. For books with ISBNs, link to Open Library:

```markdown
- *Book Title* — Author. Publisher, Year. ([ISBN 978-X-XXXX-XXXX-X](https://openlibrary.org/isbn/978XXXXXXXXXX))
```

For articles with DOIs:

```markdown
- ["Article Title"](https://doi.org/10.XXXX/xxxxx) — Author. *Journal*, Year.
```

### Update the bio

Edit `index.md`. The photo is an inline `<img>` tag at the top; the rest is plain markdown.

### Add a new page

1. Create a new directory with an `index.md` file (e.g., `new-page/index.md`)
2. Add frontmatter with a title
3. Add a nav link in `_layouts/default.html`

### Change the styling

Edit `assets/css/custom.css`. The site uses:
- **Lora** (serif) for body text
- **Source Sans 3** (sans-serif) for headings and nav
- Cream background (`#faf8f4`) with warm brown accents

Colors and fonts are defined as CSS variables at the top of the file.

## Technical details

- **Theme:** `jekyll-theme-minimal` (remote theme, loaded by GitHub Pages)
- **Custom styles** override the theme via `assets/css/custom.css`
- **Nav bar** is defined once in `_layouts/default.html` and appears on every page
- The `temp/` directory is gitignored (used for source material)
