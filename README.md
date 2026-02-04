<p align="center">
  <img src="./assets/banner_final.svg" alt="Sherif — Backend & DevTools Engineer" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/sherif69-sa"><img alt="Follow" src="https://img.shields.io/github/followers/sherif69-sa?label=Follow&style=for-the-badge&logo=github"></a>
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-20+-339933?style=for-the-badge&logo=node.js&logoColor=white">
  <img alt="SQLite" src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white">
  <img alt="CI" src="https://img.shields.io/badge/GitHub%20Actions-enabled-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
</p>

<p align="center">
  <a href="#flagship-projects-pinned"><img src="https://img.shields.io/badge/Projects-See%20pinned-8b5cf6?style=flat-square"></a>
  <a href="#pull-request-playbook"><img src="https://img.shields.io/badge/PRs-Welcome-10b981?style=flat-square"></a>
  <a href="#contact"><img src="https://img.shields.io/badge/Contact-LinkedIn-0ea5e9?style=flat-square"></a>
</p>

---

## About me
I build **reliable backends** and **developer tooling** with a focus on clean interfaces, deterministic behavior, and docs that make other engineers faster.

- **Focus:** backend systems · DevTools · Python/Node · SQLite-first workflows
- **Workflow:** design note → small PRs → tests & CI → release → docs
- **Strengths:** scoped PRs · clear tradeoffs · observability · stable contracts

---

## Focus mix
```mermaid
pie title Where my time goes
  "Dev tooling" : 45
  "AI apps" : 35
  "Data flows" : 20
````

## Operating loop

```mermaid
flowchart LR
  A[Idea] --> B[Design note]
  B --> C[Small PRs]
  C --> D[Tests + CI]
  D --> E[Release]
  E --> F[Docs + Examples]
  F --> G[Feedback -> next slice]
```

## System blueprint (typical project)

```mermaid
flowchart TD
  Dev[CLI / Web UI] --> SVC[Service Layer]
  SVC --> DB[(SQLite)]
  SVC --> OBS[Logging & Metrics]
  SVC --> JOB[Background Jobs]
  CI[GitHub Actions] --> TESTS[Unit + Integration]
  CI --> REL[Tag + Changelog + Release]
  SVC -.docs & examples.-> REL
```

## Release flow (visual)

```mermaid
flowchart LR
  I[init] --> F[feature/triage rules]
  F --> M1[merge to main]
  M1 --> T1[[tag v0.1.0]]
  T1 --> H[harden]
  H --> C1[tests + metrics]
  C1 --> M2[merge to main]
  M2 --> T2[[tag v0.3.0]]
```

---

## Public roadmap

```mermaid
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
```

---

## Flagship projects (pinned)

| Project         | What it does                                                                                           | Core tech                        |
| --------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------- |
| **IssuePilot**  | GitHub issue triage (CLI + minimal web). Deterministic rules first; optional AI label/duplicate hints. | Python, GitHub API, FastAPI (UI) |
| **SQLiteLab**   | SQLite-first data flows (manifests, scripts, tests). Portable analytics with zero infra.               | Python, SQLite, CSV/Parquet      |
| **IntlToolkit** | Intl.NumberFormat + date/currency utilities with a minimal, stable API.                                | Node.js 20+, ESM                 |

---

## Pull Request playbook

### PR checklist

* Scope fits in one review session
* Why (user impact) at the top
* What changed in bullets
* Tests updated/added and CI green
* Docs updated if behavior changed
* Changelog note if user-facing

### PR template

```markdown
### Why
Short user-facing reason. Link to issue/design note.

### What changed
- bullet
- bullet

### How to test
- steps
- expected result

### Notes
risks, tradeoffs, follow-ups
```

---

## Coding standards

### Python

* Type hints for public APIs
* `pathlib`, `subprocess.run(check=True)`, `logging` (no prints in libs)
* Small functions, single responsibility
* CLI via `python -m <pkg>.cli` with `argparse`

### Node/JS

* ESM only, Node 20+
* `node:test` for unit tests
* Keep runtime deps minimal

---

## Contact

* LinkedIn: [https://www.linkedin.com/in/sherif-atef-b1077a124/](https://www.linkedin.com/in/sherif-atef-b1077a124/)

---

## Visual metrics

<details>
<summary>Expand</summary>

* GitHub overview: [https://github.com/sherif69-sa?tab=overview](https://github.com/sherif69-sa?tab=overview)
* Repositories: [https://github.com/sherif69-sa?tab=repositories](https://github.com/sherif69-sa?tab=repositories)
* Stars: [https://github.com/sherif69-sa?tab=stars](https://github.com/sherif69-sa?tab=stars)

</details>
```
