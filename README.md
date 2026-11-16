# Muhammad Noor Ul Hassan Butt

Personal site for Muhammad Noor Ul Hassan Butt, a CS student and undergraduate researcher at George Mason University who works on systems, backend, and AI reliability.

> Build it, measure it, then break it on purpose.

---

## Why it looks like this

The site is meant to read like a lab notebook: quiet, dark, and focused on numbers instead of decoration. Every figure on the page (2,000+ req/s, 20 s to 1 s, 0 errors) comes from a real test of a real project.

| Token | Dark | Light | Used for |
|---|---|---|---|
| Background | `#0b0d13` | `#f6f7fa` | Page ground |
| Ink | `#e7eaf3` | `#0d1017` | Body text |
| Accent | `#8ea6ff` | `#3350d6` | Highlights, cursor, links |

**Type:** Bricolage Grotesque for headlines, Inter for body text, JetBrains Mono for labels and the terminal.

**Theme:** follows the visitor's system setting through CSS custom properties. No toggle and no flash.

## Built with

- **Markup and styles:** plain HTML and CSS, with no framework and no build step
- **Interaction:** about 60 lines of vanilla JavaScript
- **Fonts:** Google Fonts
- **Hosting:** any static host; one file plus a PDF

The site is deliberately framework-free. It loads fast, has nothing to update, and the whole thing fits in one file you can read top to bottom.

## What's on the page

- **Results terminal:** the hero panel types out benchmark results from each project, line by line.
- **Neon cursor:** a glowing dot with a trailing ring that grows over links. It runs only on a mouse or trackpad and leaves touch devices alone.
- **Project ledger:** numbered rows with the result pinned on the right. They slide on hover and collapse to a stack on phones.
- **Research section:** what I study (fault injection and silent data corruption in self-driving and LLM systems) and the compute behind it.
- **Résumé:** linked from the hero as `resume.pdf`.
- **Accessibility:** animations switch off under `prefers-reduced-motion`, and decorative elements are hidden from screen readers.

## Under the hood

Two small scripts at the bottom of `index.html` do all the work:

| Script | What it does |
|---|---|
| Cursor | Tracks the mouse and eases the ring toward the dot with linear interpolation on each animation frame. It detects hover over links and buttons to grow the ring. |
| Terminal replay | Splits the log into text and tag tokens, then types characters one at a time, pausing a little longer at line breaks. |

To change a project, edit its row in the `#work` section. Each row is one `<a class="row">` with a number, title, description and result.

## Run locally

```bash
git clone https://github.com/noorhusaan302-png/noor-portfolio.git
cd noor-portfolio
python3 -m http.server 8000
# open http://localhost:8000
```

## Files

```
noor-portfolio/
├── index.html    # the whole site: markup, styles, scripts
├── resume.pdf    # linked from the hero
└── README.md
```

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/muhammad-noor-ul-hassan-butt-84a553383/) · [GitHub](https://github.com/noorhusaan302-png)
