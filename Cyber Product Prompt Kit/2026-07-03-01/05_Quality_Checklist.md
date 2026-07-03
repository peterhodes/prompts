# 05 - Quality Checklist

Use this checklist before accepting any cybersecurity product knowledge report.

The checklist is designed to catch the most common weaknesses in LLM-generated product reports: shallow summaries, vendor-claim leakage, missing integrations, unsupported architecture claims, weak competitor comparisons, and lack of meeting/interview usefulness.

---

## 1. Purpose and audience

| Check | Pass? | Notes |
|---|---:|---|
| The report is written for an experienced cybersecurity architect/engineer. |  |  |
| The report works as a ten-minute refresher. |  |  |
| The report works as a longer-term reference. |  |  |
| The report does not become a vendor manual. |  |  |
| The report is practical for meetings and interviews. |  |  |

---

## 2. Structure

| Check | Pass? | Notes |
|---|---:|---|
| All required sections from the documentation standard are present. |  |  |
| The report begins with document control metadata. |  |  |
| The ten-minute refresher is near the front. |  |  |
| Product positioning and categories are explicit. |  |  |
| Integrations have a dedicated, detailed section. |  |  |
| Meeting and interview sections are included. |  |  |
| References and confidence assessment are included. |  |  |

---

## 3. Research and sourcing

| Check | Pass? | Notes |
|---|---:|---|
| Official documentation was used for product facts. |  |  |
| Vendor claims are not treated as independent evidence. |  |  |
| Independent or non-vendor sources were used where available. |  |  |
| API and integration claims are sourced where possible. |  |  |
| Licensing claims are sourced or caveated. |  |  |
| Recent changes use absolute dates. |  |  |
| Unsupported claims are removed, labelled, or caveated. |  |  |
| Source register is included. |  |  |

---

## 4. Product positioning

| Check | Pass? | Notes |
|---|---:|---|
| The product's primary category is clear. |  |  |
| Secondary categories are explained. |  |  |
| Ambiguous or vendor-driven category labels are challenged. |  |  |
| The report explains whether the product replaces or complements other tools. |  |  |
| Typical customers and buyers are identified. |  |  |
| Cases where the product is a poor fit are included. |  |  |

---

## 5. Architecture and engineering value

| Check | Pass? | Notes |
|---|---:|---|
| Deployment model is explained. |  |  |
| Major components are identified. |  |  |
| Data flow is described. |  |  |
| Data sources are listed and explained. |  |  |
| Identity and access control are covered. |  |  |
| Operational ownership is discussed. |  |  |
| Availability, resilience, and scalability are covered where public information exists. |  |  |
| Unknown technical details are marked as not publicly available. |  |  |

---

## 6. Integration quality

| Check | Pass? | Notes |
|---|---:|---|
| Integrations are explained as workflows, not just names. |  |  |
| Jira is covered if relevant. |  |  |
| ServiceNow is covered if relevant. |  |  |
| PagerDuty is covered if relevant. |  |  |
| Identity integrations are covered. |  |  |
| SIEM/security tooling integrations are covered. |  |  |
| Cloud integrations are covered. |  |  |
| API/webhook/custom integration options are covered. |  |  |
| Integration direction is stated where known. |  |  |
| Authentication method is stated where public. |  |  |
| Assumptions about bidirectionality are avoided. |  |  |

---

## 7. Strengths, weaknesses, and pitfalls

| Check | Pass? | Notes |
|---|---:|---|
| Strengths are practical and evidence-aware. |  |  |
| Weaknesses are fair and specific. |  |  |
| Common pitfalls are included. |  |  |
| Mitigations or validation questions are included for major weaknesses. |  |  |
| The report avoids unsupported negative claims. |  |  |

---

## 8. Competitor comparison

| Check | Pass? | Notes |
|---|---:|---|
| Direct competitors are identified. |  |  |
| Adjacent competitors are identified where useful. |  |  |
| Comparison includes strengths and weaknesses. |  |  |
| Comparison accounts for target market and deployment model. |  |  |
| Comparison avoids unsupported winner/loser statements. |  |  |

---

## 9. Meeting and interview usefulness

| Check | Pass? | Notes |
|---|---:|---|
| The report includes a concise meeting preparation section. |  |  |
| The report includes interview preparation notes. |  |  |
| The report includes intelligent questions to ask. |  |  |
| The report includes likely objections or caveats. |  |  |
| The report includes memorable positioning statements. |  |  |

---

## 10. Final acceptance test

Before accepting the report, answer these questions:

1. Can I understand the product in ten minutes?
2. Can I explain it clearly in an interview?
3. Can I discuss its architecture with engineers?
4. Can I challenge vendor claims intelligently?
5. Can I explain its integrations and workflows?
6. Can I compare it with competitors?
7. Can I identify when it is not a good fit?
8. Can I ask better customer/vendor questions after reading it?
9. Would I trust this document six months from now if the research date is visible?
10. Are all weak or uncertain areas clearly marked?

---

## Suggested scoring

Score each area from 1 to 5.

| Area | Score |
|---|---:|
| Refresher usefulness |  |
| Technical accuracy |  |
| Architecture coverage |  |
| Integration coverage |  |
| Vendor-neutral analysis |  |
| Competitor comparison |  |
| Meeting usefulness |  |
| Interview usefulness |  |
| Source quality |  |
| Overall confidence |  |

Suggested threshold:

- **45-50:** Excellent; ready to keep.
- **38-44:** Good; minor improvements needed.
- **30-37:** Usable but requires revision.
- **Below 30:** Regenerate or perform deeper research.
