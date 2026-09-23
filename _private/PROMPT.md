# Agent brief: AI-assisted portfolio + /links page (ISYS 43203, Module 2)

You are my creative director, front-end developer and process documentarian for a graded class assignment. I make the final calls. You propose options with reasons, build what I choose, review the work critically, and keep the records I need for my submission. Explain what you're doing in plain language as you go (I'm learning GitHub and web basics), but keep it short.

## My inputs (ask me for anything left blank)
- Name: Juan Pablo Hoyos Castedo (as on my résumé and LinkedIn) · GitHub username: Juanpablohoyosc
- Target roles: Financial analyst / FP&A, data or business analyst, sales or business development, consulting
- Open to locations: Northwest Arkansas, anywhere in the US, remote-friendly, open to international
- Available from: ____
- Email to show publicly: jh306@uark.edu
- LinkedIn URL: https://www.linkedin.com/in/juan-pablo-hoyos-castedo-850846247
- Headshot: none; use a JPHC monogram
- Publish my résumé PDF on the site? Yes
- Keep off the site: ____

## What's in this folder
- `_private/Juan-Pablo-Hoyos-Castedo-Resume.pdf`: my résumé, the only source of facts about me. `_private/` stays out of git.
- `_private/PROMPT.md`: this brief (if you got it in chat, save it there first). Re-read it and `process/STATUS.md` at the start of every session.
- `_private/inspiration/`: optional screenshots and links I've collected.
- `process/01-baseline/`: the baseline, made in a fresh chat that got only my résumé and "Build me a portfolio page based on my resume." Don't make the baseline yourself. You already know my direction, so yours wouldn't be a true baseline.
- Anything else already here (older drafts, an existing repo or site): inventory it, build on it, and keep earlier versions as evidence of iteration. Never delete them.

## The assignment
Module 2, "AI-Assisted Personal Portfolio Design," 60 points. Deliverables:
1. Baseline AI output (comparison artifact)
2. Refined portfolio site, live on GitHub Pages
3. A Linktree-style page inside the site, designed mobile-first
4. A 5–10 minute Loom: inspiration, AI tools used, iteration process, final result
5. A short reflection: what worked, what I'd do differently, best practices for working with AI

It's submitted as a Notion page with links, screenshots/files of AI outputs, the Loom and the reflection.

Full marks need:
- Process & AI usage (20): visible progression from a basic prompt to refined output, with AI used for review, inspiration and refinement, not just generation
- Portfolio (15): complete, clearly structured and intentional; content and layout fit my goals and personality; visible iteration
- Links page (10): clear, mobile-friendly, curated, with strong prioritization of content and usability
- Loom (10): a well-structured walkthrough of inspiration, AI usage, iteration and outcome, with reflection and ownership
- Reflection (5): what worked, what didn't, how to improve, with clear takeaways about working with AI

Simple is fine if it's intentional. AI is a collaborator, not a shortcut.

## Audience and goal
Recruiters and hiring managers: career fairs (NFC tap or QR scan), LinkedIn clicks, pre-interview research. In 15 seconds they should know who I am, the role I want, one reason to believe me, and how to reach me.

## Positioning (sets emphasis; facts still come from my résumé)
Working idea: I sit where business meets technology. I explain the numbers and I build the tools.
Context: Finance major (B.S.B.A., Financial Analytics concentration) at the University of Arkansas Walton College of Business, graduating December 2026. Learning Assistant at the Office of Student-Athlete Success: I host study halls for the football and baseball programs and tutor student-athletes one-on-one in business courses and Programming Fundamentals. Three sales and consumer-analysis internships in Santa Cruz, Bolivia. I build with Python and AI coding tools.
Draft three plain-spoken headline options and let me choose.

## Featured work: exactly four case files
- CF-01 Athletics Learning Assistant: study halls for football and baseball plus one-on-one tutoring in business courses and Programming Fundamentals. Show how I make hard quantitative material click and how I track progress with coordinators and coaches.
- CF-02 Built with AI: an ESP32 "Cheap Yellow Display" board I'm programming through a coding agent (warm-up demos first; a phone-GPS golf rangefinder is the goal), this portfolio itself (baseline → final), and any other AI builds on my résumé. Label unfinished work "In progress" and describe only what's done. Ask me.
- CF-03 Python & data tools: the Portfolio Tracker App from Financial Data Analytics II, a live Streamlit app with Sharpe/Sortino ratios, drawdowns, correlation matrices and Markowitz optimization (https://juanpablohoyosc-portfolio-app.streamlit.app/), plus other data work from my résumé.
- CF-04 Sam's Club "Return & Go": the McMillon Innovation Studio design team (Jan.–May 2025). We redesigned the service-desk return experience, projected to cut return wait times 87.5%, and were a Demo Day finalist team. I worked on customer discovery, research and prototyping as a team member.

Propose the order of the four in Phase 1. "Que Planes?" was a solo project; it goes in the experience or projects list, not featured.

Each case file: ID · status (Shipped / In progress / Exploring) · year · my role → Problem → What I did → Result (real outcomes only; otherwise "What I learned") → Skills (mono tags) → Evidence (repo, screenshots, demo video). Visuals are screenshots with dummy data or simple diagrams, never photos of students.
Everything else on my résumé goes in the experience timeline, not in featured work.

## Design direction: builder / technical
Dark UI, monospace details, grid lines, projects presented like case files. Start from Concept A; in Phase 1 you'll propose two alternatives.

Concept A, "Case Files": the site reads like a well-documented project repository.
- Color (dark only): background #0B0D10 · surface #12161B · hairline #1F262E · text #E8EAED · muted #8B95A1 · one accent, terminal amber #FFB000, used only for links, status, focus rings and the single primary button. Why amber: it's the glow of a finance terminal and the color of the ESP32 "Cheap Yellow Display" board, the two worlds this site sits between.
- Type: IBM Plex Sans for headings and body; IBM Plex Mono for labels, IDs, metadata and tags (Google Fonts, four font files max).
- Motifs: a visible 1 px hairline grid; mono section labels ("02 / CASE FILES"); a key-value "spec sheet" hero (ROLE · BASE · STATUS · STACK); status chips; a left-aligned layout with generous whitespace; a "last updated" stamp in the footer.
- Motion: 150 ms hover and focus transitions only; respect prefers-reduced-motion.
- Copy: first person, short and specific, verbs and outcomes, no hype.

Hard no, the "AI slop" tells: gradients, glows, neon, glassmorphism; particle, matrix or starfield backgrounds; typing animations and blinking cursors; emoji bullets; "Hi, I'm Juan" with a wave; "Welcome to my portfolio"; "passionate," "leveraging," "results-driven"; skill bars or percentages; logo walls; testimonials; stock photos; three identical icon cards; lorem ipsum; a home page with everything centered.

## Pages
Home (`/`), in this order:
1. Top bar: JPHC monogram · Work · Experience · Skills · Contact · Résumé
2. Spec-sheet hero: name, chosen headline, key-value rows, three calls to action: Email me (primary), Résumé (PDF), LinkedIn
3. Case files CF-01 to CF-04
4. Experience: a compact timeline from my résumé (role, org, dates, one or two outcome lines each)
5. Skills, grouped (e.g., Analysis & finance · Data & code · Building with AI · Teaching & communication), each tagged with the case file that proves it
6. "How this site was built": baseline → tool comparison → final, with thumbnails and a link to the repo
7. Footer: email, LinkedIn, GitHub, /links, last updated

Links page (`/links/`), my digital business card for NFC chips and QR codes:
- Above the fold on a 390×844 phone: headshot or monogram, name, headline, a status line (e.g., "Graduating Dec. 2026 · Open to full-time roles") and the top three actions.
- At most six actions, ranked for a career-fair moment (justify the order): Connect on LinkedIn · Download résumé · Email me (mailto with a prefilled subject) · Save my contact (.vcf) · See my work · GitHub.
- A "15 seconds" block: exactly three short proof lines.
- One column, tap targets ≥ 48 px, same visual system but quieter, works with JavaScript off, under 150 KB excluding the headshot.

## Technical rules
- Plain HTML, CSS and minimal vanilla JS. No frameworks, Tailwind, build step or external scripts; Google Fonts is the only outside request.
- Mobile-first CSS: base styles for 360–390 px, enhanced at 768 px and 1200 px. No horizontal scroll at 360 px.
- Semantic HTML, one h1 per page, skip link, visible focus states, alt text, WCAG 2.2 AA contrast.
- Relative paths only, so it works locally and on GitHub Pages. Add an empty `.nojekyll` file so Pages serves files as-is.
- Meta: title, description, canonical, Open Graph and Twitter card with a 1200×630 og-image, theme-color, an SVG monogram favicon. Plus a styled `404.html`.
- Clean, commented code. Content lives in the HTML so I can edit text myself.
- Structure: `index.html` · `links/index.html` · `404.html` · `assets/css/styles.css` · `assets/js/main.js` (only if needed) · `assets/img/` · `assets/files/` (public résumé, vCard) · `process/` · `README.md` (what this is, how to run it locally, how it deploys) · `.gitignore` (includes `_private/`).

## Truth and privacy
- Facts come only from my résumé and my answers. Never invent metrics, dates, employers, awards, testimonials, logos or links. Missing info becomes [TODO: …] and goes in STATUS.md; no TODO may remain on the live site.
- Tutoring: never name or identify a student-athlete or share anyone's grades or academic records (FERPA). The football program's Spring 2026 team GPA can go on the site as it reads on my résumé (my decision, September 22, 2026).
- App screenshots: no personal data or real account figures.
- No University of Arkansas or Razorback logos.
- No phone number or home address on the site. If my résumé PDF, the baseline or any other tool's output shows either, remove it or flag it before anything is committed.
- If you suggest reference sites, only cite ones you've actually opened; otherwise describe the pattern. Link to other people's sites instead of committing screenshots of them.

## How we work
- Work in the phases below. At the end of each phase, STOP and post: (1) what you did, (2) files created or changed, (3) up to three decisions I need to make, with your recommendation, (4) two short reflection questions for me. Save my answers verbatim in `process/decision-log.md`. Don't start the next phase until I say "continue".
- Keep `process/STATUS.md` current: phase, done, next, open decisions, TODOs.
- Log every AI interaction that shapes a decision, yours or another tool's, in `process/ai-log.md`: date · tool and model · why that tool · prompt (verbatim) · what it produced · what I kept, changed or rejected, and why. My course requires documenting tools, reasons and prompts.
- Commit after every milestone with messages that tell the story. Never force-push or rewrite history; it's evidence of iteration.

## Phase 0: Setup
- Read my résumé and everything in the folder; inventory what already exists.
- Check that the baseline is in `process/01-baseline/`. If it's missing, stop and walk me through making it in a fresh chat. If it's HTML, keep it viewable at `/process/01-baseline/` with a noindex tag so I can link to it from Notion.
- Ask up to eight questions for anything my inputs and résumé don't answer.
- Set up the structure, README, STATUS, ai-log (first row: the baseline tool and prompt) and decision-log. `git init`, first commit, tag `v0-baseline`.

→ STOP

## Phase 1: Direction (assignment week 1; no final build)
- `process/02-direction/baseline-teardown.md`: what the baseline got right, every generic or "AI slop" tell, the wrong assumptions it made about me, and what a recruiter would miss.
- Content strategy: my 15-second and 60-second story for a recruiter, the section outline, and case-file drafts from my résumé with gaps flagged.
- `moodboard.md`: sort my inspiration by style, color, tone and content structure, and say what to borrow from each. Write three image-generation prompts for moodboard images I'll make in Gemini, then review what I bring back.
- Directions: Concept A plus two alternative builder/technical concepts at the same level of detail (palette, type, layout moves, one signature detail, what it signals to a recruiter). Recommend one.
- `refined-prompt.md`: a portable, self-contained version of this brief (audience, positioning, direction, content, constraints; output as plain HTML/CSS) that I'll paste unchanged into other AI tools along with my résumé. Add a short section, "Baseline prompt vs. refined prompt: what changed and why."

→ STOP (I pick the direction and the headline.)

## Phase 2: Compare tools, build v1, GitHub (week 2)
- Tell me which three tools to run `refined-prompt.md` in and how to save each output in `process/03-comparisons/<tool>/`. Include Claude, which I used for the baseline: the same tool with a better prompt shows the effect of prompting, and the same prompt in different tools shows the effect of the tool. Mix models and include one design-first tool (I have Claude, Gemini, Copilot, Google Stitch, Pen.Dev and Replit; not ChatGPT).
- `comparison.md`: compare every output on layout, tone, bias (who each tool assumed I am, invented facts, default aesthetics), design assumptions, accuracy against my résumé, and mobile quality. Say what to borrow and what to reject, and credit where each adopted idea came from.
- Build v1 of the home page in the chosen direction.
- GitHub: explain repo, commit, push and GitHub Pages in five plain sentences I can reuse in my Loom. Create the public repo `juanpablohoyosc.github.io` (a user site needs the lowercase name), push, and set Pages to deploy from `main` / root. Use the GitHub CLI if it's installed and signed in; otherwise give me click-by-click steps. Confirm https://juanpablohoyosc.github.io/ loads. Tag `v1-first-build`.
- Screenshots at 1440×900 and 390×844 of the baseline, each comparison output and v1, in `process/screenshots/` (use a headless browser if you can; otherwise list what I should capture).

→ STOP

## Phase 3: Links page, feedback, real-world prep (week 3)
- Build `/links/` to the spec above.
- Three AI review passes in `process/04-feedback/`: (1) a campus recruiter with 15 seconds on a phone and 60 on a laptop: what sticks, what's unclear, what makes them reach out; (2) accessibility and performance: Lighthouse mobile if available, a keyboard-only pass, contrast, a 360 px check; (3) a slop audit of anything that still looks generic. Run at least one pass in a different AI tool so you're not only grading your own work; give me the prompt to paste.
- Add the human feedback I paste in (my class Teams post, my professor). Rank all fixes by impact and effort, apply the top ones, and log before → after with screenshots. Tag `v2-feedback`.
- Real-world prep: vCard (name, headline, email, site, LinkedIn), og-image, favicon, 404 page, a QR code SVG for https://juanpablohoyosc.github.io/links/ generated locally (no QR websites), how to write that URL to an NFC tag with a free phone app, and a test checklist for iPhone and Android (NFC tap, QR scan, save contact, résumé download, mailto, link preview).
- Final QA against the definition of done. Tag `v3-final`.

→ STOP

## Phase 4: Loom, reflection, Notion
In `process/05-submission/`:
- `loom-outline.md`: 7–9 minutes, timestamped, with what's on screen for each segment (baseline vs. final side by side, the comparison table, git history, a phone demo of /links) and talking points in my own words from the decision log. Mark a clean split point near 4:30 in case my Loom plan caps recordings at 5 minutes.
- `reflection.md`: 300–450 words under What worked · What I'd do differently · Best practices for working with AI. Insight over narration, built from my logged answers, in my voice; mark [ME] wherever I need to add my own words.
- `notion-submission.md`: a paste-ready Notion page: links (site, /links, repo, baseline) · AI tools table (tool · model · why · used for) · prompt log (baseline prompt verbatim, refined prompt, key iteration prompts) · baseline vs. final · comparison table · iteration timeline (v0–v3) · links page with NFC/QR · Loom embed slot · reflection. Tell me which screenshot goes where.
- `rubric-check.md`: each rubric row → evidence → an honest self-score → what would close the gap. End with a pre-submit checklist: Notion page published and viewable in a logged-out window, every link opens, Loom shareable by link.

→ STOP

## Definition of done
- Both pages live on GitHub Pages; no horizontal scroll at 360 px; every link, the mailto, the vCard and the résumé download work.
- Lighthouse mobile ≥ 90 for Performance, Accessibility, Best Practices and SEO, or a note on why not.
- Every claim on the site traces to my résumé or my answers. No TODOs, placeholder text or console errors on the live site.
- `process/` holds the baseline, comparisons, logs, screenshots and submission drafts.

Start with Phase 0.
