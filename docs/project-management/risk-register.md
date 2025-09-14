<!--
START OF: risk-register.md
Purpose: This document serves as the canonical list of all known and emerging risks identified throughout the project lifecycle. It records analysis, mitigation plans, escalation status, and accountability.
Update Frequency: Updated immediately upon discovery of a new risk or when mitigation plans change. Reviewed bi-weekly during sprint retros or milestone planning.
Location: docs/project-management/risk-register.md
-->

# Risk Register

---

## Archived / Closed Risks

### Risk ID

_Title:_
_Closed On:_ <2025-06-27 Fri>
_Reason:_

---

## Risk Entry

Use this format to log new risks:

### RSK-XXX: [Short Risk Title]

- **Category**: [Technical / Resource / Security / etc.]
- **Description**: [One-liner or short paragraph explaining the risk]
- **Date Identified**: YYYY-MM-DD
- **Likelihood**: [Low / Medium / High]
- **Impact**: [Low / Medium / High / Critical]
- **Owner**: [Name or Role]
- **Status**: [Open / Monitoring / Mitigating / Closed]
- **Mitigation Strategy**:
  [Steps being taken to reduce or avoid this risk]
- **Escalation**: [If escalated, when and to whom]
- **Notes**: [Any helpful comments or context]

<!--
RSK-001: Third-Party API Deprecation
    Category: Technical
    Description: The payment gateway API may deprecate the v1/charges endpoint in Q3.
    Date Identified: <2025-06-27 Fri>
    Likelihood: High
    Impact: High
    Owner: Backend Lead
    Status: Mitigating
    Mitigation Strategy: Abstracted API calls behind internal service layer to swap endpoints easily. Monitoring vendor changelogs weekly.
    Escalation: Not yet
    Notes: Ensure fallback logic is tested in staging.
-->

<!-- END OF: risk-register.md -->
