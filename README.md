# azanihs.github.io

Academic homepage built with [Quarto](https://quarto.org), published at <https://azanihs.github.io>.

## Structure

| File / folder        | Page                                                    |
|----------------------|---------------------------------------------------------|
| `_quarto.yml`        | Site config: title, navbar, footer, theme               |
| `index.qmd`          | About (home) page: bio, links, interests, education     |
| `research.qmd`       | Research projects                                       |
| `publications.qmd`   | Publications table, filled from `publications.yml`      |
| `teaching.qmd`       | Courses                                                 |
| `notes.qmd`, `notes/`| Working notes (one `.qmd` per note; RSS at `notes.xml`) |
| `cv.qmd`             | CV (put a PDF at `files/cv.pdf` and link it)            |
| `styles.scss`        | Colour and font tweaks for the light and dark themes    |

Search the files for `TODO` to find the placeholders to fill in.

## Editing

- **Add a publication:** add an entry to `publications.yml`.
- **Add a note:** create `notes/my-note.qmd` with `title` and `date` front matter.
- **Profile photo:** save it as `images/profile.jpg` and uncomment `image:` in `index.qmd`.

## Preview locally

```bash
quarto preview
```

## Deployment

Every push to `main` runs `.github/workflows/publish.yml`, which renders the site
and deploys it to GitHub Pages. One-time setup: **Settings → Pages → Build and
deployment → Source: GitHub Actions**.
