# Website Sitemap — AI & Humanity
**[Name]'s Personal Brand / Subject Matter Expert Site**

---

## Navigation Structure (Top-Level — 5 pages max)

```
[ Home ]  [ About ]  [ Tech Lab ]  [ Learn ]  [ Connect ]
```

---

## Hierarchical Sitemap

```
/  (Home)
├── /about
│   ├── /about#mission          — Who [Name] is and why this matters
│   ├── /about#credentials      — Background, expertise, speaking/media
│   └── /about#ai-twin          — Meet [Name]'s AI Twin (3D avatar intro)
│
├── /tech-lab
│   ├── /tech-lab#avatar        — 3D Avatar / Digital Twin (interactive)
│   ├── /tech-lab#chatbot       — Chat or Talk with [Name]'s AI (voice + text)
│   ├── /tech-lab#video-gen     — AI Video Generation showcase
│   └── /tech-lab#video-search  — Semantic Video Search demo
│
├── /learn
│   ├── /learn#podcast          — Podcast episodes (video format)
│   ├── /learn#ebook            — E-book (read online or download)
│   └── /learn#library          — Slides & videos from Notebook LM
│
├── /connect
│   ├── /connect#contact        — Get in touch / speaking inquiries
│   └── /connect#newsletter     — Subscribe for updates
│
└── [Persistent across all pages]
    ├── Global CTA              — "Try the AI Twin" or "Start Exploring"
    ├── Footer nav              — Privacy, About, Connect, Social links
    └── Sticky chat bubble      — Chatbot accessible from every page
```

---

## Page Breakdown

### `/` — Home
**Purpose:** First impression. Establish the brand, hook the user, drive them to Tech Lab or Learn.

**Sections:**
- Hero: Bold headline + 1-line subheading (what this is about) + primary CTA → "Meet My AI Twin"
- 30-second explainer: Short animated or video loop — "Why AI & Humanity matters now"
- Feature preview strip: 4 cards (Avatar / Chatbot / Video Gen / Video Search) → links to Tech Lab
- Quote / credibility moment: One strong stat or quote from [Name]
- Secondary CTA → "Start Learning" → /learn

---

### `/about` — About [Name]
**Purpose:** Establish [Name] as the go-to voice on this topic. Human story + credentials.

**Sections:**
- Photo + short bio (3–5 sentences max)
- Mission statement: "Why I built this"
- Credentials snapshot: speaking, media, institutions, publications
- AI Twin teaser: "Talk to my AI version" → anchors to Tech Lab chatbot
- CTA: "Invite me to speak" → /connect

---

### `/tech-lab` — Tech Lab
**Purpose:** The showpiece. Let users *experience* the technology — not just read about it. This is the differentiator.

**Sections:**
- Intro: "This is what the future of learning feels like." (1 sentence)
- **[1] 3D Avatar / Digital Twin** — Embeddable interactive 3D avatar
- **[2] AI Chatbot** — Voice + text chat widget with [Name]'s AI persona
- **[3] AI Video Generation** — Sample generated video, explanation of how it works
- **[4] Video Search** — Search across [Name]'s podcast/video library by topic or question
- Each section: brief "How this works" tooltip or accordion (for educators/curious users)
- CTA at bottom: "Dive deeper into the content" → /learn

---

### `/learn` — Learn
**Purpose:** Content hub. Structured so users can pick their format — watch, read, or skim. Not a wall of content.

**Sections:**
- **Podcast** — Featured episodes (video format), filterable by topic
- **E-book** — Cover + summary + read/download CTA
- **Library** — Slides + Notebook LM videos, organized by theme (not chronologically)
- Search bar across all content
- "Not sure where to start?" → Recommended path for: Students / Educators / Curious Explorers

---

### `/connect` — Connect
**Purpose:** Convert interest into relationship — newsletter, inquiries, social.

**Sections:**
- Speaking & collaboration inquiry form (minimal: name, email, message)
- Newsletter signup: "Get updates on AI & the future of learning"
- Social links
- Short quote from [Name] on why connection matters

---

## Recommended Navigation

```
Desktop:  [ Home ]  [ About ]  [ Tech Lab ]  [ Learn ]  [ Connect ]
                                                          [ Try AI Twin → ]  ← persistent CTA button

Mobile:   Hamburger menu (same 5 pages)
          Sticky bottom bar: [ Home ] [ Tech Lab ] [ Learn ] [ Chat ]
```

The sticky bottom bar on mobile surfaces the 3 highest-value pages + the chatbot without needing to open a menu.

---

## User Flow (Primary Journey)

```
Home
 └─→ Tech Lab (Avatar / Chatbot)       ← "wow" moment, builds trust in the tech
      └─→ Learn (Podcast / E-book)     ← deeper engagement, content consumption
           └─→ About (who is [Name]?)  ← credibility check before committing
                └─→ Connect            ← newsletter signup or speaking inquiry
```

**Secondary flow (Educator/Researcher):**
```
Home → Learn → About → Connect
```

**Secondary flow (Already knows [Name]):**
```
Home → Tech Lab → Connect
```

---

## Why This Structure

| Decision | Reason |
|---|---|
| Tech Lab as its own top-nav page | The AI features ARE the brand. Don't bury them under About or Learn. |
| All 4 tech features on one page (anchored) | Reduces cognitive load vs. 4 separate pages. Users explore naturally. |
| Learn is content-only, no tech | Clean separation: "experience" vs. "consume." Avoids confusion. |
| About comes before Connect, not after Home | Trust must be built before conversion. About is a mid-funnel stop. |
| Chatbot sticky across all pages | Makes the most interactive feature always accessible — core to the brand. |
| Anchor links (#section) not sub-pages | Keeps the nav count low; works better on mobile; faster to load. |

---

## UX Recommendations

1. **Entry choice on Home:** Add a 3-way "What brings you here?" selector (Student / Educator / Just Curious) that routes users to a recommended starting page. Reduces overwhelm.

2. **Progress hint on Tech Lab:** Show a "1 of 4 experiences" indicator so users know there's more to scroll — prevents drop-off after first feature.

3. **Gated e-book with email capture:** Offer the e-book free in exchange for email → grows [Name]'s list while giving users immediate value.

4. **AI Twin intro video on Home:** A 15-second clip of the AI Twin speaking is more convincing than any copy. Put it above the fold or as the hero background.

5. **Accessibility:** Ensure the voice chatbot has a visible text fallback. Gen Z is fine with voice, but educators may be in quiet environments.

6. **Mobile-first load order:** Load the chatbot bubble last (deferred JS) so the page feels fast. First impression speed matters for Gen Z users.

---

## Page Count Summary

| Page | URL | Priority |
|---|---|---|
| Home | / | P0 |
| Tech Lab | /tech-lab | P0 |
| Learn | /learn | P0 |
| About | /about | P1 |
| Connect | /connect | P1 |

**5 top-level pages. All content lives within them via anchor sections.**
