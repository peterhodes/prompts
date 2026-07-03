# 04 - Style Guide

This style guide defines how cybersecurity product knowledge reports should be written.

---

## Voice and tone

Write as a careful cybersecurity architect.

The tone should be:

- professional
- analytical
- practical
- vendor-neutral
- technically literate
- sceptical where appropriate
- concise but not superficial

Avoid:

- marketing language
- hype
- unnecessary adjectives
- unsupported superlatives
- sales-style claims
- vague phrases such as "seamless", "powerful", or "next-generation" unless quoted as vendor positioning

---

## Language

Use British English.

Examples:

- organisation, not organization
- centralised, not centralized
- prioritise, not prioritize
- licence as noun, license as verb only where grammatically appropriate

Use clear technical English. Do not over-explain basic cybersecurity terms for an expert reader.

---

## Analytical labels

Use explicit labels where helpful.

Examples:

```text
Vendor claim:
Public documentation confirms:
Independent evidence:
Architectural analysis:
Operational implication:
Caveat:
```

This helps prevent vendor claims from being accidentally treated as verified facts.

---

## Formatting

Use Markdown.

Required formatting practices:

- numbered main headings
- clear subheadings
- concise paragraphs
- tables for comparison and integrations
- bullet lists for meeting refreshers
- code blocks only for simple workflows or diagrams
- no decorative formatting that reduces readability

---

## Section style

Each major section should start with a short summary paragraph before deeper detail.

For long sections, use tables and subheadings.

The reader should be able to skim and still understand the main points.

---

## Ten-minute refresher style

The refresher should be direct and memorable.

Use:

- short bullets
- compact tables
- high-signal points
- minimal caveats unless they are critical

Do not turn the refresher into a mini version of the full report.

---

## Full reference style

The reference sections can be detailed, but they should not become a vendor manual.

Focus on:

- architecture
- positioning
- use cases
- design considerations
- operational considerations
- integrations
- trade-offs
- comparison
- meeting/interview usefulness

Avoid:

- step-by-step UI instructions unless essential
- exhaustive feature lists with no analysis
- unsupported implementation detail

---

## Tables

Use tables for:

- key facts
- capabilities
- integrations
- data sources
- competitors
- strengths and weaknesses
- questions to ask
- source register

Keep table entries concise but meaningful.

Do not hide important caveats inside overly compressed tables; add narrative explanation where needed.

---

## Integration writing standard

Integration sections must be workflow-oriented.

Weak wording:

```text
Integrates with Jira and PagerDuty.
```

Better wording:

```text
Jira integration is typically used to create or update issues from security alerts or incidents. Confirm whether the integration supports one-way issue creation, bidirectional status synchronisation, custom field mapping, and closure workflow before assuming it can support end-to-end SOC case management.
```

For each integration, aim to answer:

- What triggers the integration?
- What data moves?
- Which direction does it move?
- How is authentication handled?
- What operational workflow does it support?
- What are the likely caveats?

---

## Competitor writing standard

Competitor comparisons must be balanced.

Avoid:

- declaring a winner without context
- unsupported claims
- repeating vendor positioning

Use qualified language:

- `typically stronger where...`
- `often selected when...`
- `may be less suitable where...`
- `public information suggests...`
- `this depends on licensing, existing estate, and operational maturity`

---

## Strengths and weaknesses

Strengths and weaknesses must be practical.

Poor strength:

```text
Excellent product.
```

Better strength:

```text
Strong fit for organisations that want a SaaS-led detection and response platform with prebuilt integrations and lower infrastructure overhead than traditional self-managed SIEM deployments.
```

Poor weakness:

```text
Bad automation.
```

Better weakness:

```text
Automation may be limited compared with dedicated SOAR platforms, so organisations with mature playbook orchestration requirements should validate workflow depth before assuming replacement of an existing SOAR tool.
```

---

## Handling uncertainty

Use clear uncertainty markers:

- `Information not publicly available.`
- `Public documentation is limited.`
- `This appears to be...`
- `This should be validated with the vendor.`
- `Confidence: Medium because...`

Do not create false certainty.

---

## Product categories

Be precise with categories.

Products may span categories. Do not force a product into a single label if the market positioning is more nuanced.

Use categories such as:

- SIEM
- SOAR
- XDR
- EDR
- NDR
- MDR
- VM
- ASM
- CNAPP
- CSPM
- CWPP
- CIEM
- IAM
- PAM
- IGA
- DLP
- CASB
- SASE
- SSE
- ZTNA
- Email Security
- Web Security
- Threat Intelligence Platform
- Security Data Lake
- Exposure Management
- Incident Response Platform

For each category, state whether it applies fully, partially, indirectly, or not at all.

---

## Meeting/interview style

Meeting and interview sections should be practical, not academic.

Use prompts such as:

- `A good way to explain it is...`
- `A useful question to ask is...`
- `Be careful not to assume...`
- `A likely challenge is...`
- `The key architectural dependency is...`

---

## References style

Group references by type:

- official documentation
- integration documentation
- API documentation
- release notes
- security/trust documentation
- independent analysis
- competitor sources
- community/practitioner sources

For each source, include what it was used for.

Example:

| Source | Type | Used for | Date accessed |
|---|---|---|---|
| Vendor API documentation | Official API docs | API capability and authentication model | 3 July 2026 |

---

## Final writing test

Before accepting a report, ask:

1. Would this help before a meeting?
2. Would this help in an interview?
3. Would this help an architect understand fit and trade-offs?
4. Would this help an engineer understand implementation considerations?
5. Does it avoid sounding like a vendor brochure?
6. Are unsupported claims removed or labelled?
7. Are integrations explained as workflows rather than names?
