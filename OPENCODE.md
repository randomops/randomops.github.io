# OpenCode Guidelines (OPENCODE.md)

> Universal instructions for **OpenCode** interpreter and agent platform.  
> Cross-referenced with the master [AGENTS.md](file:///Users/robertusnegoro/workingdir/repo/AGENTS.md).

---

## 1. OpenCode Core Directives

1. **TDD by Default**: Write failing unit/integration tests before writing implementation code. Use vertical slices.
2. **Taste Skill Anti-Slop**: Follow tasteskill.dev guidelines for all frontend, CSS, Tailwind, and React work.
3. **Matt Pocock Workflows**: Grill-Me design tree alignment, autonomous fact finding, deep modules.
4. **Execution & Verification**: Verify exit codes of all shell executions. Run test suites to prove success.

---

## 2. Stack Commands

- **Go**: `go test -v ./...`
- **Python**: `pytest`
- **Next.js / React / TypeScript**: `npm test` & `npm run build`
- **Android / Kotlin**: `./gradlew test`
- **Swift / macOS**: `swift test`
- **Ruby / Jekyll**: `bundle exec jekyll build`
