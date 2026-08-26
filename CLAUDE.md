# Claude Code Guidelines (CLAUDE.md)

> Universal instructions for **Anthropic Claude Code** working in this workspace.  
> Cross-referenced with the master [AGENTS.md](file:///Users/robertusnegoro/workingdir/repo/AGENTS.md).

---

## 1. Quick Start & Core Directives

1. **Test-Driven Development (TDD) Mandatory**: Always write failing tests first at agreed public seams before writing implementation code.
2. **Matt Pocock Engineering Process**: Use `/grill-me` or the Grill-Me protocol before building complex features. Explore code autonomously before asking questions.
3. **Taste Skill Anti-Slop Frontend**: Output a one-line Design Read, calibrate the Three Dials (`DESIGN_VARIANCE`, `MOTION_INTENSITY`, `VISUAL_DENSITY`), and eliminate generic AI design tropes.
4. **Full Output Enforcement**: Never output placeholders or truncated comments.

---

## 2. Recommended Slash Commands & Workflows

- `/ask-matt`: Route to the best engineering skill for your current situation.
- `/grill-me`: Conduct an interactive design-tree interview with recommended options.
- `/tdd`: Run the red-green-refactor vertical slice development cycle.
- `/code-review`: Execute dual-axis code review (Standards + Spec) on recent changes.
- `/diagnosing-bugs`: Systematic root-cause debugging loop.
- `/to-spec` / `/to-tickets`: Convert conversation into formal specifications or tracer-bullet tickets.

---

## 3. Project Quick Commands by Stack

- **Go Projects** (`cd <go-project>`): `go test -v ./...` | `go build ./...`
- **Python Projects** (`cd <py-project>`): `pytest` | `python -m unittest`
- **Node / React / Next.js** (`cd <node-project>`): `npm test` | `npm run build` | `npm run dev`
- **Android / Kotlin** (`cd datawarga-android`): `./gradlew test` | `./gradlew build`
- **macOS / Swift** (`cd llm-quota-desktop`): `xcodebuild test` | `swift test`
- **Ruby / Jekyll** (`cd sol` or `cd blogdekil`): `bundle exec jekyll build` | `bundle exec jekyll serve`

---

## 4. Git Safety Guardrails

- Never execute destructive git commands (`git push --force`, `git reset --hard`, `git clean -fd`, `git branch -D`) without explicit user permission.
- Always check `git status` and run tests before committing.
- Commit using `--no-gpg-sign` in automated environments.
