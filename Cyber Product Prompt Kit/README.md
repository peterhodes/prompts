# Cybersecurity Product Knowledge Base Prompt Kit

**Version:** 1.0  
**Purpose:** Generate consistent, vendor-neutral cybersecurity product knowledge documents for personal use as a meeting refresher, interview preparation aid, and long-term architect/engineer reference.

This kit is designed for product reports like the Rapid7 InsightIDR document. It assumes the reader is an experienced cybersecurity architect or engineer who wants more than vendor marketing, but does not need a full product administrator manual.

## What this kit produces

Each product report should support two reading modes:

1. **Ten-minute refresher** - a concise briefing suitable before meetings, interviews, workshops, architecture reviews, or vendor conversations.
2. **Full reference** - a deeper cybersecurity architect/engineer view covering positioning, use cases, architecture, integrations, workflows, strengths, weaknesses, competitors, pitfalls, and questions to ask.

There is deliberately **no page-count limit**. The report should be as long as required to be useful, but it must remain structured and readable.

## Recommended workflow

Use this kit as a two-stage process.

### Stage 1 - Research and evidence pack

Use `07_Research_Evidence_Pack_Prompt.md` with Pro-level research enabled. The goal is to collect structured evidence before writing the report.

The output should include:

- source register
- vendor claims
- independently verified facts
- product categories
- architecture evidence
- integration evidence
- competitor evidence
- conflicts or uncertainty
- open questions
- confidence rating

### Stage 2 - Final product document

Use `06_Final_Generation_Prompt.md`, together with:

- `01_Master_System_Prompt.md`
- `02_Documentation_Standard.md`
- `03_Research_Specification.md`
- `04_Style_Guide.md`
- the evidence pack from Stage 1

The final output should be a polished cybersecurity product knowledge document. If the environment supports PDF generation, generate a PDF. Otherwise, output clean Markdown that can be converted to PDF later.

### Stage 3 - Quality review

Use `08_QA_Review_Prompt.md` to audit the report. This should identify weak sourcing, vendor-claim leakage, missing integrations, missing architectural detail, overconfident statements, or areas that need clearer analysis.

### Stage 4 - Future refresh

Use `09_Update_Refresh_Prompt.md` when revisiting an existing product report. This is useful because SaaS products, feature names, integrations, licensing models, and product packaging change frequently.

## File map

| File | Purpose |
|---|---|
| `01_Master_System_Prompt.md` | Defines the LLM role, objective, audience, and non-negotiable behaviour. |
| `02_Documentation_Standard.md` | Defines the exact report structure and section requirements. |
| `03_Research_Specification.md` | Defines how research must be performed, evaluated, and cited. |
| `04_Style_Guide.md` | Defines tone, formatting, terminology, and analytical style. |
| `05_Quality_Checklist.md` | Defines the completion checklist used before accepting a document. |
| `06_Final_Generation_Prompt.md` | Main prompt for generating a final report from a product name and evidence pack. |
| `07_Research_Evidence_Pack_Prompt.md` | Prompt for Pro-level research before writing the final report. |
| `08_QA_Review_Prompt.md` | Prompt for reviewing and improving a generated report. |
| `09_Update_Refresh_Prompt.md` | Prompt for refreshing an existing report when product information changes. |
| `10_Single_Session_Prompt.md` | Self-contained prompt for generating a report in one session when you do not want to upload all separate files. |
| `Templates/Product_Report_Template.md` | Skeleton structure for the final product report. |
| `Templates/Evidence_Pack_Template.md` | Skeleton structure for the research evidence pack. |
| `Templates/Source_Register_Template.md` | Source tracking table. |
| `Examples/Product_Request_Rapid7_InsightIDR.md` | Example invocation for Rapid7 InsightIDR. |

## Minimum product request

When starting a new report, provide at least:

```text
Product: <product name>
Vendor: <vendor name if known>
Research date: <date>
Audience: Experienced cybersecurity architect/engineer; personal refresher and reference
Output: PDF preferred; Markdown acceptable if PDF generation is unavailable
Special focus areas: integrations, architecture, product positioning, competitor comparison, meeting/interview preparation
```

## Standing assumptions

Unless overridden, every product report should assume:

- the audience is a cybersecurity architect/engineer
- British English should be used
- vendor claims must not be trusted in isolation
- citations and references should be included where possible
- product reports can be long
- the document must include a ten-minute refresher and a deeper reference section
- integrations are important and should include workflow-level examples, not just names
- product categories and positioning must be made explicit

## Versioning recommendation

Store this prompt kit and generated reports under version control. Suggested structure:

```text
Cyber Knowledge Base/
├── Prompt Kit/
│   ├── 01_Master_System_Prompt.md
│   ├── 02_Documentation_Standard.md
│   └── ...
├── Evidence Packs/
│   ├── Rapid7 InsightIDR Evidence Pack.md
│   └── ...
└── Product Reports/
    ├── Rapid7 InsightIDR.pdf
    ├── Microsoft Sentinel.pdf
    └── ...
```

## Important principle

The final report should not sound like a vendor brochure. It should read like the working notes of a careful cybersecurity architect: practical, sceptical, structured, evidence-aware, and useful before real conversations.
