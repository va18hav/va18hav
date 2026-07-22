<div align="center">

# Hi, I'm Vaibhav Kolekar 👋

### Full-Stack Developer — building backend-heavy systems that hold up in production

<br>

<img src="https://skillicons.dev/icons?i=ts,js,react,tailwind,nodejs,express,postgres,redis,prisma,docker,aws,nginx,vercel,git,github,jest,postman,grafana,prometheus,sentry,supabase&perline=10" />

</div>

<br>

## About

I design and ship full-stack systems solo — from database schema to deployed infrastructure. My focus is on the parts most portfolios skip: concurrency control, crash recovery, observability, and making sure a system stays reliable once real users depend on it.

Currently building a **patient records and reporting system** for a sonography clinic — in daily production use by non-technical clinical staff — alongside independent projects spanning real-time AI voice systems, distributed job queues, and production monitoring infrastructure.

📍 Based in Bengaluru, India · Open to remote full-stack & backend roles and freelance work

Also working with `Zustand`, `TanStack Query`, `BullMQ`, `k6`, and `Grafana Loki` — niche enough that they don't have official icon packs yet, called out in the project breakdowns below.

<br>

## Featured Work

### 🎙️ [Interviu](https://interviu.pro) — Real-Time AI Mock Interview Platform
Voice-based AI interview platform built solo, from scratch. Real interviews are live conversations under pressure — Interviu simulates that, not a chat window.

- Built a **WebSocket server bridging the client and the Gemini Flash Live API** for native voice-to-voice communication — bidirectional audio streaming with 400–500ms observed latency in production
- Implemented **Redis-backed session recovery** (transcript, system prompt, and resume handle persisted per session) with exponential backoff retry, so a dropped connection resumes instead of losing progress
- Integrated the **Claude Sonnet API** to generate structured, context-aware feedback from full interview transcripts
- Built a custom **JWT authentication flow** — token issuance, validation middleware, protected route lifecycle

`TypeScript` `React` `Node.js` `WebSockets` `Gemini Flash Live API` `PostgreSQL` `Redis` `AWS ECS` `Docker`

**[Live →](https://interviu.pro)** · **[Code →](https://github.com/va18hav/interviuPro)**

<br>

### 📡 [Pingdeck](https://app.pingdeck.xyz) — API Testing & Uptime Monitoring Platform
Decoupled, microservices-based monitoring platform for API health and alerting.

- Verified system throughput of **64 req/sec at sub-110ms p95 latency** under concurrent load, load-tested with **k6**
- Built a multi-stage alerting pipeline (**BullMQ**/Redis) that dispatches real-time alerts via the Resend API while isolating notification failures from the core health-check queue
- Deployed **Grafana Loki** + Promtail to parse structured container logs via the Docker socket, and instrumented the job engine with **Prometheus** (custom counters + latency histograms) on a dedicated metrics port
- Measured database-write throughput at ~125 jobs/sec (PostgreSQL/Prisma) via a custom benchmark script

`TypeScript` `Node.js` `Express` `BullMQ` `Redis` `PostgreSQL` `Prisma` `Docker` `Prometheus` `Grafana Loki` `k6`

**[Live →](https://app.pingdeck.xyz)** · **[Code →](https://github.com/va18hav/pingdeck)**

<br>

### ⚙️ [Distributed Job Scheduler](https://github.com/va18hav/distributed-job-scheduler)
A database-backed task queue built from first principles — no external queue library, just PostgreSQL.

- **Non-blocking transactional dequeue** using `FOR UPDATE SKIP LOCKED`, allowing multiple concurrent workers to safely poll and dequeue tasks without contention
- **Lease-based crash recovery** — a heartbeat mechanism that reclaims stalled tasks if a worker goes silent for 30+ seconds, inside a single SQL transaction
- **Graceful shutdown handling** — traps `SIGINT`/`SIGTERM`, halts the acquisition loop, lets active jobs finish, and tears down connections cleanly
- Lock-free telemetry endpoint computing real-time queue and worker metrics from sliding heartbeat windows

`TypeScript` `Node.js` `Express` `PostgreSQL` `Prisma` `Jest`

**[Code →](https://github.com/va18hav/distributed-job-scheduler)**

<br>

## Experience

**Freelance Full-Stack Developer** — Sonography Clinic Management System
`React` `TypeScript` `Node.js` `Express` `Supabase`

Built a patient records and diagnostic report generation system, currently in **daily production use** by non-technical clinical staff.

- Designed scan-type-specific templated form fields to minimize doctor input and reduce reporting errors
- Secured patient records with field-level encryption in Supabase for sensitive medical data
- Implemented a **multi-tenant permission architecture** — Doctor/Admin (full edit/delete rights), Typist (create/retrieve records), Receptionist (scoped to daily follow-up reminders only)

<br>

## GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=va18hav&show_icons=true&theme=tokyonight&hide_border=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=va18hav&layout=compact&theme=tokyonight&hide_border=true" />

</div>

<br>

## Let's Connect

<div align="center">

I'm currently open to full-stack / backend roles and freelance work — especially systems involving real-time infrastructure, LLM integration, or backend reliability at scale.

<br><br>

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vaibhavk.devs.surf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vaibhav-k-968883385)
[![Email](https://img.shields.io/badge/Email-333333?style=for-the-badge&logo=gmail&logoColor=white)](mailto:va18havrk3@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/va18hav)

</div>
