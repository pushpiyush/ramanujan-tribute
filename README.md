# Srinivasa Ramanujan — A Tribute Page

A single-page tribute to Srinivasa Ramanujan: his life, his 1913 letter to G. H. Hardy,
the Cambridge years, the "lost notebook," and a timeline of his major milestones.

**Live demo:** https://pushpiyush.github.io/ramanujan-tribute/

## Why this exists

This started as a practice project for responsive web design fundamentals
(semantic HTML, custom CSS, no frameworks). This version cleans it up to a
standard I'd be comfortable linking from a resume: valid, accessible markup,
a deliberate visual identity, and a stylesheet built on design tokens instead
of one-off values.

## Tech

- Plain HTML5 + CSS3 — no build step, no dependencies
- Google Fonts: Playfair Display, Lora, JetBrains Mono
- Hosted with GitHub Pages

## Design

- **Palette** — aged-paper background, deep Cambridge indigo for text,
  manuscript gold and sealing-wax red as accents.
- **Type** — a serif display face for headings, a literary serif for body
  copy, and a monospace face reserved for dates, captions, and the 1729
  equation — a nod to the notebook entries the content is drawn from.
- **Structure** — each section is styled as a numbered notebook entry
  (`§`), echoing the three notebooks Ramanujan filled by hand.

## Accessibility

- Semantic landmarks (`header`, `main`, `section`, `footer`) and a skip link
- All images carry descriptive `alt` text; decorative elements are
  `aria-hidden`
- The timeline is a real `<table>` with `scope` attributes, not a div grid
- Color contrast checked against WCAG AA; visible focus states throughout
- Respects `prefers-reduced-motion`

## Running locally

No build step is required.

```bash
git clone https://github.com/pushpiyush/ramanujan-tribute.git
cd ramanujan-tribute
# open index.html directly, or serve it:
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Project structure

```
ramanujan-tribute/
├── index.html      # page markup and content
├── style.css        # all styling, organized by section, custom properties at the top
├── images/           # local image assets
└── README.md
```

## Sources

Biographical content is drawn from public sources, including Ramanujan's
Wikipedia entry, the MacTutor History of Mathematics Archive, and *The Man
Who Knew Infinity* by Robert Kanigel. Photographs are public domain (via
Wikimedia Commons) or used with attribution as noted in their captions.

## License

Code is available under the [MIT License](LICENSE). Biographical content is
a summary of publicly available facts; please don't republish the page
verbatim as your own original writing.
