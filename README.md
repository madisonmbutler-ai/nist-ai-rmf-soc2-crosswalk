# NIST AI RMF ↔ SOC 2 Crosswalk

A mapping of all 72 NIST AI Risk Management Framework (AI RMF 1.0) subcategories to the AICPA SOC 2 Trust Services Criteria. For each AI RMF outcome it shows which SOC 2 criteria already cover it, how strong that coverage is, and which AI-specific control closes the gap.

**Who this is for:** security, compliance and GRC teams that already run a SOC 2 program and need to add AI governance without starting from scratch.

## Why this exists

Most companies adopting AI already have SOC 2 controls for risk assessment, vendor management, change management and incident response. Many AI governance requirements can be met by extending those controls instead of building a separate program. This crosswalk shows where that works, and where it doesn't.

## Summary

| AI RMF function | Strong | Partial | Gap | Total |
|---|---:|---:|---:|---:|
| Govern | 4 | 13 | 2 | 19 |
| Map | 1 | 11 | 6 | 18 |
| Measure | 4 | 11 | 7 | 22 |
| Manage | 3 | 9 | 1 | 13 |
| **Total** | **12** | **44** | **16** | **72** |

**What the numbers say:**

- **78% of AI RMF outcomes (56 of 72) have a SOC 2 starting point.** Most need AI-specific additions, but the control owner, process and evidence trail already exist.
- **Security, incident response and risk treatment carry over well.** For example, MEASURE 2.7 (security and resilience) maps directly to the CC6 and CC7 criteria.
- **The real gaps are AI-native.** Fairness and bias (MEASURE 2.11), explainability (MEASURE 2.9), environmental impact (MEASURE 2.12), human oversight (GOVERN 3.2, MAP 3.5) and model documentation (MAP 2.1, 2.2) have no SOC 2 equivalent and need new controls.
- **The Map function is weakest.** SOC 2 describes the service; it doesn't ask what an AI system is for, what its limits are, or who could be affected.

## Coverage ratings

| Rating | Meaning |
|---|---|
| **Strong** | An existing SOC 2 control can be extended to AI scope with little change. |
| **Partial** | A SOC 2 control addresses part of the outcome; AI-specific procedures or evidence must be added. |
| **Gap** | No meaningful SOC 2 equivalent; a new control is needed. |

## Files

- [`crosswalk.csv`](crosswalk.csv): the full mapping. GitHub displays it as a searchable table.

| Column | Contents |
|---|---|
| `nist_ai_rmf_id` | AI RMF subcategory (for example GOVERN 1.6) |
| `function` | Govern, Map, Measure or Manage |
| `outcome_summary` | A condensed summary of the subcategory's outcome |
| `soc2_criteria` | Related SOC 2 criteria (CC = Common Criteria; A = Availability; C = Confidentiality; PI = Processing Integrity; P = Privacy) |
| `coverage` | Strong, Partial or Gap |
| `rationale` | Why the rating was given |
| `ai_control_to_add` | The AI-specific control or evidence that closes the gap |

## How to use it

1. **Scope:** start with the Gap rows. These are the new controls your AI governance program must build.
2. **Extend:** for Partial rows, add AI scope to the existing control owner's procedures and evidence requests.
3. **Reuse:** for Strong rows, confirm the existing control's scope includes AI systems and collect evidence once for both frameworks.

## Method and limitations

- Mapped against NIST AI RMF 1.0 (January 2023) and the 2017 Trust Services Criteria (revised points of focus, 2022).
- Outcome summaries are condensed for readability. See the [official NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework) for full text. SOC 2 criteria are referenced by ID only; the criteria text is published by the AICPA.
- Mappings reflect professional judgment and assume a typical SOC 2 Security scope. Privacy-related ratings assume the Privacy category is in scope.
- This is an independent reference, not audit or legal advice, and is not endorsed by NIST or the AICPA.

## Roadmap

- [ ] Add ISO/IEC 42001 Annex A control references
- [ ] Add EU AI Act article references for high-risk system obligations
- [ ] Add example evidence for each AI control

## Author

**Madison Butler**: AI governance and compliance (ISO/IEC 42001, NIST AI RMF, SOC 2, HIPAA).
[LinkedIn](https://www.linkedin.com/in/madison-butler-005145134)

Feedback and suggested mapping changes are welcome. Open an issue.
