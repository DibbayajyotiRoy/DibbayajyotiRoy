<div align="center">

# Dibbayajyoti Roy

**Backend & Systems Engineer · Rust**

*Distributed replication · time-series data infrastructure · developer tooling*

[![Portfolio](https://img.shields.io/badge/Portfolio-dibbayajyoti.com-black?style=flat-square&logo=vercel)](https://dibbayajyoti.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-dibbayajyoti--roy-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/dibbayajyoti-roy/)
[![X](https://img.shields.io/badge/X-@DibbayajyotiRoy-000000?style=flat-square&logo=x)](https://x.com/DibbayajyotiRoy)
[![Email](https://img.shields.io/badge/Email-rdibbayajyoti@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:rdibbayajyoti@gmail.com)

</div>

---

## About

Backend and systems engineer in **Agartala, India**. I work on production Rust in
databases and developer-tooling space, and build voice/AI infrastructure at
**Yupcha Softwares**.

- **8 merged pull requests in [ReductStore](https://github.com/reductstore/reductstore)**, a time-series database for robotics and industrial IoT — replication pipeline performance and the `$system` observability layer
- Contributor to **[pyrefly](https://github.com/facebook/pyrefly)**, Meta's Python type checker
- **Currently:** SDE at Yupcha — speech-to-speech AI interview tooling (AWS Bedrock Nova Sonic, LiveKit/WebRTC), HR automation SaaS
- **Open to:** backend / systems / infrastructure roles, Rust-focused — remote or relocation (EU, Ireland, Canada, Australia)
- **B.Tech Computer Science** · ICFAI University Tripura · 2026

---

## Open Source

### ReductStore — time-series database for robotics & industrial IoT (Rust)

**Replication core — throughput and transport**

| PR | Contribution |
|----|--------------|
| **[#1527](https://github.com/reductstore/reductstore/pull/1527)** | Pipelined batch sending in the replication path, superseding a stalled prior attempt. Decouples batch construction from transmission so the sender no longer blocks on network round-trips. |
| **[#1538](https://github.com/reductstore/reductstore/pull/1538)** | Optional payload compression for replication, cutting bytes on the wire for remote and bandwidth-constrained deployments. |
| **[#1567](https://github.com/reductstore/reductstore/pull/1567)** | Replication of `$system` events, so operational telemetry propagates to replica instances rather than staying local to the source. |

**Observability & system events**

| PR | Contribution |
|----|--------------|
| **[#1496](https://github.com/reductstore/reductstore/pull/1496)** | Cross-cutting refactor unifying all `$system` event handling under one logger — **requested directly by the maintainer.** Generic event sink, type-safe event-kind enum, five pipelines consolidated with the external record format provably unchanged. |
| **[#1481](https://github.com/reductstore/reductstore/pull/1481)** | System log capture to `$system/logs` via an abstract log-sink hook in the base crate (zero reverse dependency), with a `task_local` reentrancy guard preventing an infinite logging loop. |
| **[#1474](https://github.com/reductstore/reductstore/pull/1474)** | Per-bucket usage statistics with distinct entry-level read/write counters and record counts. |
| **[#1431](https://github.com/reductstore/reductstore/pull/1431)** | Instance-wide usage statistics emitted as queryable `$system` records. |
| **[#1417](https://github.com/reductstore/reductstore/pull/1417)** | Replication diagnostics as queryable telemetry — **shipped in v1.20, credited by the co-founder.** |

### pyrefly — Meta's Python type checker (Rust)

| PR | Contribution |
|----|--------------|
| **[#3840](https://github.com/facebook/pyrefly/pull/3840)** | Fixed a false-positive `untyped-import` diagnostic for packages shipping `py.typed` (PEP 561), correctly handling submodules where the marker lives at the package root. |

---

## Selected Work at Yupcha Softwares

- **Rebuilt a production speech-to-speech AI interviewer** from a high-latency inherited codebase into a deployed service — collapsed a cascaded STT→LLM→TTS chain into a unified pipeline on AWS Bedrock (Nova Sonic) with Pipecat and LiveKit/WebRTC.
- **Cut a hot polling path ~90%** by rewriting a Redis `SCAN+GET` pattern as `MGET` batching.
- **Reduced page load 3.4s → 1.9s (~44%)** by eliminating N+1 queries, adding composite indexes, and route-splitting Next.js bundles.
- Deployed and operated services on Proxmox/Linux — `systemd` units, `nginx` reverse proxy with automated TLS, `journald`.

---

## Projects

- **[Fresco](https://github.com/DibbayajyotiRoy/Fresco)** — live wallpaper engine for
  Linux (Rust · GTK4 · libmpv). Per-output supervised subprocesses with crash isolation
  and JSON IPC. Independently reviewed by a
  [Deepin community member](https://bbs.deepin.org/post/300364) and verified on
  Deepin 25 / X11.
- **[AHTML](https://github.com/DibbayajyotiRoy)** — agent-readable HTML standard
  emitting WebMCP, OpenAPI 3.1, and JSON-LD from one source. **22k+ downloads across the
  `@ahtmljs` suite.**
- **[RoyUI](https://www.npmjs.com/package/@roy-ui/ui)** — TypeScript-first, RSC-safe
  React component library. **3.5k+ npm downloads.**
- **whatbroke** — crash-context packager for AI-assisted debugging. MCP server,
  git-anchored suspect ranking, parsers for five test runners.

---

## Tech Stack

<div align="center">

![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)

</div>

---

## Achievements

- **Winner** — NITA Arjuna 2.0 National Hackathon (2025), 200+ teams
- **Winner** — Technovate Project Exhibition (2025)
- **1st Runner-Up** — NITA–ISRO Space Hackathon (2024)
- **Top 500** — AI for Bharat

---

<div align="center">

*Open to backend / systems / infrastructure roles — [rdibbayajyoti@gmail.com](mailto:rdibbayajyoti@gmail.com)*

</div>
