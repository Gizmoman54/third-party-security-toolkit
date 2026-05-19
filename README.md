Vendor Third-party-security-toolkit
An engineering-led third‑party security toolkit designed for regulated environments. This repo provides practical templates and implementation patterns to assess supplier risk, onboard vendors securely, and maintain ongoing assurance—without turning the program into paperwork.

Who it’s for
Security Engineering, Security Architecture, Technology Risk, Procurement, and IT teams building or improving a third‑party security program.

What’s inside
Vendor tiering model (criticality-based requirements)
Secure onboarding and integration patterns (identity, connectivity, logging)
Control baselines with validation steps (“how to prove it”)
Evidence request packs by vendor tier
Exception handling approach (gap → compensating controls → expiry)
Ongoing monitoring triggers, re-assessment cadence, and metrics
Design principles
Pragmatic and verifiable: prefer technical controls and testable outcomes over “checkbox” answers
Secure-by-design onboarding: bake requirements into the intake and integration patterns
Least privilege by default: constrain access, segment connectivity, and log everything that matters
Explicit trade-offs: exceptions are time-bound and require compensating controls
Repository structure
/program-charter /operating-model /tiering-model /integration-patterns /control-baselines /evidence-packs /contracts /monitoring /metrics

How to use this repo
Start with the tiering model to classify suppliers.
Apply the baseline controls and evidence packs for the supplier’s tier.
Use integration patterns to standardise onboarding (SSO, access, connectivity, logging).
Track gaps via the exception process and report progress via the metrics pack.

Notes / disclaimer
This repository uses synthetic examples and is not affiliated with any employer or client. Control mappings are illustrative and should be adapted to your organisation’s risk appetite, regulatory obligations, and technical architecture.

Start here
Artifact Map (Start Here) 
third-party-security-toolkit/Artifact Map (Start Here).docx

