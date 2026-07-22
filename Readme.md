<div align="center">

# Hi, I'm Vaibhav Kolekar 👋

### Full-Stack Developer — building backend-heavy systems that hold up in production

</div>

<br>

## About

I design and ship full-stack systems solo — from database schema to deployed infrastructure. My focus is on the parts most portfolios skip: concurrency control, crash recovery, observability, and making sure a system stays reliable once real users depend on it.

Currently building a **patient records and reporting system** for a sonography clinic — in daily production use by non-technical clinical staff — alongside independent projects spanning real-time AI voice systems, distributed job queues, and production monitoring infrastructure.

📍 Based in Bengaluru, India · Open to remote full-stack & backend roles and freelance work

<br>

## Tech Stack

<br>

**Languages & Frontend**
<br>
<img title="TypeScript" alt="TypeScript" src="https://cdn.simpleicons.org/typescript/3178C6" width="42" height="42" hspace="6"/>
<img title="JavaScript" alt="JavaScript" src="https://cdn.simpleicons.org/javascript/F7DF1E" width="42" height="42" hspace="6"/>
<img title="React" alt="React" src="https://cdn.simpleicons.org/react/61DAFB" width="42" height="42" hspace="6"/>
<img title="Tailwind CSS" alt="Tailwind CSS" src="https://cdn.simpleicons.org/tailwindcss/06B6D4" width="42" height="42" hspace="6"/>

<br><br>

**Backend**
<br>
<img title="Node.js" alt="Node.js" src="https://cdn.simpleicons.org/nodedotjs/339933" width="42" height="42" hspace="6"/>
<img title="Express.js" alt="Express.js" src="https://cdn.simpleicons.org/express/6E7681" width="42" height="42" hspace="6"/>
<img title="Prisma" alt="Prisma" src="https://cdn.simpleicons.org/prisma/2D3748" width="42" height="42" hspace="6"/>
<img title="Socket.IO / WebSockets" alt="WebSockets" src="https://cdn.simpleicons.org/socketdotio/6E7681" width="42" height="42" hspace="6"/>

<br><br>

**Databases**
<br>
<img title="PostgreSQL" alt="PostgreSQL" src="https://cdn.simpleicons.org/postgresql/4169E1" width="42" height="42" hspace="6"/>
<img title="Redis" alt="Redis" src="https://cdn.simpleicons.org/redis/DC382D" width="42" height="42" hspace="6"/>
<img title="Supabase" alt="Supabase" src="https://cdn.simpleicons.org/supabase/3ECF8E" width="42" height="42" hspace="6"/>

<br><br>

**Cloud & DevOps**
<br>
<img title="AWS" alt="AWS" src="https://cdn.simpleicons.org/amazonaws/FF9900" width="42" height="42" hspace="6"/>
<img title="Docker" alt="Docker" src="https://cdn.simpleicons.org/docker/2496ED" width="42" height="42" hspace="6"/>
<img title="Nginx" alt="Nginx" src="https://cdn.simpleicons.org/nginx/009639" width="42" height="42" hspace="6"/>
<img title="Vercel" alt="Vercel" src="https://cdn.simpleicons.org/vercel/6E7681" width="42" height="42" hspace="6"/>
<img title="Railway" alt="Railway" src="https://cdn.simpleicons.org/railway/6E7681" width="42" height="42" hspace="6"/>
<img title="Cloudflare" alt="Cloudflare" src="https://cdn.simpleicons.org/cloudflare/F38020" width="42" height="42" hspace="6"/>

<br><br>

**Testing & Observability**
<br>
<img title="Prometheus" alt="Prometheus" src="https://cdn.simpleicons.org/prometheus/E6522C" width="42" height="42" hspace="6"/>
<img title="Grafana" alt="Grafana" src="https://cdn.simpleicons.org/grafana/F46800" width="42" height="42" hspace="6"/>
<img title="Jest" alt="Jest" src="https://cdn.simpleicons.org/jest/C21325" width="42" height="42" hspace="6"/>
<img title="k6" alt="k6" src="https://cdn.simpleicons.org/k6/7D64FF" width="42" height="42" hspace="6"/>
<img title="Sentry" alt="Sentry" src="https://cdn.simpleicons.org/sentry/6E7681" width="42" height="42" hspace="6"/>
<img title="Postman" alt="Postman" src="https://cdn.simpleicons.org/postman/FF6C37" width="42" height="42" hspace="6"/>

<br><br>

**Tools**
<br>
<img title="Git" alt="Git" src="https://cdn.simpleicons.org/git/F05032" width="42" height="42" hspace="6"/>
<img title="GitHub" alt="GitHub" src="https://cdn.simpleicons.org/github/6E7681" width="42" height="42" hspace="6"/>

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

<div align="center">

I'm currently open to full-stack / backend roles and freelance work — especially systems involving real-time infrastructure, LLM integration, or backend reliability at scale.

<br><br>

<a href="https://vaibhavk.devs.surf"><img title="Portfolio" alt="Portfolio" src="https://cdn.simpleicons.org/vercel/6E7681" width="36" height="36" hspace="8"/></a>
<a href="https://linkedin.com/in/vaibhav-k-968883385"><img title="LinkedIn" alt="LinkedIn" src="https://cdn.simpleicons.org/linkedin/0A66C2" width="36" height="36" hspace="8"/></a>
<a href="mailto:va18havrk3@gmail.com"><img title="Email" alt="Email" src="https://cdn.simpleicons.org/gmail/EA4335" width="36" height="36" hspace="8"/></a>
<a href="https://github.com/va18hav"><img title="GitHub" alt="GitHub" src="https://cdn.simpleicons.org/github/6E7681" width="36" height="36" hspace="8"/></a>

<br><br>

📧 va18havrk3@gmail.com

</div>
