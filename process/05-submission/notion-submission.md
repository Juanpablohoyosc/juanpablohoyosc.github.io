# Module 2 — AI-Assisted Personal Portfolio Design

Juan Pablo Hoyos Castedo · ISYS 43203, Infrastructure and Digital Innovation · Fall 2026

> Paste this whole file into a Notion page; Notion converts the headings, tables and lists. Then upload the screenshots where marked, add the Loom link, publish the page (Share → Publish) and submit that link on Blackboard.

## Links

| What | Where |
| --- | --- |
| Live portfolio | https://juanpablohoyosc.github.io |
| Links page (mobile-first) | https://juanpablohoyosc.github.io/links/ |
| Baseline output | https://juanpablohoyosc.github.io/process/01-baseline/ |
| First attempt, September 3 | https://juanpablohoyosc.github.io/process/00-earlier-version/ |
| Repository, with the full history | https://github.com/Juanpablohoyosc/juanpablohoyosc.github.io |
| Loom walkthrough | [ME: paste the Loom link] |

## How it progressed

| Version | Date | What it is |
| --- | --- | --- |
| First attempt | Sep 3 | My résumé styled as a web page, uploaded by hand |
| `v0-baseline` | Sep 22 | One sentence and my résumé, nothing else |
| `v1-first-build` | Sep 23 | Built from a written brief: audience, target role, four case files |
| `v2-feedback` | Sep 23 | Links page, career-fair assets, and five fixes from a review round |

[ME: upload the baseline screenshot and the final screenshot side by side here]

## AI tools used

| Tool | Model | Why I chose it | What I used it for |
| --- | --- | --- | --- |
| Claude (app) | Opus 5 | The assignment's baseline step | The one-sentence baseline |
| Claude (Cowork) | claude-opus-5 | It writes files, runs a browser against them and keeps the git history | The brief, the build, the reviews, the documentation |
| [ME: Gemini] | [ME] | A different model on the same prompt | The tool comparison |
| [ME: second tool] | [ME] | [ME] | The tool comparison |

## Prompts

**Baseline prompt, word for word**

> Build me a portfolio page based on my resume.
> Don't ask me any questions, use your best judgment.

**Refined prompt** — the full text is in the repository at `process/02-direction/refined-prompt.md`. It adds an audience, the role I'm looking for, four case files in priority order, a palette and type system, build constraints, and a list of patterns to never use.

**What changed between them**

| Baseline | Refined |
| --- | --- |
| No audience | Recruiters at a career fair, on LinkedIn, before an interview |
| No goal | Analyst roles, locations, graduation date |
| Résumé order | Four case files ordered by what a recruiter values |
| No look named | Palette, type, layout rules, and an explicit "never do these" list |
| No constraints | Plain HTML and CSS, mobile-first, accessible, GitHub Pages-ready |
| No guard on facts | Résumé is the only source; gaps become visible TODOs |
| No self-review | Asks the tool to critique its own output |

## Comparing the tools

[ME: paste the comparison here after running the refined prompt in two more tools. The prompt to use is in `process/02-direction/refined-prompt.md`, and the outputs go in `process/03-comparisons/`.]

| Tool | Layout | Tone | What it assumed about me | Accuracy vs. my résumé | What I took from it |
| --- | --- | --- | --- | --- | --- |
| | | | | | |

## What the baseline got wrong

- It called "Que Planes?" a team project. It was solo.
- It wrote "Email is the fastest way to reach me," which I never said.
- It never stated what role I want or when I'm available.
- It reproduced my résumé's order instead of making a case.

Full teardown: `process/02-direction/baseline-teardown.md`.

## The links page

Six actions, ranked for the moment someone taps an NFC chip at a career fair: LinkedIn, résumé, email, save contact, portfolio, GitHub. All six fit on the first screen of a 390-pixel phone, each 56 pixels tall. There's a vCard so a recruiter can save me in one tap, and a QR code in `assets/img/links-qr.svg` for printing.

[ME: upload the phone screenshot of the links page here]

## Review round

Three passes before the final version: a recruiter skim, an accessibility and performance audit, and a slop audit. Lighthouse scores 100 for performance, accessibility, best practices and SEO on both pages, on mobile and desktop. Five fixes came out of it, including removing a claim the build had invented on its own. Details: `process/04-feedback/reviews.md`.

## Reflection

[ME: paste the final version of `process/05-submission/reflection.md` here]
