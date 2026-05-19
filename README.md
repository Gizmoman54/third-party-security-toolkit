Third-Party Security Transformation (Pragmatic / Engineering-led)
This repository is a reference implementation of an engineering-led third‑party security program for a mid-sized, FCA-regulated wealth management firm. It focuses on secure-by-design vendor onboarding, repeatable integration patterns, measurable control validation, and a clear escalation path when a supplier can’t meet baseline requirements.

What this is
A practical toolkit: tiering model, evidence packs, control baselines, integration patterns, and acceptance tests.
Designed to be implemented by Security + IT Engineering + Procurement + Legal without “paper-only” controls.
What this is not
Not tied to any specific firm, environment, or proprietary configuration.
Not a compliance claim. Mappings are illustrative.
Core outcomes
Reduce time-to-onboard while raising minimum security controls.
Ensure critical suppliers are integrated with least privilege, strong logging, and resilient connectivity.
Make exceptions explicit, time-bound, and technically compensated.
Repo structure
/program-charter Program goals, governance, escalation /tiering-model Criticality tiers + required control baselines /integration-patterns Standard connectivity and access patterns (with diagrams) /control-baselines Verifiable technical requirements + validation steps /evidence-packs Vendor evidence request lists by tier /contracts Security schedule + DPA talking points (templates) /monitoring Ongoing review triggers + re-assessment cadence /metrics KPIs/KRIs + sample reporting pack

tiering-model/vendor-tiering.md

Vendor Tiering Model (Engineering-led)
Tiering dimensions (how we decide)
Data sensitivity (PII, financial, auth secrets, trading/portfolio data)
Privilege level (admin, production access, ability to change configurations)
Connectivity (inbound/outbound, persistent links, API integrations, SSO)
Service criticality (impact to client service, trading, regulatory reporting)
Sub-processors & concentration risk (fourth parties, single points of failure)
Tiers
Tier 1 — Critical / High Trust Integration
Typical: managed service providers, core SaaS with PII, platforms with production access. Minimum requirements:

SSO + MFA enforced; no local accounts for privileged access where possible
Strong privileged access controls (PAM or equivalent), break-glass, session logging where feasible
Audit-grade logging: access/auth/admin events available and retained per requirement
Vulnerability management: defined patch SLAs, external attack surface controls
Secure integration pattern: segmented connectivity, least privilege APIs, key rotation
Incident comms: time-bound notification commitments + named contacts
Resilience: tested recovery approach aligned to agreed RTO/RPO expectations
Tier 2 — Important / Standard Integration
Typical: business SaaS with limited PII, non-prod integrations, internal tools. Minimum requirements:

SSO preferred; MFA required for admin accounts
Documented security controls and incident process
Logging available on request; basic retention
Patch and vulnerability process documented
Basic resilience statement (backups/restore, service availability)
Tier 3 — Low Risk / No Integration or Low Sensitivity
Typical: marketing tools with no PII, low-impact suppliers, no connectivity. Minimum requirements:

Basic security questionnaire + confirmation of MFA for admin access where relevant
Contractual security language proportionate to risk
Re-assess only on trigger events (breach, scope change, new data types)
Exceptions (how we stay pragmatic)
Exceptions are allowed only with: documented gap, compensating controls, owner, and expiry date.
Preferred compensating controls are technical (segmentation, reduced privilege, brokered access, enhanced logging).
