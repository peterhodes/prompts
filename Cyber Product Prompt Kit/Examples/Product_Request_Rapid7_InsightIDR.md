# Example Product Request - Rapid7 InsightIDR

Use this as an example of how to invoke the prompt kit.

---

## Stage 1 - Evidence pack request

```text
Use the attached prompt kit documents and run the Research Evidence Pack Prompt.

Product: Rapid7 InsightIDR
Vendor: Rapid7
Research date: 3 July 2026
Audience: Experienced cybersecurity architect/engineer
Purpose: Personal ten-minute refresher plus full architect/engineer reference
Output format: Markdown evidence pack
Special focus areas: product positioning, SIEM/SOAR/XDR categorisation, architecture, data sources, Jira integration, ServiceNow integration, PagerDuty integration, APIs, incident workflow, competitor comparison, meeting/interview preparation
Known context or notes: I do not want vendor claims trusted in isolation. Include references where available. Identify naming or packaging caveats, especially if Rapid7 uses newer SecOps or Incident Command terminology alongside InsightIDR.
```

---

## Stage 2 - Final report request

```text
Use the attached prompt kit documents and the evidence pack already produced.

Generate the final product knowledge report.

Product: Rapid7 InsightIDR
Vendor: Rapid7
Research date: 3 July 2026
Report version: 1.0
Audience: Experienced cybersecurity architect/engineer
Purpose: Personal ten-minute refresher plus full architect/engineer reference
Output format: PDF preferred; Markdown acceptable if PDF generation is unavailable
Special focus areas: product positioning, SIEM/SOAR/XDR categorisation, architecture, data sources, Jira integration, ServiceNow integration, PagerDuty integration, APIs, incident workflow, competitor comparison, meeting/interview preparation
Known context or notes: The report must be vendor-neutral and should not trust vendor claims in isolation. Include references where available. Make the ten-minute refresher useful for interviews and customer/vendor meetings.
```

---

## Stage 3 - QA request

```text
Use the QA Review Prompt to audit the generated Rapid7 InsightIDR report.

Focus particularly on:

- whether the report is useful as a ten-minute refresher
- whether it is useful for interview preparation
- whether product positioning is accurate
- whether InsightIDR is correctly categorised
- whether Jira, ServiceNow, and PagerDuty integrations are described as workflows, not just named
- whether vendor claims are clearly separated from verified facts
- whether references are adequate
- whether the document contains overconfident or unsupported claims
```
