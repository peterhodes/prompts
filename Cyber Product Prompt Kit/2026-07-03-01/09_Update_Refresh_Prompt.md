# 09 - Update and Refresh Prompt

Use this prompt when refreshing an existing product report.

This is important because cybersecurity products change frequently: names, packaging, integrations, APIs, licensing, and positioning can all shift.

---

## Prompt

You are refreshing an existing cybersecurity product knowledge report.

Use the prompt kit standards:

- `01_Master_System_Prompt.md`
- `02_Documentation_Standard.md`
- `03_Research_Specification.md`
- `04_Style_Guide.md`
- `05_Quality_Checklist.md`

## Existing report

```text
{{EXISTING_REPORT_TEXT_OR_FILE}}
```

## Product

```text
Product: {{PRODUCT_NAME}}
Vendor: {{VENDOR_NAME}}
Original report date: {{ORIGINAL_REPORT_DATE}}
Refresh date: {{REFRESH_DATE}}
Special focus areas: {{SPECIAL_FOCUS_AREAS}}
```

## Refresh requirements

Perform current research and identify changes since the original report date.

Focus especially on:

- product naming
- product packaging
- acquisitions or platform consolidation
- category positioning
- new capabilities
- deprecated capabilities
- integration changes
- API changes
- licensing changes
- deployment model changes
- security/trust/compliance changes
- competitor changes
- public roadmap or release-note changes

Use absolute dates.

Do not rewrite unchanged sections unnecessarily. Identify what changed and why it matters.

## Output structure

### 1. Refresh summary

Include:

- refresh date
- original report date
- overall change level: Low / Medium / High
- most important changes
- whether the report requires minor update, major update, or full regeneration

### 2. Change log

Use a table:

| Area | Previous report position | Current evidence | Change | Impact |
|---|---|---|---|---|

### 3. Source register for refresh

Use a table:

| Source | Publisher | Type | URL | Date accessed | Used for | Reliability |
|---|---|---|---|---|---|---|

### 4. Sections requiring update

Use a table:

| Section | Update required? | Reason | Priority |
|---|---:|---|---|

### 5. Replacement text

Provide replacement text for changed sections.

### 6. New caveats

Identify any caveats that should be added to the report.

### 7. Updated confidence assessment

Include:

- updated confidence rating
- strongest evidence areas
- weakest evidence areas
- next refresh triggers

## Output instruction

Produce the refresh assessment first. If the changes are substantial, then produce an updated version of the full report using the current documentation standard.
