[README-portfolio.md](https://github.com/user-attachments/files/32678719/README-portfolio.md)
# Ahmed Hassan — Portfolio Site

A personal portfolio site built with plain HTML, CSS, and JavaScript — no frameworks, build tools, or dependencies required.

## Features

- **Sections**: About, Skills, Projects, Experience, Resume, and Contact, all on a single scrolling page.
- **File-explorer style navigation** — a fixed side rail (inspired by a code editor's sidebar) links to each section; the active link highlights automatically as you scroll (scrollspy).
- **Smooth scrolling** — clicking a nav link glides to the section instead of jumping.
- **Scroll-reveal animations** — each section fades and slides into view the first time it enters the viewport, using `IntersectionObserver`.
- **Hover effects** — project cards lift with a shadow, skill chips and buttons shift on hover, contact cards highlight on hover.
- **Responsive layout** — the side rail collapses into a hamburger-triggered slide-in menu on screens narrower than 900px; the skills grid and hero metadata stack into a single column on mobile.
- **Downloadable résumé** — a "Download résumé" button serves a real PDF from the `assets` folder.
- **Accessibility touch** — respects `prefers-reduced-motion` by disabling animations and hover transforms for users who've asked their OS to reduce motion.

## File structure

```
task3-portfolio/
├── index.html        → page structure and content
├── style.css          → all styling, layout, and responsive rules
├── script.js          → scrollspy, scroll-reveal, and mobile nav toggle logic
└── assets/
    └── resume.pdf      → downloadable résumé (linked from the Resume and About sections)
```

## How to run it

Unzip the folder and open `index.html` directly in any modern browser (Chrome, Firefox, Safari, Edge) — no server or build step needed, since it only uses relative paths within the folder.

## How to customize

**Update your info** — edit the text directly inside `index.html`. Each section is clearly marked with an HTML comment-style `id` (`#about`, `#skills`, `#projects`, `#experience`, `#resume`, `#contact`) matching the nav links.

**Add or remove a project** — copy one `<article class="card">…</article>` block inside the `#projects` section and edit its title, description, and tag chips.

**Add or remove a skill** — add or remove a `<span class="chip">…</span>` inside the relevant `.skill-group` in the `#skills` section.

**Swap the résumé file** — replace `assets/resume.pdf` with your own file (keep the same filename, or update the `href` in both `download` links in `index.html`).

**Change the color palette** — edit the CSS custom properties at the top of `style.css`:

```css
:root{
  --bg: #12141c;        /* page background */
  --panel: #1a1e29;     /* card/rail background */
  --accent: #5fd9b0;    /* primary accent (mint) */
  --accent-2: #e8a33d;  /* secondary accent (amber) */
}
```

**Change fonts** — the site uses "JetBrains Mono" for headings/labels and "Inter" for body text, loaded from Google Fonts via `<link>` tags in `index.html`. Swap the font names in the `<link>` tag and in the `font-family` rules near the top of `style.css`.

## Deploying it

**GitHub Pages**
1. Create a new GitHub repository and push the contents of `task3-portfolio/` to it (keep `index.html` at the repo root).
2. Go to Settings → Pages, set the source to your main branch, and save.
3. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

**Netlify**
1. Go to your Netlify dashboard and choose "Deploy manually" (drag-and-drop).
2. Drag the unzipped `task3-portfolio` folder onto the drop zone.
3. Netlify assigns a live URL immediately — no configuration needed.

## Browser support

Uses standard, widely supported web features (CSS Grid, `IntersectionObserver`, CSS custom properties, `scroll-behavior: smooth`). Works in all current versions of Chrome, Firefox, Safari, and Edge.
