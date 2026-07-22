<div align="center">

# Hi, I'm Vaibhav Kolekar 👋

### Full-Stack Developer — building backend-heavy systems that hold up in production

[![Portfolio](https://img.shields.io/badge/Portfolio-vaibhavk.devs.surf-0A0E12?style=for-the-badge&logo=vercel&logoColor=white)](https://vaibhavk.devs.surf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vaibhav-k-968883385)
[![Email](https://img.shields.io/badge/Email-va18havrk3%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:va18havrk3@gmail.com)

</div>

<br>

## About

I design and ship full-stack systems solo — from database schema to deployed infrastructure. My focus is on the parts most portfolios skip: concurrency control, crash recovery, observability, and making sure a system stays reliable once real users depend on it.

Currently building a **patient records and reporting system** for a sonography clinic — in daily production use by non-technical clinical staff — alongside independent projects spanning real-time AI voice systems, distributed job queues, and production monitoring infrastructure.

📍 Based in Bengaluru, India · Open to remote full-stack & backend roles and freelance work

<br>

## Tech Stack

<div align="left">

**Languages & Frontend**
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

**Backend**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socket.io&logoColor=white)

**Databases**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)

**Cloud & DevOps**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

**Testing & Observability**
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

</div>

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
- Built a multi-stage alerting pipeline (BullMQ/Redis) that dispatches real-time alerts via the Resend API while isolating notification failures from the core health-check queue
- Deployed **Grafana Loki + Promtail** to parse structured container logs via the Docker socket, and instrumented the job engine with **Prometheus** (custom counters + latency histograms) on a dedicated metrics port
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

<img height="165" src="https://github-readme-stats.vercel.app/api?username=va18hav&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=va18hav&layout=compact&theme=tokyonight&hide_border=true" />

</div>

<br>

## Let's Connect

I'm currently open to full-stack / backend roles and freelance work — especially systems involving real-time infrastructure, LLM integration, or backend reliability at scale.

📧 [va18havrk3@gmail.com](mailto:va18havrk3@gmail.com) · 💼 [LinkedIn](https://linkedin.com/in/vaibhav-k-968883385) · 🌐 [Portfolio](https://vaibhavk.devs.surf)

</div>
