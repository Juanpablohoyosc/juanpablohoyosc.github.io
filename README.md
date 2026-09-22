# juanpablohoyosc.github.io

Personal portfolio and links page for Juan Pablo Hoyos Castedo, built for Module 2 (AI-Assisted Personal Portfolio Design) of ISYS 43203, Infrastructure and Digital Innovation, at the Sam M. Walton College of Business, University of Arkansas.

## What's here

- `index.html`: the portfolio home page (added in Phase 2)
- `links/`: the mobile-first links page for NFC chips and QR codes (added in Phase 3)
- `assets/`: styles, scripts, images and downloadable files
- `process/`: the record of how the site was built with AI
  - `01-baseline/`: the generic page Claude made from my résumé and a one-sentence prompt
  - `02-direction/`: baseline teardown, moodboard, design directions and the refined prompt
  - `03-comparisons/`: the same refined prompt run in different AI tools, compared
  - `04-feedback/`: AI and human reviews, and the fixes that came out of them
  - `05-submission/`: Loom outline, reflection and the Notion page draft
  - `ai-log.md`: every AI interaction that shaped a decision
  - `decision-log.md`: my decisions and reflections, in my own words
  - `STATUS.md`: where the project stands

## Run it locally

From this folder, run `python3 -m http.server 8000`, then open http://localhost:8000.

## How it deploys

GitHub Pages user site: the repository `juanpablohoyosc.github.io` deploys from `main`, root folder. The empty `.nojekyll` file tells GitHub Pages to serve the files as they are.
