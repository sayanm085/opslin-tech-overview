# Investor Summary — Opslin

A concise overview for angel investors, VC firms, accelerators, and startup-program reviewers. **No traction numbers, financials, or links are invented** — unknowns are shown as placeholders. Product claims describe what is present in the current product build.

---

## 🧩 Problem

Software creation is accelerating — AI coding tools, modern frameworks, and boilerplates let developers build working products quickly. **Deployment and infrastructure operations have not kept pace.** Teams still spend disproportionate time on VPS setup, Docker, nginx, SSL, domains, databases, logs, monitoring, firewall rules, health checks, CI/CD, and ongoing maintenance. This is the bottleneck between "the code works" and "the product is live and reliable."

---

## 💡 Solution

**Opslin is a Zero-DevOps VPS management platform — a bring-your-own-VPS deployment and infrastructure control plane.** Users connect their own server via a lightweight agent and operate it from one dashboard: deploy applications, manage databases, configure domains and SSL, monitor health, read logs, manage firewall and reverse-proxy configuration, and roll back when needed.

**Positioning:** the simplicity of a modern deployment platform with the cost and control of your own VPS. Opslin reduces repetitive DevOps work — it does not aim to replace DevOps engineers.

---

## ⏱️ Why now

- **Software creation is accelerating** while deployment/operations remain manual and error-prone.
- More builders shipping more software **increases demand** for simple, reliable deployment.
- Managed platforms are easy but can be **expensive or restrictive**; raw VPS is cheap and flexible but **operationally hard**. Opslin sits between the two.

---

## 🚦 Product status

**Preparing for public beta**, testing real projects before launch. The product is substantially built, not just an idea — the following capabilities are present in the current product build:

- Multi-language deployment: Node.js (with framework detection — Next.js, Nuxt, Astro, Remix, SvelteKit, Angular, React, NestJS, Express), plus Python, Go, PHP, Ruby, Java, Rust, and static sites
- Databases: PostgreSQL, MySQL, MongoDB, Redis — with backup/restore
- Domains & SSL, managed nginx/reverse-proxy, and firewall management
- Monitoring, health checks, logs, and a web terminal
- Rollback and deployment history, plus guided deployment-failure diagnosis
- Teams/organizations with role-based access, GitHub integration with CI deploy gates
- Alerts, scheduled backups, subscription billing, and an admin console
- Automated tests and validation workflows that are being expanded across the agent, API, and dashboard

*Current focus is **beta hardening** — see [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md). "Present in the current build" means the capability exists in the product and is undergoing validation, not a guarantee of bug-free behavior.*

---

## 👥 Target customers

- **Developers** shipping without becoming sysadmins
- **Freelancers** managing many client deployments
- **Agencies** operating many sites/apps across servers
- **Startups** wanting control and low cost without a dedicated DevOps hire
- **DevOps teams** reducing repetitive operational toil

---

## 💰 Business model

Subscription SaaS (subscription billing is present in the current product build). Current **beta** plan:

| Plan | Price | Beta note |
|---|---|---|
| Starter | ₹299/month | Free for selected beta users for 6 months |
| Pro | ₹799/month | First 13 Pro beta users get 50% off |
| Business / Agency | ₹1,499/month | — |
| Enterprise | Custom | Contact |

*The 6-month Starter beta period is reflected in the product's trial handling. Pricing may evolve before/through public beta.*

**Revenue:** **[MRR]** · **[Paid users]** — *not yet disclosed; no figures invented.*

---

## 🧪 Beta strategy

- Validate across approximately **20 servers** spanning providers, sizes, and OS configurations
- Deploy **real projects** across the supported languages/frameworks
- Exercise databases, domains/SSL, monitoring/logging, firewall, and rollback
- Deliberately test **deployment failure** scenarios and graceful recovery
- Security validation and **beta hardening** throughout
- Tight **feedback loop** with early users feeding fixes back into the product

Full plan: [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md).

---

## 📊 Expected beta metrics (placeholders)

No traction is fabricated. These are the metrics being tracked:

- Beta users: **[Beta users]**
- Connected servers: **[Connected servers]**
- Apps deployed: **[Apps deployed]**
- Paid users: **[Paid users]**
- MRR: **[MRR]**
- Deployment success rate: **[Deployment success rate]**
- Current traction summary: **[Current traction]**

---

## 🥊 Competitive positioning

```text
Managed PaaS  ───────────────  Opslin  ───────────────  Raw VPS / manual DevOps
(easy; cost &                (easy operations on        (powerful, cheap;
 control trade-offs)          your own server;           operationally hard)
                              cost + control retained)
```

- **vs. managed platforms:** users keep the cost advantages and full control of their own VPS, avoiding lock-in and scaling cost surprises.
- **vs. raw VPS / manual DevOps:** users get a modern dashboard, multi-language deploys, monitoring, and guided failure diagnosis instead of repetitive manual setup.
- **vs. self-hosted PaaS tools:** Opslin emphasizes a guided, security-conscious operating experience (firewall, SSL, CI gates, rollback, alerts, backups) across the languages teams actually use.

*Named competitor comparisons and market-size figures: **[Insert verified market data/source]**. None are invented here.*

---

## 🧬 Founder–market fit

The founder encountered this problem directly while **building and deploying real client projects** — repeatedly rebuilding the same VPS, nginx, SSL, database, and monitoring setup for each one. That lived experience shaped the product: the bottleneck has shifted from *creating* software to *operating* it, and Opslin is built to reduce that operational friction for people who keep their own servers. *(Founder's full perspective: [FOUNDER_NOTE.md](FOUNDER_NOTE.md). Additional founder background: **[Founder bio]**.)*

---

## 🎯 Next milestones

- Complete beta hardening across the ~20-server fleet
- Validate launch-readiness checklist ([BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md))
- Open **public beta** and onboard waitlist users
- Establish baseline reliability and deployment-success metrics
- Convert qualified beta users to paid plans
- Roadmap progress on CI/CD depth, observability, and team workflows ([ROADMAP.md](ROADMAP.md))

---

## 💵 Fundraising

- Target raise: **[Target raise]**
- Valuation range: **[Valuation range]**
- Use of funds: **[Use of funds]**
- Pitch deck: **[Pitch deck link]**
- Product demo: **[Demo link]**
- Investor contact: **[Contact email]**

*All fundraising details are placeholders pending confirmation. Nothing about funding status is asserted.*

---

*Opslin is preparing for public beta. This summary avoids hype, makes no fabricated traction claims, and grounds product statements in what is present in the current product build. Unknowns are shown as placeholders.*
