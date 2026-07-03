# 06 - Final Generation Prompt

Use this prompt to generate a final cybersecurity product knowledge report after completing research or producing an evidence pack.

Replace the placeholders before use.

---

## Prompt

You are to create a cybersecurity product knowledge report using the attached or provided prompt kit documents:

- `01_Master_System_Prompt.md`
- `02_Documentation_Standard.md`
- `03_Research_Specification.md`
- `04_Style_Guide.md`
- `05_Quality_Checklist.md`

You must follow those standards strictly.

## Product to document

```text
Product: {{PRODUCT_NAME}}
Vendor: {{VENDOR_NAME}}
Research date: {{RESEARCH_DATE}}
Report version: 1.0
Audience: Experienced cybersecurity architect/engineer
Purpose: Personal ten-minute refresher plus full architect/engineer reference
Output format: {{OUTPUT_FORMAT}}
Special focus areas: {{SPECIAL_FOCUS_AREAS}}
Known context or notes: {{KNOWN_CONTEXT}}
```

## Source material

Use the following evidence pack if provided:

```text
{{EVIDENCE_PACK}}
```

If an evidence pack is not provided and research tools are available, perform Pro-level research first. Use multiple source types and do not rely solely on vendor claims. If research tools are not available, state clearly that the report is based only on provided material and internal knowledge, and mark confidence accordingly.

## Required behaviour

Generate a complete product knowledge report that satisfies all of the following:

1. The report must be useful as a ten-minute refresher before meetings, interviews, workshops, or vendor discussions.
2. The report must also be a longer-term architect/engineer reference.
3. The report must explain what cyber problems the product solves.
4. The report must explain product positioning and categories, such as SIEM, SOAR, XDR, EDR, ASM, VM, IAM, PAM, DLP, SASE, CNAPP, or other relevant categories.
5. The report must explain where the product fits in enterprise security architecture.
6. The report must include architecture, components, data flow, deployment model, data sources, detection/analytics, incident workflow, automation, APIs, identity/RBAC, operations, resilience, and licensing overview where information is publicly available.
7. The integration section must be detailed and workflow-oriented.
8. For integrations such as Jira, ServiceNow, PagerDuty, Microsoft Sentinel, Splunk, Microsoft Defender, CrowdStrike, Okta, Entra ID, AWS, Azure, GCP, Palo Alto, Cisco, and similar tools, explain practical use cases where relevant and supported by evidence.
9. Do not assume bidirectional integration, workflow depth, or automation depth unless evidence supports it.
10. Include strengths, weaknesses, common pitfalls, competitor comparison, meeting preparation notes, interview preparation notes, questions to ask, misconceptions, recent changes, key takeaways, references, and confidence assessment.
11. Use British English.
12. Use Markdown headings and tables.
13. Do not write marketing language.
14. Do not invent missing information.
15. Where information is unavailable, write: `Information not publicly available.`
16. Clearly distinguish vendor claims from verified facts and architectural analysis where useful.
17. Include references and citations where possible.
18. Use absolute dates.

## Required report structure

Use the exact section order from `02_Documentation_Standard.md`:

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

## Quality self-check

Before finalising, silently apply the quality checklist from `05_Quality_Checklist.md`.

Then include a short final section named `Quality Notes` with:

- strongest sections
- weakest sections
- information that should be refreshed later
- any important caveats

## Output instruction

Produce the final report now.

If file generation is available and `{{OUTPUT_FORMAT}}` requests PDF, create a PDF file and provide a download link. Otherwise, produce the report in clean Markdown.
