# Product Overview — Opslin

**Category:** Zero-DevOps VPS management platform — a *bring-your-own-VPS* deployment and infrastructure control plane.

**Status:** Preparing for public beta. Testing real projects before launch.

This document is a deeper, non-technical overview of Opslin for investors, startup programs, partners, advisors, and early beta users. It contains **no source code and no sensitive implementation details.**

---

## 🌌 Vision

Software creation is getting faster. Deployment and operations should keep up.

Opslin's vision is a world where shipping and operating software on your **own infrastructure** is as simple as using a managed platform — without giving up the **cost advantages and control** of running your own VPS. Opslin aims to be the **control plane** that sits on top of servers people already own, turning repetitive DevOps work into a few clear dashboard actions.

---

## 🧩 The problem

Modern tooling has dramatically reduced the time it takes to **build** software. AI coding assistants, frameworks, templates, and boilerplates mean a working product can come together quickly.

**Deployment and infrastructure have not simplified at the same pace.** Developers still spend disproportionate time on:

- VPS setup and hardening
- Docker and container orchestration
- nginx and reverse proxies
- SSL certificates and renewals
- Domains and DNS
- Databases (provisioning, connection, maintenance)
- Logs and debugging deployment failures
- Monitoring and health checks
- Firewall rules
- CI/CD wiring
- Ongoing server maintenance

This is repetitive, error-prone, and easy to get wrong — and it sits directly between "the code works on my machine" and "the product is live and reliable."

---

## 💡 Founder insight

The founder hit this problem directly while **building and deploying real client projects.**

The pattern was consistent: writing the application kept getting faster, but **getting it deployed, secured, monitored, and kept running** stayed slow and manual. Each new project meant repeating the same VPS setup, the same nginx and SSL steps, the same database and monitoring chores.

The insight: the bottleneck has moved. It is no longer *creating* software — it is **operating** it. Opslin is built to reduce that operational friction for people who want to keep using their own servers.

*More on the founder's perspective is in [FOUNDER_NOTE.md](FOUNDER_NOTE.md).*

---

## 👥 Target users

| User | What they want | How Opslin helps |
|---|---|---|
| **Developers** | Ship without becoming sysadmins | One dashboard for deploy, logs, monitoring |
| **Freelancers** | Manage many client projects efficiently | Consistent workflow across servers and clients |
| **Agencies** | Operate many sites/apps reliably | Centralized control over multiple VPS deployments |
| **Startups** | Control + low cost without a DevOps hire | Modern deployment experience on owned infrastructure |
| **DevOps teams** | Reduce repetitive toil | Faster, repeatable infrastructure workflows |

> Opslin is **not** trying to replace DevOps engineers. It reduces repetitive DevOps work so teams can operate infrastructure faster.

---

## 😖 User pain points

- "I can build the app fast, but deploying it takes a whole day."
- "Every new project means redoing nginx, SSL, and firewall setup."
- "I'm not sure my server is configured safely."
- "When a deploy fails, I have to SSH in and dig through logs."
- "Managed platforms are easy but get expensive or restrictive."
- "A raw VPS is cheap and powerful, but operating it is a chore."

---

## 🧰 Use cases

- Deploying a Node.js or static web app to a personal VPS
- An agency standing up client projects across several servers
- A freelancer managing deployments and databases for multiple clients
- A startup running its product on owned infrastructure to control costs
- A team that wants dashboard-driven operations instead of manual SSH workflows

---

## ⚙️ Product capabilities

The following capabilities are **present in the current product build** and are undergoing validation and hardening through the pre-launch beta:

- Connect a user-owned VPS via a lightweight agent
- Deploy, stop, restart, and delete applications from the dashboard
- **Multi-language deployment** — Node.js (with framework detection for Next.js, Nuxt, Astro, Remix, SvelteKit, Angular, React, NestJS, Express), plus Python, Go, PHP, Ruby, Java, Rust, and static sites
- **Roll back** to a previous deployment and review deployment history
- Manage databases — PostgreSQL, MySQL, MongoDB, Redis — including queries, seeding, backup, and restore
- Configure custom domains and SSL
- Managed, versioned **reverse-proxy / nginx** configuration
- **Firewall management** — discover, preview, apply, and revert policies
- Monitor server and per-container metrics, with application **health checks**
- View application and deployment logs
- Browser-based **web terminal** to the server
- **Guided failure diagnosis** — deployment failures are classified into clear, actionable categories
- **Teams & roles** — organizations with role-based access (owner/admin/member/viewer) and invites
- **GitHub integration with CI deploy gates** — optional checks before a deploy proceeds
- **Alerts** (rules, events, channels) and **scheduled database backups** with restore drills
- API keys, session management, email verification, and password reset
- Subscription billing and plan management

**Planned / not yet in the product (future direction):**

- AI-assisted deployment guidance
- A marketplace of reusable deployment building blocks
- Enterprise SSO / SAML and advanced enterprise controls

*Capabilities listed above are present in the current product build. Forward-looking items are clearly separated and detailed in [ROADMAP.md](ROADMAP.md). "Present in the current build" means the capability exists in the product and is undergoing beta validation — not a guarantee of bug-free behavior.*

---

## 🔄 Before / after workflow

**Before Opslin (typical manual flow):**

```text
Write code → SSH into VPS → install dependencies → configure Docker →
set up nginx → request SSL cert → point domain → set up database →
configure firewall → add monitoring → tail logs manually →
debug failures over SSH → repeat for every project
```

**With Opslin:**

```text
Write code → connect VPS via agent → deploy from dashboard →
configure domain & SSL in the UI → monitor health & logs in one place →
manage running apps from the dashboard
```

The goal is to collapse repetitive, multi-step server operations into a small number of clear, dashboard-driven actions.

---

## 🪢 Why "Bring Your Own VPS" matters

Most teams face a trade-off between **two ends of a spectrum**:

### Managed platforms — easy, but can be expensive or restrictive
- ✅ Very simple to use
- ✅ Minimal infrastructure knowledge required
- ⚠️ Costs can grow significantly with scale
- ⚠️ Less control over the underlying environment
- ⚠️ Potential lock-in to a single vendor's model

### Raw VPS — powerful, but difficult
- ✅ Low cost and high flexibility
- ✅ Full control of the environment
- ⚠️ Operationally demanding (setup, security, maintenance)
- ⚠️ Repetitive, error-prone manual work
- ⚠️ Steep learning curve for non-specialists

### Where Opslin sits

```text
Managed Platform  ───────────────  Opslin  ───────────────  Raw VPS
(easy, costly,                  (easy operations,         (powerful,
 less control)                   your server,              difficult,
                                 your control)             full control)
```

**Opslin aims to combine the simplicity of a managed deployment experience with the cost and control of your own VPS.** You keep ownership of the server; Opslin makes operating it dramatically simpler.

---

## 🚦 Beta status

Opslin is **preparing for public beta** and is currently **testing real projects before launch.**

Current focus areas:

- Validating deployment workflows across real applications
- Hardening monitoring, logging, database, and SSL/domain flows
- Deliberately testing deployment failure scenarios
- Security-conscious validation (beta hardening)

No completion claims are made. Detailed plan: [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md).

---

## 🧭 Future product direction

Opslin's direction splits into **deepening what already exists** and **genuinely new** areas.

**Deepening existing capabilities** (already in the product; planned to go further):

- **Stronger CI/CD workflows** — building on the existing GitHub integration and CI deploy gates
- **Deeper observability** — richer metrics, logs, and insights on top of current monitoring
- **Team / agency workflows** — expanding the existing organizations and role-based access
- **Managed security layer** — extending the current firewall and security-conscious design

**Genuinely new (not yet in the product):**

- **AI-assisted deployment guidance** — help users resolve issues and configure faster *(not yet implemented)*
- **Marketplace** — reusable deployment building blocks *(not yet implemented)*
- **Enterprise SSO / SAML and advanced enterprise controls** *(not yet implemented)*

Forward-looking items are intended direction, **not** shipped features. Specifics and timing are in [ROADMAP.md](ROADMAP.md).

---

*Opslin is preparing for public beta. This overview avoids hype and uses placeholders wherever exact figures or links are not yet confirmed.*
