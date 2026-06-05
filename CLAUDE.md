# CLAUDE.md — AI × Humanity Website Prototype

## Project overview

A website prototype for a personal brand / subject matter expert in the AI & Humanity space. The site positions [Name] as the go-to voice on how artificial intelligence is reshaping education, learning, and human connection — and demonstrates that thesis live through four AI technologies.

**Core message:** AI × Humanity isn't a concept. It's happening now — and this site is proof of it.

**GitHub:** https://github.com/kacwq/ai_and_humanity  
**Branch:** master  
**Stack:** Vanilla HTML + CSS + minimal vanilla JS. No frameworks, no build step. Each page is a self-contained `.html` file.

---

## File structure

```
index.html       — Home page
about.html       — About [Name]: bio, stats, mission, credentials, AI Twin teaser, speaking CTA
tech-lab.html    — Tech showcase: 3D Avatar, AI Chatbot, Video Generation, Video Search
learn.html       — Content hub: podcast, e-book, library (positioned as "ideas behind the tech")
connect.html     — Contact page (removed from nav; kept in repo for reference)
sitemap.md       — Original sitemap and navigation rationale
CLAUDE.md        — This file
README.md        — Repo readme
.gitignore       — Standard ignores (Python, Node, env, OS, IDE)
```

---

## Design system

All pages share the same CSS custom properties. Never introduce new colour values — use these tokens:

```css
--bg:            #080810    /* page background */
--bg-card:       #10101A    /* card backgrounds */
--bg-card-hover: #15152A    /* card hover state */
--border:        rgba(255,255,255,0.07)
--border-hover:  rgba(255,255,255,0.15)
--text:          #FFFFFF
--text-muted:    #8888A0    /* secondary text */
--text-dim:      #44445A    /* tertiary / placeholder text */
--accent:        #7C3AED
--accent-light:  #A78BFA
--grad:          linear-gradient(135deg, #6366F1 0%, #8B5CF6 50%, #EC4899 100%)
--grad-text:     linear-gradient(135deg, #A78BFA, #F472B6)
--radius:        12px
--radius-lg:     20px
```

**Typography:** Inter (Google Fonts). Weights used: 300, 400, 500, 600, 700, 800, 900.

**Style:** Dark, minimal, professional. Appeals to Gen Z and educators alike. No light mode.

---

## Nav logo

Every page uses the same "AI × Humanity" SVG Venn logo. The logo links to `index.html` and serves as the Home button — there is no Home link in the nav. SVG gradient IDs must be unique per page instance (nav vs footer) to avoid conflicts.

Pattern used:
- Nav SVG: IDs `nlg1`, `nlg2`
- Footer SVG: IDs `flg1`, `flg2`
- About page nav: `anlg1`, `anlg2` / footer: `aflg1`, `aflg2`

---

## Navigation structure

All pages share the same 3-link nav:

```
[Logo → Home]   About   Tech Lab   Learn
                                           [Try AI Twin → (button)]
```

- Connect page exists (`connect.html`) but is **not linked** from the nav
- Contact is handled via a direct email address on the About page speaking CTA
- The "Try AI Twin →" persistent CTA in the nav links to `tech-lab.html#chatbot`

---

## Page summaries

### `index.html` — Home
Sections: sticky nav, hero (animated avatar orb + CTAs), trust bar, "why this matters" stat section, 4-card tech strip, pull quote, learn preview (3 cards), email CTA, footer, floating chat bubble.

Primary CTA flow: **Home → Tech Lab → Learn → About**

### `about.html` — About
Sections: sticky sub-nav (Intro / Mission / Credentials / AI Twin), hero with photo placeholder + bio tags, stats strip, mission + 3 pillars, credentials with Speaking/Media tabs, AI Twin teaser, speaking CTA with email link.

Sub-nav highlights sections on scroll via JS.

### `tech-lab.html` — Tech Lab
The centrepiece. Four full-width sections, each with:
- Visual mockup (left or right, alternating)
- Content: label, h2, body, feature list
- **"Why this matters"** callout (purple left-border card) — ties the specific tech back to the AI × Humanity theme
- **"How does this work?"** accordion — plain-language technical explanation
- CTAs

Sections: 01 3D Avatar, 02 AI Chatbot (live chat mockup), 03 Video Generation (player + pipeline diagram), 04 Video Search (semantic results mockup).

Closing CTA is a mission statement: *"This is what AI × Humanity looks like."*

Sticky feature nav highlights current section on scroll. Accordions are mutually exclusive (one open at a time).

### `learn.html` — Learn
Positioned as "the ideas behind the tech," not a content library. Sections: hero with search bar + quick-topic tags, Start Here (3 audience path cards: Student / Educator / Curious), podcast grid with topic filter tabs, e-book spotlight with CSS 3D book cover + chapter list, library with type tabs (Talks / Notebook LM / Slides), email newsletter CTA.

Filter tabs and library tabs are visual-only (toggle active class). Start Here cards highlight on click.

---

## Component patterns

### Buttons
```html
<a href="#" class="btn btn-primary btn-lg">Label →</a>
<a href="#" class="btn btn-outline btn-lg">Label</a>
```

### Section label
```html
<div class="label">Section Name</div>
```

### Accordion (Tech Lab)
```html
<div class="accordion">
  <button class="accordion-trigger">Title <span class="accordion-arrow">▾</span></button>
  <div class="accordion-body">
    <div class="accordion-body-inner">content</div>
  </div>
</div>
```
Controlled by the JS at bottom of `tech-lab.html`.

### Why this matters callout (Tech Lab only)
```html
<div class="why-matters">
  <span class="why-matters-label">Why this matters</span>
  <p>Insight text connecting the tech to the AI × Humanity theme.</p>
</div>
```

### Floating chat bubble (all pages)
```html
<div class="chat-fab">
  <div class="chat-tooltip">Chat with [Name]'s AI</div>
  <button class="chat-btn" aria-label="Open AI chat">💬</button>
</div>
```

---

## Placeholder convention

All content waiting for real data uses `[square brackets]`:
- `[Name]` — the subject matter expert's real name
- `[Title / Role]` — e.g. "AI Strategist & Future of Learning Advocate"
- `[email@domain.com]` — real contact email
- `[E-Book Title]` — actual title of the e-book
- `[X]` — numeric placeholders (talk count, episode count, etc.)
- `[Conference Name]`, `[University]`, `[Guest Name]` — credential placeholders

When filling in real content, search for `[` to find all placeholders across the project.

---

## Git conventions

- Commits use imperative subject line + body explaining *why*, not *what*
- All commits include `Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>`
- Push to `origin/master` after every meaningful change
- Avoid `×` or other special Unicode in commit messages (PowerShell here-string limitation)

---

## What's been built vs. what's placeholder

| Feature | Status |
|---|---|
| Site structure & navigation | Done |
| Design system | Done |
| Home page | Done — placeholder content |
| About page | Done — placeholder content |
| Tech Lab page | Done — all 4 mockups, narrative thread complete |
| Learn page | Done — placeholder content |
| Connect page | Built, not linked — kept for reference |
| Real name / branding | Placeholder |
| Actual e-book content | Placeholder |
| Real podcast episodes | Placeholder |
| Credential / speaking history | Placeholder |
| Live AI integrations | Placeholder (mockups only) |

---

## Key decisions on record

- **No Connect page in nav** — contact lives as a direct email on the About speaking CTA. The site is a showcase, not a CRM.
- **Tech Lab is the centrepiece** — nav order and CTA flow prioritise it above Learn.
- **"Why this matters" thread** — each tech demo explicitly connects back to the AI × Humanity thesis. Without this, the page reads as a portfolio of tools.
- **Learn reframed as "ideas behind the tech"** — prevents users from getting lost in a content library; positions it as intellectual support for the Tech Lab experience.
- **Anchor links over sub-pages** — `/tech-lab#avatar` not `/tech-lab/avatar`. Keeps nav count low and mobile performance fast.
- **No frameworks** — vanilla HTML/CSS keeps the prototype portable, fast, and editable by anyone without a build environment.
