# 08 - QA Review Prompt

Use this prompt to review a generated cybersecurity product knowledge report before accepting it into the knowledge base.

---

## Prompt

You are acting as a senior cybersecurity architect and critical reviewer.

Review the following cybersecurity product knowledge report against the attached prompt kit standards:

- `01_Master_System_Prompt.md`
- `02_Documentation_Standard.md`
- `03_Research_Specification.md`
- `04_Style_Guide.md`
- `05_Quality_Checklist.md`

Your task is to find weaknesses, omissions, unsupported claims, vendor-claim leakage, structural issues, integration gaps, and areas where the report is not useful enough for meeting or interview preparation.

## Report to review

```text
{{REPORT_TEXT_OR_FILE}}
```

## Review requirements

Assess the report in the following areas.

### 1. Structural completeness

Check whether all required sections are present and in the correct order.

### 2. Ten-minute refresher quality

Assess whether the refresher is genuinely useful before a meeting or interview.

### 3. Product positioning accuracy

Check whether categories are clear and justified. Look for overclaiming, such as calling a product full SOAR, XDR, CNAPP, or SIEM without sufficient evidence.

### 4. Vendor-neutrality

Identify any vendor marketing language or claims that have been repeated as fact.

### 5. Research and citation quality

Identify unsupported factual claims, missing citations, weak sources, old sources, or contradictory information.

### 6. Architecture quality

Assess whether deployment model, components, data flow, trust boundaries, and operational dependencies are explained clearly.

### 7. Integration depth

This is critical.

Check whether integrations are described as practical workflows rather than simple product lists.

Pay special attention to:

- Jira
- ServiceNow
- PagerDuty
- identity providers
- SIEMs
- EDR/XDR products
- cloud platforms
- APIs
- webhooks

Flag any unsupported assumptions about bidirectional sync, automation depth, or ticket lifecycle management.

### 8. Strengths and weaknesses

Assess whether strengths and weaknesses are practical, fair, and evidence-aware.

### 9. Competitor comparison

Check whether competitors are relevant and the comparison is balanced.

### 10. Meeting and interview usefulness

Assess whether the report would help the reader prepare for:

- interviews
- customer meetings
- architecture reviews
- vendor discussions
- SOC design discussions

### 11. Missing architect/engineer considerations

Identify missing points that an architect or engineer would care about.

### 12. Confidence and caveats

Check whether uncertainty is clearly marked and whether the confidence rating is justified.

## Output format

Produce the review in this structure:

### Overall assessment

Include:

- overall score out of 50
- acceptance recommendation: Accept / Accept with minor changes / Revise / Regenerate
- one-paragraph summary

### Major issues

List the most important issues.

### Minor issues

List smaller improvements.

### Unsupported or overconfident claims

Use a table:

| Claim | Issue | Recommended fix |
|---|---|---|

### Missing sections or weak sections

Use a table:

| Section | Issue | Recommended improvement |
|---|---|---|

### Integration review

Use a table:

| Integration area | Quality | Missing detail | Recommended improvement |
|---|---|---|---|

### Competitor review

Assess relevance and balance.

### Meeting/interview usefulness review

Identify what would make the document more useful before a real meeting or interview.

### Recommended edits

Provide specific edits or replacement text for the most important sections.

### Final checklist

Summarise pass/fail against the quality checklist.
