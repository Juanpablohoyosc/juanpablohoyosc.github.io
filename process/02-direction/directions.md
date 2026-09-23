# Design directions

All three sit inside the builder/technical look I chose: dark interface, monospace details, visible structure, projects presented as documented work. The point of writing three was to choose deliberately instead of accepting the first thing a model produced.

## A — Case Files (chosen)

The site reads like a well-documented project repository. Each featured project is a case file with an ID, a status chip, a stack line and evidence links.

- Color: background #0B0D10, raised surface #12161B, hairline #1F262E, text #E8EAED, muted #8B95A1, one accent, terminal amber #FFB000, used only for links, status, focus rings and the single primary button.
- Type: IBM Plex Sans for headings and body, IBM Plex Mono for labels, IDs, metadata and tags. Self-hosted, four files, no third-party font request.
- Layout: hairline rules, mono section labels ("01 / CASE FILES"), a key-value spec sheet in the hero, left-aligned, generous whitespace.
- Signature detail: the status chip. Shipped, Demo Day finalist, Ongoing, In progress. It says honestly where each piece of work stands, which is rarer on a student site than polish.
- What it signals to a recruiter: this person documents their work and tells you what's finished and what isn't.

Why amber: it reads like a finance terminal and like the yellow ESP32 board I'm learning on, the two worlds this site sits between. One accent keeps the page calm and makes the single primary action obvious.

## B — Ledger

An accounting ledger: ruled rows, right-aligned figures, tabular numbers, one hairline column grid holding everything. Palette closer to paper, ink on warm off-white, with a single deep red.

- Strength: it looks like the finance side of my work and would print beautifully.
- Why not: it lands close to the baseline, which is already paper-and-red, so the comparison between the two would show much less. It also underplays the building I do.

## C — Changelog

The site as a release log. Every entry is dated and versioned, newest first, with the site's own version history running alongside my work history.

- Strength: the process is the design, which fits the assignment.
- Why not: dates as the primary ordering buries the work a recruiter cares about most under whatever happened last. It would make a strong "how this site was built" section, so that idea moves into A.

## Decision

Direction A, with the changelog idea folded in as the "How this site was built" section. It is the furthest from the baseline, it carries the builder/technical brief, and its status chips make honesty a design feature instead of a disclaimer.

## Moodboard notes

I had no saved inspiration files when we started, so the references here are described rather than linked. Three image prompts to run in Gemini if I want moodboard images for the Notion page:

1. "A dark editorial web page for a finance analyst's portfolio: near-black background, hairline grid rules, one amber accent, large sans-serif headline, monospace labels, generous whitespace, no gradients."
2. "A project case file layout: ID code, status chip, three short columns of metadata, evidence links, dark UI, amber accent."
3. "A phone-sized links page on a dark background: one column of large tap targets, a monogram at the top, one amber primary button."
