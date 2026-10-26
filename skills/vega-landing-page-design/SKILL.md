---
name: vega-landing-page-design
description: "VegaShares ETFs version of landing-page-design: builds or restyles a landing page, fund page mockup, campaign page, page section, or web prototype for VegaShares (vegasharesetfs.com) in the VegaShares brand (Poppins, Vega Blue #0055FF, Deep Navy #0A0E27) with ETF marketing compliance guardrails. Covers intake, page structure, copy, SEO, and the visual system (type, color, spacing, radius, icons, motion). Use when building, mocking up, styling, or reviewing any VegaShares web page or section, a fund page (XSPC, VAIE, VAIC, ODTE, COOL, CGPT, AIJR, TRIL, CLBL), a launch or campaign landing page, or an education page, even if the user does not say 'design'. Not for non-VegaShares projects."
---

# VegaShares Landing Page Design

A landing page is not a homepage. A homepage serves multiple intents. A landing page wins one intent:

**one fund or idea → one audience → one primary action.**

This skill has three parts. **The brand block** holds every VegaShares value. **Part A** decides what the page says and how it is structured. **Part B** is the visual system, and every value in it resolves through the brand block. Work through A before touching B.

## Scope

Apply to VegaShares web work: fund pages and fund page mockups, launch and campaign landing pages, education pages, page sections, components, prototypes, and design reviews. When a rule here conflicts with a framework default, this file wins. When the user's explicit prompt conflicts with a rule, the user wins, except for the compliance rules in A0, which are never relaxed without the user saying so in so many words.

When the work is a change to the live site, the site's existing components and tokens come first; use this file to fill gaps and to check consistency.

**Companion skills.** `vega-design-to-motion` for animating visuals on the page. The `fund-seo` skill, when installed, owns titles, meta descriptions and schema. For upgrading an existing site in general, see [elayadesign/redesign-skill](https://github.com/elayadesign/redesign-skill).

---

# VegaShares brand

Source: the Vega Brand Guide PDF in the brand guide folder (see the project CLAUDE.md for where it lives). If the guide and this block ever disagree, the guide wins; update this block.

## Color

| Token | Hex | Use |
|---|---|---|
| `--vega-blue` | `#0055FF` | Primary brand color. CTAs, accents, key moments. Use it strategically, not everywhere |
| `--deep-navy` | `#0A0E27` | Primary dark. Dark backgrounds, headers, body text on light |
| `--slate-navy` | `#151932` | Secondary dark. Raised surfaces and alternate sections on dark |
| `--medium-gray` | `#666666` | Body text on light backgrounds |
| `--light-gray` | `#F8F9FA` | Subtle backgrounds, section dividers, cards on white |
| `--white` | `#FFFFFF` | Breathing room. Use liberally |

**Bold but calm.** Navy and white do the heavy lifting. Blue appears where it should feel intentional and powerful: the primary CTA, one highlighted phrase, an active state, a key data point. **One bold blue moment per view** is the target.

**Never** add colors outside this table (no greens, purples, oranges, rainbow charts). Charts use blue, navy, and grays; if a chart truly needs more series, use tints of Vega Blue and the grays. Functional colors for form errors are the one exception, and only on the error text and border.

## Typography

**Primary font: Poppins.** One typeface for the interface.

| Role | Weight | Size |
|---|---|---|
| Hero statements, major headings | Bold 700 | 48px and up (`text-5xl` or larger) |
| Section titles | Semibold 600 | `text-3xl` to `text-4xl` |
| Subheadings, supporting headlines, pull quotes | Regular 400 | `text-xl` to `text-2xl` |
| Body copy, descriptions, long form | Light 300 | 16px, line height 1.6 |
| Buttons | Semibold 600 | `text-base` (main), `text-sm` (header) |

- **Tighten headlines** by 1 to 2px of letter spacing (`tracking-tight` or `-0.02em`).
- **Hierarchy comes from size and weight, not color.** Do not color a heading blue to make it important.
- **Allowed accents** (approved for VegaShares pages, use sparingly):
  - **Instrument Serif italic** for one or two words inside a hero or section headline, as a flourish. Never for whole headings or body.
  - **Geist Mono** for tickers, data labels, fund facts tables, and numeric UI where tabular figures help.
- **Never use:** Inter, Roboto, Arial, Open Sans, Helvetica. **Never** weights above 700.
- Load Poppins 300, 400, 600, 700 from Google Fonts unless the site already self hosts it.

## Logo

- Use the official logo files only (VegaShares ETFs primary logo, or the "V" mark). Never redraw, retype, recolor, or approximate the logo in SVG or CSS. If the file is not available in the build, leave a clearly labelled placeholder box.
- **Primary** (blue V) on white or light backgrounds. **Reversed** (white) on dark navy. **Accent** (white on Vega Blue) only for special applications.
- **Clear space** around the logo equals the height of the "V" on all sides. Never crowd it.
- Where the files live: see "Brand guide + logos" in the project CLAUDE.md. The website folder holds the official SVGs.

## Brand don'ts

- No gradient backgrounds. Backgrounds are flat navy, white, or light gray.
- No extra colors (see Color).
- No crowded logo.
- No gradient text. The hero heading is solid color (B5).

---

# PART A: Strategy, structure, and compliance

## A0. Compliance (read first)

Every public string on a VegaShares page is fund marketing material and goes through compliance review before it is published. The page you build is a draft for co-founder and compliance review, never a final.

- **Never invent fund data.** Expense ratios, yields, distribution rates, AUM, performance, holdings, inception dates, and index names come from the live fund page or the fund documents. If you do not have the number, use a labelled placeholder such as `[30-day SEC yield, from fund page]`. This overrides any instinct toward "realistic sample numbers".
- **Never write, edit, or shorten risk disclosures, performance tables, or prospectus language.** Reuse the exact disclosure blocks from the live site, or leave a labelled `[Required disclosures]` slot. Do not add disclosures that are not required.
- **No testimonials, endorsements, or client quotes** unless the user supplies an approved one.
- **No promissory language:** never "guaranteed", "safe", "risk free", "protects your portfolio", "can't lose", "beat the market", or forecasts of returns. Income language says what the fund seeks or aims to do, not what it will pay.
- **Name the fund in full at first mention**, followed by the ticker: "VegaShares [Fund Name] ETF (TICKER)". Never lead with a bare ticker.
- **Prospectus access** is part of every fund page: a clear link to the prospectus and fact sheet near the fund facts and in the footer.
- Follow any further house rules in the project CLAUDE.md and memory (fund specific wording, positioning).

## A1. Intake

Gather these before designing or writing. Ask only for what is missing, in one batch.

**Purpose**
- Which fund, fund family, or idea is the page about?
- What is the ONE primary action? (view the fund page, read the prospectus, download the fact sheet, subscribe to updates, contact the team)
- What counts as a conversion?

**Audience and context**
- Financial advisors, self directed investors, or both?
- What question are they trying to answer? (what is this fund, how does it generate income, how does it fit a portfolio)
- Top three objections or confusions
- Traffic source: social, search, email, press
- What do visitors already know when they land?

**Assets**
- Approved graphics, charts, holdings tiles, or photography
- The live fund page URL, so facts and disclosures can be copied exactly
- Any approved quotes from VegaShares leadership

If the user cannot answer, make a reasonable assumption, state it in one line, and continue. Do not stall the build.

## A2. Page structure

**Above the fold (required)**
1. Headline: what the fund does, for whom
2. Subheadline: how it does it, in plain English
3. Primary CTA: clear verb plus what they get
4. One credibility signal: ticker and exchange, a sourced fund fact, or an "as seen in" press strip
5. Hero visual: an approved graphic, a chart from real data, or a labelled placeholder

**Mid page (the explanation)**
6. The idea or problem the fund addresses, one section
7. How the fund works, three steps in plain English
8. Key features, three to five, each tied to how the fund is built
9. Fund facts: a table of sourced figures with an "as of" date

**Bottom**
10. FAQ, six to twelve questions
11. Risks and required disclosures, exactly as on the live site
12. Final CTA, identical to the top, plus the prospectus link

The tagline reveal section (B11) is optional; use it on launch and education pages, placed after "How it works".

## A3. Layout selection

Pick one and say why.

| Type | Use when |
|---|---|
| **A. Classic hero plus sections** | A single fund page or launch page. Most common. |
| **B. Long form story** | Education pages that explain a theme or strategy before the fund. |
| **C. Minimal page** | Email driven traffic with one action, such as a webinar signup or a fact sheet download. |
| **D. Comparison page** | Search intent includes alternatives ("covered call ETF vs dividend ETF"). Compare structures factually; never disparage another issuer. |

## A4. Conversion rules

**Match message to source.** If traffic comes from a social post, mirror the post's headline and keep the same promise and visual.

**One primary CTA.** Never place competing CTAs above the fold.

**Explain before you sell.** Investors convert when they understand the mechanism. Lead with what the fund holds and how it seeks its objective.

**Be specific, with sourced specifics.**
- ❌ "Earn more income"
- ✅ "Seeks weekly distributions from an options strategy on [index]", with the strategy wording taken from the fund page

**Treat confusion as a section, not a footnote.** Move the FAQ earlier for complex strategies. Put the source and "as of" date directly beside any number.

## A5. Copywriting

**Voice.** Clear, confident, plain English. Professional, never hype.

**Headline formulas**
- "{What the fund does} for {audience}"
- "{Theme} in one ETF"
- "How {strategy} works"

**Subheadline.** One or two sentences: what it is and who it is for.

**CTA.** Verb plus what they get. Never "Learn more" or "Submit". Use "View the fund", "Read the prospectus", "Get the fact sheet".

**Feature bullets.** Bold feature, then the plain explanation. Example: **Weekly distributions**: the fund seeks to pay distributions every week, in the fund page's own wording.

## A6. Build order

Work section by section, in this order:

1. Hero
2. How it works
3. Key features
4. Fund facts
5. FAQ
6. Disclosures and final CTA

Never rebuild the whole page on each iteration.

## A7. SEO and AEO

Defer to the `fund-seo` skill for titles, meta descriptions, schema, and keyword choices. Without it: index evergreen fund and education pages, noindex time bound campaign pages, and write the FAQ in plain question and answer form.

## A8. Pitfalls

- Too many CTAs above the fold
- Jargon without explanation ("synthetic covered call", "0DTE") on a page for general investors
- Numbers without a source or "as of" date
- Disclosures rewritten, shortened, or missing
- Blue used everywhere so nothing stands out
- Mobile layout that breaks readability, especially fund facts tables

---

# PART B: Visual system

Every visual value resolves through the brand block and these rules, never ad hoc.

## B1. Typography

Fonts, weights and roles come from the brand block.

### Copy rules

- **No em dashes or en dashes** in copy. Rewrite with a comma, colon, or a new sentence. Ordinary hyphens in compound words and in a quote attribution ("... value - Name") are fine.
- **No orphaned words.** Apply `text-wrap: balance` for headings and `text-wrap: pretty` for body copy.
- **Sentence case** for headings and buttons. Fund names and tickers keep their official capitalization.

### Type scale

Resolve font sizes to Tailwind's default type scale. Never leave arbitrary values such as `text-[19px]` or `font-size: 22px`. If a size does not land on a step, snap it to the closest step below.

| Class | Size | Line height |
|---|---|---|
| `text-xs` | 12px | 16px |
| `text-sm` | 14px | 20px |
| `text-base` | 16px | 24px (body copy: 1.6, per brand) |
| `text-lg` | 18px | 28px |
| `text-xl` | 20px | 28px |
| `text-2xl` | 24px | 32px |
| `text-3xl` | 30px | 36px |
| `text-4xl` | 36px | 40px |
| `text-5xl` | 48px | 1 |
| `text-6xl` | 60px | 1 |
| `text-7xl` | 72px | 1 |

The one sanctioned exception is body copy at 16px with a 1.6 line height, from the brand guide.

Fine print (disclosures, footnotes, "as of" lines) is `text-xs` or `text-sm` in Medium Gray on light, or white at 70% on dark, and must stay readable.

## B2. Spacing

Only these values.

| Token | Value |
|---|---|
| Spacing-0 | 0 |
| Spacing-25 | 2px |
| Spacing-50 | 4px |
| Spacing-75 | 8px |
| Spacing-100 | 12px |
| Spacing-200 | 16px |
| Spacing-300 | 24px |
| Spacing-400 | 32px |
| Spacing-500 | 40px |
| Spacing-600 | 48px |
| Spacing-700 | 64px |
| Spacing-800 | 80px |
| Spacing-900 | 96px |

**Main buttons:** 12px vertical padding, 24px horizontal padding. Sections breathe: at least 80px between major sections on desktop, 48px on mobile.

## B3. Corner radius

Only Tailwind radius values. Cards `rounded-xl` or `rounded-2xl`, buttons `rounded-lg`, chips `rounded-full`.

**Nested radius formula.** When a shape sits inside another and the gap is less than 32px: `inner radius = outer radius − gap`, applied only when the result is greater than 2.

## B4. Borders and backgrounds

- Backgrounds are flat: White, Light Gray, Deep Navy, or Slate Navy. Never gradients.
- Alternate light and dark sections to pace a long page; dark sections use Deep Navy with Slate Navy cards.
- Borders go all the way around a card or not at all. Use a 1px border in `#0A0E27` at 8 to 10% on light, or white at 10% on dark.
- Photography may sit behind a dark navy overlay; the overlay is flat, not a gradient.

## B5. Hero section

### Heading color

- **Light theme:** Deep Navy `#0A0E27`, solid.
- **Dark theme:** White, solid.
- Optionally set one key phrase in Vega Blue, or in Instrument Serif italic. Not both on the same phrase, and never more than one phrase.

### Layout

- Heading and subheading capped at **680px** wide.
- Break heading lines where the thought breaks, never mid phrase.
- The primary CTA is a solid Vega Blue button with white text. A secondary action, if any, is a text link or an outline button, never a second blue button.

## B6. Icons

**Use:** Phosphor, Solar, or Iconamoon, in a single weight across the page, colored navy, gray, or white. Blue only on an active or highlighted item.

**Never use:** Material Icons, Material Symbols, emoji as icons.

**No hand drawn illustrations.** Do not draw scenes, objects, or decorative illustrations in SVG. Use approved photography or graphics, or a labelled placeholder. SVG is for true diagrams and charts only.

## B7. Motion

Motion is calm and decelerates into place. Never ship a browser default curve (`ease`, `linear`, `ease-in-out`).

**Base curve:** `cubic-bezier(0.22, 1, 0.36, 1)` with 500ms for layout and position changes. Hover color and opacity shifts use 300ms, never under 200ms.

Animate only `transform` and `opacity`. Respect `prefers-reduced-motion` with a plain opacity change.

### Navigation

A compact bar, translucent Deep Navy (or white on light pages) over a background blur, with the logo at left respecting its clear space. The menu toggle animates between states. The mobile menu opens as a full height panel; links fade up 24px one after another, 60ms apart, capped at 400ms total.

### Scroll reveals

Sections rise 32px and fade in over 600 to 800ms on the base curve, once. Use `IntersectionObserver` or Framer Motion's `whileInView`, never an unthrottled scroll listener.

For animated charts, cards, and product visuals, use `vega-design-to-motion` (website context).

## B8. Content realism

- **Write the copy.** No placeholder Latin. Draft real sentences in the VegaShares voice.
- **Facts are sourced or placeholdered** (A0). Never invent a figure to make a mockup look real. Placeholders are visibly labelled so they cannot ship by accident.
- **People.** Only real, approved VegaShares team members and quotes. No invented testimonials or customers.
- **Banned filler words:** "revolutionize", "supercharge", "cutting edge", "game changing", "effortless", "unlock", "harness the power", "world class", "next level".
- **System messages** are calm and specific. Errors say what failed and what to do next. No exclamation marks.

## B9. States

Every interactive element ships with hover, active (`scale(0.98)`), a visible focus ring in Vega Blue, loading (skeletons shaped like the layout), empty, and inline error states. Never `window.alert()`.

No dead links. A link with no destination yet is visibly marked as a placeholder. The current page is indicated in the navigation.

## B10. Ship requirements

- Prospectus, fact sheet, and holdings links for every fund mentioned
- Required disclosures and distributor language exactly as on the live site, in the footer and wherever the live site places them
- Privacy policy and terms links
- `<title>`, meta description, `og:image`, social sharing tags (see A7)
- Alt text on every meaningful image; charts get a text summary
- Semantic HTML, a skip to content link, keyboard focus order that matches the visual order
- Color contrast at WCAG AA: Vega Blue on white passes for large text and buttons; for small body text use Deep Navy or Medium Gray
- A branded favicon (the "V" mark)

## B11. Tagline reveal section (optional)

One large type section stating the core idea in two or more lines, separate from the hero.

- `text-4xl` to `text-6xl`, Poppins Semibold, capped at 680px, meaningful line breaks.
- Words start at about 25 to 35% opacity of the text color and turn full color one at a time, in reading order, as they cross a trigger line. The final key word may land in Vega Blue.
- Use `IntersectionObserver` per word or a `requestAnimationFrame` throttled listener.

---

# Output format

When generating a page from scratch, return these before writing code:

1. **Page outline**: sections and order
2. **Hero copy**: headline, subheadline, CTA, credibility line
3. **How it works**: three steps
4. **Key features**: three to five
5. **Fund facts needed**: the list of figures to pull from the live page, with their placeholders
6. **FAQ**: six to twelve questions and answers
7. **SEO / AEO**: index or noindex, plus title and meta if indexed
8. **Layout recommendation**: A, B, C, or D, and why

Then build section by section per A6. When done, list every placeholder still on the page and remind the user that the copy needs compliance review before it is published.

---

# Quick checklist

**Compliance**
- [ ] No invented numbers; every figure sourced with an "as of" date, or a labelled placeholder
- [ ] Disclosures copied exactly or left as a labelled slot; none rewritten or added
- [ ] No testimonials, no promissory language
- [ ] Full fund name and ticker at first mention
- [ ] Prospectus and fact sheet links present

**Brand**
- [ ] Poppins only, plus approved accents (Instrument Serif italic phrase, Geist Mono data)
- [ ] Colors only from the brand table; one bold blue moment per view
- [ ] No gradients anywhere, no gradient text
- [ ] Official logo file with clear space, correct version for the background
- [ ] No hand drawn SVG illustrations

**Visual**
- [ ] No em or en dashes in copy, no orphaned words
- [ ] Sizes on the Tailwind scale; spacing from the table; nested radii follow the formula
- [ ] Hero heading and subheading capped at 680px
- [ ] Icons from Phosphor, Solar, or Iconamoon
- [ ] Transitions use the base curve; scroll reveals use IntersectionObserver

**Ship**
- [ ] Hover, active, focus, loading, empty, and error states
- [ ] No dead links, current nav item indicated
- [ ] Meta tags, alt text, contrast, favicon

---

## Credits

Adapted for VegaShares ETFs from `landing-page-design` in [elayadesign/ai-design-skills](https://github.com/elayadesign/ai-design-skills), MIT licensed.

Parts of the original skill were adapted from [taste-skill](https://github.com/Leonxlnx/taste-skill) by Leon Lin ([@LexnLin](https://x.com/LexnLin)), MIT licensed. Its redesign audit structure, content realism checks, and motion and navigation ideas informed the matching sections, which have since been rewritten.

<details>
<summary>taste-skill license</summary>

```
MIT License

Copyright (c) 2026 Leonxlnx

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
</details>
