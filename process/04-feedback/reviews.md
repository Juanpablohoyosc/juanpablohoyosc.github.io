# Review round, September 23, 2026

Three passes on v1 plus the new links page, before any fixes. Everything here was found by Claude playing three different roles; an outside review from a second tool is in `cross-tool-review-prompt.md`.

## Pass 1 — Campus recruiter (15 seconds on a phone, 60 on a laptop)

**What sticks in 15 seconds:** the name, "finance and financial analytics", and that he builds Python tools that measure portfolio risk.

**What's missing in those 15 seconds:** on a phone the role he wants and his graduation date sit below the fold, under the buttons. The one thing a recruiter needs first, "what are you looking for and when are you free", arrives third.

**At 60 seconds on a laptop:** the four case files land well. The status chips (Shipped, Demo Day finalist, Ongoing, In progress) make it obvious what's real and what's underway, which is unusual on a student site. The Sam's Club entry is the one most recruiters here will recognise.

**What would make me reach out:** the live app link, and the fact that he explains quantitative material to other people. Both are rare in a student portfolio.

**Friction:** the opening paragraph runs six lines on a phone before anything actionable.

## Pass 2 — Accessibility and performance

Lighthouse, September 23, 2026, both presets:

| Page | Preset | Performance | Accessibility | Best practices | SEO |
| --- | --- | --- | --- | --- | --- |
| Home | Desktop | 100 | 100 | 100 | 100 |
| Home | Mobile | 100 | 100 | 100 | 100 |
| Links | Mobile | 100 | 100 | 100 | 100 |

Home page on mobile: largest contentful paint 1.4 s, layout shift 0.015, 102 KiB total. Links page: 0.9 s, 0.033, 92 KiB.

Manual checks: no horizontal scrolling at 360, 390, 768 or 1440 px; one `h1` per page; skip link works; every link reachable by keyboard with a visible amber focus ring; link tap targets on the links page are 56 px tall; text contrast is 16:1 for body, 6.4:1 for muted text and 10.6:1 for the amber accent against the background, all above the 4.5:1 requirement; `prefers-reduced-motion` turns off the scrolling behaviour and transitions.

## Pass 3 — Slop audit

The page avoids the usual machine-made tells: no gradients, no glassmorphism, no emoji, no skill bars, no stock photography, no "passionate about". Three things to watch:

1. **A claim I never made.** The contact section says "I answer email quickly". That is exactly the kind of invented detail I criticised in the baseline, and it came from the build, not from me.
2. **Links that don't render.** "Read the brief" points at a `.md` file. GitHub Pages serves it as raw text, and some phones download it instead of showing it.
3. **The case file metaphor** works because each entry really does carry a status and evidence. If any entry ends up without either, it turns into decoration.

## Fixes applied (see the next commit)

1. A compact status line under the name: role, graduation, location, so the 15-second questions are answered before any scrolling.
2. The opening paragraph cut to two sentences.
3. The "I answer email quickly" claim removed.
4. Process links pointed at GitHub's rendered view instead of raw markdown.
5. The links page added to the footer of every page.

## Still open

- Real evidence images: a screenshot of the Portfolio Tracker App, and something showable from the Sam's Club project.
- The current state of the ESP32 project, so CF-04 says what it actually does.
- A start date, so "available from" can replace "graduating".
