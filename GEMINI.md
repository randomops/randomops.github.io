# Google Antigravity / Gemini CLI Guidelines (GEMINI.md)

> Universal instructions for **Google Antigravity (AGY / Gemini CLI)** working in this workspace.  
> Cross-referenced with the master [AGENTS.md](file:///Users/robertusnegoro/workingdir/repo/AGENTS.md).

---

## 1. Operating Rules for Antigravity

1. **Mandatory TDD**: Follow the Red-Green-Refactor loop on every code change. Run project test suites to verify failures before writing implementation code.
2. **Matt Pocock Engineering Process**: Execute the Grill-Me protocol for complex requirements. Keep modules deep with clear public seams.
3. **Taste Skill (Anti-Slop)**: Always output a one-line Design Read for UI changes. Calibrate the Three Dials (`DESIGN_VARIANCE`, `MOTION_INTENSITY`, `VISUAL_DENSITY`).
4. **Tool Discipline**:
   - Use `view_file` to inspect code before modifying.
   - Use `replace_file_content` for surgical edits.
   - Use `write_to_file` only for new files.
5. **Artifacts**: Store architecture plans, comprehensive reports, and multi-step execution plans in `<appDataDir>/brain/<conversation-id>`.

---

## 2. Customizations & Skills Location

- **Workspace Skills**: `.agents/skills/` (includes all Taste Skill and Matt Pocock skills).
- **Workspace Rules**: `.agents/rules/` (`tdd-mandate.md`, `taste-skill-frontend.md`, `matt-pocock-workflows.md`).
- **Global Skills**: `~/.gemini/config/skills/`.

---

## 3. Monorepo Verification Matrix

Before completing any task, execute the respective test runner:
- **Go**: `go test -v ./...`
- **Python**: `pytest`
- **Node/TS/React**: `npm test` && `npm run build`
- **Android**: `./gradlew test`
- **macOS/Swift**: `swift test`
- **Ruby/Jekyll**: `bundle exec jekyll build`
