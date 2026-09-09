# CDE Teaching — Landing Page

Landing page for the [CDEteaching](https://github.com/CDEteaching) GitHub organisation. 
This platform is hosted by the [Centre for Development and Environment (CDE)](https://www.cde.unibe.ch), a leading research centre for sustainable development. CDE combines research, education, and practice to co-create knowledge for just and sustainable transformations worldwide.

This platform provides an overview of all open education resources (OER) developed at CDE with a focus on Education for Sustainable Development (ESD) and Sustainability Transformations.
You can find an overview of all published OER here: https://cdeteaching.github.io/CDEteaching/


---

## What this repo contains

| File | Purpose |
|------|---------|
| `index.html` | The complete landing page — single self-contained file, no build step |
| `README.md` | This file |

---

## Adding or updating a course card

Each course appears as a card in the "Course Materials" section of `index.html`. To add a new course, copy one of the existing `<div class="card">` blocks and update the four fields:

```html
<div class="card">
  <div class="card-accent"></div>       <!-- green accent bar; use class="card-accent teal" for methods/tools -->
  <div class="card-body">
    <span class="card-tag">Course Material</span>   <!-- or "Methods & Tools" -->
    <h3>Your Course Title</h3>
    <p>A short description of the course — 2–3 sentences is enough.</p>
  </div>
  <div class="card-footer">
    <a href="https://cdeteaching.github.io/YOUR-REPO/" class="card-link" target="_blank" rel="noopener">Open course</a>
    <span class="card-gh"><a href="https://github.com/CDEteaching/YOUR-REPO" target="_blank" rel="noopener">GitHub</a></span>
  </div>
</div>
```

**Only list repos that have an active GitHub Pages site.** Repos without a published page should not appear as cards — they have no destination to link to.

---

## Repo hygiene checklist

Before adding a repo to the landing page, make sure it has:

- [ ] A clear **description** set on GitHub (Settings → About → Description)
- [ ] Relevant **topic tags** set (e.g. `oer`, `sustainability`, `course-material`, `esd`)
- [ ] A clean `README.md` in the repo itself — this is what visitors see when they click through to GitHub
- [ ] GitHub Pages enabled and working (Settings → Pages)

---

## Local preview

No build tools required. Open `index.html` directly in any browser:

```bash
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

---

## Deployment

This repo is served automatically by GitHub Pages. Any push to the `main` branch updates the live site within ~1 minute.

```bash
git add index.html
git commit -m "add course card: Your Course Title"
git push
```

No CI/CD, no build step, no dependencies.

---

## Design

The page uses CDE's official brand colours and Inter as the typeface (loaded from Google Fonts). The layout is fully responsive and works without JavaScript — no frameworks, no bundlers.

| Token | Value | Usage |
|-------|-------|-------|
| `--green-dark` | `#0c641f` | Header, hero background, primary accents |
| `--teal` | `#046178` | Methods & Tools card accent |
| `--red` | `#d6002b` | Reserved for University of Bern institutional use |

---

## License

Teaching materials across the CDEteaching repositories are published under [Creative Commons Attribution 4.0 International (CC BY NC SA 4.0)]([https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by-nc-sa/4.0/)) unless stated otherwise in the individual repository.

---

*Centre for Development and Environment (CDE) · University of Bern · [www.cde.unibe.ch](https://www.cde.unibe.ch)*
