# christophkronenberg.github.io

Personal academic website, built by GitHub Pages with plain Jekyll (no theme, no plugins).

## Editing

| What | File |
|---|---|
| Bio, news, contact | `index.html` |
| Publications and working papers | `research.md` |
| Teaching | `teaching.md` |
| Workshop page | `workshop/index.md` |
| Workshop archive (one entry per year) | `_data/emhw.yml`, flyer in `assets/img/emhw/emhw-YEAR.jpg` |
| Resources | `resources.md` |
| Navigation, site title, email | `_config.yml` |
| Layout and styling | `_layouts/default.html`, `assets/css/style.css` |
| CV | replace `files/CV_Kronenberg.pdf` (keep the file name) |

Edit a file on github.com (pencil icon) and commit. The site rebuilds within about a minute.

## Local preview (optional)

```
gem install jekyll
jekyll serve
```

Then open http://localhost:4000.
