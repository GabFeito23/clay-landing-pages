# Clay Personalized Landing Pages — Project Brief

## What We're Building
Personalized landing pages for 10 prospects, each showing how Clay.com can help their specific company and role. One HTML file per prospect, all sharing a common CSS/JS asset layer. A hub `index.html` links to all 10 pages.

## Project Decisions (Already Agreed)
- **Personalization:** Research each company, address prospect by first name, tailor messaging to their job title and company context
- **Tech:** Individual HTML files per prospect, no build script needed, styles inlined per page
- **CTA:** "Book a Meeting" → `https://clay.com/demo`
- **Design:** Modern dark theme (`#07070D` bg, orange-to-amber gradient accents `#F97316 → #FCD34D`, Bricolage Grotesque + Outfit + JetBrains Mono fonts) — inspired by Clay but not a copy
- **Hosting:** Vercel — `https://clay-landing-pages-blue.vercel.app`
- **GitHub:** `https://github.com/GabFeito23/clay-landing-pages` (public, connected to Vercel)
- **Vercel project name:** `clay-landing-pages` (deployed via CLI, auto-aliased to `-blue`)

## Deployment
- **Vercel CLI** is used to deploy (`npx vercel --prod --yes`)
- GitHub is connected but auto-deploy was not set up — deploy manually via CLI
- `vercel.json` uses `cleanUrls: true` and `trailingSlash: false` — pages are served without `.html`
- Root `/` serves `index.html` (the hub page)

## Live URLs
| Page | URL |
|------|-----|
| Hub | `https://clay-landing-pages-blue.vercel.app` |
| Sarah Mitchell | `https://clay-landing-pages-blue.vercel.app/sarah-mitchell-retool` |
| Marcus Chen | `https://clay-landing-pages-blue.vercel.app/marcus-chen-linear` |
| Emily Rodriguez | `https://clay-landing-pages-blue.vercel.app/emily-rodriguez-loom` |
| James Okonkwo | `https://clay-landing-pages-blue.vercel.app/james-okonkwo-webflow` |
| Rachel Goldstein | `https://clay-landing-pages-blue.vercel.app/rachel-goldstein-airtable` |
| David Park | `https://clay-landing-pages-blue.vercel.app/david-park-monday` |
| Amanda Sullivan | `https://clay-landing-pages-blue.vercel.app/amanda-sullivan-asana` |
| Kevin Nakamura | `https://clay-landing-pages-blue.vercel.app/kevin-nakamura-mixpanel` |
| Jessica Thompson | `https://clay-landing-pages-blue.vercel.app/jessica-thompson-amplitude` |
| Michael Santos | `https://clay-landing-pages-blue.vercel.app/michael-santos-calendly` |

## File Structure
```
LandPagesCohort2/
├── CLAUDE.md                          ← this file
├── vercel.json                        ← cleanUrls + trailingSlash config
├── clay_value_prop.txt                ← Clay's value proposition reference
├── clay_icp.txt                       ← Clay's ICP reference
├── landing-page-prospects.csv        ← 10 prospects with live URLs
├── index.html                         ← Hub page — links all 10 prospect pages
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

## Page Structure (Each Prospect Page Has)
1. **Sticky Nav** — Clay logo (gradient text) + "Book a Meeting" CTA button
2. **Hero** — Personalized headline with prospect's first name + company context, subheadline, two CTAs
3. **Logos Strip** — "Trusted by" bar with Clay's real customers (OpenAI, Ramp, Notion, etc.)
4. **Pain Points** — 3 cards, tailored to their job title and company situation
5. **Features (4 cards)** — Clay capabilities framed through their role's lens
6. **Stats** — 4 animated counters (3x enrichment, 80% time saved, 5000+ customers, 150+ providers)
7. **Testimonial** — Quote from a peer persona matching their role
8. **Final CTA Banner** — Personalized closing line + "Book a Meeting"
9. **Footer** — Clay logo + copyright

## Design System
- **Background:** `#07070D` (deep dark), `#0B0B16` (surface layer)
- **Cards:** `rgba(255,255,255,0.03)` bg with `rgba(255,255,255,0.07)` border
- **Accent gradient:** `#F97316` (orange) → `#FCD34D` (amber)
- **Text:** `#EEF2FF` primary, `#8B95A8` secondary, `#3C4557` muted
- **Fonts:** Bricolage Grotesque (display/headings), Outfit (body), JetBrains Mono (labels/mono)
- **Animations:** `.r` + `.in` classes via IntersectionObserver for fade-up reveals
- **Film grain:** Fixed `body::after` SVG noise overlay at 0.45 opacity
- **Buttons:** Orange primary with glow shadow, ghost border secondary

## Current Status
All 10 pages + hub index are built and live on Vercel.

| File | Status |
|------|--------|
| index.html | DONE ✅ — live |
| sarah-mitchell-retool.html | DONE ✅ — live |
| marcus-chen-linear.html | DONE ✅ — live |
| emily-rodriguez-loom.html | DONE ✅ — live |
| james-okonkwo-webflow.html | DONE ✅ — live |
| rachel-goldstein-airtable.html | DONE ✅ — live |
| david-park-monday.html | DONE ✅ — live |
| amanda-sullivan-asana.html | DONE ✅ — live |
| kevin-nakamura-mixpanel.html | DONE ✅ — live |
| jessica-thompson-amplitude.html | DONE ✅ — live |
| michael-santos-calendly.html | DONE ✅ — live |

## Personalization Notes Per Prospect

**Sarah Mitchell — Retool — VP of Revenue Operations**
- Retool is a dev tooling company with a complex GTM. Focus on CRM hygiene, consolidating enrichment tools, automating RevOps workflows.

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
