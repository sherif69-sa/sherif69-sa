<p align="center"> <img src="./assets/banner_final.svg" alt="Sherif — Backend & DevTools Engineer" width="100%" /> </p> <p align="center"> <a href="https://github.com/sherif69-sa"><img alt="Follow" src="https://img.shields.io/github/followers/sherif69-sa?label=Follow&style=for-the-badge&logo=github"></a> <img alt="Python" src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white"> <img alt="Node.js" src="https://img.shields.io/badge/Node.js-20+-339933?style=for-the-badge&logo=node.js&logoColor=white"> <img alt="SQLite" src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white"> <img alt="CI" src="https://img.shields.io/badge/GitHub%20Actions-enabled-2088FF?style=for-the-badge&logo=githubactions&logoColor=white"> </p> <p align="center"> <a href="#flagship-projects-pinned"><img src="https://img.shields.io/badge/Projects-See%20pinned-8b5cf6?style=flat-square"></a> <a href="#pull-request-playbook"><img src="https://img.shields.io/badge/PRs-Welcome-10b981?style=flat-square"></a> <a href="#contact"><img src="https://img.shields.io/badge/Contact-LinkedIn-0ea5e9?style=flat-square"></a> </p> --- ## Table of Contents - [About me](#about-me) - [Focus mix](#focus-mix) - [Operating loop](#operating-loop) - [System blueprint](#system-blueprint-typical-project) - [Release flow (visual)](#release-flow-visual) - [One-year public roadmap](#one-year-public-roadmap) - [Flagship projects (pinned)](#flagship-projects-pinned) - [Pull Request playbook](#pull-request-playbook) - [Coding standards](#coding-standards) - [CI/CD](#cicd) - [Design notes (ADRs)](#design-notes-adrs) - [Security & quality stance](#security--quality-stance) - [FAQ](#faq) - [Public activity plan (first 8 weeks)](#public-activity-plan-first-8-weeks) - [Contact](#contact) - [Visual metrics](#visual-metrics) --- ## About me I design and ship **small, reliable backends** and **developer tools**. I optimize for simple interfaces, predictable behavior, and documentation that helps other engineers move fast. - **Focus:** practical AI apps · Python/Node tooling · SQLite-first data flows - **Style:** design note → small PRs → tests & CI → release → docs - **Strengths:** focused PRs · explicit tradeoffs · observability · tidy changelogs ### Signature deliverables - Product-grade **READMEs** with runnable examples - **CI always green**; fast checks; minimal dependencies - **Versioned releases** with concise changelogs - **Design notes (ADRs)** capturing why/why-not --- ## Focus mix
mermaid
pie title Where my time goes
  "Dev tooling" : 45
  "AI apps" : 35
  "Data flows" : 20
## Operating loop
mermaid
flowchart LR
  A[Idea] --> B[Design note]
  B --> C[Slice into small PRs]
  C --> D[Tests + CI]
  D --> E[Release v0.x]
  E --> F[Docs + Examples]
  F --> G[Feedback → next slice]
## System blueprint (typical project)
mermaid
flowchart TD
  Dev[CLI / Web UI] --> SVC[Service Layer]
  SVC --> DB[(SQLite)]
  SVC --> OBS[Logging & Metrics]
  SVC --> JOB[Background Jobs]
  CI[GitHub Actions] --> TESTS[Unit + Integration]
  CI --> REL[Tag + Changelog + Release]
  SVC -.docs & examples.-> REL
## Release flow (visual) > GitHub’s Mermaid renderer is picky; this **flowchart** version renders reliably (no gitGraph tag:).
mermaid
flowchart LR
  I[init commit] --> F[rules on feature/triage]
  F --> M1[merge to main]
  M1 --> T1[[tag v0.1.0]]
  T1 --> H[branch harden]
  H --> C1[add tests + metrics]
  C1 --> M2[merge to main]
  M2 --> T2[[tag v0.3.0]]
--- ## One-year public roadmap
mermaid
gantt
  dateFormat  YYYY-MM-DD
  title  12-month plan
  section Project A — IssuePilot
  MVP 0.1.0           :active,  a1, 2025-10-20, 14d
  Rules + reports     :        a2, 2025-11-10, 21d
  Minimal web UI      :        a3, 2025-12-15, 21d
  0.6.x hardening     :        a4, 2026-02-01, 30d
  0.9.x API freeze    :        a5, 2026-04-01, 30d
  1.0.0 GA            :        a6, 2026-06-01, 21d
  section Project B — SQLiteLab
  Ingest + schema     :done,    b1, 2025-10-20, 10d
  Manifests + tests   :active,  b2, 2025-11-05, 24d
  Checks + examples   :        b3, 2025-12-20, 24d
  0.6.x polish        :        b4, 2026-03-01, 30d
  1.0.0 GA            :        b5, 2026-06-15, 20d
  section Project C — IntlToolkit
  Numbers + currency  :done,    c1, 2025-10-20, 7d
  Dates + tz          :active,  c2, 2025-11-15, 20d
  Benchmarks          :        c3, 2026-01-05, 20d
  API freeze          :        c4, 2026-03-10, 15d
  1.0.0 GA            :        c5, 2026-05-01, 14d
### Quarterly goals * **Q4 (now):** ship public MVPs (0.1.x), pin repos, enable CI, write short design notes. * **Q1:** harden APIs, add tests/benchmarks, publish usage guides & examples. * **Q2:** stabilize 0.9.x, add minimal UIs where useful, cut **1.0.0** for the two most used. * **Q3:** maintenance cadence, docs deepening, upstream contributions monthly. --- ## Flagship projects (pinned) I keep a **small, sharp set** of public repos and treat each like a product. | Project | What it does | Core tech | Quality signals | | --------------- | ------------------------------------------------------------------------------------------------------ | ----------------------------------------- | ---------------------------------------- | | **IssuePilot** | GitHub issue triage (CLI + minimal web). Deterministic rules first; optional AI label/duplicate hints. | Python (stdlib), GitHub API, FastAPI (UI) | CI green · 0.1.x releases · design notes | | **SQLiteLab** | SQLite-first data flows (manifests, scripts, tests). Portable analytics with zero infra. | Python, SQLite, CSV/Parquet | CI green · fixtures · example datasets | | **IntlToolkit** | Intl.NumberFormat + date/currency utilities with a minimal, stable API. | Node.js 20+, ESM | Node tests · semver · benchmarks | --- ## Pull Request playbook **Goal:** predictable, readable changes that reviewers can trust. ### PR checklist * [ ] Scope fits in **one review session** (< ~400 LOC diff when possible) * [ ] **Why** (user-facing reason) at top of PR description * [ ] **What changed**: bullets, not prose * [ ] **Tests**: updated/added; CI passing * [ ] **Docs**: README/ADR snippet if behavior or API changed * [ ] **Changelog**: entry prepared if user-facing ### PR description template
markdown
### Why
Short business or user-facing reason. Link to issue or design note.

### What changed
- bullet
- bullet

### How to test
- command / steps
- expected result

### Notes
risks, tradeoffs, follow-ups
### Review philosophy * Comment on **behavior and contracts** first; then style. * Suggest code if it’s shorter to show than to explain. * Prefer **clarity over cleverness**; boring tech that scales. ### Commit style (Conventional Commits) feat: add triage rules engine · fix: handle empty manifest · docs: add README examples · refactor: simplify formatter API · test: add currency fixtures · chore: bump actions/setup-node to v4 --- ## Coding standards ### Python * Type hints for public APIs. * Keep functions short; single responsibility. * Use pathlib, subprocess.run(check=True), and logging (no prints in libs). * CLI entry via python -m <pkg>.cli with argparse. ### Node/JS * ESM only; type: "module"; Node 20+. * node:test for unit tests; no heavy test frameworks. * Zero runtime deps for small libs when possible. --- ## CI/CD **Principles:** fast, deterministic, minimal. Each repo has a single ci workflow that runs on PR and main. --- ## Design notes (ADRs) I keep lightweight ADRs under /docs/ in each repo. --- ## Security & quality stance * **Least privilege** in tokens and secrets. * **No secrets in code**; use environment variables or GitHub Actions secrets. * **Dependabot alerts** on by default; patch weekly. * **Static checks** (type hints, unit tests) before any new feature ships. --- ## FAQ **Why SQLite?** Portable, fast, inspectable, and reliable for many workflows. **Why small repos?** They age better, review faster, and stay maintainable. --- ## Public activity plan (first 8 weeks) * Week 1: create the 3 repos; add README, LICENSE, CI; pin them. * Week 2: one-page design notes; cut v0.1.0 in each. * Week 3: 2 small upstream PRs to projects I use. * Week 4: tests & small benchmarks (IntlToolkit); publish to npm if ready. * Week 5–6: examples + minimal web UI (IssuePilot). * Week 7: example datasets + checks (SQLiteLab). * Week 8: cut v0.3.x with release notes. --- ## Contact * LinkedIn: [https://www.linkedin.com/in/sherif-atef-b1077a124/](https://www.linkedin.com/in/sherif-atef-b1077a124/) * Collaboration: open an issue in this profile repo --- ## Visual metrics <details> <summary>Expand</summary> ![activity graph](https://github-readme-activity-graph.vercel.app/graph?username=sherif69-sa&theme=github-compact&hide_border=true) </details>
