# Baseline teardown

The baseline page: Claude, claude.ai app, Opus 5 Max, September 22, 2026. Input: my résumé PDF plus "Build me a portfolio page based on my resume. Don't ask me any questions, use your best judgment." Saved in `../01-baseline/`.

## What it got right

- Every fact came from the résumé. No invented employers, dates or numbers.
- Sensible sections and a readable page: clear hierarchy, generous spacing, real links (email, LinkedIn, the Streamlit app).
- Honest about the chart: it captioned the efficient-frontier drawing as an illustration rather than passing it off as output from my app.
- It grouped my two Athletics roles and my two EnviosPet internships under one employer each, which reads better than five separate blocks.

## Where it is generic

1. **It is my résumé in HTML.** Same order, same sections, same emphasis. A portfolio should make a case; this one just restates the document a recruiter already has.
2. **No target.** Nothing says what work I want. A recruiter reads it and still has to guess whether I want finance, analytics or sales.
3. **The first screen doesn't do a job.** The hero is a dense paragraph. In 15 seconds a recruiter should get who I am, what I want, one reason to believe me, and how to reach me.
4. **The chart is decoration.** It illustrates a concept anyone can look up instead of showing my work. A screenshot of my actual app would carry more weight.
5. **Nothing to take away.** No résumé download, no way to save my contact details, no links page, nothing for a career fair.
6. **Phone was an afterthought.** At phone width the page runs 6,912 px. It reflows, but nothing was prioritized for a small screen.
7. **No proof of process.** The assignment is about directing AI, and the page says nothing about how it was made.
8. **Not built to ship.** As a design canvas it has no title tag, no description, no link preview image, no favicon, no 404 page.

## Assumptions it made that are wrong

- It calls "Que Planes?" a team project ("Our team took first place… out of seven teams"). It was a solo project.
- "Email is the fastest way to reach me." I never said that.
- "Happy to talk in English, Spanish or Portuguese." My résumé lists Portuguese as conversational.

## What a recruiter would miss

The role I'm after, when I'm available, where I'll work, and a résumé they can keep. Those four gaps set the brief for the refined version.

## What this tells me about the tool

With one sentence, Claude optimized for looking finished rather than being useful. The layout is competent, so the gap between the baseline and the refined version is not craft, it's direction: audience, priority and intent are exactly what the prompt left out.
