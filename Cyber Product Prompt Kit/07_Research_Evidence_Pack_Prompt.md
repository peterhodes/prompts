# 07 - Research Evidence Pack Prompt

Use this prompt before writing the final product report. It is designed for Pro-level research.

The purpose is to create a structured evidence pack, not a polished report.

---

## Prompt

You are conducting Pro-level research for a cybersecurity product knowledge report.

Use the standards in:

- `01_Master_System_Prompt.md`
- `03_Research_Specification.md`
- `04_Style_Guide.md`

Do not write the final report yet. Produce only a structured evidence pack that will later be used to generate the final report.

## Product to research

```text
Product: {{PRODUCT_NAME}}
Vendor: {{VENDOR_NAME}}
Research date: {{RESEARCH_DATE}}
Audience: Experienced cybersecurity architect/engineer
Purpose: Personal ten-minute refresher plus full architect/engineer reference
Special focus areas: {{SPECIAL_FOCUS_AREAS}}
Known context or notes: {{KNOWN_CONTEXT}}
```

## Research requirements

Research from multiple source types:

- official product documentation
- product overview pages
- architecture guides
- deployment guides
- admin guides
- integration documentation
- API documentation
- release notes
- trust/security/compliance pages
- credible independent analysis
- analyst or market commentary where available
- practitioner/community commentary where useful
- competitor documentation for comparison

Do not rely solely on vendor claims.

Use primary sources for technical facts and independent sources for context, critique, and comparison.

## Evidence pack structure

Produce the evidence pack with these sections.

### 1. Product identity

Include:

- product name
- vendor
- product family/platform
- current naming or packaging caveats
- research date
- product status if publicly evident

### 2. Category and positioning evidence

Include:

- primary category
- secondary categories
- vendor positioning
- independent/industry positioning where available
- whether labels such as SIEM, SOAR, XDR, EDR, ASM, VM, CNAPP, IAM, PAM, or other categories apply fully, partially, or not at all

Use a table:

| Category | Applies? | Evidence | Caveat |
|---|---:|---|---|

### 3. Problems solved and buying drivers

Capture evidence for:

- security problems solved
- operational problems solved
- compliance drivers
- business drivers
- customer buying triggers
- where the product is a strong fit
- where it is not a strong fit

### 4. Capability evidence

Use a table:

| Capability | Evidence | Source | Confidence | Caveat |
|---|---|---|---|---|

### 5. Architecture evidence

Capture:

- deployment model
- components
- data flow
- collectors/agents/connectors
- SaaS/on-prem/hybrid details
- trust boundaries
- admin plane
- data plane
- event ingestion model

### 6. Deployment evidence

Capture:

- prerequisites
- onboarding steps
- identity requirements
- network requirements
- endpoint or collector requirements
- cloud requirements
- operational handover considerations

### 7. Data source evidence

Use a table:

| Data source | Collection method | Purpose | Source | Notes |
|---|---|---|---|---|

### 8. Detection, analytics, and response evidence

Capture:

- detection types
- analytics model
- behavioural analytics/UEBA
- threat intelligence usage
- MITRE ATT&CK mapping if available
- tuning
- false-positive management
- response workflow
- automation/playbooks
- SOAR depth

### 9. Integration evidence

This section is critical.

Use a table:

| Product / platform | Direction | Authentication | Workflow | Evidence | Caveats |
|---|---|---|---|---|---|

Research integrations such as:

- Jira
- ServiceNow
- PagerDuty
- Slack
- Microsoft Teams
- email
- Microsoft Sentinel
- Splunk
- QRadar
- Elastic
- Google SecOps
- Entra ID
- Okta
- Active Directory
- Microsoft Defender
- CrowdStrike
- SentinelOne
- AWS
- Azure
- GCP
- Palo Alto
- Cisco
- Fortinet
- Check Point
- Zscaler
- Rapid7 InsightVM
- Tenable
- Qualys
- APIs/webhooks/custom connectors

Only include integrations that are relevant or publicly evidenced. If a likely integration is not found, say so.

For Jira, ServiceNow, and PagerDuty, specifically determine whether the product supports practical workflows such as ticket creation, incident creation, alert notification, on-call escalation, or status synchronisation. Do not assume bidirectional sync unless documented.

### 10. API and extensibility evidence

Capture:

- API types
- authentication
- common use cases
- webhooks
- custom integrations
- event export
- rate limits if public
- documentation links

### 11. Identity, RBAC, and administration evidence

Capture:

- SSO
- SAML/OIDC
- MFA
- RBAC
- audit logging
- admin roles
- service accounts/API keys
- tenant model

### 12. Data security, privacy, and compliance evidence

Capture:

- encryption
- data residency
- retention
- compliance certifications
- trust/security documentation
- audit reports if public
- privacy caveats

### 13. Operational evidence

Capture:

- day-to-day administration
- detection tuning
- alert triage
- incident workflow
- ownership model
- integration maintenance
- reporting
- health monitoring
- common operational issues

### 14. Licensing and commercial evidence

Capture public evidence only.

Include:

- licensing metric
- packaging/editions
- add-ons
- cost drivers
- caveats
- what must be validated with the vendor

Do not invent pricing.

### 15. Strengths and weaknesses evidence

Use a table:

| Observation | Strength / weakness | Evidence | Source type | Confidence | Caveat |
|---|---|---|---|---|---|

### 16. Competitor evidence

Use a table:

| Competitor | Category | Evidence of overlap | Where product may be stronger | Where competitor may be stronger | Caveats |
|---|---|---|---|---|---|

### 17. Common pitfalls evidence

Capture likely pitfalls supported by evidence or careful architectural analysis.

Clearly label analysis versus sourced evidence.

### 18. Recent changes and roadmap evidence

Capture:

- product renaming
- packaging changes
- acquisitions
- major releases
- public roadmap items
- deprecations

Use absolute dates.

### 19. Conflict log

Use a table:

| Topic | Source A | Source B | Conflict | Likely resolution |
|---|---|---|---|---|

### 20. Open questions

List questions that remain unresolved and should be validated with the vendor, customer, or further research.

### 21. Source register

Use this table:

| Source | Publisher | Type | URL | Date accessed | Used for | Reliability |
|---|---|---|---|---|---|---|

### 22. Confidence assessment

Include:

- overall confidence: High / Medium / Low
- strongest evidence areas
- weakest evidence areas
- areas likely to change
- suggested refresh triggers

## Output instruction

Produce the evidence pack only. Do not write the final report yet.
