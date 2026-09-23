# Refined prompt

Paste everything between the lines into another AI tool, with my résumé attached, and save what it gives back in `../03-comparisons/<tool>/`. Don't edit it between tools: the point is the same prompt in different tools.

---

Build my personal portfolio website. Attached is my résumé; use it as the only source of facts about me.

**Who it's for.** Recruiters and hiring managers who find me at a career fair (by tapping an NFC chip or scanning a QR code), from a LinkedIn click, or while preparing for an interview. In 15 seconds they should know who I am, the role I want, one reason to believe me, and how to reach me.

**Me, in one line.** Juan Pablo Hoyos Castedo, finance with a financial analytics concentration at the University of Arkansas Walton College of Business, graduating December 2026. I build Python analytics tools, I've sold and analyzed customers across three internships in Bolivia, and I tutor student-athletes in quantitative business courses.

**What I'm after.** Analyst roles first, financial or data. Also open to sales and business development, and to consulting. Based in Fayetteville, Arkansas; open to Northwest Arkansas, anywhere in the US, remote, or international.

**Featured work, exactly these four, in this order.**

1. Portfolio Tracker App (Spring 2026, class project): a live Streamlit app in Python computing Sharpe and Sortino ratios, rolling volatility and drawdowns, correlation and covariance matrices, and Markowitz optimization (global minimum variance, tangency, efficient frontier), with per-asset risk contribution, a weight-slider builder and estimation-window sensitivity. Live at juanpablohoyosc-portfolio-app.streamlit.app
2. Return & Go (Jan–May 2025): with the Sam's Club design team at the McMillon Innovation Studio, a redesigned service-desk return experience projected to cut wait times 87.5% without losing the associate–member interaction that drives loyalty. Demo Day finalist team. I worked on customer discovery, research and prototyping.
3. Athletics Learning Assistant (since Jan 2025): one-on-one tutoring for student-athletes across 1000–4000-level business courses and Programming Fundamentals, study halls for the football and baseball programs, and contributing to the football program's 3.27 cumulative GPA in Spring 2026, the highest in program history.
4. Built with AI (2026, in progress): this site, directed with a written brief and a version history, plus an ESP32 "Cheap Yellow Display" board I'm programming through a coding agent.

Everything else on the résumé belongs in a compact experience timeline. "Que Planes?" was a solo project.

**Structure.** Top bar with a JPHC monogram and links to Work, Experience, Skills, Contact and my résumé. A spec-sheet hero: my name, the one-line positioning, four key-value rows (role sought, base, status, stack), and three calls to action, with "Email me" as the single primary button. Then the four case files, each with an ID, a status (Shipped, Demo Day finalist, Ongoing, In progress), a year, a problem, what I did, the result, the skills it proves and its evidence links. Then the experience timeline, then skills grouped and tagged with the case file that proves each group, then a short "How this site was built" section, then contact.

**Look.** Builder/technical. Dark interface: background #0B0D10, surface #12161B, hairlines #1F262E, text #E8EAED, muted text #8B95A1, and exactly one accent, amber #FFB000, used only for links, status, focus rings and the primary button. IBM Plex Sans for headings and body, IBM Plex Mono for labels, IDs and tags. Visible hairline structure, mono section labels, left-aligned, generous whitespace, motion limited to 150 ms hover and focus transitions.

**Never do these.** Gradients, glows, neon or glassmorphism; particle, matrix or starfield backgrounds; typing animations or blinking cursors; emoji bullets; "Hi, I'm Juan" with a wave; "Welcome to my portfolio"; the words "passionate", "leveraging" or "results-driven"; skill bars or percentages; logo walls; testimonials; stock photos; three identical icon cards; lorem ipsum; a home page with everything centered.

**Rules.** Facts only from my résumé. Invent nothing: no metrics, employers, dates, awards or testimonials. Anything missing becomes a visible [TODO] and a list at the end. Never name a student-athlete or show anyone's grades. No photo of me; use a JPHC monogram.

**Build it as.** Plain HTML, CSS and minimal vanilla JavaScript. No frameworks, no build step. Mobile-first CSS: base styles for 360–390 px, enhanced at 768 px and 1200 px, no horizontal scrolling at 360 px. Semantic HTML, one h1, a skip link, visible focus states, alt text, WCAG 2.2 AA contrast, and prefers-reduced-motion respected. Relative paths only, so it works on GitHub Pages. Include title, description, Open Graph and Twitter tags, a theme color and an SVG monogram favicon.

**Give me.** A short design brief in your own words, the file tree, the complete code for each file with nothing truncated, the list of [TODO] items, and finally your own critique: three specific things you'd improve in the next pass.

---

## Baseline prompt versus refined prompt: what changed and why

| Baseline | Refined | Why |
| --- | --- | --- |
| "Build me a portfolio page based on my resume." | Everything above | The baseline asked for a page; this asks for a page that does a job. |
| No audience | Recruiters at a career fair, on LinkedIn, before an interview | Audience decides what goes first. |
| No goal | Analyst roles first, plus locations and availability | The baseline never said what I want, so a recruiter couldn't act. |
| Résumé order | Four case files ordered by what a recruiter values | A portfolio makes a case; a résumé lists. |
| No look named | Palette, type, layout rules and an explicit "never do these" list | Naming the anti-patterns is what keeps the output from looking machine-made. |
| No constraints | Plain HTML/CSS, mobile-first, accessible, GitHub Pages-ready | The result has to ship, not just look finished. |
| No guard on facts | Résumé is the only source; gaps become visible [TODO]s | The baseline invented small things (a team that didn't exist, a preference I never stated). |
| No self-review | Asks for a critique of its own output | Uses the tool as a reviewer, not just a generator. |
