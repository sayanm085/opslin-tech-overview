# Opslin

> **Bring your own VPS. Get the simplicity of a modern deployment platform — without losing server control.**

Opslin is a **Zero-DevOps VPS management platform** — a *bring-your-own-VPS* deployment and infrastructure control plane. You connect your own server through a lightweight agent, and Opslin gives you a single dashboard to deploy applications, manage databases, configure domains and SSL, monitor server health, and view logs.

This repository is a **public, non-technical overview** of Opslin for investors, startup programs, accelerators, partners, advisors, and early beta users. **It does not contain product source code or sensitive implementation details.**

---

## 🎯 One-line explanation

Opslin lets developers, freelancers, agencies, startups, and DevOps teams operate their own VPS infrastructure from one dashboard — reducing the repetitive DevOps work that sits between writing code and running it in production.

---

## 🧩 The problem

Software creation is getting faster. AI coding tools, modern frameworks, templates, and full-stack boilerplates mean developers can build working products in days instead of months.

But **deployment and infrastructure operations are still painful.** Developers still wrestle with:

- VPS setup and hardening
- Docker
- nginx / reverse proxies
- SSL certificates
- Domains and DNS
- Databases
- Logs
- Monitoring
- Firewall rules
- Health checks
- CI/CD wiring
- Ongoing server maintenance
- Diagnosing deployment failures

The result is a bottleneck: code is ready, but shipping and operating it reliably still takes specialized, repetitive effort.

---

## ⏱️ Why now

- **Software creation is accelerating** thanks to AI-assisted development, while deployment and operations have not simplified at the same pace.
- More people are building and shipping software, which **increases the demand for simple, reliable deployment**.
- Managed platforms are convenient but can become **expensive or restrictive** at scale.
- Raw VPS hosting remains **low-cost and flexible**, but **operationally difficult** for many teams.

Opslin exists to close this gap: **software creation is getting faster, but deployment is still a bottleneck.**

---

## 🛠️ What Opslin does

Opslin helps users:

- Connect their own VPS using a lightweight agent
- Deploy applications from a dashboard
- Manage databases
- Configure domains and SSL
- Monitor server health and resource usage
- View application and deployment logs
- Track deployment progress
- Manage running applications
- Reduce repetitive DevOps setup
- Keep the **low cost and control of a VPS** while getting a **modern deployment-platform experience**

---

## 👥 Who it is for

- **Developers** who want to ship without becoming part-time sysadmins
- **Freelancers** managing deployments for multiple client projects
- **Agencies** operating many sites and apps across servers
- **Startups** that want control and low cost without a dedicated DevOps hire
- **DevOps teams** looking to reduce repetitive setup and operational toil

> Opslin is **not** trying to replace DevOps engineers. It reduces repetitive DevOps work and helps teams operate infrastructure faster.

---

## ⚙️ Core capabilities

| Capability | Description |
|---|---|
| **VPS connection** | Connect a user-owned VPS via a lightweight agent |
| **Application deployment** | Deploy, stop, restart, and delete applications from the dashboard |
| **Multi-language deploys** | Node.js (Next, Nuxt, Astro, Remix, SvelteKit, Angular, React, NestJS, Express), plus Python, Go, PHP, Ruby, Java, Rust, and static sites |
| **Rollback & deploy history** | Roll back to a previous deployment; review deployment history |
| **Database management** | Create and manage PostgreSQL, MySQL, MongoDB, and Redis; run queries; backup/restore |
| **Domains & SSL** | Configure custom domains and SSL for deployed apps |
| **Reverse proxy / nginx** | Managed, versioned web-server configuration |
| **Firewall management** | Discover, preview, and apply firewall policies |
| **Monitoring & health** | Server and per-container metrics, plus app health checks |
| **Logs** | Access application and deployment logs |
| **Web terminal** | Browser-based terminal session to the server |
| **Guided failure diagnosis** | Deployment failures are classified into clear, actionable categories |
| **Teams & roles** | Organizations with role-based access (owner/admin/member/viewer) |
| **GitHub & CI gates** | GitHub integration with optional CI checks before deploy |
| **Alerts & backups** | Alert rules/events and scheduled database backups with restore |

*Core capabilities above are present in the current product build and are undergoing validation and hardening through the pre-launch beta. Forward-looking items (e.g., AI-assisted deployment guidance, a marketplace, enterprise SSO) are clearly marked as future in [ROADMAP.md](ROADMAP.md).*

---

## 🔄 High-level product workflow

```text
1. Connect your VPS        → install the lightweight Opslin agent on your server
2. Link to the dashboard   → your server appears in the Opslin control plane
3. Deploy an application   → choose your app, deploy from the dashboard
4. Configure domain & SSL  → point your domain, enable SSL
5. Monitor & operate       → watch metrics, read logs, manage running apps
```

---

## 🚦 Current status

**Preparing for public beta.**

Opslin is being tested with real projects before a public beta launch. The current focus is **beta hardening** — validating deployment workflows, monitoring, databases, SSL/domains, and security-conscious design across a range of real-world scenarios.

See the full plan in [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md).

---

## 🧪 Beta testing summary

The pre-launch beta is designed to validate Opslin against realistic usage:

- Testing across approximately **20 servers** (see [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md))
- Deploying **real projects** in multiple languages/frameworks
- Database, SSL, and domain workflows
- Monitoring and logging validation
- Deliberate **deployment failure** scenarios
- Load handling observations
- Security validation and beta hardening

> Testing is **in progress**. No completion or success-rate claims are made here. See placeholders in [INVESTOR_SUMMARY.md](INVESTOR_SUMMARY.md).

---

## 💳 Pricing & beta access (beta plan)

| Plan | Price | Beta note |
|---|---|---|
| **Starter** | ₹299/month | Free for selected beta users for 6 months |
| **Pro** | ₹799/month | First 13 Pro beta users get 50% off |
| **Business / Agency** | ₹1,499/month | — |
| **Enterprise** | Custom | Contact us |

*Pricing reflects the current beta plan and may evolve before and during public beta.*

---

## 🏗️ Architecture (safe, high-level)

Opslin uses a **lightweight agent** installed on the user's VPS. The agent connects securely to the **Opslin control plane** and enables dashboard-driven deployment, monitoring, logs, and infrastructure workflows.

```text
User → Opslin Dashboard → Opslin Control Plane → Lightweight VPS Agent → User-Owned VPS
                                                                          ├─ Application Containers
                                                                          ├─ Databases
                                                                          └─ Monitoring / Logs
```

A more detailed (still high-level) breakdown is in [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md), and the security posture is summarized in [SECURITY_OVERVIEW.md](SECURITY_OVERVIEW.md). This repository intentionally **excludes** internal implementation details, credentials, and anything that could help misuse the platform.

---

## 📈 Investor & startup-program note

Opslin targets a real, persistent gap: **as software creation accelerates, deployment and operations remain a bottleneck.** This repository is structured to help investors, accelerators, and startup-program reviewers understand the problem, the product, the beta strategy, and the roadmap.

Start here:

- [INVESTOR_SUMMARY.md](INVESTOR_SUMMARY.md) — concise investor view
- [PRODUCT_OVERVIEW.md](PRODUCT_OVERVIEW.md) — deeper product story
- [ARCHITECTURE_OVERVIEW.md](ARCHITECTURE_OVERVIEW.md) — safe, high-level architecture
- [SECURITY_OVERVIEW.md](SECURITY_OVERVIEW.md) — public-safe security posture
- [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md) — how Opslin is validated before launch
- [ROADMAP.md](ROADMAP.md) — where Opslin is headed
- [FOUNDER_NOTE.md](FOUNDER_NOTE.md) — why the founder is building Opslin
- [MEDIA.md](MEDIA.md) — demos, screenshots, and deck

---

## 🔗 Links

| Resource | Link |
|---|---|
| Website | [Website URL] |
| Beta waitlist | [Beta waitlist link] |
| Founder intro video | [Founder video link] |
| Product demo | [Product demo link] |
| Pitch deck | [Pitch deck link] |

*All links are placeholders until confirmed. No links are invented.*

---

## 📬 Contact

- **General / Investor contact:** [Contact email]
- **Press / partnerships:** [Contact email]

---

*Opslin is preparing for public beta. This document describes the product and plan at a high level and uses placeholders wherever exact figures, links, or traction are not yet confirmed.*
# opslin-tech-overview
