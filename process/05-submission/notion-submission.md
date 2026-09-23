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
| Gemini | [ME: which model the chat was set to] | A different company's model on the identical refined prompt | The tool comparison |

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

I ran the refined prompt, unchanged, in Gemini as well as Claude. Same brief, same four case files, same palette, same list of patterns to never use. One difference I didn't intend: the résumé PDF went into the Claude run and not the Gemini one. That matters, and the fourth finding below is about exactly that.

| Tool | Layout | Tone | What it assumed about me | Accuracy vs. my résumé | What I took from it |
| --- | --- | --- | --- | --- | --- |
| Claude (Cowork) | Spec-sheet hero, four case files, timeline, skills, build log | Plain; case files written as what changed | Nothing — flagged gaps instead | One invented claim ("I answer email quickly"), removed in review | — |
| Gemini (prompt only, no résumé attached) | Same structure plus a scroll-spy nav, a résumé modal and a copy-email button | Elevated, "lab-grade"; technical language doing the work enthusiasm language usually does | A Gmail address, a LinkedIn handle, three internship job titles, "Spanish (Native)", on-site interviews at Sam's Club | 10 gaps correctly flagged as TODO; 6 details invented, 2 of them contact details | The "Skills proved" label above each case file's tags; its `?source=nfc` quick-connect idea, parked |

Three things came out of running the same prompt twice:

**Both tools produced the same page structure.** The brief named the sections and their order, and neither rearranged them. Every difference was an addition on Gemini's side, which says the specific part of the prompt was doing its job.

**The anti-slop list constrained vocabulary, not register.** Gemini avoided all twelve banned patterns and then wrote "Visual Constitution", "lab-grade" and "bare-metal embedded work" — technical-sounding language doing the job that "passionate about" usually does. Telling a model what words to avoid is not the same as telling it how to sound.

**Stating a rule is not following it.** Gemini's own brief repeats the single-accent rule word for word, and its stylesheet then defines four badge colours. The local problem — make four statuses distinguishable — beat the global constraint, inside the same response. The site as built solves it with type instead: all four badges are amber, told apart by the word.

**And the accident that taught me the most.** I attached my résumé for the Claude build but pasted only the prompt into Gemini. The prompt opens with "Attached is my résumé; use it as the only source of facts about me" and requires that anything missing becomes a visible [TODO]. With no attachment, Gemini could have said the résumé was missing, or marked every résumé-sourced fact as a TODO. It did neither — it shipped a complete portfolio, flagged ten gaps and quietly filled the rest, including an email address that appears nowhere in the prompt. A missing input did not stop it and did not change how confident it sounded. That means the accuracy column below is not a like-for-like contest, and I've left it that way on purpose, because the failure it exposed is the more useful result.

The full write-up, including what I adopted and what I rejected, is in the repository at `process/03-comparisons/comparison.md`, and Gemini's output is saved beside it.

[ME: upload a screenshot of the Gemini response here]

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
