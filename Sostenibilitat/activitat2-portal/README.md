# Responsible Investment Section — ASIX1 Web Project

Web section for **ASIX1** combining *Llenguatges de marques i sistemes de gestió d'informació (MP0373)* and *Sostenibilitat aplicada al sistema productiu (MP1708)*.

**Team:** Andrei, Hugo and Unai
**Branch:** `feature/inversio-responsable`
**Technologies:** HTML5, CSS3, Git/GitHub, Gemini Notebook (NotebookLM)

## Project overview

Our section of the collaborative sustainability portal covers **Responsible Investment (ISR)** and is divided into three separate pages:

1. **Rendibilitat amb impacte positiu** — double return: financial profit plus measurable environmental and social impact, with indicators and a comparison against traditional investment.
2. **Selecció positiva d'empreses** — how companies are chosen: exclusion, best-in-class selection, ESG integration and intentional impact, plus a three-step selection process.
3. **Principis PRI** — the six Principles for Responsible Investment launched by the United Nations in 2006, how they are applied and how they relate to the EU SFDR and Taxonomy frameworks.

## Structure

| File | Description |
|---|---|
| `rendibilitat.html` | Page 1: Return with positive impact |
| `seleccio.html` | Page 2: Positive selection of companies |
| `pri.html` | Page 3: PRI Principles |
| `style.css` | Shared external stylesheet (CSS variables, Flexbox and Grid) |
| `mockups/mockup.html` | High-fidelity visual mockup of the section |
| `README.md` | This document (AICLE deliverable) |

## How we used NotebookLM / Gemini Notebook

1. We created a shared workspace in Gemini Notebook and uploaded the sustainability notes provided in class.
2. The assistant extracted key definitions, clear explanations and real examples of responsible investment.
3. It drafted the explanatory texts and suggested the page structure (return with impact, company selection, PRI principles).
4. The drafts were then synthesised to be short and readable on a web page, and manually verified against the class notes before publishing.

The AI was used as a research and drafting assistant, not as a final source: every claim was checked against the original material.

## Checklist of requirements

- [x] Semantic HTML5 tags: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`
- [x] Global navigation menu linking the three pages of the section
- [x] Multimedia elements: comparative tables, lists and highlighted quote blocks
- [x] Single external stylesheet `style.css` shared by the section
- [x] Responsive layout using CSS Grid and Flexbox (mobile-first, breakpoints at 900px)
- [x] Validated with the W3C HTML and CSS validators
- [x] Mockup delivered in `mockups/`
- [x] Frequent commits with conventional messages (`feat:`, `style:`, `docs:`)
- [x] Work done on a dedicated branch, ready for a pull request to `main`
- [x] Content written in Catalan; documentation in English

## Self-assessment of collaborative work

- **Work distribution:** the three members shared the research, writing and code review tasks; commits are attributed across the team.
- **Version control:** we worked on `feature/inversio-responsable` with descriptive commits, keeping `main` clean until the pull request.
- **Difficulties:** agreeing on a single colour palette with the other groups and keeping the shared stylesheet compatible with every section.
- **Improvements:** add more verified real-world cases and a screenshot of the rendered mockup once the design is approved by all groups.

## Design tokens (shared palette)

| Token | Hex | Use |
|---|---|---|
| `--verd` | `#14532d` | Primary green |
| `--verd-clar` | `#e8f3ec` | Section background |
| `--ambre` | `#c77d19` | Accent (investment tone) |
| `--text` | `#1f2933` | Body text |
| `--fons` | `#fafbfa` | Page background |

Typography: **Inter** for body text and **Fraunces** for headings, both with system fallbacks.
