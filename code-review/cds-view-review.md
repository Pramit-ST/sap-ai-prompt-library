# Prompt — CDS View Review (HANA On-Premise)

## Purpose
Use this prompt to get a structured AI review 
of any CDS view in SAP HANA On-Premise.
Designed for views consumed by CAPM services
in mixed teams (senior + junior developers).

---

## When To Use This
- Before submitting a CDS view for peer review
- When a junior developer needs feedback
- When you suspect performance issues
- Before exposing a view via a CAPM service

---

## Pre-Requisite
Use together with:
system-prompts/sap-btp-architect.md
Paste that as your SYSTEM PROMPT first,
then use the prompt below as your USER PROMPT.

---

## The Prompt

You are reviewing a SAP HANA On-Premise CDS view
that is consumed by a CAPM service.

Context:
- Environment: SAP HANA On-Premise
- Consumed by: CAPM OData service
- Team: Mixed (senior + junior developers)
- Goal: Production-ready, performant, maintainable code

[PASTE YOUR CDS VIEW HERE]

Task:
Review this CDS view across these 4 areas only:

1. Performance
   - Filter pushdown opportunities
   - Unnecessary joins or associations
   - Missing or incorrect indexes

2. CAPM Compatibility
   - Correct annotations for CAPM consumption
   - Association definitions suitable for OData
   - Naming conventions aligned with CAPM standards

3. Security
   - DCL (Data Control Language) in place
   - No unnecessary exposure of sensitive fields
   - Access control annotations present

4. Maintainability
   - Clarity of view for junior developers
   - Comments where logic is complex
   - Consistent naming conventions

Constraints:
- Limit to TOP 5 issues maximum
- Prioritise by severity: High → Medium → Low
- Skip cosmetic issues unless they affect readability
- If the view is well written, say so clearly

Format:
Return a table with these exact columns:
| Area | Issue | Severity | Recommendation |

Followed by:
- One paragraph: Overall assessment
- One line: The single most critical thing to fix first

---

## Example Output Structure

| Area | Issue | Severity | Recommendation |
|------|-------|----------|----------------|
| Performance | No filter pushdown on CompanyCode | High | Add WHERE clause push... |
| Security | No DCL assigned | High | Create and assign DCL... |
| CAPM | Association not OData compatible | Medium | Change to managed assoc... |

Overall Assessment:
This view has solid structure but two critical gaps
in security and performance that must be addressed
before CAPM service exposure.

Most Critical Fix:
Assign a DCL before exposing via OData.

---

## Prompt Variations

### For Quick Review (Senior Dev)
Add this line to constraints:
"Assume senior developer audience.
Skip basic explanations."

### For Learning Review (Junior Dev)
Add this line to constraints:
"Explain each issue in simple terms.
Include a code example for each fix."

### For Performance-Only Review
Replace Task section with:
"Focus ONLY on performance optimisation.
Ignore security and style."