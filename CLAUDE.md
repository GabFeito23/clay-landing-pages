# Clay Personalized Landing Pages — Project Brief

## What We're Building
Personalized landing pages for 10 prospects, each showing how Clay.com can help their specific company and role. One HTML file per prospect, all sharing a common CSS/JS asset layer.

## Project Decisions (Already Agreed)
- **Personalization:** Research each company, address prospect by first name, tailor messaging to their job title and company context
- **Tech:** Split assets (shared CSS + JS), individual HTML files per prospect, no build script needed
- **CTA:** "Book a Meeting" → `https://clay.com/demo`
- **Design:** Modern dark theme (deep navy-black bg, purple-to-cyan gradient accents, Inter font) — inspired by Clay but not a copy
- **Hosting:** Local files for now, can configure deployment later

## File Structure
```
LandPagesCohort2/
├── CLAUDE.md                          ← this file
├── clay_value_prop.txt                ← Clay's value proposition reference
├── clay_icp.txt                       ← Clay's ICP reference
├── landing-page-prospects.csv        ← 10 prospects
├── assets/
│   ├── css/styles.css                ← shared styles (DONE)
│   └── js/main.js                    ← shared JS / animations (DONE)
├── sarah-mitchell-retool.html        ← DONE ✅
├── marcus-chen-linear.html           ← DONE ✅
├── emily-rodriguez-loom.html         ← DONE ✅
├── james-okonkwo-webflow.html        ← DONE ✅
├── rachel-goldstein-airtable.html    ← DONE ✅
├── david-park-monday.html            ← DONE ✅
├── amanda-sullivan-asana.html        ← DONE ✅
├── kevin-nakamura-mixpanel.html      ← DONE ✅
├── jessica-thompson-amplitude.html   ← DONE ✅
└── michael-santos-calendly.html      ← DONE ✅
```

## Prospects List
| Name | Title | Company | Website |
|------|-------|---------|---------|
| Sarah Mitchell | VP of Revenue Operations | Retool | retool.com |
| Marcus Chen | Head of Growth | Linear | linear.app |
| Emily Rodriguez | Director of Sales Development | Loom | loom.com |
| James Okonkwo | GTM Engineer | Webflow | webflow.com |
| Rachel Goldstein | VP of Sales | Airtable | airtable.com |
| David Park | Head of Revenue Operations | monday.com | monday.com |
| Amanda Sullivan | Director of Growth Marketing | Asana | asana.com |
| Kevin Nakamura | VP of Marketing | Mixpanel | mixpanel.com |
| Jessica Thompson | Head of Demand Generation | Amplitude | amplitude.com |
| Michael Santos | Director of RevOps | Calendly | calendly.com |

## Page Structure (Each Page Has)
1. **Sticky Nav** — Clay logo (gradient text) + "Book a Meeting" CTA button
2. **Hero** — Personalized headline with prospect's first name + company context, subheadline, two CTAs
3. **Logos Strip** — "Trusted by" bar with Clay's real customers (OpenAI, Ramp, Notion, etc.)
4. **Pain Points** — 3 cards, tailored to their job title and company situation
5. **Features (4 cards)** — Clay capabilities framed through their role's lens
6. **Stats** — 4 animated counters (3x enrichment, 80% time saved, 5000+ customers, 150+ providers)
7. **Testimonial** — Quote from a peer persona matching their role
8. **Final CTA Banner** — Personalized closing line + "Book a Meeting"
9. **Footer** — Clay logo + copyright

## Design System (styles.css)
- **Background:** `#07070e` (deep dark)
- **Cards:** `#0f0f1c` with `rgba(255,255,255,0.07)` border
- **Accent gradient:** `#7c3aed` (purple) → `#06b6d4` (cyan)
- **Text gradient:** `#a78bfa` → `#22d3ee`
- **Font:** Inter (Google Fonts), weights 300–900
- **Animations:** `.fade-up` class + IntersectionObserver, animated stat counters

## Current Status
All 10 pages are built. Deployment to Vercel is pending.

| File | Status |
|------|--------|
| sarah-mitchell-retool.html | DONE ✅ |
| marcus-chen-linear.html | DONE ✅ |
| emily-rodriguez-loom.html | DONE ✅ |
| james-okonkwo-webflow.html | DONE ✅ |
| rachel-goldstein-airtable.html | DONE ✅ |
| david-park-monday.html | DONE ✅ |
| amanda-sullivan-asana.html | DONE ✅ |
| kevin-nakamura-mixpanel.html | DONE ✅ |
| jessica-thompson-amplitude.html | DONE ✅ |
| michael-santos-calendly.html | DONE ✅ |

**Hosting:** Vercel — production URL: `https://clay-sarah-retool-ruby.vercel.app`
Root `/` routes to Sarah Mitchell's page. Each prospect's page is at `/<filename>.html`.

## Personalization Notes Per Remaining Prospect

**Marcus Chen — Linear — Head of Growth**
- Linear is a PLG issue-tracking tool beloved by engineers. Focus on converting product-led interest into enterprise pipeline, enriching trial signups, intent signals.

**Emily Rodriguez — Loom — Director of Sales Development**
- Loom (acquired by Atlassian) has an SDR-heavy outbound motion. Focus on SDRs spending too much time on research, personalization at scale, enrichment gaps.

**James Okonkwo — Webflow — GTM Engineer**
- GTM Engineer = technical champion. Speak to API access, webhook integrations, waterfall logic, Claygent for custom workflows. He builds the stack, not just uses it.

**Rachel Goldstein — Airtable — VP of Sales**
- VP Sales owns quota. Focus on pipeline quality, accurate data = better conversion, reps not wasting cycles on bad leads, missing timing signals.

**David Park — monday.com — Head of Revenue Operations**
- monday.com is publicly traded, scaling enterprise. Focus on consolidating point solutions, CRM hygiene, single source of GTM truth.

**Amanda Sullivan — Asana — Director of Growth Marketing**
- Growth Marketing = ABM and demand gen. Focus on account-level enrichment, intent signals to trigger campaigns, personalization at scale across ads/email/landing pages.

**Kevin Nakamura — Mixpanel — VP of Marketing**
- Analytics company = data-savvy audience. Speak their language. Focus on precision targeting, building ICP lists, intent signals for campaign timing.

**Jessica Thompson — Amplitude — Head of Demand Generation**
- Demand gen = MQL volume and inbound pipeline. Focus on real-time inbound enrichment, lead scoring and routing, speed-to-lead.

**Michael Santos — Calendly — Director of RevOps**
- Calendly sells scheduling automation — ironic if their own RevOps is manual. Focus on CRM data hygiene, consolidating fragmented tools, automating RevOps processes.
