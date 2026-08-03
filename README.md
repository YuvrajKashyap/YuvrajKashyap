<div align="center">

# Yuvraj Kashyap

**I build search systems, backend infrastructure, computer vision, and full-stack AI products.**

Computer Science at UT Dallas · graduating May 2027 · Dallas, Texas

**Looking for software engineering roles.**

[**Portfolio**](https://yuvrajkashyap.com) · [**Resume**](https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf) · [**LinkedIn**](https://www.linkedin.com/in/yuvraj-kashyap) · [**Email**](mailto:ykyuvrajkashyap@gmail.com)

</div>

Hey, I'm Yuvraj. I like turning interesting technical ideas into products people can explore and systems other engineers can understand. I work mostly in Python and TypeScript, and I enjoy following a feature through the data model, API, interface, deployment, tests, and documentation.

Right now, I'm building [**WorldState**](https://github.com/YuvrajKashyap/worldstate), which turns webcam or phone video into a persistent, queryable model of a physical space.

| **0.8429 Recall@10** | **10,000 pages** | **11.2 FPS** | **370K → 20.5K points** |
| :---: | :---: | :---: | :---: |
| Aletheia hybrid retrieval | Atlas failure benchmark | Vision Lock local run | NOVA point-cloud reduction |

<p align="center">
  <a href="https://aletheia.yuvrajkashyap.com"><img src="https://raw.githubusercontent.com/YuvrajKashyap/aletheia/main/docs/assets/screenshots/overview.png" width="49%" alt="Aletheia search and evaluation dashboard" /></a>
  <a href="https://visionlock.yuvrajkashyap.com"><img src="https://raw.githubusercontent.com/YuvrajKashyap/vision-lock/main/screenshots/portfolio-hero.png" width="49%" alt="Vision Lock tracking several objects in a local vision run" /></a>
</p>

## A few things I've built

### [Aletheia](https://github.com/YuvrajKashyap/aletheia) · Search infrastructure and retrieval evaluation

Aletheia is a search system I built to compare BM25, dense retrieval, hybrid RRF, and cross-encoder reranking on BEIR SciFact. It records scores, rank changes, latency, and provenance at each retrieval stage, so I can see why a result showed up instead of only looking at the final list.

Across 5,183 documents and 300 benchmark queries, hybrid RRF reached **0.8429 Recall@10**.

[Live system](https://aletheia.yuvrajkashyap.com) · [Source](https://github.com/YuvrajKashyap/aletheia) · [Benchmark](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/benchmark-results.md) · [Architecture](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/architecture.md)

`Python` `FastAPI` `PostgreSQL` `Redis/RQ` `OpenSearch` `Qdrant` `Next.js`

### [Atlas](https://github.com/YuvrajKashyap/atlas) · Durable distributed crawl and search

Atlas came from wanting to build a crawler that would not fall apart as soon as a worker died or OpenSearch went down. PostgreSQL keeps the real state, fetch, extract, and index are separate idempotent stages, and a durable outbox makes indexing recoverable without repeating the network fetch.

Its checked **10,000-page fault benchmark** passed every published release check. The repository also includes an operator console, runbooks, a threat model, AWS/Terraform infrastructure, CodeQL, container scanning, and SBOM generation.

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

## Experience

- **Software Engineering Intern, IDK Studios / Medceptor:** I ship product and backend features for an AI-driven medical-education platform using Next.js, TypeScript, Django, and Supabase/Postgres.
- **Undergraduate Researcher, UT Dallas:** I work on UAV and smart-city simulation across multi-agent path planning, urban geometry, occlusion, visibility, and sensing constraints.
- **Systems & Electrical Engineer, NOVA Autonomous Driving:** I built Python point-cloud preprocessing and worked on dual battery banks, high-voltage lines, and vehicle I/O systems.

## More of my work

[Beyond Chat](https://github.com/YuvrajKashyap/Beyond-Chat) · [Answer Map](https://github.com/YuvrajKashyap/answer-map) · [Dallas 3D](https://github.com/YuvrajKashyap/dallas-3d-city-model) · [Axis](https://github.com/YuvrajKashyap/Axis) · [Capital case study](https://github.com/YuvrajKashyap/capital-case-study) · [Full project archive](https://yuvrajkashyap.com/#projects)

## What I work with

- **Languages:** Python, TypeScript, JavaScript, C++, SQL
- **Backend and data:** FastAPI, Node.js, PostgreSQL, Supabase, Redis, OpenSearch, Qdrant
- **Product and infrastructure:** React, Next.js, PyTorch, OpenCV, AWS, Terraform, Docker, GitHub Actions

I also study finance and entrepreneurship. I played competitive tennis for most of my life, including at the NCAA Division II level, and I still get on court when I can.

## Say hi

I'm graduating in May 2027 and looking for software engineering roles. If you're working on search, AI infrastructure, developer tools, computer vision, or a product that needs someone comfortable moving across the stack, send me an email.

<div align="center">

[**Email me**](mailto:ykyuvrajkashyap@gmail.com) · [**Explore the portfolio**](https://yuvrajkashyap.com) · [**Read my resume**](https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf)

</div>
