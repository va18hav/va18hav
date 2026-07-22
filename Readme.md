<div align="center">

  <h1>Hi, I'm Vaibhav Kolekar 👋</h1>
  <p><strong>Full-Stack & Systems Developer</strong> based in Bengaluru, India 🇮🇳</p>

  <p align="center">
    <a href="https://vaibhavk.devs.surf" target="_blank" rel="noreferrer" title="Portfolio Website">
      <img src="https://skillicons.dev/icons?i=net" height="40" alt="Portfolio" />
    </a>
    &nbsp;&nbsp;
    <a href="https://github.com/va18hav" target="_blank" rel="noreferrer" title="GitHub Profile">
      <img src="https://skillicons.dev/icons?i=github" height="40" alt="GitHub" />
    </a>
    &nbsp;&nbsp;
    <a href="https://linkedin.com/in/vaibhav-kolekar-968883385" target="_blank" rel="noreferrer" title="LinkedIn Profile">
      <img src="https://skillicons.dev/icons?i=linkedin" height="40" alt="LinkedIn" />
    </a>
    &nbsp;&nbsp;
    <a href="https://x.com/va18hav_k" target="_blank" rel="noreferrer" title="X (Twitter)">
      <img src="https://skillicons.dev/icons?i=twitter" height="40" alt="X" />
    </a>
    &nbsp;&nbsp;
    <a href="mailto:va18havk3@gmail.com" target="_blank" rel="noreferrer" title="Email Direct">
      <img src="https://skillicons.dev/icons?i=gmail" height="40" alt="Email" />
    </a>
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

## 🛠️ Technical Stack & Tools

<table align="center">
  <tr>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="42" height="42" alt="TypeScript" />
      <br />
      <sub><b>TYPESCRIPT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" width="42" height="42" alt="React" />
      <br />
      <sub><b>REACT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/va18hav/VaibhavK/main/public/icons/zustand.svg" width="42" height="42" alt="Zustand" />
      <br />
      <sub><b>ZUSTAND</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/va18hav/VaibhavK/main/public/icons/react-query.svg" width="42" height="42" alt="TanStack Query" />
      <br />
      <sub><b>TANSTACK QUERY</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/tailwindcss/tailwindcss-original.svg" width="42" height="42" alt="Tailwind CSS" />
      <br />
      <sub><b>TAILWIND CSS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" width="42" height="42" alt="Node.js" />
      <br />
      <sub><b>NODE.JS</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" width="42" height="42" alt="Express" />
      <br />
      <sub><b>EXPRESS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/va18hav/VaibhavK/main/public/icons/Socket.io.svg" width="42" height="42" alt="WebSockets" />
      <br />
      <sub><b>WEBSOCKETS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/va18hav/VaibhavK/main/public/icons/bullmq.svg" width="42" height="42" alt="BullMQ" />
      <br />
      <sub><b>BULLMQ</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" width="42" height="42" alt="PostgreSQL" />
      <br />
      <sub><b>POSTGRESQL</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original.svg" width="42" height="42" alt="Redis" />
      <br />
      <sub><b>REDIS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/prisma/prisma-original.svg" width="42" height="42" alt="Prisma" />
      <br />
      <sub><b>PRISMA</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" width="42" height="42" alt="Docker" />
      <br />
      <sub><b>DOCKER</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="42" height="42" alt="AWS" />
      <br />
      <sub><b>AWS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" width="42" height="42" alt="Nginx" />
      <br />
      <sub><b>NGINX</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vercel/vercel-original.svg" width="42" height="42" alt="Vercel" />
      <br />
      <sub><b>VERCEL</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="42" height="42" alt="Git" />
      <br />
      <sub><b>GIT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jest/jest-plain.svg" width="42" height="42" alt="Jest" />
      <br />
      <sub><b>JEST</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postman/postman-original.svg" width="42" height="42" alt="Postman" />
      <br />
      <sub><b>POSTMAN</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/prometheus/prometheus-original.svg" width="42" height="42" alt="Prometheus" />
      <br />
      <sub><b>PROMETHEUS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/grafana/grafana-original.svg" width="42" height="42" alt="Grafana Loki" />
      <br />
      <sub><b>GRAFANA LOKI</b></sub>
    </td>
    <td align="center" width="125">
      <img src="https://raw.githubusercontent.com/va18hav/VaibhavK/main/public/icons/k6.svg" width="42" height="42" alt="k6" />
      <br />
      <sub><b>K6</b></sub>
    </td>
    <td align="center" width="125"></td>
    <td align="center" width="125"></td>
  </tr>
</table>

---

<div align="center">
  <p>Designed & built by <strong>Vaibhav Kolekar</strong> · <a href="https://vaibhavk.devs.surf">vaibhavk.devs.surf</a></p>
</div>
