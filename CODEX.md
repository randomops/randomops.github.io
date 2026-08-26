# OpenAI Codex Guidelines (CODEX.md)

> Universal instructions for **OpenAI Codex** working in this workspace.  
> Cross-referenced with the master [AGENTS.md](file:///Users/robertusnegoro/workingdir/repo/AGENTS.md).

---

## 1. Codex Development Standards

1. **Test-Driven Development (TDD)**:
   - Always agree on public seams first.
   - Write failing tests (Red) verifying behavior.
   - Write minimal implementation to pass (Green).
   - Refactor after green.
   - Work in vertical slices (Tracer Bullets).

2. **Taste Skill Framework**:
   - Enforce anti-slop rules on all HTML/CSS/React/Next.js files.
   - Output a one-line Design Read.
   - Set Three Dials: `DESIGN_VARIANCE`, `MOTION_INTENSITY`, `VISUAL_DENSITY`.
   - Ensure WCAG AA button/form contrast and hero viewport stability (`min-h-[100dvh]`).

3. **Matt Pocock Engineering Discipline**:
   - Conduct Grill-Me alignment interviews before big tasks.
   - Read codebase files first; do not ask users for discoverable facts.
   - Design deep modules with narrow public interfaces.

4. **Skill & Rule Discovery**:
   - Codex reads skills from `.agents/skills/` and rules from `.agents/rules/`.
