<div align="center">

# Yuvraj Kashyap

Computer Science at UT Dallas · graduating May 2027 · Dallas, Texas

**Incoming SWE Intern @ Base Power · Open to new-grad SWE roles**

[**Portfolio**](https://yuvrajkashyap.com) · [**Resume**](https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf) · [**LinkedIn**](https://www.linkedin.com/in/yuvraj-kashyap) · [**Email**](mailto:ykyuvrajkashyap@gmail.com)

</div>

Hey, I'm Yuvraj. I study computer science, finance, and entrepreneurship at UT Dallas. I like figuring out how things work, building something useful from that understanding, and getting it into people's hands. My work spans software products, research, and client projects, and I'm happy to learn a new field when the problem is worth working on.

Recently, I've been building [**LegacyDiff**](https://github.com/YuvrajKashyap/legacydiff), which compares old and rewritten software on the same inputs, and [**WorldState**](https://github.com/YuvrajKashyap/worldstate), which gives a physical workspace persistent, searchable visual memory.

## Experience

**Incoming Software Engineering Intern · Base Power**

**Software Engineering Intern · Medceptor · Apr–Aug 2026**

I shipped 14+ PRs for question-bank and exam workflows used by paying customers, helping expand the product into CNA/LPN exam preparation. My work covered question filtering, import validation, scoring, and review flows across Next.js, TypeScript, Django, and Postgres.

**Undergraduate Researcher · UT Dallas · Oct 2025–present**

I work on UAV and smart-city simulation, combining urban geometry with multi-agent path planning, visibility, occlusion, and sensing constraints.

**Engineering Lead & Senior Consultant · Consult Your Community · Jan 2026–present**

I translated Glydr's client requirements into a web-based gaming hub prototype and led the technical work from scoping through final handoff.

**Software Research Assistant · NOVA Autonomous Driving · Sep 2023–Aug 2025**

I built Python preprocessing pipelines that reduced a point cloud from 370,277 to 20,528 points while preserving its geometry. I also worked on sensor and I/O reliability across the vehicle's subsystems.

## Selected projects

<p align="center">
  <a href="https://aletheia.yuvrajkashyap.com"><img src="https://raw.githubusercontent.com/YuvrajKashyap/aletheia/main/docs/assets/screenshots/overview.png" width="49%" alt="Aletheia search and evaluation dashboard" /></a>
  <a href="https://visionlock.yuvrajkashyap.com"><img src="https://raw.githubusercontent.com/YuvrajKashyap/vision-lock/main/screenshots/portfolio-hero.png" width="49%" alt="Vision Lock tracking several objects in a local vision run" /></a>
</p>

### [LegacyDiff](https://github.com/YuvrajKashyap/legacydiff) · Reviewing software rewrites

LegacyDiff runs old and new implementations on the same inputs and shows exactly where their behavior differs. AI specialists help investigate the evidence; a reviewer chooses the intended behavior, approves a specific version, and exports acceptance checks. The local app includes 384 authored inputs across four synthetic scenarios, shared review state, and version-specific approvals.

[Source and walkthrough](https://github.com/YuvrajKashyap/legacydiff) · [Architecture](https://github.com/YuvrajKashyap/legacydiff/blob/main/docs/ARCHITECTURE.md) · [Verification](https://github.com/YuvrajKashyap/legacydiff/blob/main/docs/VERIFICATION.md)

`TypeScript` `React` `Python` `SpacetimeDB` `NVIDIA Nemotron`

### [Aletheia](https://github.com/YuvrajKashyap/aletheia) · Search infrastructure and retrieval evaluation

Aletheia is a search system I built to compare BM25, dense retrieval, hybrid RRF, and cross-encoder reranking on BEIR SciFact. It records scores, rank changes, latency, and provenance at each retrieval stage, so I can see why a result showed up instead of only looking at the final list.

Across 5,183 documents and 300 benchmark queries, hybrid RRF reached **0.8429 Recall@10**.

[Live system](https://aletheia.yuvrajkashyap.com) · [Source](https://github.com/YuvrajKashyap/aletheia) · [Benchmark](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/benchmark-results.md) · [Architecture](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/architecture.md)

`Python` `FastAPI` `PostgreSQL` `Redis/RQ` `OpenSearch` `Qdrant` `Next.js`

### [Atlas](https://github.com/YuvrajKashyap/atlas) · Durable distributed crawl and search

Atlas came from wanting to build a crawler that would not fall apart as soon as a worker died or OpenSearch went down. PostgreSQL keeps the real state, fetch, extract, and index are separate idempotent stages, and a durable outbox makes indexing recoverable without repeating the network fetch.

Its **10,000-page fault benchmark** passed the published release checks. The repository includes an operator console, recovery runbooks, and AWS/Terraform infrastructure.

[Project record](https://atlas.yuvrajkashyap.com) · [Source](https://github.com/YuvrajKashyap/atlas) · [Benchmark](https://github.com/YuvrajKashyap/atlas/blob/main/docs/benchmark.md) · [Runbooks](https://github.com/YuvrajKashyap/atlas/tree/main/docs/runbooks)

`Python` `FastAPI` `PostgreSQL` `Redis/RQ` `OpenSearch` `AWS` `Terraform`

### [Vision Lock](https://github.com/YuvrajKashyap/vision-lock) · Real-time local computer vision

With Vision Lock, I wanted to see whether I could describe an object in plain text, track it in a moving scene, and lock onto it with a click or hand gesture. It combines open-vocabulary detection, multi-object tracking, image-text ranking, and browser telemetry, all running locally without saving frames or crops.

A reproducible RTX 4060 run reached **11.239 FPS** and **64.294 ms p50** end-to-end latency. The backend has 28 passing tests.

[Live showcase](https://visionlock.yuvrajkashyap.com) · [Source](https://github.com/YuvrajKashyap/vision-lock) · [Performance](https://github.com/YuvrajKashyap/vision-lock/blob/main/docs/PERFORMANCE.md) · [Architecture](https://github.com/YuvrajKashyap/vision-lock/blob/main/docs/ARCHITECTURE.md)

`Python` `FastAPI` `PyTorch` `OpenCV` `React` `WebSockets`

### [Sticky](https://github.com/YuvrajKashyap/sticky) · The task system I actually use

Sticky handles my task capture, recurring work, reminders, calendar planning, realtime sync, and agent access. Browser writes go through a versioned Hono API, Postgres writes and outbox events commit together, and personal data stays behind owner-scoped row-level security. Because the production data is private, the repository ships with a sanitized local demo.

The release gate includes unit and API tests, client/server secret audits, and **84 Playwright cases** across desktop and mobile.

[Source and demo](https://github.com/YuvrajKashyap/sticky) · [Architecture](https://github.com/YuvrajKashyap/sticky/blob/main/docs/connected-platform.md)

`TypeScript` `Next.js` `Hono` `PostgreSQL` `Supabase` `Realtime` `MCP`

## More of my work

[Beyond Chat](https://github.com/YuvrajKashyap/Beyond-Chat) · [Answer Map](https://github.com/YuvrajKashyap/answer-map) · [Dallas 3D](https://github.com/YuvrajKashyap/dallas-3d-city-model) · [Axis](https://github.com/YuvrajKashyap/Axis) · [Capital case study](https://github.com/YuvrajKashyap/capital-case-study) · [Full project archive](https://yuvrajkashyap.com/#projects)

Try the [Beyond Chat live prototype](https://beyond-chat-production.vercel.app/). Early access is limited while the product is being rebuilt.

## What I work with

- **Languages:** Python, TypeScript, JavaScript, C++, SQL
- **Backend and data:** FastAPI, Node.js, PostgreSQL, Supabase, Redis, OpenSearch, Qdrant
- **Product and infrastructure:** React, Next.js, PyTorch, OpenCV, AWS, Terraform, Docker, GitHub Actions

Away from the keyboard, I've played competitive tennis for most of my life, including at the NCAA Division II level. I still get on court when I can.

## Say hi

I'm graduating in May 2027 and open to opportunities across industries. I'm interested in work where I can build, learn from people who know their craft, and contribute to the product and business as well as the technology. If you think we'd work well together, I'd be happy to hear from you.

<div align="center">

[**Email me**](mailto:ykyuvrajkashyap@gmail.com) · [**Explore the portfolio**](https://yuvrajkashyap.com) · [**Read my resume**](https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf)

</div>
