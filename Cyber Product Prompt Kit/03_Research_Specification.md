# 03 - Research Specification

This document defines how research should be conducted before writing a cybersecurity product knowledge report.

The goal is not simply to collect facts. The goal is to build an evidence base that supports a vendor-neutral, architect/engineer-focused document.

---

## Research principles

1. **Vendor documentation is necessary but not sufficient.** Use official sources for product facts, but do not treat marketing claims as independent evidence.
2. **Prefer primary sources for technical detail.** Official docs, API docs, integration docs, admin guides, and release notes are usually the best sources for capabilities.
3. **Use independent sources for interpretation.** Analyst reports, practitioner blogs, forums, customer reviews, and competitor material can help identify trade-offs and limitations.
4. **Separate evidence from analysis.** The evidence pack should preserve source facts before the final report synthesises them.
5. **Capture uncertainty.** If something cannot be verified, say so.
6. **Use dates.** Product capabilities, names, licensing, integrations, and UI workflows change frequently.
7. **Do not invent details.** If information is not public, write `Information not publicly available.`

---

## Minimum research scope

For each product, research the following areas.

### Product identity and positioning

Find:

- official product name
- vendor
- product family/platform
- current packaging or naming
- primary category
- secondary categories
- market positioning
- target buyers
- target users

### Product capabilities

Find:

- core features
- key modules
- deployment model
- supported data sources
- detection/analytics capabilities
- automation and response capabilities
- reporting capability
- administration model

### Architecture and deployment

Find:

- SaaS/on-prem/hybrid model
- collectors, agents, sensors, connectors, forwarders, or appliances
- data ingestion mechanisms
- control plane and data plane information where public
- identity integration
- data flow
- retention and storage information
- high availability and resilience claims where public

### Integrations

Find integration evidence for:

- ticketing platforms such as Jira and ServiceNow
- alerting/on-call platforms such as PagerDuty
- SIEM platforms such as Microsoft Sentinel, Splunk, QRadar, Elastic, and Google SecOps
- identity platforms such as Entra ID, Okta, Ping, and Active Directory
- endpoint products such as Microsoft Defender, CrowdStrike, SentinelOne, Sophos, and Carbon Black
- cloud platforms such as AWS, Azure, and Google Cloud
- network/security platforms such as Palo Alto, Cisco, Fortinet, Check Point, Zscaler, and Netskope
- vulnerability management platforms such as Rapid7 InsightVM, Tenable, and Qualys
- APIs, webhooks, event export, and custom connectors

For each integration, determine:

- whether it is inbound, outbound, bidirectional, or authentication-only
- authentication method if public
- practical workflow
- limits or caveats
- whether the integration is native, connector-based, API-based, webhook-based, or third-party

### Operations

Find:

- onboarding process
- tuning process
- alert workflow
- incident workflow
- roles and responsibilities
- administrative overhead
- common operational considerations
- monitoring or health-check capabilities

### Licensing and commercial model

Find only public information.

Capture:

- public licensing metric, if available
- editions or packages
- add-ons
- consumption drivers
- cost risk areas
- pricing caveats

Never invent pricing.

### Security, privacy, and compliance

Find:

- security documentation
- encryption claims
- compliance certifications
- data residency information
- audit logging
- access control
- trust centre information
- status page if available

### Competitors

Identify direct and adjacent competitors.

For each, determine:

- category overlap
- target market difference
- architectural difference
- strengths relative to the product
- weaknesses relative to the product

---

## Source hierarchy

Use the following source hierarchy.

### Tier 1 - Strong technical evidence

- official product documentation
- integration documentation
- API documentation
- administrator guides
- deployment guides
- release notes
- official security/trust documentation

### Tier 2 - Strong contextual evidence

- reputable analyst reports
- recognised industry research
- conference presentations
- technical blogs from respected practitioners
- competitor documentation when comparing capabilities

### Tier 3 - Useful but lower confidence

- community forums
- Reddit discussions
- customer reviews
- sales decks
- reseller summaries
- training notes

Tier 3 sources can help identify operational issues or perceptions, but should not be treated as definitive without corroboration.

---

## Vendor claim handling

When a vendor makes a claim, classify it.

Use this structure where useful:

| Claim | Source | Classification | Evidence | Confidence |
|---|---|---|---|---|
|  | Vendor claim / verified fact / independent observation / analysis |  |  |  |

Do not convert vendor claims into neutral facts unless supported by documentation or independent evidence.

Example wording:

- `Vendor claim: The vendor positions the product as...`
- `Public documentation confirms...`
- `Independent evidence is limited; treat this as a vendor positioning statement.`
- `Architectural analysis: This suggests the product is strongest when...`

---

## Conflicting information

If sources disagree:

1. Prefer the most recent official documentation for product facts.
2. Prefer current API/integration documentation over old blog posts.
3. Preserve the conflict in a conflict log.
4. Explain the likely reason, such as rebranding, packaging changes, product consolidation, acquisition, or deprecated features.
5. Use absolute dates.

Conflict log format:

| Topic | Source A | Source B | Conflict | Resolution / interpretation |
|---|---|---|---|---|

---

## Evidence pack requirements

Before writing the final report, produce an evidence pack with these sections:

1. Product identity
2. Category and positioning evidence
3. Capability evidence
4. Architecture evidence
5. Deployment evidence
6. Data source evidence
7. Integration evidence
8. API/extensibility evidence
9. Identity/RBAC evidence
10. Security/privacy/compliance evidence
11. Operational evidence
12. Licensing evidence
13. Competitor evidence
14. Strengths and weaknesses evidence
15. Common pitfalls evidence
16. Recent changes and roadmap evidence
17. Source register
18. Conflict log
19. Open questions
20. Confidence assessment

---

## Citation expectations

The final document should include references where possible.

Citations are especially important for:

- product naming and packaging
- architecture
- deployment model
- integrations
- API capability
- licensing
- security/compliance claims
- recent changes
- competitor comparisons

When a citation cannot be included, explain the basis for the statement or mark it as analysis.

---

## Quality bar for research completion

Research is sufficient when the evidence pack can answer:

- What is the product?
- What problem does it solve?
- What category or categories does it belong to?
- What are the top capabilities?
- How is it deployed?
- What are the key architectural components?
- What are the main data flows?
- What does it integrate with?
- How would Jira, ServiceNow, or PagerDuty integration work if relevant?
- What are the strengths and limitations?
- What competitors should be considered?
- What should an architect ask before recommending or deploying it?
- What would be important in an interview or meeting?

If these cannot be answered, continue research or explicitly mark the gaps.
