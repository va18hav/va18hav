<div align="center">

  <h1>Hi, I'm Vaibhav Kolekar 👋</h1>
  <p><strong>Full-Stack & Systems Developer</strong> based in Bengaluru, India 🇮🇳</p>

  <p>
    <a href="https://vaibhavkolekar.dev"><img src="https://img.shields.io/badge/Website-vaibhavkolekar.dev-3b82f6?style=for-the-badge&logo=react&logoColor=white" alt="Website"></a>
    <a href="https://linkedin.com/in/vaibhav-kolekar-968883385"><img src="https://img.shields.io/badge/LinkedIn-Vaibhav_Kolekar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
    <a href="mailto:va18havk3@gmail.com"><img src="https://img.shields.io/badge/Email-va18havk3@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
    <a href="https://x.com/va18hav_k"><img src="https://img.shields.io/badge/X-@va18hav__k-000000?style=for-the-badge&logo=x&logoColor=white" alt="Twitter"></a>
  </p>

  <p>
    <code>🟢 Open to Full-Stack, Backend & TypeScript Roles · Available Now</code>
  </p>

  ---

</div>

## ⚡ About Me

I design and build production-grade, event-driven full-stack systems in **TypeScript** — handling everything from low-latency WebSocket bridges and distributed background queues to database schemas, containerization, and cloud infrastructure.

- 🛠️ **Core Expertise**: Full-Stack TypeScript (PERN Stack: PostgreSQL, Express, React, Node.js), Redis, WebSockets, Docker, AWS, & Distributed Systems.
- ⚡ **Real-Time & AI Systems**: Built **Interviu**, an AI-powered voice-to-voice mock interview engine using Google's Gemini Flash Live API & Claude Sonnet.
- 📊 **Distributed Systems & Observability**: Engineered **Pingdeck**, a microservices uptime & metrics platform (Prometheus, Grafana Loki, BullMQ), and a **Distributed Job Scheduler** using PostgreSQL `FOR UPDATE SKIP LOCKED`.

---

## 🚀 Featured Engineering Projects

### 01. [Interviu — AI Mock Interview Platform](https://interviu.pro)
> **Live Web App**: [interviu.pro](https://interviu.pro) &nbsp;|&nbsp; **Repository**: [`va18hav/interviuPro`](https://github.com/va18hav/interviuPro)

An end-to-end, voice-first mock interview platform that simulates realistic technical, system design, and behavioral interviews with bidirectional audio streaming and live code synchronization.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat-square&logo=socketdotio&logoColor=white)
![Gemini Live API](https://img.shields.io/badge/Gemini_Live_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Claude 3.5 Sonnet](https://img.shields.io/badge/Claude_3.5_Sonnet-D97706?style=flat-square&logo=anthropic&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS ECS](https://img.shields.io/badge/AWS_ECS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

- **Real-Time Voice Bridge (400–500ms TTFT)**: Implemented a raw WebSocket proxy server piping 16kHz PCM audio buffers between the client and Google GenAI Live API for fluid conversational pacing.
- **Monaco Code Editor Sync**: Built a debounced `[EDITOR_UPDATE]` context synchronization pipeline that injects live candidate code edits into the model's window without disturbing audio streaming.
- **Resilient Session Persistence**: Engineered a Redis session cache layer with a 30-second connection recovery window to preserve active interview state during network dropouts.
- **Dual-Model Feedback Pipeline**: Decoupled voice interaction from evaluation; flushes full transcripts to Anthropic's Claude 3.5 Sonnet to generate structured JSON scorecards and actionable feedback.

---

### 02. [Pingdeck — API Testing & Uptime Monitoring Platform](https://app.pingdeck.xyz)
> **Live Web App**: [app.pingdeck.xyz](https://app.pingdeck.xyz) &nbsp;|&nbsp; **Repository**: [`va18hav/pingdeck`](https://github.com/va18hav/pingdeck)

A decoupled, microservices-based API monitoring and telemetry platform featuring distributed alerting queues, container log aggregation, and Prometheus metrics exporting.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![BullMQ](https://img.shields.io/badge/BullMQ-CC0000?style=flat-square&logo=redis&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana Loki](https://img.shields.io/badge/Grafana_Loki-F46800?style=flat-square&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

- **Decoupled Worker Engine**: Separated health-check pings from the HTTP runtime using BullMQ and Redis queues; verified **64 req/sec** API gateway throughput with **sub-110ms p95 latency** via k6 and **125 jobs/sec** DB write performance.
- **Multi-Stage Alert Dispatching**: Created isolated event queues for failure notifications (via Resend API) so downstream alerting retries never stall primary health monitor workers.
- **Container Observability Pipeline**: Configured Promtail daemons scraping `/var/run/docker.sock` to parse structured Pino JSON logs into indexable Grafana Loki streams without application overhead.
- **Prometheus Telemetry Instrumentation**: Embedded custom `prom-client` counters and execution duration histograms exposed on dedicated metrics ports.

---

### 03. [Distributed Job Scheduler](https://github.com/va18hav/distributed-job-scheduler)
> **Repository**: [`va18hav/distributed-job-scheduler`](https://github.com/va18hav/distributed-job-scheduler)

A lightweight, database-backed background task processing engine built from scratch with ACID transactional guarantees, non-blocking polling, and lease-based worker crash recovery.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)

- **Non-Blocking Dequeue (`FOR UPDATE SKIP LOCKED`)**: Leverages PostgreSQL row-level locking to allow multiple worker processes to concurrently claim tasks without lock contention or double-allocation.
- **Lease-Based Crash Recovery**: Implemented heartbeat timestamp pings (`lockedAt`); automatically reclaims and reschedules stalled jobs if a worker node crashes or freezes for over 30 seconds.
- **Graceful OS Interrupt Traps**: Trapped `SIGINT`/`SIGTERM` process signals to halt polling loops, drain in-flight jobs, clear heartbeat timers, and release database client connections cleanly.
- **Strategy Pattern Registry & Telemetry**: Built a type-safe handler execution registry alongside lock-free `/job/stats` real-time queue depth telemetry.

---

## 🛠️ Technical Stack & Skills

Unlike traditional split views, my stack operates as a cohesive unit centered around modern TypeScript development across the entire software lifecycle:

| Domain | Technologies & Frameworks |
| :--- | :--- |
| **Languages & Core** | **TypeScript**, JavaScript (ES6+), SQL, HTML5/CSS3 |
| **Frontend Engineering** | **React**, Next.js, Zustand, TanStack Query, Tailwind CSS, WebSockets |
| **Backend & Microservices** | **Node.js**, Express.js, **BullMQ**, RESTful APIs, WebSockets, JWT Authentication |
| **Databases & Caching** | **PostgreSQL**, **Redis**, Prisma ORM, Supabase |
| **DevOps & Cloud Systems** | **Docker**, AWS (ECS, S3, EC2), Nginx, Cloudflare, Vercel |
| **Observability & Testing** | **Prometheus**, **Grafana Loki**, Promtail, k6 Load Testing, Jest, Postman |

---

## 🌐 Connect With Me

- **Portfolio Website**: [vaibhavkolekar.dev](https://vaibhavkolekar.dev)
- **LinkedIn**: [linkedin.com/in/vaibhav-kolekar-968883385](https://linkedin.com/in/vaibhav-kolekar-968883385)
- **Email**: [va18havk3@gmail.com](mailto:va18havk3@gmail.com)
- **X / Twitter**: [@va18hav_k](https://x.com/va18hav_k)
