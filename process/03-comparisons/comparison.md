# Same prompt, two tools

`02-direction/refined-prompt.md` went into Claude (Cowork, claude-opus-5) on September 23 and into Gemini on September 23. Same brief, same four case files, same palette, same banned-patterns list. What follows is what each one did with it.

Gemini's output is saved in `gemini/output.md`. Claude's output is the site itself.

## The short version

| | Claude (Cowork) | Gemini |
| --- | --- | --- |
| **Layout** | Spec-sheet hero, four case files, timeline, skills, build log, contact | Same sections, same order, plus a scroll-spy nav and a résumé modal |
| **Tone** | Plain sentences; case files written as what changed and who it was for | Elevated and technical — "Visual Constitution", "lab-grade", "bare-metal embedded work" |
| **What it assumed** | Nothing new; asked for the gaps instead | A Gmail address, a LinkedIn handle, three internship job titles, "Spanish (Native)", on-site interviews at Sam's Club |
| **Accuracy** | One invented claim, caught in review and removed | Two invented contact details and four invented facts; ten gaps correctly flagged as TODO |
| **Followed the constraints** | Zero JavaScript, one accent, self-hosted fonts | Three JavaScript features, four badge colours, fonts loaded from Google's CDN |
| **What I took** | — | A visible "Skills proved" label on each case file; the `?source=nfc` idea, parked |

One thing to hold on to while reading the rest: I attached my résumé for the Claude build, and ran Gemini on the prompt alone. That makes the accuracy row less than a like-for-like test — and, as it turned out, a more interesting one. The last section deals with it.

## Layout

Both landed on nearly the same page. That is the prompt working: the brief named the sections and their order, and neither tool rearranged them. The differences are all additions on Gemini's side.

It added a sticky navigation bar that highlights the current section as you scroll, a résumé preview in a modal dialog with proper focus handling, and a copy-to-clipboard button next to the email address. Each is competently built — the modal traps focus, restores it on close and responds to Escape, which is more care than most hand-written modals get.

The brief said "minimal vanilla JavaScript". Gemini read that as permission; Claude read it as a ceiling and shipped none. Both readings are defensible, but the consequence is measurable: the site as built loads 102 KiB and scores 100 on Lighthouse performance. Gemini's version would ship a fourth file and a render-blocking font request to Google's CDN, which the brief had ruled out by asking for GitHub Pages portability.

Gemini also introduced a section-numbering scheme of its own — `SEC-01 // PRODUCTION WORK` above `CF-01` — which is a second ID system layered on the one the brief specified.

## Tone

This is where the two are furthest apart.

Gemini's register is inflated. Its design brief calls the palette a "Visual Constitution", describes the site as "engineered" to "respect the 15-second scan window", and promises "immutable version history" and "zero telemetry" for a page that has neither a database nor a script tag. The case file copy follows: an ESP32 hobby project becomes "tangible proof of bare-metal embedded work".

The irony is that the brief's anti-slop list is what produced this. It banned the obvious tells — gradients, skill bars, "passionate about" — and Gemini avoided every one of them. It then wrote in a different flavour of the same thing: technical-sounding language doing the job that enthusiasm language usually does. Naming twelve patterns to avoid does not teach a model to write plainly; it teaches it to avoid those twelve patterns.

Worth keeping in mind for the reflection: **an anti-slop list constrains vocabulary, not register.**

## What it assumed about me

Ten TODOs is good behaviour — the brief asked for visible gaps rather than invented filler, and most of the missing pieces came back marked. But the flagging was inconsistent in a specific way.

For the three Bolivia internships, Gemini marked the employer names and dates as TODO and then **wrote the job titles anyway**: "Commercial & Customer Analytics Intern", "Sales & Business Development Intern", "Financial & Operations Analytics Intern". Three plausible titles for three real roles it knew nothing about. Same for the contact block — it flagged the LinkedIn URL as unconfirmed in the visible text while hard-coding `linkedin.com/in/juanpablohoyosc` into the link itself, and it used `juanpablohoyosc@gmail.com` as the contact address with no flag at all. No email address appears anywhere in the prompt. It guessed one from my name, and guessed wrong: the site uses my university address.

It also added, unprompted and unflagged:

- "Bilingual Fluency: Spanish (Native), English (Professional)" — plausible, but not stated anywhere in the brief, and it drops the Portuguese
- "Conducted on-site member and associate interviews at Sam's Club" — a research method the project did not use
- "Pandas, NumPy, SciPy" in the stack, inferred from the word Python
- `og:url` pointing at the Streamlit app rather than the portfolio, so every link preview would carry the wrong destination

The pattern: the closer a fact is to a recognisable shape — a job title, a student's email address, a Spanish-speaker's fluency — the more willing it was to fill it in. Gaps it could not pattern-match, like a Demo Day slide deck URL, it flagged correctly.

## Accuracy, and the mirror it holds up

Claude did the same thing once. The first build wrote "I answer email quickly" into the contact section, a preference nobody had stated. It came out in the slop audit.

Two different models, same failure, different rates: one invented claim that survived to review, against six from Gemini. The useful conclusion is not that one tool is honest and the other isn't. It is that **an instruction to only use given facts reduces invention without eliminating it**, so a fact-check pass is not optional regardless of which tool is holding the pen.

## Design assumptions

The brief asked for exactly one accent colour: amber `#FFB000`, restricted to links, focus rings and the primary call to action. Gemini's brief repeats that sentence back word for word, then its stylesheet defines four status-badge colours — green for Shipped, amber for Demo Day Finalist, blue for Ongoing, orange for In Progress.

This is the most interesting failure in the comparison, because the tool stated the rule correctly and broke it anyway, in the same response. The status badges needed to be distinguishable, colour is the obvious way to distinguish things, and the local problem beat the global constraint. The site as built solves the same problem with type: all four badges are amber-on-dark in mono caps, and they're told apart by the word, not the colour.

## What I took from it

**Adopted.** Gemini labels each case file's tag row "SKILLS PROVED" — the cross-reference exists on the site already, but only in the skills section, pointing back at the case files. Putting a small label on the case-file side makes the relationship legible in both directions for a recruiter reading top to bottom. Added in `v3`.

**Parked, and worth doing later.** Its third self-critique suggests detecting `?source=nfc` on the URL and showing a compact sticky bar with "Save contact" and "Email" for someone who just tapped the chip at a career fair. That is a real insight about the moment the links page exists for, and it would take about fifteen lines. It stays out for now because the site is deliberately zero-JavaScript and the links page already puts both actions on the first screen.

**Rejected.** The résumé modal (the PDF download is one tap and a modal adds a layer between a recruiter and the file), the four-colour badge system (breaks the single-accent rule), the CDN fonts (an external dependency on a page that does not need one), and the two-tier `SEC-01 / CF-01` numbering (one ID system is enough).

## The line for the Notion table

| Tool | Layout | Tone | What it assumed about me | Accuracy vs. my résumé | What I took from it |
| --- | --- | --- | --- | --- | --- |
| Claude (Cowork) | Spec-sheet hero, four case files, timeline, skills, build log | Plain; case files written as what changed | Nothing — flagged gaps instead | One invented claim ("I answer email quickly"), removed in review | — |
| Gemini | Same structure plus scroll-spy nav, résumé modal, copy-email button | Elevated, "lab-grade"; technical language doing the work enthusiasm language usually does | Gmail address, LinkedIn handle, three internship titles, "Spanish (Native)", on-site Sam's Club interviews | 10 gaps correctly flagged; 6 details invented, 2 of them contact details | "Skills proved" label on each case file; the `?source=nfc` quick-connect idea, parked |

## What this test controlled, and what it didn't

Only the prompt went into Gemini. The résumé PDF did not.

That was not the plan — `refined-prompt.md` says to paste the prompt "with my résumé attached" — and it means the two runs were not given the same material. Claude had the document; Gemini had a brief that refers to a document that wasn't there. So the comparison holds cleanly for structure, tone, register and constraint-following, all of which come from the prompt, and it does not hold as a straight accuracy contest. Worth saying out loud rather than hiding.

What it turned into is a better test than the one I meant to run.

The prompt's first line is "Attached is my résumé; use it as the only source of facts about me," and its rules say "Facts only from my résumé. Invent nothing. Anything missing becomes a visible [TODO]." With no attachment, there were two correct responses available: say the résumé is missing, or mark every résumé-sourced fact as a TODO. Gemini did neither. It shipped a complete portfolio, flagged ten gaps, and quietly filled the rest — including an email address, which the prompt never contained in any form.

So the finding is not "Gemini is less accurate than Claude." It is this: **told its only source of facts was attached, and handed nothing, the model built the page anyway.** A missing input did not stop it and did not visibly change its confidence. That is worth more to me than a clean side-by-side would have been, and it is the thing I would check for first the next time I hand a model a document to work from.
