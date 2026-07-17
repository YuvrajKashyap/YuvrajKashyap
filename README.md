<h1 align="center">Yuvraj Kashyap</h1>

<p align="center"><strong>Software engineer building search, distributed, spatial, and product systems.</strong></p>

<p align="center">Computer Science at UT Dallas | Class of 2027 | Open to software engineering opportunities</p>

<p align="center">
  <a href="https://yuvrajkashyap.com"><strong>Portfolio</strong></a> &nbsp;|&nbsp;
  <a href="https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf"><strong>Resume</strong></a> &nbsp;|&nbsp;
  <a href="https://www.linkedin.com/in/yuvraj-kashyap"><strong>LinkedIn</strong></a> &nbsp;|&nbsp;
  <a href="mailto:ykyuvrajkashyap@gmail.com"><strong>Email</strong></a>
</p>

I am a Computer Science student at UT Dallas who likes turning interesting technical ideas into products people can explore and systems other engineers can understand.

I work across Python and TypeScript and enjoy following a feature through the data model, API, interface, deployment, tests, and documentation. I am happiest on small, ambitious teams where people move quickly, ask good questions, and care about the details without making the process heavier than it needs to be.

## A few concrete results

- Evaluated four retrieval modes across **300 BEIR SciFact queries** in [Aletheia](https://github.com/YuvrajKashyap/aletheia); hybrid retrieval reached **0.8429 Recall@10** with zero failed queries.
- Built Atlas around recoverable work, idempotent stages, and durable indexing; its backend has **69 passing tests** and **91.03% coverage**.
- Turned **1,553 OpenStreetMap building footprints** into a reproducible Dallas geometry model with **93.33% sampled visibility coverage** and a **4.99 km A-star route**.
- Reduced a NOVA autonomous vehicle point cloud from **370,277 to 20,528 points** while preserving its geometry, then worked on the vehicle's primary and secondary power systems.

## Featured engineering work

### [Aletheia](https://github.com/YuvrajKashyap/aletheia) | Search infrastructure, ranking, and evaluation

<a href="https://aletheia.yuvrajkashyap.com">
  <img src="https://raw.githubusercontent.com/YuvrajKashyap/aletheia/main/docs/assets/screenshots/overview.png" alt="Aletheia search and evaluation dashboard" width="100%" />
</a>

Aletheia compares BM25, dense, hybrid, and cross-encoder reranked retrieval over a real benchmark corpus. The full stack includes OpenSearch, Qdrant, PostgreSQL, Redis workers, explicit index versions, query traces, experiment comparison, replay, and system health.

The public site is generated from real full-stack runs. It exposes traces, evaluations, index metadata, and corpus records without running the full search cluster around the clock.

[`Live demo`](https://aletheia.yuvrajkashyap.com) [`Source`](https://github.com/YuvrajKashyap/aletheia) [`Benchmark`](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/benchmark-results.md) [`Architecture`](https://github.com/YuvrajKashyap/aletheia/blob/main/docs/architecture.md)

`Python` `FastAPI` `PostgreSQL` `Redis/RQ` `OpenSearch` `Qdrant` `Next.js`

### [Atlas](https://github.com/YuvrajKashyap/atlas) | Durable web crawl and search platform

Atlas keeps crawl runs, leases, stage tasks, versions, and incidents in PostgreSQL. Redis helps workers pick up work, while fetch, extract, and index remain separate idempotent stages. A durable outbox lets indexing recover cleanly after an OpenSearch outage without repeating the network fetch.

The repository includes an operator console, threat model, service objectives, architecture decisions, runbooks, Terraform, CodeQL, container scanning, SBOM generation, and an explicit runtime status contract.

[`Project record`](https://atlas-rho-brown.vercel.app) [`Source`](https://github.com/YuvrajKashyap/atlas) [`Threat model`](https://github.com/YuvrajKashyap/atlas/blob/main/docs/threat-model.md) [`Runbooks`](https://github.com/YuvrajKashyap/atlas/tree/main/docs/runbooks)

`Python` `FastAPI` `PostgreSQL` `Redis/RQ` `OpenSearch` `AWS` `Terraform`

### [Dallas 3D Urban Geometry Lab](https://github.com/YuvrajKashyap/dallas-3d-city-model) | Geospatial modeling and path planning

<a href="https://github.com/YuvrajKashyap/dallas-3d-city-model">
  <img src="https://raw.githubusercontent.com/YuvrajKashyap/dallas-3d-city-model/main/screenshots/portfolio-hero.png" alt="Downtown Dallas 3D model with a planned route and visibility observers" width="100%" />
</a>

This pipeline converts OpenStreetMap footprints into a traceable LOD1-style city model. It records the source and confidence of every building height, works in the correct UTM projection, runs 2.5D line-of-sight coverage, and plans fixed-altitude routes around obstacles.

I report the results as geometry experiments, not real flight guidance. The repository includes methodology, provenance, unit tests, processed outputs, an inspectable Blender scene, and final renders.

[`Source`](https://github.com/YuvrajKashyap/dallas-3d-city-model) [`Methodology`](https://github.com/YuvrajKashyap/dallas-3d-city-model/blob/main/docs/METHODOLOGY.md) [`Project dossier`](https://yuvrajkashyap.com/projects/dallas-3d-city-model)

`Python` `GeoPandas` `Shapely` `Blender` `Pytest`

### [Sticky](https://github.com/YuvrajKashyap/sticky) | Private task platform with durable workflows

Sticky is the task system I use. It combines fast capture, recurring work, reminders, calendar planning, realtime sync, and an agent-facing API in one installable web app.

Browser writes pass through a versioned Hono API. Postgres writes and outbox events commit together. Realtime events invalidate client caches. Private tables live behind owner-scoped row-level security, and integration credentials stay encrypted on the server. The production app remains allow-listed because it contains personal data; the repository starts with a sanitized local demo.

[`Source and demo instructions`](https://github.com/YuvrajKashyap/sticky) [`Architecture`](https://github.com/YuvrajKashyap/sticky/blob/main/docs/connected-platform.md)

`Next.js` `TypeScript` `Hono` `Supabase` `PostgreSQL` `Realtime` `MCP`

### [Axis](https://github.com/YuvrajKashyap/Axis) | A spatial interface for personal alignment

<a href="https://axis.yuvrajkashyap.com">
  <img src="https://raw.githubusercontent.com/YuvrajKashyap/Axis/main/public/showcase/axis-orrery.png" alt="Axis orrery interface showing life domains as planets" width="100%" />
</a>

Axis replaces the usual productivity dashboard with an orrery. Domains drift outward when they need attention, commitments pull them back into orbit, and a guided reset helps choose the next concrete action.

Under the visual idea are time-derived state, user-scoped data with row-level security, signed QStash callbacks, stale-notification checks, responsive drag and keyboard interaction, and a read-only public fallback.

[`Live demo`](https://axis.yuvrajkashyap.com) [`Source`](https://github.com/YuvrajKashyap/Axis) [`Case study`](https://github.com/YuvrajKashyap/Axis/blob/main/docs/CASE_STUDY.md)

`Next.js` `React` `TypeScript` `Supabase` `PostgreSQL` `QStash` `Resend`

## More product work

- **[Beyond Chat](https://github.com/YuvrajKashyap/Beyond-Chat):** Collaborative AI workspace organized around durable artifacts and dedicated writing, research, image, data, and finance studios. I have more than 80 authored commits in the shared repository.
- **[Arcade](https://github.com/YuvrajKashyap/arcade):** Personal arcade platform built with Next.js.
- **[Capital case study](https://github.com/YuvrajKashyap/capital-case-study):** Public product and engineering record for a private finance application, separated so the real app and its data remain protected.
- **[Personal website](https://github.com/YuvrajKashyap/personal-website):** The source behind [yuvrajkashyap.com](https://yuvrajkashyap.com), including the project archive, experience record, and portfolio interface.

## Experience beyond personal projects

- **Undergraduate Researcher, UT Dallas:** Building UAV and smart-city simulation work over a 4 km by 4 km OpenStreetMap and Blender environment, with multi-agent path planning, occlusion, visibility, and sensing constraints.
- **VP of Finance and Project Team Lead, Consult Your Community:** Leading client work across product operations, financial strategy, go-to-market planning, and delivery; built a web gaming hub prototype for a hardware client.
- **Systems and Electrical Engineer, NOVA Autonomous Driving:** Built Python preprocessing for 3D sensor data and worked on dual battery banks, high-voltage lines, and vehicle I/O systems.
- **Peer Advisor, UT Dallas University Housing:** Primary point of contact for more than 120 residents.

## A bit about me

I grew up in Saudi Arabia and Texas, and competitive tennis was a big part of my life, including time as an NCAA Division II player. I still play whenever I can. I also study finance and entrepreneurship alongside computer science because I enjoy the product and business side of building, too.

## What I work with

- **Languages:** Python, TypeScript, JavaScript, SQL
- **Backend and data:** FastAPI, Hono, PostgreSQL, Supabase, Redis, OpenSearch, Qdrant
- **Frontend:** React, Next.js, Vite, realtime interfaces, responsive interaction design
- **Infrastructure and quality:** AWS, Terraform, Docker, GitHub Actions, Pytest, Playwright, Ruff
- **Spatial and autonomy:** OpenStreetMap, GeoPandas, Shapely, Blender, point clouds, visibility, path planning

## Let's talk

I am looking for software engineering, ML systems, platform, developer tools, and product engineering opportunities.

I would love to join a small team where I can learn quickly, take real ownership, and help turn rough ideas into software people enjoy using. If anything here overlaps with what you are building, email me. I am always happy to talk through the work.

<p align="center">
  <a href="mailto:ykyuvrajkashyap@gmail.com"><strong>Email me</strong></a> &nbsp;|&nbsp;
  <a href="https://yuvrajkashyap.com"><strong>See the full portfolio</strong></a> &nbsp;|&nbsp;
  <a href="https://yuvrajkashyap.com/media/resume/yuvraj-kashyap-resume.pdf"><strong>Read my resume</strong></a>
</p>
