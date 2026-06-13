# Security Overview — Opslin

A **public-safe, high-level** description of how Opslin approaches security. This document is written for investors, startup programs, accelerators, partners, advisors, and early beta users. It is intentionally **non-technical** and **omits low-level security internals.**

> **This document is a high-level overview only.** It deliberately excludes authentication formats, signing methods, token structures, privileged execution paths, internal routes, command internals, infrastructure domains, and anything else that could help someone misuse the platform.

Opslin does **not** describe itself as "unhackable," "fully enterprise-grade," "guaranteed secure," or "free of vulnerabilities." Opslin follows a **security-conscious design** and treats security as an ongoing process of validation and hardening through the pre-launch beta.

---

## 🧭 Security philosophy

Opslin operates on infrastructure that **users already own and control.** That shapes the entire security posture:

- **Least surprise, user control:** the user remains the owner of their VPS; Opslin operates on top of it.
- **Security-conscious by design:** sensitive workflows are designed to protect sensitive values rather than expose them.
- **Defense through clear boundaries:** the dashboard, control plane, and on-server agent have distinct, separated responsibilities.
- **Honest, ongoing hardening:** security is validated and improved continuously through beta, not claimed as "finished."

---

## 🖥️ User-owned infrastructure model

Opslin is a **bring-your-own-VPS** control plane. The server belongs to the user.

- Applications, databases, and monitoring run on the **user's own server.**
- Opslin provides a control plane and a lightweight agent that let the user operate that server from a dashboard.
- Because the infrastructure is user-owned, the user retains ultimate control over their environment.

---

## 🔗 Agent / control-plane boundary

Opslin uses a **lightweight agent** installed on the user's VPS. The agent connects securely to the **Opslin control plane** to enable dashboard-driven workflows.

At a high level:

- The **control plane** coordinates requests and state and communicates with agents.
- The **agent** carries out dashboard-driven actions locally on the user's server.
- Communication between the agent and the control plane is **designed to be authenticated and secure.**

*Exact protocols, handshake details, signing methods, and message formats are intentionally not described here.*

---

## 🔑 Authentication & authorization (high level)

- Access to the dashboard and control plane is restricted to **authorized users.**
- The product includes account-security building blocks such as session management, email verification, and password reset.
- Programmatic access is gated through managed API keys for authorized users.

*Implementation specifics — including formats, lifetimes, and verification mechanisms — are intentionally omitted from this public document.*

---

## 👥 Role & access control (high level)

Opslin supports **organizations with role-based access** so teams can collaborate with appropriate permissions.

- Roles span a range from full administrative control to view-only access (e.g., owner / admin / member / viewer).
- The intent is to ensure that **only authorized users** can perform sensitive operations on connected servers.

*Detailed permission matrices and enforcement internals are not published here.*

---

## 🔐 Secrets handling (high level)

- Opslin's design aims to **protect sensitive values** rather than surface them in the interface or logs.
- Secrets and credentials are treated as sensitive material and handled with care across workflows.

*This document does not describe how secrets are stored, encrypted, transmitted, or rotated. Those details are intentionally excluded.*

---

## 📜 Logs & sensitive data handling (high level)

- Logs are surfaced to help users understand and diagnose their applications and deployments.
- The design intent is to **avoid exposing sensitive values** through logs and the dashboard.
- Users are responsible for the contents of their own applications and data running on their own servers.

Before publishing any screenshots or shared media, **redact** server IPs, domains, email addresses, tokens, secrets, and customer-identifying data (see [MEDIA.md](MEDIA.md)).

---

## 🖧 Terminal & server access (safe language)

Opslin offers a browser-based terminal experience and dashboard-driven operations so authorized users can operate their own servers.

- Access is limited to **authorized users** of the relevant organization/server.
- The capability exists to help users operate infrastructure they already own and control.

*Opslin intentionally does not publish details of how privileged actions are executed on the server. This protects both the platform and its users.*

---

## 🧱 Firewall & security posture (high level)

- Opslin includes **firewall management** with a deliberate **preview-before-apply** pattern and the ability to **revert** changes.
- The intent is to let authorized users review proposed changes before they take effect, reducing the risk of accidental misconfiguration.
- This reflects the broader **security-conscious design** approach across the product.

---

## 🛡️ Beta security hardening scope

Security validation is an explicit workstream in the pre-launch beta (see [BETA_TESTING_PLAN.md](BETA_TESTING_PLAN.md)):

- Reviewing the security-conscious design under real usage
- Verifying that sensitive values are protected, not exposed
- Confirming separation between dashboard, control plane, and agent layers
- Hardening based on findings throughout the beta

This is described as **ongoing work**, not a completed certification. Opslin makes no claims of formal compliance, audits, or certifications unless and until they are independently verified — **[Insert verified security certifications/audits, if any]**.

---

## 📨 Responsible disclosure

Opslin welcomes responsible disclosure of potential security issues from researchers and users.

- Security contact: **[Security contact email]**
- Disclosure policy: **[Responsible disclosure policy link]**
- Preferred reporting process: **[Reporting process placeholder]**

*Please do not publicly disclose potential vulnerabilities before they can be reviewed and addressed.*

---

## 🚫 What this document intentionally excludes

To keep the platform and its users safe, this public overview **does not** include:

- Source code or private API routes
- Authentication formats, token structures, or signing methods
- Privileged command-execution details or internal agent control mechanics
- Production credentials, environment variables, or private keys
- Internal infrastructure domains or network topology
- Database schemas or exact deployment command internals
- Any known unresolved vulnerabilities, exploit paths, or attack techniques

---

*This is a high-level, public-safe security overview. It reflects a security-conscious design and an ongoing hardening process during beta. Specifics that could aid misuse are intentionally withheld, and placeholders are used where exact details (such as a published disclosure policy) are not yet confirmed.*
