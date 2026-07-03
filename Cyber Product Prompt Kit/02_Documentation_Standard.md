# 02 - Documentation Standard

This document defines the standard structure for every cybersecurity product knowledge report.

The structure is designed to support two use cases:

1. **Ten-minute refresher** before a meeting, interview, workshop, or vendor call.
2. **Full architect/engineer reference** for deeper preparation and long-term knowledge retention.

There is no fixed page limit. Completeness, clarity, and usefulness are more important than brevity.

---

# Required Report Structure

Every report must contain the following sections in this order.

---

## 0. Document Control

Include a short metadata table.

Required fields:

| Field | Requirement |
|---|---|
| Product | Product name. |
| Vendor | Vendor name. |
| Product family / platform | Parent platform or suite if relevant. |
| Primary categories | Example: SIEM, SOAR, XDR, EDR, ASM, VM, IAM, PAM, SASE, CNAPP. |
| Document purpose | Personal refresher and architect/engineer reference. |
| Research date | Use an absolute date. |
| Report version | Start at 1.0 unless instructed otherwise. |
| Confidence rating | High, Medium, or Low. |
| Key caveats | Include naming, packaging, public documentation, or licensing caveats. |

---

## 1. Ten-Minute Refresher

This is the most important section for fast preparation.

It must be readable in under ten minutes and include:

- what the product is
- why it exists
- primary product categories
- core use cases
- typical buyers and users
- top strengths
- top weaknesses
- most important integrations
- key competitors
- the most important points to remember before a meeting

Suggested sub-sections:

### 1.1 One-paragraph summary

A concise description of the product and its purpose.

### 1.2 Key facts

Use a table.

| Area | Summary |
|---|---|
| Vendor |  |
| Category |  |
| Deployment model |  |
| Main users |  |
| Core problem solved |  |
| Best fit |  |
| Less suitable for |  |
| Main competitors |  |

### 1.3 Five things to remember

Use short, direct bullets.

### 1.4 Five useful meeting points

These should be points the reader can use in conversation.

---

## 2. Product Positioning

Explain where the product sits in the market and security architecture.

Must include:

- product family and platform context
- primary category
- secondary categories
- whether category labels are clear, overlapping, or vendor-driven
- market segment
- target customer maturity
- whether it replaces, complements, or overlaps with other controls

Example category table:

| Category | Applies? | Explanation |
|---|---:|---|
| SIEM | Yes / No / Partial |  |
| SOAR | Yes / No / Partial |  |
| XDR | Yes / No / Partial |  |
| UEBA | Yes / No / Partial |  |
| EDR | Yes / No / Partial |  |
| Vulnerability Management | Yes / No / Partial |  |

---

## 3. Problems Solved and Buying Drivers

Explain the cyber problems the product solves.

Include:

- operational pain points before adoption
- business drivers
- security drivers
- compliance drivers
- SOC maturity drivers
- threat detection and response drivers
- why an organisation would pay for the product
- why the product might be selected over alternatives

Include a table:

| Problem | How the product addresses it | Limitations / assumptions |
|---|---|---|

---

## 4. Typical Customers and Use Cases

Describe who uses the product and why.

Include:

- typical organisation size
- industry fit
- SOC maturity level
- buyer personas
- operator personas
- managed service provider use
- common deployment scenarios
- cases where the product is not a good fit

Suggested personas:

- CISO
- Head of Security Operations
- SOC Manager
- Security Architect
- Security Engineer
- Detection Engineer
- Incident Responder
- IT Operations
- Compliance / GRC

---

## 5. Core Capabilities

Describe the main capabilities in practical terms.

For each capability, include:

- what it does
- why it matters
- architectural or operational dependency
- limitations or caveats

Use a table:

| Capability | Purpose | Business / security value | Dependencies | Caveats |
|---|---|---|---|---|

---

## 6. Architecture Overview

Explain the high-level architecture.

Include:

- SaaS, on-premises, hybrid, or appliance-based model
- management plane
- data plane
- control plane, if relevant
- collectors, agents, sensors, connectors, or forwarders
- log/event ingestion
- normalisation and enrichment
- analytics/detection layer
- alerting and case management
- response actions
- administrative access
- trust boundaries

If diagrams cannot be drawn, describe them textually.

Suggested format:

```text
Data sources -> collectors/connectors/agents -> cloud service / analytics platform -> detections -> investigations -> alerts/cases -> response workflow -> ticketing/notification/SOAR tools
```

---

## 7. Major Components

Break the product into its major components.

For each component, describe:

- purpose
- deployment location
- owner/operator
- key configuration considerations
- dependency on other components
- failure or limitation considerations

Use a table:

| Component | Purpose | Location | Notes |
|---|---|---|---|

---

## 8. Deployment Model

Explain how the product is deployed.

Include:

- SaaS/on-prem/hybrid model
- prerequisites
- network requirements
- identity requirements
- endpoint requirements
- cloud requirements
- collector requirements
- required permissions
- data residency considerations where available
- onboarding approach

Also describe common deployment phases:

1. design and scoping
2. identity integration
3. data source onboarding
4. collector or agent deployment
5. detection tuning
6. alert routing
7. operational handover
8. optimisation

---

## 9. Data Sources and Collection

Explain what data the product consumes and how.

Include:

- endpoint data
- identity data
- network data
- cloud logs
- SaaS logs
- firewall logs
- vulnerability data
- threat intelligence
- third-party security tool alerts
- custom logs

Use a table:

| Data source | Collection method | Purpose | Notes / limitations |
|---|---|---|---|

---

## 10. Detection, Analytics, and Correlation

Explain the detection model.

Include:

- rule-based detection
- behavioural analytics
- UEBA, if relevant
- threat intelligence matching
- anomaly detection
- machine learning or AI claims, if any
- detection tuning
- false-positive management
- custom detections
- MITRE ATT&CK mapping, if available

Clearly distinguish vendor claims from verified public evidence.

---

## 11. Alerting, Investigation, and Incident Response Workflow

Describe the operational workflow.

Include:

- alert generation
- alert enrichment
- prioritisation
- triage
- investigation views
- incident/case creation
- escalation
- ticket creation
- notification
- response action
- closure and lessons learned

Use a simple workflow diagram in text:

```text
Event -> Detection -> Alert -> Enrichment -> Triage -> Case/Incident -> Ticket/Notification -> Response -> Closure
```

---

## 12. Automation and SOAR Capability

Explain whether the product provides automation, orchestration, response playbooks, or SOAR-like features.

Include:

- native automation
- third-party automation
- playbooks or workflows
- response actions
- approval gates
- ticketing workflows
- notification workflows
- limitations compared with dedicated SOAR tools

Be precise. Do not label a product as full SOAR unless the evidence supports it.

---

## 13. Integrations

This section must be detailed. Do not merely list integrations.

For every major integration, include:

| Product / platform | Direction | Authentication | Purpose | Typical use case | Notes / limitations |
|---|---|---|---|---|---|

Direction should be one of:

- inbound
- outbound
- bidirectional
- authentication only
- enrichment only
- notification only
- ticketing only

Important integration categories:

- ticketing: Jira, ServiceNow, Zendesk
- alerting/on-call: PagerDuty, Opsgenie, Slack, Teams, email
- identity: Entra ID, Okta, Ping, Active Directory
- SIEM: Microsoft Sentinel, Splunk, QRadar, Elastic, Google SecOps
- EDR/XDR: Microsoft Defender, CrowdStrike, SentinelOne, Sophos, Carbon Black
- cloud: AWS, Azure, GCP
- network: Palo Alto, Cisco, Fortinet, Check Point, Zscaler
- vulnerability management: Rapid7 InsightVM, Tenable, Qualys
- threat intelligence: MISP, commercial TI platforms, STIX/TAXII where relevant
- APIs/webhooks: REST APIs, webhook integrations, event export

For Jira, ServiceNow, and PagerDuty, explicitly describe practical workflows where publicly documented or reasonably inferable from documented integration capability.

Example:

```text
Detection alert -> incident created or enriched -> Jira issue created -> assignee/team workflow -> status updates -> closure
```

Do not assume bidirectional sync unless the documentation supports it.

---

## 14. APIs and Extensibility

Include:

- available APIs
- authentication method
- main API use cases
- event export
- custom integrations
- webhooks
- SDKs or libraries if available
- rate limits if publicly documented
- limitations

Use a table:

| API / extensibility feature | Purpose | Authentication | Common use | Notes |
|---|---|---|---|---|

---

## 15. Identity, Access Control, and Administration

Include:

- SSO support
- SAML/OIDC support if applicable
- MFA support
- RBAC
- admin roles
- tenant model
- audit logging
- service accounts/API keys
- least-privilege considerations

---

## 16. Data Security, Privacy, and Compliance

Include public information on:

- data storage
- data residency
- encryption in transit
- encryption at rest
- customer data handling
- retention
- compliance certifications
- audit reports, if public
- privacy considerations

If details are not public, state that clearly.

---

## 17. Operational Considerations

Explain what it takes to run the product well.

Include:

- day-to-day administration
- onboarding new data sources
- tuning detections
- handling false positives
- user and role management
- alert routing
- change management
- runbooks
- reporting
- monitoring product health
- maintaining integrations
- operational ownership

---

## 18. Scalability, Availability, and Resilience

Include where publicly available:

- scaling model
- ingestion limits
- event volume considerations
- collector sizing
- availability model
- failover
- disaster recovery
- retention options
- performance considerations

For SaaS products, avoid inventing backend details that are not public.

---

## 19. Licensing and Commercial Model

Include high-level public licensing information only.

Do not invent pricing.

Cover:

- licensing metric, if public
- editions/packages
- add-ons
- consumption drivers
- cost-risk areas
- renewal considerations
- procurement questions

State clearly where pricing or packaging is not publicly available or varies by contract.

---

## 20. Strengths

Include practical strengths, not marketing claims.

For each strength, explain:

- why it matters
- what evidence supports it
- when the strength is most relevant

---

## 21. Weaknesses and Limitations

Include practical weaknesses and limitations.

For each weakness, explain:

- what the limitation is
- why it matters
- what assumptions or deployment patterns affect it
- how an organisation might mitigate it

Be fair. Do not exaggerate weaknesses without evidence.

---

## 22. Common Pitfalls

Include mistakes customers, engineers, or architects may make.

Examples:

- onboarding too many logs without a detection strategy
- underestimating integration work
- assuming full SOAR capability when only basic automation exists
- failing to tune detections
- poor ownership of incident workflow
- unclear data retention requirements
- misunderstanding licensing drivers

---

## 23. Competitor Comparison

Compare with relevant competitors.

For each competitor, include:

- where the product is stronger
- where the competitor is stronger
- target market difference
- architectural difference
- operational difference

Use a table:

| Competitor | Category | Where this product is stronger | Where competitor may be stronger | Notes |
|---|---|---|---|---|

Do not make unsupported claims. When unsure, qualify the comparison.

---

## 24. Enterprise Architecture Fit

Explain how the product fits into an enterprise security architecture.

Include:

- upstream dependencies
- downstream dependencies
- overlap with existing tooling
- reference architecture placement
- identity integration
- network/logging integration
- cloud integration
- SOC process integration
- governance considerations
- design decisions for architects

---

## 25. Engineer's Implementation View

Explain what an engineer should care about.

Include:

- prerequisites
- deployment tasks
- configuration tasks
- integration tasks
- test plan
- validation steps
- common troubleshooting areas
- operational handover

This section should not become a full implementation manual, but it should identify the engineering work required.

---

## 26. Meeting Preparation Notes

This section should be highly practical.

Include:

- five things to remember
- five strengths to mention
- five weaknesses or caveats to be aware of
- five likely customer questions
- five intelligent questions to ask
- five integration points to discuss
- five competitor comparison points

---

## 27. Interview Preparation Notes

Include likely interview-relevant talking points.

Cover:

- how to explain the product in two minutes
- architecture explanation
- integration explanation
- strengths and weaknesses
- example deployment scenario
- example incident response workflow
- comparison with alternatives
- likely interview questions and model answer outlines

---

## 28. Questions to Ask Customers, Vendors, or Interviewers

Include questions grouped by theme.

Suggested themes:

- business objective
- security operations
- architecture
- integrations
- data sources
- identity and access
- detection engineering
- incident response
- automation
- compliance
- licensing
- operational ownership
- success criteria

---

## 29. Common Misconceptions

Identify statements that are often misunderstood.

Examples:

- confusing SIEM with SOAR
- assuming XDR replaces SIEM
- assuming vendor-native integrations are always bidirectional
- assuming SaaS means no operational overhead
- assuming detection content works without tuning

---

## 30. Recent Changes and Public Roadmap

Include recent public changes, product renaming, packaging updates, or roadmap information.

Use absolute dates and cite sources.

Do not speculate beyond public information.

---

## 31. Key Takeaways

Conclude with a concise summary.

Include:

- what the product is best at
- where it fits
- main caveats
- best meeting/interview memory anchors

---

## 32. References and Source Register

List references grouped by type.

Suggested grouping:

- official product documentation
- integration documentation
- API documentation
- release notes
- security/trust documentation
- independent analysis
- competitor sources
- community/practitioner sources

Each source should include:

- title
- publisher
- URL if available
- access/research date
- what it was used for

---

## 33. Confidence Assessment

End with a confidence assessment.

Include:

- overall confidence: High / Medium / Low
- strongest evidence areas
- weakest evidence areas
- unresolved questions
- information likely to change
- suggested refresh triggers

Refresh triggers may include:

- product rebranding
- new licensing model
- major acquisition
- major feature launch
- new integration framework
- changes to API documentation
- major competitor release
- major security incident
