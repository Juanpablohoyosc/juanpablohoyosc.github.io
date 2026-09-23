# AI log

Every AI interaction that shaped a decision. My course asks for the tool, why I chose it, the prompt and what I did with the result.

## 0. First attempt at the page

- Date: September 3, 2026
- Tool and model: Claude (chat) [TODO: confirm which model]
- Why this tool: it was the assistant I was already using for this class
- Prompt (verbatim): [TODO: paste the prompt I used]
- What it produced: a one-page site built from my résumé content, uploaded to GitHub through the web interface
- What I kept, changed or rejected: kept unedited in `00-earlier-version/` as the first point of comparison. It reads like my résumé in a browser, which is what the refined version sets out to fix.

## 1. Writing the agent brief

- Date: September 22, 2026
- Tool and model: Claude, Cowork mode (configured model claude-opus-5)
- Why this tool: it's the AI assistant I already use for this class
- Prompt (verbatim): "I want you to generate one prompt in order to perform the following activity for my Digital Innovation class assignment." followed by the full Module 2 assignment text and rubric
- What it produced: `PROMPT.md`, an agent brief with five phases, stop-and-wait checkpoints, a design direction, and truth and privacy rules
- What I kept, changed or rejected: I chose the all-in-one agent version over a single build prompt. I picked recruiters as the audience, the builder/technical look, and three featured case files (Athletics Learning Assistant, AI-built projects, Python & data tools). The brief was later updated to match my real résumé and to drop ChatGPT, which I can't use.

## 2. Turning my résumé into a PDF

- Date: September 22, 2026
- Tool and model: Claude, Cowork mode (configured model claude-opus-5)
- Why this tool: I was away from my laptop and needed my résumé as a PDF to attach for the baseline
- Prompt (verbatim): "Review the following artifact, it contains all my resume information" plus the link to my résumé page
- What it produced: `Juan-Pablo-Hoyos-Castedo-Resume.pdf` (two pages, every bullet word for word) and a review of the résumé
- What I kept, changed or rejected: kept three fixes (expected graduation Dec. 2026, the official B.S.B.A. degree name, the full LinkedIn link). Still open: where the Spring 2026 GPA bullet belongs, mismatched number tiles, adding USD next to bolivianos, where "Que Planes?" happened, a personal email, and a one-page version.

## 3. The baseline

- Date: September 22, 2026
- Tool and model: Claude, claude.ai app, regular chat; model shown as "Opus 5 Max"
- Why this tool: the assignment's baseline step; Claude because I can't use ChatGPT
- Prompt (verbatim), with my résumé PDF attached:
  > Build me a portfolio page based on my resume.
  > Don't ask me any questions, use your best judgment.
- What it produced: a one-page portfolio design on a Claude Design canvas, with an accent-color tweak (https://claude.ai/artifact/GdrLC4R25DDps2U3me83y2)
- What I kept, changed or rejected: kept unedited as the comparison artifact in `01-baseline/`

## 4. Building and reviewing the site

- Date: September 22–23, 2026
- Tool and model: Claude, Cowork mode (configured model claude-opus-5)
- Why this tool: it can write the files, run a browser against them and keep the git history, so the brief in `PROMPT.md` could be carried out end to end
- Prompt (verbatim): "For now, I want you to keep going by just using your best judgement."
- What it produced: the Phase 1 documents, the home page, the links page, the contact card, the QR code, the 404 page, and three review passes (recruiter skim, accessibility and performance with Lighthouse, slop audit)
- What I kept, changed or rejected: kept the "Case Files" direction over two alternatives. From the review I applied five fixes, including removing a claim ("I answer email quickly") the build had invented, which is the same kind of mistake the baseline made.

## 5. The tool comparison

- Date: September 23, 2026
- Tool and model: Gemini
- Why this tool: a different company's model, run on the identical refined prompt, to see what changes when only the tool changes
- Prompt (verbatim): the full text of `02-direction/refined-prompt.md`, unchanged
- What it produced: a design brief, a four-file tree, complete code for `index.html`, `style.css`, `script.js` and `favicon.svg`, ten [TODO] items and a three-point self-critique. Saved in `03-comparisons/gemini/output.md`.
- What I kept, changed or rejected: kept its "Skills proved" label above each case file's tag row and added it to the site. Parked its `?source=nfc` quick-connect idea. Rejected the résumé modal, the four-colour badge system, the CDN-hosted fonts and its second layer of section IDs. Full write-up in `03-comparisons/comparison.md`.
