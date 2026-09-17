---
title: Agent instructions
description: How to navigate this repository as a read-only marketing knowledge wiki.
---

# Agent instructions

This repository is a portable, read-only marketing knowledge wiki: plain Markdown files linked to each other. **No server, MCP connection, or installed tool of any kind is required or expected.** Open the repository (locally, via `git clone`, or through the GitHub UI/API) and navigate by reading files and following the relative links inside them, the same way you would follow links in an online wiki.

## Where to start

1. [`index.md`](./index.md) — the repository's front door.
2. [`knowledge/index.md`](./knowledge/index.md) — the table of contents for the corpus: one entry per chapter, plus a set of cross-chapter records.
3. [`knowledge/cross-chapter-authority-map.md`](./knowledge/cross-chapter-authority-map.md) — start here instead when a question could span more than one chapter or concept. It names the preferred detailed record for overlapping topics.

From either starting point, follow `[text](./path.md)`-style links to move between documents. Every chapter folder (`knowledge/chapter-NN-*/`) has its own `index.md` listing that chapter's concept files.

## Routing a user's question to the right knowledge

Do this before opening any concept file — it narrows 132 files down to a handful.

**Step 1 — match the question's topic to a chapter below.** Match on meaning, not exact wording.

| If the question is mainly about... | Start in |
| --- | --- |
| What a marketing role/executive is responsible for, marketing decisions | `knowledge/chapter-01-marketing-executive-role/` |
| How buyers choose, memory, mental availability, repertoires, loyalty, buyer evidence | `knowledge/chapter-02-buyer-behaviour/` |
| Measuring marketing performance, KPIs, metric validity, causal claims | `knowledge/chapter-03-marketing-metrics/` |
| Designing research, sampling, qualitative/quantitative methods | `knowledge/chapter-04-market-research/` |
| External forces on the business: competitors, economy, technology, culture, SWOT | `knowledge/chapter-05-marketing-environment/` |
| Segmentation, targeting, who to sell to, broad vs. narrow reach | `knowledge/chapter-06-segmentation-and-targeting/` |
| Product/offer design, features, innovation, product lifecycle | `knowledge/chapter-07-product-offer-management/` |
| Retail, distribution, channels, making purchase easy | `knowledge/chapter-08-physical-availability-retailing/` |
| Pricing, discounts, elasticity, promotions | `knowledge/chapter-09-pricing-and-discounting/` |
| Sales, B2B selling, key accounts, sales-team management | `knowledge/chapter-10-selling-and-sales-management/` |
| Advertising, creative briefing, ad research/effectiveness | `knowledge/chapter-11-advertising/` |
| Media planning, reach/frequency, channel/media selection | `knowledge/chapter-12-media-decisions/` |
| Writing or executing a marketing plan, implementation, control | `knowledge/chapter-13-marketing-planning/` |
| International/global marketing, standardisation vs. localisation | `knowledge/chapter-14-global-marketing/` |
| Ethics, corporate social responsibility, stakeholders | `knowledge/chapter-15-ethics-and-social-responsibility/` |
| Social marketing, behaviour-change campaigns | `knowledge/chapter-16-social-marketing/` |
| The question spans more than one row, or none fit clearly | Skip to [`knowledge/cross-chapter-authority-map.md`](./knowledge/cross-chapter-authority-map.md) instead |

**Step 2 — open that chapter's `index.md`** (e.g. `knowledge/chapter-02-buyer-behaviour/index.md`) and scan its list of concept files and one-line descriptions for the closest match.

**Step 3 — if the question overlaps more than one topic** (e.g. "how do I price my product to reach light buyers" touches both pricing and buyer behaviour), check [`knowledge/cross-chapter-authority-map.md`](./knowledge/cross-chapter-authority-map.md) before picking a file yourself. It already resolves which chapter's record is the preferred authority when topics overlap — use that instead of merging two records on your own judgement.

**Step 4 — open the matched concept file(s)** and confirm fit against its frontmatter `description` and `tags` before treating it as the answer.

**Step 5 — follow `Related` links** only for adjacent concepts the question genuinely needs — don't pull in unrelated files just because they're linked.

## How one knowledge file is structured

Every file under `knowledge/` carries YAML frontmatter followed by a body with a predictable shape. This is the whole contract — there is no external schema or app to consult:

- **Frontmatter**: `type`, `title`, `description`, `tags`, and a `sources` entry (`id` plus an internal `resource` link — never an external URL or named work).
- **Core statement / Definitions** — the concept in plain terms.
- **Mechanism and relationships** — how it works and what it connects to.
- **Evidence and data requirements**, **Conditions and limits** — what supports the claim and where it stops applying.
- **Decision implications** — bounded, conditional next actions.
- **Related** — links to sibling concept files worth reading next. Follow these to explore adjacent knowledge.
- Numbered footnotes at the bottom (e.g. `[^mechanism]`) cite the file named in `sources[].resource`, with a chapter/page locator. The source's bibliographic identity is intentionally not disclosed anywhere in this release — locators exist only as internal traceability.

## Checking the wiki holds together (linting)

There is no bundled linter or app dependency. To check the wiki is well-formed, an agent or script needs only three things, all checkable by reading plain text:

1. Every `.md` file under `knowledge/` has frontmatter with at least `type`, `title`, and `description`.
2. Every relative Markdown link (`[text](./path.md)`) resolves to a file that actually exists in the repository.
3. Every footnote reference in a file's body (`[^id]`) has a matching `[^id]: ...` definition in that same file.

A quick manual spot-check when in doubt: open the linked target and confirm it exists and is itself a knowledge file with frontmatter — the same way you'd verify any wiki link.

## What counts as knowledge, and what doesn't

Only files under `knowledge/` are approved marketing evidence. `index.md` and this file are navigation aids, not evidence — do not cite them as a source for a marketing claim.

## Once you've found the record(s): how to answer

1. Answer the user's actual question — don't just summarize the record.
2. Separate what the retrieved record actually supports from your own inference, and say so explicitly.
3. Name the specific file(s) you used when giving a substantive answer (e.g. "per `chapter-09-pricing-and-discounting/price-elasticity-promotions-and-segmentation.md`").
4. State material limits or conditions the record itself names — don't drop them for a cleaner-sounding answer.
5. If the corpus doesn't support an answer, say that plainly rather than filling the gap from general knowledge.
