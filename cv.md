# Daniel Vargas Díaz

**Location:** San José, Costa Rica · **Phone:** +506 86753981 · **Email:** dan.vargasdiaz@gmail.com  
**LinkedIn:** [linkedin.com/in/daniel-vargas-d](https://www.linkedin.com/in/daniel-vargas-d/) · **Portfolio:** [danielvargas portfolio](https://portfolio-two-black-s7bro55mlr.vercel.app/) · **Google Scholar:** [profile](https://scholar.google.com/citations?user=YhmlanYAAAAJ&hl=en)

## Summary

HCI and applied AI professional with an M.S. in Computer Science from Virginia Tech (GPA 3.9/4). Head of Learning and AI at ProjectUs.ai, building multi-platform AI data pipelines (social/web scraping, GPT-based filtering, Pinecone hybrid vector search, BigQuery analytics) and multi-agent LLM systems for pharma clients — including a 3-layer report-generation pipeline with deterministic metrics and automated hallucination-detection QA, and a citation-backed deep research agent. Background in teaching (TA), SD-WAN/UI internship (HPE), STEM education, and research on voice agents, joint parent–child reading, CS education and AI assistants (CHI, IJHCS, UIST, VL/HCC, IMWUT). Open to roles outside Costa Rica, freelance, or relocation to Spain; targeting HCI and AI engineering only.

## Work Experience

### ProjectUs.ai — Head of Learning and AI *(Remote)*  
**May 2024 – Present**

- Built **Pulse-AI**, a two-stage pharma social-intelligence system: an agentic deep-research engine (~3,000 lines of **Python**) that decomposes a question into ~20 sub-queries, runs multi-pass hybrid retrieval (**Pinecone** dense + BM25 sparse vectors, **Cohere** reranking, LLM relevance filtering), performs automated gap analysis with follow-up retrieval, and synthesizes citation-backed reports with adversarial self-review — plus a modular report pipeline with **JSON-Schema** contracts between stages that turns a client profile into verified, human-reviewable intelligence reports.
- Built and maintained the ProjectUs.ai web platform (**React**, **Next.js 15**, **Node.js**, Vercel serverless API routes), including a client-facing analytics dashboard with an NLP-driven "Patient Language" feature: tokenization, layered stopword filtering, unigram/bigram frequency, and a log-likelihood-style distinctiveness score contrasting personal vs. institutional language, served via versioned **Firestore**-backed datasets.
- Designed and built a multi-platform social and web scraping pipeline (Reddit, YouTube, X/Twitter, TikTok, Facebook, LinkedIn, web search) in **Python** for pharma clients, tracking online conversation about their medications and the diseases they treat.
- Built GPT-based relevance filtering and emotion/sentiment analysis (OpenAI, Hume) and standardized multi-source results into a common schema.
- Built the storage and retrieval layer: **MongoDB** and **BigQuery** (SQL) for structured data, and **Pinecone** (hybrid dense + sparse vectors with **Cohere** reranking) for retrieval-augmented search over scraped content.
- Architected a 3-layer multi-agent LLM pipeline (OpenAI + **Claude**) for monthly pharma social-listening PDF reports: Layer 1 drafts a narrative brief grounded in a deterministic metrics engine, Layer 2 (Claude) packages it into structured claims and charts, Layer 3 (Claude) audits the draft for hallucinations and gaps before delivery.
- Built an L2 verification layer: Track A checks quote-to-source fidelity (token overlap, URL existence, source/platform diversity, date compliance); Track B validates metric-based claims against numeric indices. Includes LLM-as-judge calibration tools comparing deterministic verdicts against LLM fact-checkers.
- Designed the human-in-the-loop review workflow: automated stages produce draft artifacts (topic pick-lists in plain language, narrative drafts, chart proposals) that humans edit, approve, or reject in a **Next.js** UI before PDF render — verification is advisory, never blocking.
- Built parallel subprocess orchestration (thread pools, batching, checkpoint/resume, failure isolation) and hardened for cross-platform ops (Windows cp1252/Unicode-safe stdout, structured logging, resumable reruns).

### Virginia Polytechnic Institute and State University — Graduate Teaching Assistant *(VA, USA)*  
**Aug. 2022 – May 2024**

- **CS2506 Computer Organization II** (Fall 2023, Spring 2024): Guided students; evaluated assembly assignments.
- **CS3724 Introduction to HCI** (Spring 2023): Supported CS students on HCI foundations and Agile final projects.
- **CS1064 Introduction to Python** (Fall 2022): Office hours; graded projects with feedback.

### Hewlett Packard Enterprise — Software Engineer Intern *(CA, USA)*  
**Jun. 2023 – Aug. 2023**

- Built 3D network topology visualization for Silver Peak–HPE SD-WAN Orchestrator.
- Proposed UI/Orchestrator features; collaborated with UX/UI on solutions.

### Equal Education Partners — Computer Science Instructor, STEMHaus Online Summer School *(UK, virtual)*  
**Jul. 2022 – Aug. 2022**

- Designed lectures and workshops on CS topics; prepared learners for GCSE/A Level STEM.

### Marian Backer School — Makerspace Teacher *(San José, CR)*  
**Jan. 2022 – Jun. 2022**

- Combined coding, electronics, and robotics for ages 7–16; piloted preschool coding/circuits program; elective on AI principles.

## Research Experience

### Echolab (Virginia Tech) — Graduate Volunteer RA · Advisor: Sang Won Lee, Ph.D.  
**Nov. 2022 – May 2024**

- TaleMate: voice agents for joint parent–child e-book reading; built with **React**, **Node.js**, and **Next.js**; user studies; qualitative/quantitative analysis.

### CoDes Lab (Virginia Tech) — Graduate Volunteer RA · Advisor: Koeun Choi, Ph.D.  
**Sep. 2022 – May 2024**

- UI for conversational agent supporting children’s math learning; Dialogflow intents; supervised undergrad helpers.

### PRIME Lab (Virginia Tech) — Graduate Volunteer RA · Advisor: Yan Chen, Ph.D.  
**Jan. 2023 – Aug. 2023**

- Studied impact of ChatGPT/Copilot on CS education; proposed course adaptations; user studies with instructors.

### MIT Media Lab, Fluid Interfaces Group — Undergraduate Virtual RA · Advisor: Camilo Rojas, Ph.D.  
**Apr. 2020 – Sep. 2021**

- Co-led technical work on **Us** (AI web platform for socio-cognitive skills) and **Saving Face** (COVID-era face-touch detection via earbuds).
- Signal processing/ML; user testing protocols; coordination across MIT, Wellesley, and international students.

### PRIS-Lab, UCR — Undergraduate RA · Advisors: Francisco Siles, Ph.D.; Marvin Coto, Ph.D.  
**Jun. 2020 – Dec. 2020; Jan. 2018 – Dec. 2020** *(multiple periods)*

- Biocomputational platform for coronavirus protease inhibitor identification; docking evaluation with biotechnologists; outreach with design students.
- Assistive tech for special education; ML for speech classification; Costa Rican child speech data toward synthetic child voice.
- Augmentative communication device for vocalization classification (CONESCAPAN).

### DCLab, UCR — Undergraduate RA · Advisor: Francisco Siles, Ph.D.  
**Jul. 2019 – Dec. 2019**

- Pattern recognition for cancer prediction; supported clinicians and workshops; organized monthly talks.

### LAFTLA, UCR — Undergraduate RA · Advisor: Jaime Cascante, Ph.D.  
**Jan. 2017 – Dec. 2019**

- DIY fiber optic fusion splicer assembly; LabVIEW control programming.

## Selected Publications & Presentations

- **CHI 2026**: When Less Can Be More — animated/interactive demos in voice-assisted counting games for young children (Karunaratna, **Vargas-Diaz**, Kim, Wang, Lee, Choi).
- **IJHCS** (2025): Exploring parent involvement in e-book joint reading with voice agents (**Vargas-Diaz** et al.; IJHCS 198, 103461).
- **IEEE VL/HCC 2023**: Towards adapting CS courses to AI assistants’ capabilities (Wang, **Vargas-Diaz**, Brown, Chen).
- **UIST 2023** (adjunct): TaleMate — collaborating with voice agents for parent–child joint reading.
- **IMWUT** (2021): Saving Face — scalable signaling of face touches (Rojas et al.; includes **Vargas**).
- **CSCW 2024** companion: Evaluation of interactive demonstration in voice-assisted counting for young children.
- Additional: CSCW/CDS workshops, CONESCAPAN, CARLA, Spanish-language speech characterization — see [Google Scholar](https://scholar.google.com/citations?user=YhmlanYAAAAJ&hl=en) for full list.

## Education

- **M.S. Computer Science & Applications** — Virginia Tech (Aug. 2022 – May 2024), GPA **3.9/4**
- **Graduate Certificate, Human–Computer Interaction** — Virginia Tech (Aug. 2022 – May 2024)
- **B.S. Electrical Engineering (Computers & Networks emphasis)** — Universidad de Costa Rica (Mar. 2017 – Feb. 2022), GPA **8.6/10**
- **Exchange** — Universidad Politécnica de Madrid (Jan.–Jun. 2020), biomedical engineering focus, UCR full scholarship
- **Diploma, Industrial Design & Digital Fabrication** — Universidad Don Bosco (Jan. 2016 – Dec. 2016), top-30 of 200+
- **Technical electromechanics + high school** — Don Bosco Technical High School (Jan. 2011 – Dec. 2016)

## Grants, Awards & Certifications

- Opportunity Funds Scholarship (EducationUSA / U.S. Department of State), Jan. 2021  
- UCR Study Abroad Scholarship (~$12,000, UPM), Jan. 2020  
- **Introduction to Agent Skills** (Anthropic, May 2026) · **AI Fluency Framework & Foundations** (Anthropic, Apr 2026) · **Claude Code 101** (Anthropic, May 2026)  
- **Aruba Accredited SD-WAN Professional** (HPE) · **Introduction to UI/UX** (Skillsoft) · Huawei Seeds for the Future · MIT Delta V (2021)

## Skills

**Software:** C/C++, Python, Java/JavaScript, React, Node.js, Next.js, HTML, SQL, BigQuery, MongoDB, Pinecone (vector DB), LLM APIs (OpenAI, Anthropic), ML fundamentals, SPICE, LaTeX, AWS, LabVIEW, Verilog, Assembly, Arduino, MATLAB, Bash, Android, Swift  

**Education / tools:** Code.org, Tinkercad, Scratch, Lego Education  

**Prototyping / design:** 3D modeling, circuit design, laser cut, 3D printing; Figma, Illustrator, Photoshop  

**Languages:** Spanish (native), English (advanced), Japanese (basic)

## Leadership & Outreach (abbreviated)

- Board member, Latin American and Iberian Graduate Students Association, VT (May 2023 – May 2024)  
- SalsaTech performance team, VT (Aug.–Dec. 2022)  
- Student rep / IEEE Women in Engineering leadership, UCR (2019–2021)  
- STEM community volunteer (Tirrases), electoral tribunal, FundaVida robotics mentor, PRIS-Lab team lead on assistive tech — see full CV for detail.
