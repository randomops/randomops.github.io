---
trigger: always_on
description: Mandatory Test-Driven Development (TDD) protocol across all project codebases.
---

# Test-Driven Development (TDD) Mandate

Every code feature, bugfix, or refactor must strictly adhere to the **Test-Driven Development (TDD)** lifecycle.

## 1. The Red-Green-Refactor Loop

1. **Agree Seams First**: Define the public boundary/interface under test. Confirm the seam before writing tests.
2. **Red (Failing Test)**:
   - Write an executable test verifying desired behavior against the public interface.
   - Run the test and confirm it **fails** for the expected reason (not a syntax error or missing import).
   - Expected values must come from independent truth (spec, worked examples), never tautological recomputations.
3. **Green (Minimal Passing Code)**:
   - Write *only* enough implementation code to make the failing test pass.
   - Do not write anticipatory code or speculate on future requirements.
4. **Refactor**:
   - Clean up implementation, remove duplication, and optimize while keeping all tests passing.
   - Refactoring happens after green, never during the implementation cycle.

## 2. Vertical Slices & Tracer Bullets
- **Never Horizontal Slice**: Do not write dozens of tests first and then write all code.
- **Vertical Slices**: Implement one vertical slice at a time: `1 Seam -> 1 Test -> 1 Minimal Implementation -> Green`.

## 3. Test Runner Quick Reference by Project Type

| Language / Framework | Test Command | Watch Command |
| :--- | :--- | :--- |
| **Go** | `go test -v ./...` | `gow test ./...` |
| **Python / Django / FastAPI** | `pytest` or `python -m pytest` | `pytest-watch` or `ptw` |
| **Node.js / React / Next.js** | `npm test` or `pnpm test` | `npm test -- --watch` |
| **Android / Kotlin** | `./gradlew test` | `./gradlew test --continuous` |
| **macOS / Swift** | `swift test` or `xcodebuild test` | Xcode Test Navigator |
| **Ruby / Jekyll** | `bundle exec rspec` / `bundle exec jekyll build` | `bundle exec guard` |
| **Terraform / IaC** | `terraform validate` | `terraform plan` |
