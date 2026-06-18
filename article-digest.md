# Article Digest — Proof Points (Daniel Vargas Díaz)

Compact publication anchors for CV tailoring. **Cite only claims supported by the papers** — numbers below are from the PDFs in this repo.

**Local PDFs (project root):**

- `Exploring parent involvement in e-book joint reading with voice agents.pdf` — *IJHCS* **2025**
- `3586182.3616699.pdf` — TaleMate, **UIST ’23 Adjunct**
- `3772318.3791550.pdf` — voice-assisted counting, **CHI ’26**
- `Exploring_the_Role_of_AI_Assistants_in_Computer_Science_Education_Methods_Implications_and_Instructor_Perspectives.pdf` — **IEEE VL/HCC 2023**

Also: [Google Scholar](https://scholar.google.com/citations?user=YhmlanYAAAAJ&hl=en), `cv.md`.

---

## TaleMate — parent involvement in joint e-book reading (*IJHCS*)

**Full title:** *Exploring parent involvement in e-book joint reading with voice agents*  
**Venue:** *International Journal of Human-Computer Studies* **198** (2025) 103461 — [DOI 10.1016/j.ijhcs.2025.103461](https://doi.org/10.1016/j.ijhcs.2025.103461)  
**Authors:** **Vargas-Diaz** (first), Kim, Karunaratna, Hornburg, Choi, Lee.

**Study design:** User study with **11 parent–child dyads** (**N = 22** total); children **3–6 years**. Three reading scenarios: parent as narrator with two VAs; parent as character with two VAs; parent and child each as a character with one VA.

**System:** **TaleMate** — joint reading app: assign AI voices to characters; parent can embody a character; participatory role selection with voice agents.

**Findings (abstract-level):** Supports children’s **engagement** and **story recall**; parents valued **interactivity** and **participatory** joint reading where parent and child choose roles.

**Hero lines for JDs:** Voice agents for **family joint reading**; empirical work with **parents + preschoolers**; design implications for **parent–child–voice-agent** collaboration.

---

## TaleMate — system design (*UIST ’23 Adjunct*)

**Full title:** *TaleMate: Collaborating with Voice Agents for Parent-Child Joint Reading Experiences*  
**Venue:** UIST ’23 Adjunct, San Francisco, CA — [DOI 10.1145/3586182.3616699](https://doi.org/10.1145/3586182.3616699) — **3 pages**.

**Design highlights:** **Six** distinct voice agents (“**Mates**”); drag-and-drop assignment of readers to book characters; parent **paces** reading (“Next”) so VAs and humans **alternate turns**; integrates children in voice assignment; book **“Birthday Beeps and Boops”** (*Pattern Pals*, Purdue Science and Stories Collaborative), ages **3–6**.

**Hero lines for JDs:** End-to-end **interaction design** for conversational/joint reading; **multimodal** pacing (human + TTS); bridges **audiobook limitations** and **parent involvement**.

---

## Voice-assisted counting — “when less is more” (*CHI ’26*)

**Full title:** *When Less Can Be More: Evaluating the Impact of Animated and Interactive Demonstrations in Voice-Assisted Counting Games for Young Children*  
**Venue:** CHI ’26, Barcelona, Spain (April 13–17, 2026) — [DOI 10.1145/3772318.3791550](https://doi.org/10.1145/3772318.3791550) — **16 pages**.

**Authors:** Karunaratna, **Vargas-Diaz**, Kim, Wang, Lee, Choi.

**Study design:** Tablet counting game; **within-subjects** study with **32 children** aged **2–4 years**. Conditions: **baseline** (static image + voice); **animated** (animation + voice); **interactive** (touch + animation + voice) — TTS used to simulate a voice assistant.

**Key results:** **Animated** demonstration improved **cardinal number word** understanding vs **baseline** and vs **interactive** condition. **Concurrent touch** demands increased **cognitive load**, limiting **counting aloud** — “more interactivity” not always better for very young children.

**Hero lines for JDs:** Empirical **multimodal HCI** (voice + touch + animation); **developmentally appropriate** design for **voice-assisted** early math; rigorous child study (**n=32**).

---

## AI assistants in CS education (*IEEE VL/HCC 2023*)

**Full title:** *Exploring the Role of AI Assistants in Computer Science Education: Methods, Implications, and Instructor Perspectives*  
**Venue:** 2023 IEEE Symposium on Visual Languages and Human-Centric Computing (VL/HCC) — DOI **10.1109/VL-HCC57772.2023.00018**.

**Authors:** Wang, **Vargas Díaz**, Brown, Chen.

**Study design:** (1) Evaluated **ChatGPT** on **187 problems** from **six** undergraduate CS courses (multiple topics/levels). (2) Two **problem-modification** strategies to adapt materials to model capabilities. (3) **Semi-structured interviews** with **11** CS instructors.

**Findings (paper framing):** Instructor perspectives on fairness, mental models, feasibility of adapting materials (**advanced** courses seen as easier to adapt than **intro**); false answers risk **incorrect mental models**; design implications for **tools** and **course adaptation**.

**Hero lines for JDs:** **CS education × LLMs** at scale (187 tasks); **instructor-facing** qualitative research; **curriculum** and **integrity**-aware framing.

---

## Related line (arXiv / duplicate theme)

A separate arXiv paper (*Towards adapting computer science courses to AI assistants’ capabilities*, **2306.03289**) overlaps the VL/HCC thread — use **one** primary citation per bullet on a tailored CV to avoid clutter.

---

## Wearables (breadth)

**Saving Face** — IMWUT lineage (face-touch detection). Cite from Scholar/`cv.md` when JD is sensing/wearables.

---

## Speech (Costa Rica children)

CARLA / *Tecnología en marcha* speech characterization — co-authored; use for **speech/HCI** or **language-resource** JDs.

---

## Thesis

**An Exploratory Study of Involving Parents in E-book Joint Reading with Voice Agents** — Virginia Tech **2024** (master’s thesis).

---

## ProjectUs.ai — Pulse-AI: Deep Research + Report Pipeline

**One-line framing:** A two-stage, human-in-the-loop pharma social-intelligence system that turns raw social/online posts into reviewer-ready monthly intelligence reports: an LLM deep-research engine that retrieves and synthesizes evidence, and a report pipeline that profiles a client, orchestrates research, verifies factual integrity, and produces editable narrative drafts and PDFs.

---

### Product 1 — Deep Research Pipeline (~3,000-line Python orchestrator)

Answers a research question against a proprietary post corpus and produces a cited intelligence report.

**End-to-end flow:**
1. **Query decomposition** — expands one research question into ~20 targeted sub-queries using an LLM (OpenAI Responses API), with prompt design tuned for hybrid retrieval (dense semantic embeddings + sparse BM25 keyword matching), so brand names and rare drug terms are matched precisely.
2. **Multi-pass retrieval** — runs each sub-query against a live search service (Next.js API at `/api/deep-research` backed by Pinecone + relevance filter), in parallel via `ThreadPoolExecutor`.
3. **Deduplication + gap analysis** — merges results across passes, identifies coverage gaps, and reruns follow-up queries to fill them (an agentic retrieve→critique→retrieve loop).
4. **Synthesis** — composes a structured report (Executive Summary + Key Themes with verbatim quotes), including a finalization pass that enforces English quotes and annotates translations.
5. **Adversarial review** — re-reads its own report with web search to flag weak or unsupported claims (self-critique stage).
6. **Delivery** — drafts a client email and writes JSON / Markdown / DOCX outputs, with date-window inference and resumable "email-only" reruns.

**Engineering notes:** date-filter inference from natural language, cross-platform robustness (Windows cp1252/Unicode-safe stdout), structured LLM logging, clean separation between search infrastructure (shared Next.js app) and report-specific synthesis prompts.

**Hero lines for JDs:** End-to-end **agentic RAG** system (query decomposition → hybrid retrieval → reranking → gap-driven re-search → cited synthesis) with full **provenance/traceability** over every retrieved document. **~3,000 lines of Python**, production-grade.

---

### Product 2 — Report Pipeline (modular, schema-driven)

Converts a client profile into a verified, human-reviewable report. Built as small composable "boxes," each with clear inputs/outputs and JSON-Schema contracts.

**Stage flow:**
1. **Company profile → research plan.** JSON profile declares focus_topics, market_topics, business_questions, framing, and emotion lens. `expand_prompt_manifest.py` deterministically expands into ~11 deep-research prompts including index-wide trends.
2. **Batched deep research.** Runs deep-research engine per prompt as parallel subprocess pool, with checkpointing and resume.
3. **Topic extraction + enrichment.** Parses research outputs into topic candidates, expands supporting corpora, runs adversarial gate applying each report's self-critique to drop/replace weak topics.
4. **Quantitative metrics.** Emotion shares, topic counts, engagement, platform breakdowns with month-over-month comparison.
5. **Section mapping.** Routes topics into report sections (primary narrative vs. secondary watch) based on origin.
6. **GPT normalization for human selection.** Rewrites topics into plain, non-specialist language for a pick-list, using XML-tagged, grounded prompts and schema-constrained JSON output.
7. **Rendering.** Produces analyst Markdown plus curated pick-list MD/DOCX.

**Hero lines for JDs:** Production **multi-agent LLM pipeline** mixing OpenAI + Claude with clean separation between deterministic computation and generative packaging; **schema-driven pipeline architecture** with JSON-Schema contracts between stages.

---

### L2 Verification Layer (integrity audit)

Runs before narrative is written; advisory, not blocking — produces per-topic flag list for human review.

**Track A** (quote-backed topics): URL existence in raw export (A1), quote-to-source fidelity via token overlap (A2), article-level source-diversity and platform diversity (A4), within-topic duplicate citation (A4a), cross-platform duplicate content (A4b), report-window date compliance (A5), cross-topic source over-reliance (A6).

**Track B** (metric-only topics): statistical fragility (low-n) and narrative-vs-metric direction alignment.

**LLM-as-judge calibration tools** that compare deterministic verdicts against an LLM fact-checker to validate thresholds.

**Hero lines for JDs:** Built a **hallucination-detection / LLM-output-auditing framework** combining text-similarity checks, numeric cross-validation, and an optional LLM judge — runs automatically as part of the pipeline (not a one-off review).

---

### Narrative Enrichment + Human-in-the-Loop UI

After a human assigns topics to roles, an enrichment step rebuilds richer section narratives and executive bullets from source material, extracts representative evidence posts, and proposes charts. Output is an editable draft reviewed and approved in a **Next.js UI** before PDF render.

**Hero lines for JDs:** Designed a **human-in-the-loop review workflow** where automated stages produce draft artifacts that humans edit, delete, and explicitly approve before anything ships — verification is advisory, never blocking.

---

### Next.js Dashboard + NLP "Patient Language" Feature

**Next.js 15** + Tailwind/SCSS dashboard on Vercel with serverless API routes. Built the precompute pipeline for a "Language Patterns" analytics block: normalizes and tokenizes post text, applies layered (core + platform + custom + optional health-domain) stopwords, computes unigram/bigram frequencies, and scores **distinctiveness** as a log-likelihood-style ratio comparing personal/caregiver language vs. non-personal (news/clinical/institutional) language — `ln(personal_rate) - ln(nonpersonal_rate)` with additive smoothing. Precomputes word-cloud layouts (`d3-cloud` with deterministic fallback) across all segment/persona/language filter combinations, versions the artifact, and uploads it to Firestore (manifest + bucket docs); the dashboard reads the active version via `/api/dashboard-language`. Pipeline is config-driven per client (custom stopword lists, optional segment field) with no code changes needed to onboard a new dataset.

**Hero lines for JDs:** Productionized an **NLP feature pipeline** (tokenization → stopword layering → frequency/effect-size scoring → versioned data delivery) feeding a live **Next.js/Vercel** dashboard; designed for **multi-tenant** reuse via config, not code changes.

---

### Cross-Cutting Technical Themes

| Theme | Details |
|-------|---------|
| **LLM orchestration & RAG** | Query decomposition, hybrid retrieval, agentic gap-filling, multi-model use (OpenAI for synthesis, Claude for judging/narrative), adversarial self-review, grounding/anti-hallucination constraints, XML-tagged and schema-constrained prompting |
| **Trust & verification** | Deterministic fact-checks layered with LLM judges; calibration harness; audit logs over auto-deletion |
| **Software engineering** | Modular pipeline with JSON-Schema contracts, subprocess orchestration, concurrency, checkpoint/resume, idempotent artifacts, cross-platform hardening, extensive unit-test suite (pytest + no-dependency runner) |
| **HCI / human-in-the-loop** | Every automated output is reviewable; "advisory, not blocking" verification; plain-language normalization for non-expert decision-makers; curated pick-lists; editable drafts with explicit approval gates |

---

### Translated Experience by Target Role

**For HCI / UX JDs:**
- Designed a human-in-the-loop review workflow for an AI report system: automated stages produce draft artifacts (topic pick-lists, narrative drafts, chart proposals) that humans edit, delete, and explicitly approve before anything ships — verification is advisory, never blocking.
- Reframed dense, technical analyst output into plain-language summaries for non-specialist decision-makers, treating the topic pick-list as a usability surface (scannable titles, jargon removal, evidence shown alongside claims).
- Specified the review UI flow (draft-by-section editing, deletable evidence cards/charts, approval gating, status polling) and the intermediate artifact schema that the front end consumes.
- Built trust-and-transparency UX: per-topic flag lists with severities, audit trails, and source-grounded evidence so reviewers can judge AI output rather than take it on faith.

**For AI Engineer JDs:**
- Built an agentic deep-research pipeline: LLM query decomposition into ~20 sub-queries, multi-pass hybrid (dense + BM25) retrieval, cross-pass dedup, automated gap analysis with follow-up retrieval, and structured synthesis with cited evidence.
- Engineered an adversarial self-review stage (LLM re-reads its own report with web search to flag unsupported claims) and a separate LLM-as-judge calibration harness to validate deterministic thresholds against human-equivalent judgments.
- Practiced production prompt engineering: grounding constraints to curb hallucination, XML-tagged inputs, schema-constrained JSON outputs, and deliberate multi-model selection (OpenAI vs. Claude) per task.
- Implemented an LLM fact-verification layer combining deterministic checks (quote-to-source token overlap, URL existence, date-window compliance, source/platform diversity, cross-topic reuse) with LLM judgment.

**For Software Engineer JDs:**
- Architected a modular, schema-driven data pipeline (profile → research plan → batched research → metrics → verification → narrative → PDF) with JSON-Schema contracts between stages and idempotent, checkpointed artifacts.
- Built a parallel subprocess orchestrator (thread pools, batching, checkpoint/resume, failure isolation so partial failures still yield output) over an external LLM/search service.
- Hardened for real-world ops: cross-platform Unicode/encoding handling (Windows cp1252), structured logging, resumable reruns, and graceful degradation.
- Wrote an extensive automated test suite (deterministic fixtures + real-data tests that skip cleanly) with both a pytest path and a zero-dependency runner; addressed code-review feedback on resource handling and edge cases.

---

### Keyword Bank (for CV tailoring)

RAG, hybrid retrieval (dense + BM25), Pinecone, query decomposition, agentic LLM pipelines, OpenAI Responses API, Claude, prompt engineering, hallucination mitigation, LLM-as-judge / evaluation, adversarial review, JSON Schema, Python, Next.js, subprocess orchestration, concurrency/ThreadPoolExecutor, checkpoint/resume, data pipeline architecture, human-in-the-loop, review/approval UX, plain-language content design, fact verification, unit testing, DOCX/PDF generation, matplotlib, Cohere reranking, Firestore, MongoDB, BigQuery, Vercel.
