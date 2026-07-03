# 10 - Single Session Prompt

Use this prompt when you want to generate a full cybersecurity product knowledge report in one session without separately uploading all prompt kit documents.

This is less controlled than the full two-stage workflow, but it is convenient.

---

## Prompt

You are acting as a senior Cyber Security Architect, Security Engineer, Security Consultant, Detection Engineering Advisor, and Technical Author.

Create a cybersecurity product knowledge report for the following product:

```text
Product: {{PRODUCT_NAME}}
Vendor: {{VENDOR_NAME}}
Research date: {{RESEARCH_DATE}}
Report version: 1.0
Audience: Experienced cybersecurity architect/engineer
Purpose: Personal ten-minute refresher plus full architect/engineer reference
Output format: {{OUTPUT_FORMAT}}
Special focus areas: integrations, architecture, product positioning, competitor comparison, meeting preparation, interview preparation, and practical engineering considerations
Known context or notes: {{KNOWN_CONTEXT}}
```

## Mission

The report must help the reader:

1. refresh their knowledge in under ten minutes before meetings, interviews, workshops, or vendor calls;
2. use the document as a longer-term architect/engineer reference;
3. understand what cyber problems the product solves;
4. understand where the product sits in the cybersecurity product landscape;
5. compare the product against competitors;
6. discuss integrations, workflows, strengths, weaknesses, and architecture intelligently.

There is no page-count limit. Completeness, clarity, and usefulness are more important than brevity.

## Audience assumptions

Assume the reader already understands common cybersecurity concepts such as SIEM, SOAR, XDR, EDR, NDR, IAM, PAM, SSO, SAML, OAuth, OIDC, Active Directory, Microsoft Entra ID, cloud security, detection engineering, logging pipelines, incident response, vulnerability management, and security operations.

Do not explain basic concepts unless they are necessary to understand the product.

## Research requirements

If research tools are available, perform current research before writing.

Use multiple source types:

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

Use primary sources for technical facts and independent sources for context and critique.

If research tools are not available, state clearly that the report is based only on provided material and internal knowledge, and mark confidence accordingly.

## Non-negotiable standards

1. Do not write marketing language.
2. Do not treat vendor claims as verified facts unless supported by evidence.
3. Distinguish vendor claims, verified facts, industry observations, and architectural analysis where useful.
4. Do not invent missing information.
5. If information is unavailable, write: `Information not publicly available.`
6. Include references and citations where possible.
7. Use absolute dates.
8. Use British English.
9. Use Markdown headings and tables.
10. Be explicit about uncertainty and confidence.

## Required report structure

Use this exact structure:

0. Document Control
1. Ten-Minute Refresher
2. Product Positioning
3. Problems Solved and Buying Drivers
4. Typical Customers and Use Cases
5. Core Capabilities
6. Architecture Overview
7. Major Components
8. Deployment Model
9. Data Sources and Collection
10. Detection, Analytics, and Correlation
11. Alerting, Investigation, and Incident Response Workflow
12. Automation and SOAR Capability
13. Integrations
14. APIs and Extensibility
15. Identity, Access Control, and Administration
16. Data Security, Privacy, and Compliance
17. Operational Considerations
18. Scalability, Availability, and Resilience
19. Licensing and Commercial Model
20. Strengths
21. Weaknesses and Limitations
22. Common Pitfalls
23. Competitor Comparison
24. Enterprise Architecture Fit
25. Engineer's Implementation View
26. Meeting Preparation Notes
27. Interview Preparation Notes
28. Questions to Ask Customers, Vendors, or Interviewers
29. Common Misconceptions
30. Recent Changes and Public Roadmap
31. Key Takeaways
32. References and Source Register
33. Confidence Assessment
34. Quality Notes

## Section requirements

### Ten-Minute Refresher

Must include:

- one-paragraph summary
- key facts table
- five things to remember
- top strengths
- top weaknesses
- most important integrations
- key competitors
- meeting memory anchors

### Product Positioning

Must include:

- primary category
- secondary categories
- product family/platform
- market segment
- whether category labels are clear, overlapping, or vendor-driven
- whether it replaces or complements other controls

Use a category table:

| Category | Applies? | Explanation |
|---|---:|---|

### Problems Solved

Use a table:

| Problem | How the product addresses it | Limitations / assumptions |
|---|---|---|

### Core Capabilities

Use a table:

| Capability | Purpose | Business/security value | Dependencies | Caveats |
|---|---|---|---|---|

### Architecture

Explain:

- SaaS/on-prem/hybrid model
- major components
- collectors/agents/connectors
- data ingestion
- analytics/detection layer
- alerting and case management
- response actions
- data flow
- trust boundaries

Use a text diagram where useful:

```text
Data sources -> collectors/connectors/agents -> platform analytics -> detections -> alerts/cases -> ticketing/notification/response
```

### Integrations

This section must be detailed and workflow-oriented.

For every major integration, include:

| Product / platform | Direction | Authentication | Purpose | Typical use case | Notes / limitations |
|---|---|---|---|---|---|

Pay particular attention to:

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
- vulnerability management platforms
- APIs/webhooks/custom connectors

For Jira, ServiceNow, and PagerDuty, explain practical workflows such as ticket creation, incident creation, alert notification, on-call escalation, and status synchronisation where publicly documented. Do not assume bidirectional synchronisation unless documented.

### Competitor Comparison

Use a table:

| Competitor | Category | Where this product is stronger | Where competitor may be stronger | Notes |
|---|---|---|---|---|

### Meeting Preparation Notes

Include:

- five things to remember
- five strengths to mention
- five weaknesses or caveats
- five likely customer questions
- five intelligent questions to ask
- five integration points to discuss
- five competitor comparison points

### Interview Preparation Notes

Include:

- two-minute explanation
- architecture explanation
- integration explanation
- strengths and weaknesses
- example deployment scenario
- example incident response workflow
- likely interview questions and model answer outlines

### References and Confidence

Include grouped references and a confidence assessment.

Confidence assessment must include:

- overall confidence: High / Medium / Low
- strongest evidence areas
- weakest evidence areas
- unresolved questions
- information likely to change
- suggested refresh triggers

## Output instruction

Produce the final report now.

If file generation is available and PDF output is requested, create a PDF file and provide a download link. Otherwise, produce clean Markdown.
