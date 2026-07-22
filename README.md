<div align="center">

  <h1>Hi, I'm Vaibhav Kolekar 👋</h1>
  <p><strong>Full-Stack & Systems Developer</strong> based in Bengaluru, India 🇮🇳</p>

  <p align="center">
    <a href="https://vaibhavk.devs.surf" target="_blank" rel="noreferrer" title="Portfolio Website">
      <img src="./icons/globe.svg" width="32" height="32" alt="Portfolio" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://linkedin.com/in/vaibhav-kolekar-968883385" target="_blank" rel="noreferrer" title="LinkedIn Profile">
      <img src="./icons/linkedin.svg" width="32" height="32" alt="LinkedIn" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="https://x.com/va18hav_k" target="_blank" rel="noreferrer" title="X (Twitter)">
      <img src="./icons/twitter.svg" width="32" height="32" alt="X" />
    </a>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <a href="mailto:va18havk3@gmail.com" target="_blank" rel="noreferrer" title="Email Direct">
      <img src="./icons/gmail.svg" width="32" height="32" alt="Email" />
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

<p align="left">
  <img src="./icons/TypeScript.svg" width="28" height="28" alt="TypeScript" />&nbsp;
  <img src="./icons/react.svg" width="28" height="28" alt="React" />&nbsp;
  <img src="./icons/nodejs.svg" width="28" height="28" alt="Node.js" />&nbsp;
  <img src="./icons/socketio.svg" width="28" height="28" alt="WebSockets" />&nbsp;
  <img src="./icons/postgresql.svg" width="28" height="28" alt="PostgreSQL" />&nbsp;
  <img src="./icons/Redis.svg" width="28" height="28" alt="Redis" />&nbsp;
  <img src="./icons/prisma.svg" width="28" height="28" alt="Prisma" />&nbsp;
  <img src="./icons/AWS.svg" width="28" height="28" alt="AWS" />&nbsp;
  <img src="./icons/Docker.svg" width="28" height="28" alt="Docker" />&nbsp;
  <img src="./icons/Vercel.svg" width="28" height="28" alt="Vercel" />
</p>

- **Real-Time Voice Bridge (400–500ms TTFT)**: Implemented a raw WebSocket proxy server piping 16kHz PCM audio buffers between the client and Google GenAI Live API for fluid conversational pacing.
- **Monaco Code Editor Sync**: Built a debounced `[EDITOR_UPDATE]` context synchronization pipeline that injects live candidate code edits into the model's window without disturbing audio streaming.
- **Resilient Session Persistence**: Engineered a Redis session cache layer with a 30-second connection recovery window to preserve active interview state during network dropouts.
- **Dual-Model Feedback Pipeline**: Decoupled voice interaction from evaluation; flushes full transcripts to Anthropic's Claude 3.5 Sonnet to generate structured JSON scorecards and actionable feedback.

---

### 02. [Pingdeck — API Testing & Uptime Monitoring Platform](https://app.pingdeck.xyz)
> **Live Web App**: [app.pingdeck.xyz](https://app.pingdeck.xyz) &nbsp;|&nbsp; **Repository**: [`va18hav/pingdeck`](https://github.com/va18hav/pingdeck)

A decoupled, microservices-based API monitoring and telemetry platform featuring distributed alerting queues, container log aggregation, and Prometheus metrics exporting.

<p align="left">
  <img src="./icons/TypeScript.svg" width="28" height="28" alt="TypeScript" />&nbsp;
  <img src="./icons/react.svg" width="28" height="28" alt="React" />&nbsp;
  <img src="./icons/Express.svg" width="28" height="28" alt="Express" />&nbsp;
  <img src="./icons/bullmq.svg" width="28" height="28" alt="BullMQ" />&nbsp;
  <img src="./icons/Redis.svg" width="28" height="28" alt="Redis" />&nbsp;
  <img src="./icons/postgresql.svg" width="28" height="28" alt="PostgreSQL" />&nbsp;
  <img src="./icons/prisma.svg" width="28" height="28" alt="Prisma" />&nbsp;
  <img src="./icons/Docker.svg" width="28" height="28" alt="Docker" />&nbsp;
  <img src="./icons/AWS.svg" width="28" height="28" alt="AWS" />&nbsp;
  <img src="./icons/Nginx.svg" width="28" height="28" alt="Nginx" />&nbsp;
  <img src="./icons/Prometheus.svg" width="28" height="28" alt="Prometheus" />&nbsp;
  <img src="./icons/Grafana.svg" width="28" height="28" alt="Grafana Loki" />&nbsp;
  <img src="./icons/k6.svg" width="28" height="28" alt="k6" />
</p>

- **Decoupled Worker Engine**: Separated health-check pings from the HTTP runtime using BullMQ and Redis queues; verified **64 req/sec** API gateway throughput with **sub-110ms p95 latency** via k6 and **125 jobs/sec** DB write performance.
- **Multi-Stage Alert Dispatching**: Created isolated event queues for failure notifications (via Resend API) so downstream alerting retries never stall primary health monitor workers.
- **Container Observability Pipeline**: Configured Promtail daemons scraping `/var/run/docker.sock` to parse structured Pino JSON logs into indexable Grafana Loki streams without application overhead.
- **Prometheus Telemetry Instrumentation**: Embedded custom `prom-client` counters and execution duration histograms exposed on dedicated metrics ports.

---

### 03. [Distributed Job Scheduler](https://github.com/va18hav/distributed-job-scheduler)
> **Repository**: [`va18hav/distributed-job-scheduler`](https://github.com/va18hav/distributed-job-scheduler)

A lightweight, database-backed background task processing engine built from scratch with ACID transactional guarantees, non-blocking polling, and lease-based worker crash recovery.

<p align="left">
  <img src="./icons/TypeScript.svg" width="28" height="28" alt="TypeScript" />&nbsp;
  <img src="./icons/nodejs.svg" width="28" height="28" alt="Node.js" />&nbsp;
  <img src="./icons/Express.svg" width="28" height="28" alt="Express" />&nbsp;
  <img src="./icons/postgresql.svg" width="28" height="28" alt="PostgreSQL" />&nbsp;
  <img src="./icons/prisma.svg" width="28" height="28" alt="Prisma" />&nbsp;
  <img src="./icons/Docker.svg" width="28" height="28" alt="Docker" />&nbsp;
  <img src="./icons/Jest.svg" width="28" height="28" alt="Jest" />
</p>

- **Non-Blocking Dequeue (`FOR UPDATE SKIP LOCKED`)**: Leverages PostgreSQL row-level locking to allow multiple worker processes to concurrently claim tasks without lock contention or double-allocation.
- **Lease-Based Crash Recovery**: Implemented heartbeat timestamp pings (`lockedAt`); automatically reclaims and reschedules stalled jobs if a worker node crashes or freezes for over 30 seconds.
- **Graceful OS Interrupt Traps**: Trapped `SIGINT`/`SIGTERM` process signals to halt polling loops, drain in-flight jobs, clear heartbeat timers, and release database client connections cleanly.
- **Strategy Pattern Registry & Telemetry**: Built a type-safe handler execution registry alongside lock-free `/job/stats` real-time queue depth telemetry.

---

## 🛠️ Technical Stack & Tools

<table align="center">
  <tr>
    <td align="center" width="125">
      <img src="./icons/TypeScript.svg" width="42" height="42" alt="TypeScript" />
      <br />
      <sub><b>TYPESCRIPT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/react.svg" width="42" height="42" alt="React" />
      <br />
      <sub><b>REACT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/zustand.svg" width="42" height="42" alt="Zustand" />
      <br />
      <sub><b>ZUSTAND</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/react-query.svg" width="42" height="42" alt="TanStack Query" />
      <br />
      <sub><b>TANSTACK QUERY</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/tailwind.svg" width="42" height="42" alt="Tailwind CSS" />
      <br />
      <sub><b>TAILWIND CSS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/nodejs.svg" width="42" height="42" alt="Node.js" />
      <br />
      <sub><b>NODE.JS</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="./icons/Express.svg" width="42" height="42" alt="Express" />
      <br />
      <sub><b>EXPRESS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/socketio.svg" width="42" height="42" alt="WebSockets" />
      <br />
      <sub><b>WEBSOCKETS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/bullmq.svg" width="42" height="42" alt="BullMQ" />
      <br />
      <sub><b>BULLMQ</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/postgresql.svg" width="42" height="42" alt="PostgreSQL" />
      <br />
      <sub><b>POSTGRESQL</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Redis.svg" width="42" height="42" alt="Redis" />
      <br />
      <sub><b>REDIS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/prisma.svg" width="42" height="42" alt="Prisma" />
      <br />
      <sub><b>PRISMA</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="./icons/Docker.svg" width="42" height="42" alt="Docker" />
      <br />
      <sub><b>DOCKER</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/AWS.svg" width="42" height="42" alt="AWS" />
      <br />
      <sub><b>AWS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Nginx.svg" width="42" height="42" alt="Nginx" />
      <br />
      <sub><b>NGINX</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Vercel.svg" width="42" height="42" alt="Vercel" />
      <br />
      <sub><b>VERCEL</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Git.svg" width="42" height="42" alt="Git" />
      <br />
      <sub><b>GIT</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Jest.svg" width="42" height="42" alt="Jest" />
      <br />
      <sub><b>JEST</b></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="125">
      <img src="./icons/Postman.svg" width="42" height="42" alt="Postman" />
      <br />
      <sub><b>POSTMAN</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Prometheus.svg" width="42" height="42" alt="Prometheus" />
      <br />
      <sub><b>PROMETHEUS</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/Grafana.svg" width="42" height="42" alt="Grafana Loki" />
      <br />
      <sub><b>GRAFANA LOKI</b></sub>
    </td>
    <td align="center" width="125">
      <img src="./icons/k6.svg" width="42" height="42" alt="k6" />
      <br />
      <sub><b>K6</b></sub>
    </td>
    <td align="center" width="125"></td>
    <td align="center" width="125"></td>
  </tr>
</table>
