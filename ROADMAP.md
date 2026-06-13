# Roadmap — Opslin

A forward-looking view of where Opslin is headed. **Future features are clearly marked as future** and are not presented as available. Timeframes are directional, not commitments. Where exact dates or metrics are not finalized, placeholders are used.

> **Legend:** ✅ **In current build** (present in the product, being validated through beta) · 🔧 **Hardening** (active beta focus) · 🔜 **Planned** (committed direction, not yet built) · 🌱 **Exploring** (early-stage idea)

---

## 🟢 Current beta

**Status: preparing for public beta; testing real projects before launch.**

Already in the product and being validated/hardened:

- ✅ Connect a user-owned VPS via a lightweight agent
- ✅ Deploy / stop / restart / delete applications
- ✅ Multi-language deploys — Node.js (Next.js, Nuxt, Astro, Remix, SvelteKit, Angular, React, NestJS, Express), Python, Go, PHP, Ruby, Java, Rust, static sites
- ✅ Rollback and deployment history
- ✅ Databases (PostgreSQL, MySQL, MongoDB, Redis) with backup/restore
- ✅ Domains & SSL, managed nginx/reverse-proxy
- ✅ Firewall management (preview-before-apply, revert)
- ✅ Monitoring, health checks, logs, web terminal
- ✅ Guided deployment-failure diagnosis
- ✅ Teams/organizations with role-based access
- ✅ GitHub integration with CI deploy gates
- ✅ Alerts, scheduled backups, subscription billing
- 🔧 **Beta hardening focus:** reliability across the ~20-server fleet, failure handling, security validation, onboarding polish

*See [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md) for how this is being validated.*

---

## 📅 Next 30 days

*Directional; subject to beta findings.*

- 🔧 Complete priority items on the launch-readiness checklist
- 🔧 Tighten deployment reliability and failure recovery based on real-project testing
- 🔧 Onboarding flow improvements informed by early-user feedback
- 🔧 Security validation pass (beta hardening)
- 🔜 Open **public beta** to waitlist users — **[Public beta date]**
- 🔧 Establish baseline metrics: **[Deployment success rate]**, **[Connected servers]**, **[Apps deployed]**

---

## 📆 Next 3 months

- 🔜 **Stronger CI/CD workflows** — deepen the existing GitHub integration and CI deploy gates
- 🔜 **Deeper observability** — richer metrics, logs, and insights on top of current monitoring
- 🔜 **Expanded team / agency workflows** — building on existing organizations and role-based access
- 🔜 Broader, more resilient multi-language deployment coverage and edge-case handling
- 🔜 Reliability and performance improvements driven by beta data
- 🌱 Improved guided remediation for common deployment failures

---

## 🗓️ Next 6 months

- 🔜 **Managed security layer** — extend current firewall and security-conscious design with safer defaults and guidance
- 🔜 **DevOps productivity features** — reduce more repetitive operational work
- 🔜 Strengthen backup/restore and disaster-recovery workflows
- 🌱 **AI-assisted deployment guidance** *(not yet implemented)* — help users diagnose and resolve issues faster
- 🌱 Early **enterprise controls** for larger teams with stricter requirements
- 🔧 Continued hardening and reliability work as usage grows

---

## 🔭 Long-term vision

Opslin aims to be the **control plane teams reach for to operate software on infrastructure they own** — combining the simplicity of a managed deployment experience with the cost and control of a VPS.

Long-term directions (**all future, not built**):

- 🌱 **AI-assisted deployment & operations** — guided setup, diagnosis, and optimization
- 🌱 **Marketplace** — reusable deployment building blocks and templates
- 🌱 **Enterprise controls** — SSO / SAML, advanced governance, and compliance-oriented features
- 🌱 **Deeper observability platform** — unified metrics, logs, and alerting
- 🌱 **Broader collaboration** — richer agency/team operations across many servers and clients

> These represent intended direction and are explicitly **not** shipped features. Specifics and timing depend on beta learnings, demand, and resourcing.

---

## ⚠️ Notes on this roadmap

- Items marked ✅ are present in the current product build and are being validated through beta — this is **not** a claim of bug-free behavior.
- Items marked 🔜 / 🌱 are **future** and should not be treated as available.
- Dates and metrics shown as **[placeholders]** are not yet finalized; none are invented.
- Opslin makes no claims of being "fully enterprise-grade," "unhackable," or offering "guaranteed deployment." Security and reliability are treated as ongoing work.

---

*Opslin is preparing for public beta. This roadmap separates what exists today from what is planned, and uses placeholders wherever specifics are not yet confirmed.*
