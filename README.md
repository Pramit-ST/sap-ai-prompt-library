# SAP AI Prompt Library 🤖

> Production-ready AI prompts for SAP BTP, 
> HANA, and CAP development workflows.

---

## What Is This?

A structured collection of prompts designed 
specifically for SAP consultants and developers 
who use AI tools (ChatGPT, Claude, Copilot) 
in their daily SAP work.

These are not generic prompts.
Every prompt is built for real SAP scenarios —
tested against actual SAP HANA, CAPM, and 
BTP development workflows.

---

## Who Is This For?

| Role | How You Use This |
|------|-----------------|
| SAP BTP Consultant | Code review, design decisions, tech specs |
| HANA Developer | CDS view review, query optimisation |
| CAP Developer | Service review, OData design |
| Tech Lead | Reviewing junior code, writing standards |
| Project Manager | Generating documentation, status reports |

---

## How To Use This Library
Step 1 — Find the prompt relevant to your task
Step 2 — Open the .md file
Step 3 — Copy the prompt
Step 4 — Paste into your AI tool
(ChatGPT / Claude / Copilot)
Step 5 — Replace placeholder text with your content
Step 6 — Get structured, SAP-specific output

### Pro Tip
For best results, always start with the 
System Prompt first:
`system-prompts/sap-btp-architect.md`
Paste it as your System or Custom Instruction,
then use any prompt from this library.

---

## Library Contents

### 🔧 System Prompts
Foundation prompts that define AI behaviour
for SAP contexts.

| File | Purpose |
|------|---------|
| [SAP BTP Architect](system-prompts/sap-btp-architect.md) | Core system prompt for all SAP AI work |

---

### 🔍 Code Review
Prompts for reviewing SAP code across 
different layers.

| File | Purpose |
|------|---------|
| [CDS View Review](code-review/cds-view-review.md) | Review HANA CDS views for performance, security, CAPM compatibility |
| [CAPM Service Review](code-review/capm-service-review.md) | Review CAP service files for best practices |

---

### 🏗️ Design
Prompt chains for designing SAP data models
and integration flows.

| File | Purpose |
|------|---------|
| [Data Model Design Chain](design/data-model-design-chain.md) | Step-by-step AI-assisted data model design |
| [Integration Design Chain](design/integration-design-chain.md) | Design BTP integration flows with AI |

---

### 📄 Documentation
Prompts for generating SAP technical documentation.

| File | Purpose |
|------|---------|
| [Tech Spec Generator](documentation/tech-spec-generator.md) | Generate technical specs from requirements |

---

## Prompt Quality Standard

Every prompt in this library follows 
the 5-element framework:
✅ ROLE        — AI is given a specific SAP expert persona
✅ CONTEXT     — SAP environment and constraints defined
✅ TASK        — Single, clear objective
✅ FORMAT      — Output structure specified
✅ CONSTRAINTS — Guardrails to keep output focused

---

## Contributing

Found a gap? Have a prompt that works well 
for your SAP work?

1. Fork this repository
2. Add your prompt following the same structure
3. Submit a pull request

All contributions welcome.

---

## About

Built by an SAP BTP/HANA consultant with 8 years 
of enterprise experience, learning and applying 
Gen AI to real SAP project scenarios.

---

## License
MIT — Free to use, share, and adapt.