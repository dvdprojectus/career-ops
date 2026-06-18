# User Profile Context — Daniel Vargas Díaz

## Workflow

**Primary goal:** Use career-ops to **adapt `cv.md` to specific job descriptions** (English PDF/HTML). Skip or ignore modes you do not need (scan, tracker, batch) unless you choose to use them later.

## Professional Summary — how it is built (PDF mode)

The repo **does not** programmatically assemble the summary. In **`/career-ops pdf`**, the model follows **`modes/pdf.md`**: it reads **`cv.md`**, **`config/profile.yml`**, **`article-digest.md`**, **`modes/_shared.md`**, then **`modes/pdf.md`**, then **this file** (`_profile.md`). It writes **`{{SUMMARY_TEXT}}`** into **`templates/cv-template.html`** — typically **3–4 short lines**, dense with JD keywords but **never invented facts**.

**Ignore** the generic example bridge in `pdf.md` (“Built and sold a business…”). For Daniel, the spine is always:

- **`narrative.headline`** and **`narrative.exit_story`** in `config/profile.yml`
- First‑person proof from **`cv.md`** + metrics/titles from **`article-digest.md`** when citing papers

### Mandatory structure (each JD)

1. **Line 1 — Hook + JD fit:** Open with the role’s domain in their vocabulary (keywords from the JD: product area, users, tech — e.g. voice, child‑facing, learning, LLM, evaluation). Tie to **`headline`** without repeating it verbatim.
2. **Line 2 — Proof of relevance:** One concrete anchor — e.g. **ProjectUs.ai** (Learning & AI, HCI in product, metrics, pipelines, **SQL** when data/analytics JD), or **peer‑reviewed** venues (**CHI, IJHCS, UIST, VL/HCC**) when research JD.
3. **Line 3 — Differentiator:** One **superpower** from `profile.yml` that matches the JD (hacker/prototyping; children/education; hardware; full stack + research). Only if true for this role.
4. **Line 4 (optional) — Mobility / scope:** One phrase from **`exit_story`** (outside Costa Rica, freelance, **Spain relocation**) **only** if space allows or the JD mentions location/remote EU — do not waste line budget if JD is silent on geography.

### Keyword rules

- Extract **15–20** JD keywords in `pdf.md`; place **top ~5** in the summary (nouns/phrases the ATS expects).
- **Rephrase** existing experience with JD vocabulary; **never** add tools or outcomes not in `cv.md` / `article-digest.md`.
- If the JD names a stack (e.g. Python, AWS, SQL), mention only what appears in **`cv.md` Skills** or **experience bullets**.

### URLs (recruiter may read only the summary)

Per **`modes/_shared.md`**: if the summary mentions portfolio, demos, or publications, put **`portfolio_url`** or **`google_scholar`** (from `profile.yml`) **in this paragraph** as plain linked text so one scan captures them.

### JD archetype → emphasis

| JD emphasis | Weight in summary |
|-------------|-------------------|
| **HCI / UX / research** | TaleMate, IJHCS/CHI/UIST; user studies; voice agents; child/family context |
| **AI / ML engineering** | ProjectUs pipelines, metrics, analysis, **SQL**, infra support; ship learning systems |
| **EdTech / learning products** | AI for children, coaching/worker metrics, teaching + makerspace line |
| **Full stack + research** | VT + papers + implementation; single sentence |

### Quality bar

- **English**, short sentences, active verbs (align with **`modes/_shared.md`** “Writing Style”).
- No filler (“passionate”, “synergy”). No skills missing from `cv.md`.
- After drafting, mentally check: **Would every sentence still be true if this company fact‑checked against `cv.md`?**

## Role focus (three lanes)

Target roles in three lanes:

- **AI Engineer** — agent design, LLM pipelines, RAG systems, applied ML. This is the primary lane. Especially roles involving multi-agent systems, AI product infrastructure, or automation.
- **Software Engineer** — full stack, backend, or frontend. React, Node.js, Python, Next.js. Broad but real — Daniel has shipped production software at ProjectUs.ai and interned at HPE.
- **HCI / UX** — research, research engineer, UX research, voice/joint reading, learning technologies, child–computer interaction. The academic strength.

**Also open to:** consulting, freelancing, and contract roles in any of the three lanes.

**Do not** optimize for roles that are purely DevOps/infra-only, mobile-native-only (iOS/Android), or unrelated stacks (.NET, Java-heavy, PHP, Ruby) unless the JD clearly overlaps with AI, HCI, or Daniel's tech stack.

### Open-mindedness policy (IMPORTANT)

**Do NOT auto-dismiss roles** because of years-of-experience requirements Daniel doesn't meet or technical skills he hasn't used yet. His relocation goal (Spain / EU) requires casting a wide net and trying hard, even for stretch roles. When evaluating:

- **Years of experience:** Note the gap factually but do not penalize the score heavily. A JD asking for "8+ years" when Daniel has ~4 is worth flagging, not discarding.
- **Missing technical skills:** If the core role aligns with one of his three lanes and he could learn the missing skill, treat it as a minor gap, not a dealbreaker. Flag it as "skill to highlight or learn" rather than "disqualifying."
- **Seniority titles:** Don't filter out "Staff" or "Principal" roles if the actual responsibilities match his experience.
- **Score floor:** Only recommend against applying if the role is genuinely outside all three lanes (e.g., pure iOS, COBOL, SAP admin). For anything within the lanes, evaluate honestly but keep the door open.

## Target geography

- **Top priority:** Spain — full-time employment or digital nomad visa (freelance/consulting).
- **High priority:** Remote roles from anywhere worldwide; EU-based remote (especially **Germany** and **Netherlands** for higher salaries).
- **Open to:** Consulting, freelancing, contract work globally.
- **Current situation:** Working as a contractor, actively looking for new opportunities.
- **Citizenship:** Costa Rica only — flag visa/work-permit reality in evaluations when relevant. Spain digital nomad visa is viable for freelance.

## Your Target Roles (scoring lens)

| Archetype | Thematic axes | What they buy |
|-----------|---------------|---------------|
| **AI Engineer (agents/pipelines)** | Multi-agent LLM systems, RAG, hallucination QA, scraping pipelines | Production AI sense, not paper-only |
| **Software Engineer (full stack)** | React, Node, Next.js, Python, APIs, data pipelines | Ships working systems, end to end |
| **HCI / learning tech** | Voice agents, e-books, parent–child, metrics for skills | Research + product judgment for learning |
| **AI for education** | Coaching platforms, child-facing AI, responsible design | Safe, measurable learning outcomes |
| **Consultant / Freelancer** | Agent design, AI pipelines, full stack builds | Flexible engagement, immediate impact |
| **Hardware + prototyping** | Arduino, fabrication, sensors | Physical prototypes and demos |

## Adaptive framing

| If the JD emphasizes… | Lead with… |
|------------------------|------------|
| AI agents / LLM pipelines | ProjectUs multi-agent pipeline, RAG, hallucination QA, deep research agent |
| Software engineering / full stack | ProjectUs platform (React, Next.js, Node), HPE internship, production shipping |
| Voice / conversational AI | TaleMate line, Dialogflow, CHI/UIST/IJHCS story |
| AI in education / CS education | VL/HCC + instructor studies + PRIME Lab |
| Learning & coaching products | ProjectUs — metrics, HCI in product, pipelines |
| UX / user research | HCI cert from VT, user studies across 3 labs, CHI/UIST publications |
| Hardware / makers / STEM | Marian Backer, assistive tech, PRIS-Lab, fabrication diploma |
| Consulting / freelance | Current contractor experience, breadth across AI + full stack + research |
| Remote / EU-based | Timezone flexibility (CR = overlaps with US + EU afternoon), Spain relocation plan |

## Exit narrative

Use `exit_story` from `config/profile.yml`: currently contracting, seeking full-time or digital-nomad freelance; Spain relocation top priority; Germany/Netherlands for salary; remote worldwide OK; three lanes (AI engineer, software engineer, HCI/UX).

## Superpowers (tailored summaries)

From `profile.yml` — always available to inject into Professional Summary when truthful for the JD:

1. Fast generalist / hacker — prototype and unblock.
2. **Education + children** — teaching experience; graduate research on **AI for children**.
3. **Hardware** — prototypes, circuits, building things that work.
4. **Full stack + research** — HCI, UX, implementation, data science.

## Cross-cutting advantage

Rare blend: **peer-reviewed HCI (voice, joint reading, AI in CS education)** + **shipping AI in a learning product** + **hardware/teaching muscle**.

## Portfolio / Scholar

- Portfolio: `profile.yml` → `portfolio_url`
- Scholar: `profile.yml` → `google_scholar`
- Optional alternate site: `https://www.danielvargasdiaz.net/` (listed on Scholar as homepage)

## Humanizing generated text

After drafting any free-form prose for external use — Professional Summary (`pdf` mode), cover letters / application answers (`apply` mode), LinkedIn outreach (`contacto` mode) — run it through the **`humanizer`** skill (`~/.claude/skills/humanizer`) as a final pass.

- If `writing-samples/` contains any files (besides its `README.md`), pass one or two to the skill as the voice-calibration sample so the rewrite matches Daniel's voice instead of the skill's generic default.
- Humanize **after** the content/keyword rules above are satisfied — it should not remove JD keywords, metrics, or factual claims, only smooth AI-sounding phrasing.

## Daniel's writing voice (calibrated from writing-samples/)

Use these patterns when generating any prose for Daniel — summaries, cover letters, application answers, outreach messages. The goal is text that sounds like him, not like a template.

### Structure
- **Story-first:** Open with a concrete personal experience or specific moment before stating the broader point. He grounds abstract goals in lived episodes (a science fair, a classroom, a volunteer project).
- **Claim → example:** After stating something, follow with a specific instance. Never leave claims unsupported.
- **Paragraph-based:** He writes in flowing paragraphs, not bullet-point prose. Reserve bullets for skills lists or structured sections only.
- **Long compound sentences:** He connects ideas with commas and conjunctions ("and", "which", "where") rather than chopping into short fragments. Mix in shorter sentences for emphasis, but his baseline rhythm is longer than typical AI output.

### Tone & word choice
- **Earnest, not performative:** His social-impact framing (mental health, education access, Latin America) comes from genuine experience. Never inflate it into marketing copy.
- **Academic but accessible:** Uses technical terms naturally when relevant (FMCW, Dialogflow, biosignals) but doesn't pile them up for credibility. Explains when the audience warrants it.
- **First-person, direct:** "I built", "I witnessed", "I plan to". Not passive ("a system was developed") unless citing group work.
- **Identity anchors he leans into:** Costa Rican, first-generation student, international background, inventor, educator. Weave these in when they're relevant to the role — don't force them.

### What to AVOID (anti-patterns not found in his writing)
- No buzzword chains ("passionate about leveraging synergies")
- No em dash cascading (one per paragraph max)
- No rule-of-three lists in prose ("innovative, dynamic, and forward-thinking")
- No filler openers ("In today's rapidly evolving landscape...")
- No "I am passionate about" — he shows motivation through stories, not declarations
- No corporate-speak ("value proposition", "stakeholder alignment", "thought leadership")
- No over-hedging ("I believe I could potentially be a good fit") — he states intent directly
- Minimal use of "Additionally" and "Furthermore" as paragraph openers — vary transitions

### Calibration samples (in writing-samples/)
- `VargasDiaz, DanielAlfredo_SoO.pdf` — MIT Media Lab SoO: strongest voice sample; personal narrative → problem → technical approach → social impact
- `VargasDiaz_DanielAlfredo_SoP.pdf` — Stanford SoP: copper metaphor opening; same narrative arc with more entrepreneurship framing
- `SOO_DanielVargasDiaz.pdf` — EPFL/ETH JDPLS SoO: education-focused; Intel Club House story; tangible interfaces; most learning-sciences-aligned
- `Cover_letter_DanielVargasDiaz.pdf` — identifeye HEALTH cover letter: shorter, more conventional; weakest voice sample (more generic than others)
- `PersonalStatement_VT.docx` — Virginia Tech personal statement (binary; not directly readable but available)

## Comp & negotiation

Set `compensation` in `profile.yml` when you start interviewing (Spain/EU bands vs remote USD). Scripts in template apply; negotiate in **English** unless the process is Spanish.

## Location policy

- Prefer clarity on **Spain/EU work authorization** and **remote-from-CR** vs on-site.
- Remote roles: score hybrid generously unless JD demands full on-site without relocation support.
