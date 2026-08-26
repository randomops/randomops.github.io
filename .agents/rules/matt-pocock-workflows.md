---
trigger: model_decision
description: Engineering workflows, Grill-Me protocol, and domain modeling inspired by Matt Pocock's skills.
---

# Matt Pocock Engineering Workflows & Discipline

## 1. Grill-Me First Protocol
Before starting complex feature work, architectural refactors, or ambiguous plans, conduct an interactive alignment interview:
- **Design Tree & Frontier**: Map high-level requirements into branching technical decisions. The frontier is all unblocked questions.
- **Round-by-Round Q&A**:
  ```markdown
  ❓ **Q1** - **<Question Title>**: <Clear context and decision options>
  ➡️ **Recommendation**: <Specific proposed answer with rationale>
  ```
- **Autonomous Fact-Finding**: Always search and read codebase files first. Never ask the user for facts discoverable via tools.
- **Frontier Completion**: Stop grilling when all dependencies are resolved and the plan is approved.

## 2. Deep Modules & Seams
- Keep module interfaces simple and narrow while hiding implementation depth.
- Establish clean architectural boundaries (seams) for testing and domain isolation.
- Maintain Architecture Decision Records (ADRs) and `CONTEXT.md` glossary where domain concepts evolve.

## 3. Skill Router (`ask-matt`)
- Consult the skill catalog: `tdd`, `grill-me`, `grill-with-docs`, `codebase-design`, `diagnosing-bugs`, `code-review`, `to-spec`, `to-tickets`, `wayfinder`.
