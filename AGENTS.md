# AGENTS.md

> **Universal Master Agent Configuration & Engineering Standards**  
> **Target Platforms**: Google Antigravity (AGY / Gemini CLI), Anthropic Claude Code, OpenAI Codex, Cursor IDE, and OpenCode.  
> **Scope**: Root workspace and all 40 subprojects across Go, Python, TypeScript/React/Next.js, Swift, Android/Kotlin, Ruby/Jekyll, and Terraform.

---

## 1. Core Operating Principles

1. **Mandatory Test-Driven Development (TDD)**: Every feature, bug fix, or refactor must follow the strict Red-Green-Refactor cycle using vertical slices against agreed public seams.
2. **Matt Pocock Engineering Process & Grill-Me Protocol**: Conduct an interactive alignment interview before starting complex tasks or architectural refactors. Explore the codebase autonomously before asking the user questions.
3. **Taste Skill Anti-Slop Discipline**: All UI, frontend, styling, and design work must adhere to the **Taste Skill Framework** (`https://tasteskill.dev`). Emit a one-line Design Read, calibrate the Three Dials, and reject generic AI defaults.
4. **Autonomous Fact Finding**: Investigate codebase files, configurations, schemas, and dependencies before asking questions. Only ask the user for genuine product, UX, or architectural decisions.
5. **Full Output Enforcement**: Never output placeholder comments (e.g. `// TODO`, `/* remaining code */`). Always write complete, functional, production-ready code.
6. **Rigorous Verification Gates**: Run project-specific test suites and build checks before declaring any task complete. Evidence before assertions always.

---

## 2. Mandatory Protocol 1: Test-Driven Development (TDD)

Every coding task must be developed test-first. Consult the `tdd` skill (`.agents/skills/tdd/SKILL.md`) for detailed patterns.

```
┌────────────────────────────────────────────────────────┐
│ 1. AGREE SEAMS                                         │
│    • Define the public boundary / interface under test │
│    • Confirm seam with user / specification            │
└──────────────────────────┬─────────────────────────────┘
                           ▼
┌────────────────────────────────────────────────────────┐
│ 2. RED (Failing Test First)                            │
│    • Write test verifying public behavior              │
│    • Run test -> confirm it FAILS for the right reason │
└──────────────────────────┬─────────────────────────────┘
                           ▼
┌────────────────────────────────────────────────────────┐
│ 3. GREEN (Minimal Implementation)                      │
│    • Write ONLY enough code to pass the test           │
│    • No anticipatory or speculative code               │
└──────────────────────────┬─────────────────────────────┘
                           ▼
┌────────────────────────────────────────────────────────┐
│ 4. REFACTOR (Clean Code Under Test)                    │
│    • Simplify, remove duplication, keep tests passing  │
│    • Repeat next vertical slice (Tracer Bullet)        │
└────────────────────────────────────────────────────────┘
```

### 2.1 Rules of the TDD Loop
- **Seams First**: Tests verify behavior through public interfaces, never private internals or implementation details. If a refactor breaks tests without changing behavior, the test was coupled to implementation.
- **Vertical Slices (Tracer Bullets)**: Work one slice at a time: `1 Seam -> 1 Test -> 1 Minimal Implementation -> Green`. Never horizontal slice (writing 20 tests upfront before writing code).
- **Independent Truth**: Assertions must verify against known-good specifications, worked examples, or literal values—never tautological recomputations.

### 2.2 Test Runners Matrix by Technology

| Stack | Primary Test Command | Watch Mode | Notes |
| :--- | :--- | :--- | :--- |
| **Go** (`imsakiyah`, `k8ctl`, `kompetisi`, `go-todo-cli`) | `go test -v ./...` | `gow test ./...` | Table-driven tests, check `-race` |
| **Python** (`chatbot-backend`, `mbuddy`, `pico-erp`, `sidikara`, `dreamchaser`, `datawarga`) | `pytest` or `python -m pytest` | `ptw` / `pytest-watch` | Fast test fixtures, SQLite in-memory |
| **Node / Next.js / React** (`ipolens`, `jasapro`, `cloud-network-learning-materials`, `pico-erp-frontend`) | `npm test` or `pnpm test` | `npm test -- --watch` | Vitest / Jest + React Testing Library |
| **Android / Kotlin** (`datawarga-android`) | `./gradlew test` | `./gradlew test --continuous` | Unit tests under `src/test/` |
| **macOS / Swift** (`llm-quota-desktop`, `pico-desktop`) | `swift test` or `xcodebuild test` | Xcode Test Runner | Native XCTest / Swift Testing |
| **Ruby / Jekyll** (`sol`, `blogdekil`, `robertusnegoro.github.io`) | `bundle exec jekyll build` / `rspec` | `bundle exec guard` | HTML / Liquid verification |
| **Terraform / IaC** (`aws-tf-sample`, `cloud-network-learning-materials`) | `terraform init -backend=false && terraform validate` | N/A | Syntax & provider schema validation |

---

## 3. Mandatory Protocol 2: Matt Pocock Engineering Process

Inspired by Matt Pocock's skills repository (`.agents/skills/`), development follows structured engineering discipline over ad-hoc generation.

### 3.1 The Grill-Me Protocol
Before implementing complex features, major refactors, or new architectural modules:
1. Map the problem space as a **Design Tree** with branching technical decisions.
2. Formulate the **Frontier** (all unblocked questions ready for decision).
3. Present questions in rounds strictly formatted as:
   ```markdown
   ❓ **Q1** - **<Question Title>**: <Clear context and decision options>

   ➡️ **Recommendation**: <Specific proposed answer with rationale>

   ---

   ❓ **Q2** - **<Question Title>**: <Clear context and decision options>

   ➡️ **Recommendation**: <Specific proposed answer with rationale>
   ```
4. Unblock layer by layer until the frontier is empty and the user approves the execution plan.

### 3.2 Deep Modules & Seams
- Modules should have simple, narrow interfaces that hide deep, complex functionality.
- Domain concepts, glossary terms, and Architecture Decision Records (ADRs) must be respected.
- Keep a high ratio of module functionality to interface complexity.

### 3.3 Engineering Skills Catalog
- `/ask-matt`: Skill router to determine the right engineering workflow.
- `/grill-me` & `/grill-with-docs`: Interactive alignment interview that generates ADRs and glossaries.
- `/tdd`: Red-Green-Refactor vertical slice workflow.
- `/codebase-design`: Vocabulary for deep modules, interfaces, depth, seams, and adapters.
- `/diagnosing-bugs`: Root-cause diagnosis loop for complex bugs and performance regressions.
- `/code-review`: Parallel standards and specification verification review.
- `/to-spec` & `/to-tickets`: Decompose conversation and plans into traceable tracer-bullet tickets.

---

## 4. Mandatory Protocol 3: Taste Skill (Anti-Slop Frontend Framework)

All UI, frontend, layout, CSS/Tailwind, and HTML templates must adhere to the **Taste Skill Framework** (`.agents/skills/design-taste-frontend/SKILL.md` and `https://tasteskill.dev`).

### 4.1 Anti-Default Discipline (Zero AI Slop)
Strictly banned default AI aesthetics:
- ❌ Centered hero headlines floating over dark mesh purple/indigo gradient blobs.
- ❌ Three identical floating feature cards with generic rounded icons.
- ❌ Default unstyled `Inter` + `slate-900` boilerplates without typographic character.
- ❌ Generic, unstyled glassmorphism / excessive backdrop blur without purpose.
- ❌ Infinite loop micro-animations that distract from content and readability.
- ❌ Hand-rolled div-based fake screenshots / mock dashboards (use real screenshots or component previews).

### 4.2 Mandatory One-Line "Design Read"
Before generating or modifying any UI component, output:
> `Reading this as: <page kind> for <audience>, with a <vibe> language, leaning toward <design system or aesthetic family>.`

### 4.3 The Three Dials Calibration
Calibrate global parameters for every frontend surface:
- **`DESIGN_VARIANCE`** (1–10): *Layout experimentation & asymmetry* (Default: `7` or `8`)
- **`MOTION_INTENSITY`** (1–10): *Micro-interactions & transition energy* (Default: `5` or `6`)
- **`VISUAL_DENSITY`** (1–10): *Information density vs. airy negative space* (Default: `4`)

### 4.4 Strict UI & Accessibility Guardrails
- **Hero Viewport Fit**: Hero must fit initial viewport (`min-h-[100dvh]`). Max 2 lines headline, max 20 words subtext. CTAs visible without scroll.
- **Hero Top Padding Cap**: Max `pt-24` (≈6rem) on desktop.
- **Navigation Bar**: Single line on desktop, max height 80px (default 64–72px).
- **Eyebrow Restraint**: Maximum 1 small-caps uppercase eyebrow per 3 sections.
- **Button Contrast (WCAG AA)**: Strict 4.5:1 minimum contrast. Never wrap CTA button text at desktop.
- **No Duplicate CTA Intent**: One label per intent across the page (e.g. don't mix "Contact Us", "Get in touch", and "Let's talk").
- **Motion & Accessibility**: All animations above `MOTION_INTENSITY > 3` must honor `prefers-reduced-motion`. Animate only `transform` and `opacity`.

---

## 5. Monorepo Projects Catalog & Quick Reference

This repository is a monorepo containing 40 individual subprojects:

| # | Project Directory | Tech Stack | Primary Focus & Description | Test Command |
| :-: | :--- | :--- | :--- | :--- |
| 1 | `aws-tf-sample/` | Terraform, Atlantis | AWS & GCP infrastructure migration blueprints | `terraform validate` |
| 2 | `bartuku/` | HTML, CSS, Vanilla JS | Toko Bartuku landing page | Manual / Browser |
| 3 | `blogdekil/` | Ruby, Jekyll | Minimal personal blog template | `bundle exec jekyll build` |
| 4 | `bukukas/` | React, Docker | Personal and business bookkeeping financial app | `npm test` |
| 5 | `chatbot-backend/` | Python, FastAPI, RAG | Confluence/Jira RAG chatbot backend | `pytest` |
| 6 | `cloud-network-learning-materials/` | Vue 3, VitePress, TS, IaC | Principal Cloud Network Engineer interactive learning platform | `npm run build` |
| 7 | `cvmaker/` | Node.js, React | CV & Resume builder tool | `npm test` |
| 8 | `datawarga/` | Python, Django | Community / citizen management web platform | `pytest` / `python manage.py test` |
| 9 | `datawarga-android/` | Kotlin, Android SDK | Mobile native Android client for DataWarga | `./gradlew test` |
| 10 | `dreamchaser/` | Python, Flask/FastAPI | Cognitive therapy and remedial training tool | `pytest` |
| 11 | `flux-test-local/` | GitOps, FluxCD | Local Kubernetes GitOps experiments | `kubectl / flux check` |
| 12 | `flyio-hiring-129053/` | Go / Containers | Fly.io infrastructure engineering project | `go test ./...` |
| 13 | `go-learn/` | Go | Go language patterns and learning modules | `go test ./...` |
| 14 | `go-todo-cli/` | Go | Lightweight CLI todo application | `go test ./...` |
| 15 | `iamiaman/` | Python, CLI | Identity & access helper CLI tool | `pytest` |
| 16 | `imsakiyah/` | Go 1.25, PostgreSQL | Muslim prayer schedule REST API | `go test ./...` |
| 17 | `infra-robee-cloud/` | Python, Ansible | Infrastructure automation & playbooks | `ansible-lint` |
| 18 | `infra-robee-cloud-example/` | Python, Ansible | Example infrastructure playbooks | `ansible-lint` |
| 19 | `ipolens/` | Next.js, React, TS, Postgres | Financial report analyzer (Peter Lynch methodology) | `npm test` |
| 20 | `jadwalsholat/` | Flutter / Multiplatform | Multi-platform prayer times app | `flutter test` |
| 21 | `jasapro/` | Next.js, React, Tailwind | Professional service marketplace web app | `npm test` |
| 22 | `k8ctl/` | Go, Kubernetes | Enhanced kubectl CLI with colored tables | `go test -v ./...` |
| 23 | `k8s_exercise/` | Kubernetes, Shell | CKA Exam hands-on lab exercises | Lab verification scripts |
| 24 | `kompetisi/` | Go, REST API | Competition & tournament organizer backend | `go test -v ./...` |
| 25 | `kube-ansible/` | Ansible, Kubernetes | HA Kubernetes cluster deployment playbooks | `ansible-lint` |
| 26 | `laundry-pos-oss/` | Node.js, React | Laundry POS point-of-sale management system | `npm test` |
| 27 | `llm-quota-desktop/` | Swift, SwiftUI, macOS | Native macOS menu bar & desktop widget for LLM quota | `xcodebuild test` / `swift test` |
| 28 | `mbuddy/` | Python, FastAPI, Jira | Cloud migration project tracker with Jira integration | `pytest` |
| 29 | `nadhira-cp/` | HTML, CSS, JS | Company profile landing page | Manual / Browser |
| 30 | `pico-desktop/` | Swift, SwiftUI, macOS | Native macOS ERP client desktop application | `xcodebuild test` |
| 31 | `pico-erp/` | Python, FastAPI, SQLAlchemy | Lightweight ERP backend for online shops (RBAC) | `pytest` |
| 32 | `pico-erp-app/` | Swift / SwiftUI | Mobile / desktop companion for Pico ERP | `swift test` |
| 33 | `pico-erp-frontend/` | React, Vite, Tailwind | Responsive frontend management UI for Pico ERP | `npm test` |
| 34 | `randomops.github.io/` | Ruby, Jekyll | Tech blog static site | `bundle exec jekyll build` |
| 35 | `restopesto/` | React, Node.js | Restaurant ordering and management frontend | `npm test` |
| 36 | `robertusnegoro.github.io/` | Ruby, Jekyll, Node | Personal Jekyll portfolio and blog | `bundle exec jekyll build` |
| 37 | `sidikara/` | Python, FastAPI, Alembic | Identity Governance & Administration (IGA) backend | `pytest` |
| 38 | `sol/` | Ruby 3.3, Jekyll 3.10, SCSS | Premium editorial Jekyll blog theme | `bundle exec jekyll build` |
| 39 | `tradingbot/` | Python / Trading | Automated trading system experiments | `pytest` |
| 40 | `web-game/` | HTML5, Canvas, JS | Collection of classic web games (2048, Tetris, etc.) | Manual / Browser |

---

## 6. Multi-Platform Compatibility Reference

| Agent Platform | Configuration Entry Point | Rule Locations | Skill Directories |
| :--- | :--- | :--- | :--- |
| **Google Antigravity (AGY / Gemini CLI)** | `AGENTS.md`, `GEMINI.md` | `.agents/rules/*.md` | `.agents/skills/`, `~/.gemini/config/skills/` |
| **Anthropic Claude Code** | `CLAUDE.md`, `AGENTS.md` | Root instructions | `.claude/skills/`, `.agents/skills/` |
| **OpenAI Codex** | `AGENTS.md`, `CODEX.md` | `.agents/rules/*.md` | `.agents/skills/` |
| **Cursor IDE** | `.cursorrules`, `.cursor/rules/*.mdc` | `.cursor/rules/` | `.agents/skills/` |
| **OpenCode** | `OPENCODE.md`, `AGENTS.md` | `.agents/rules/*.md` | `.agents/skills/` |

---

## 7. Public Repository Security & Git Hygiene

- **Zero Secrets Policy**: Never commit credentials, `.env` files with real keys, API secrets, private keys (`.pem`, `.key`), or sensitive corporate tokens.
- **Sanitized Placeholders**: Use RFC standard IP blocks (`10.0.0.0/16`, `192.0.2.0/24`, `198.51.100.0/24`) and dummy account IDs (`123456789012`).
- **Destructive Command Ban**: Never execute `git push --force`, `git reset --hard`, `git clean -fd`, or `git branch -D` without explicit user confirmation.
- **Commit Signing**: AI agents must use `--no-gpg-sign` when executing commits automatically in CLI/sandbox environments.
