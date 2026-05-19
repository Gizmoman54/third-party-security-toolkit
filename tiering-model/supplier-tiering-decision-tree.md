Supplier Tiering Decision Tree (T1/T2/T3)
Purpose: classify suppliers into Tier 1/2/3 based on impact, access, connectivity, and data handled. When in doubt, tier up.

Step 1 — Is it business critical?
Tier 1 if any are true:

Outage would materially impact client service, trading/portfolio activity, payments, or regulatory reporting
Supplier supports a “critical business service” or core platform
Supplier is an MSP/outsourcer that operates your environment or security controls
If none apply, continue.

Step 2 — Does the supplier have privileged access or production influence?
Tier 1 if any are true:

Administrative access (tenant admin, domain admin, “super user”), or can change configs/security settings
Interactive access into your environment (support access, remote sessions)
CI/CD, code deployment, infrastructure as code, or ability to modify production systems
If none apply, continue.

Step 3 — What data do they store/process/transmit?
Tier 1 if any are true:

Processes/stores PII, financial account data, authentication secrets, or sensitive client data at meaningful scale
Processes data that would trigger regulatory/customer notification if breached
Tier 2 if:

Limited PII or internal business data only, and no privileged access
If neither, continue.

Step 4 — What integration pattern is used?
Tier 1 if any are true:

Persistent network connectivity (VPN/private link), inbound connectivity, or non-standard firewall rules
Broad API permissions or write access to critical systems/data
Tier 2 if:

SaaS with SSO + least-privilege roles, limited API scope, and no network connectivity
If neither, continue.

Step 5 — Fourth parties / concentration risk
Tier 1 if any are true:

Material reliance on sub-processors you cannot identify or control
Single point of failure provider for a critical function (no viable workaround)
Otherwise Tier 3.

Tier outcomes
Tier 1 (Critical): highest baseline controls, strongest evidence pack, named security contact, contract security schedule, time-bound remediation for gaps.
Tier 2 (Important): standard baseline controls + proportionate evidence.
Tier 3 (Low): lightweight controls; re-assess on trigger events only.
Trigger events (re-tier required)
Scope change, new data types, new integrations/connectivity, privileged access requested, major incident/breach, or significant subcontractor change.
