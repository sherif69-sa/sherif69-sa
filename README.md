<p align="center">
  <img src="./assets/hero_signature.svg" alt="Sherif Atef — Python SDET and AI Evaluation Engineer" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/sherif69-sa"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-sherif69--sa-181717?style=flat-square&logo=github"></a>
  <a href="https://www.linkedin.com/in/devs69/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-devs69-0A66C2?style=flat-square&logo=linkedin"></a>
  <a href="https://leetcode.com/u/sherif69/"><img alt="LeetCode" src="https://img.shields.io/badge/LeetCode-sherif69-FFA116?style=flat-square&logo=leetcode&logoColor=black"></a>
</p>

## Evidence-first engineering profile

I build validation systems for code, CI, repositories, and AI-generated outputs.

My strongest work is in the gap between **what a system says happened** and **what the evidence proves happened**: reproducing failures, extracting exact signals, validating behavior, and turning noisy output into decisions a reviewer can trust.

```text
Clone → Reproduce → Inspect → Prove → Report
```

---

<p align="center">
  <img src="./assets/validation_surfaces.svg" alt="What I validate" width="100%" />
</p>

| Surface | What I validate |
| --- | --- |
| **Python test behavior** | pytest contracts, regression signals, edge cases, hidden-test safety |
| **AI-generated code** | task logic, rubric alignment, unsafe assumptions, hallucinated behavior |
| **CI and repository signals** | failing checks, owner files, artifacts, logs, proof commands |
| **Benchmark tasks** | correctness, performance, memory, implementation clarity |

---

<p align="center">
  <img src="./assets/engineering_proof_surface.svg" alt="Engineering proof surface" width="100%" />
</p>

```text
failure_vector:
  check=<workflow/check>
  first_failing_line=<exact signal>
  failure_class=<formatter|lint|type|test|dependency|security|unknown>
  safe_fix_candidate=<yes|no>
```

```text
review_decision:
  diagnosis=<what failed and why>
  proof=<focused command>
  blocked_actions=<what must not be changed>
  next_human_action=<exact command or review step>
```

---

## Flagship project — DevS69 SDETKit

**DevS69 SDETKit** is my main public engineering project.

It is growing into a local-first reliability platform for SDET workflows: extracting failure evidence, preserving review-first boundaries, recording diagnostic trajectories, and producing reports that help maintainers know what to do next.

Repository: **https://github.com/sherif69-sa/DevS69-sdetkit**

<p align="center">
  <img src="./assets/devs69_platform_map.svg" alt="DevS69 SDETKit reliability platform map" width="100%" />
</p>

| Component | Product role |
| --- | --- |
| **FailureVectorEngine** | extracts the first real failure and turns it into structured evidence |
| **SafetyGate** | keeps unknown, broad, security, release, and dependency work review-first |
| **TrajectoryStore / RepoMemory** | records action → response → diagnosis → proof → outcome |
| **ReplayableBenchmarkHarness** | evaluates no-op, oracle, and unsafe repair scenarios |
| **ProtectedVerifier** | checks patch scope, proof validity, and anti-cheat boundaries |
| **PRReporter / PatchScorer** | renders exact failure, safety decision, proof, next action, and repair score |

---

<p align="center">
  <img src="./assets/practice_engine.svg" alt="Practice engine" width="100%" />
</p>

LeetCode is part of my long-term engineering practice system. I use it to strengthen algorithm selection, hidden-test safety, runtime awareness, memory tradeoffs, and debugging speed.

Profile: **https://leetcode.com/u/sherif69/**

---

<p align="center">
  <img src="./assets/reviewer_briefing.svg" alt="Reviewer briefing" width="100%" />
</p>

## Core stack

```text
Python · pytest · Pandas · Docker · Git · GitHub Actions
CLI workflows · JSON evidence · Markdown reports · CI-style validation
AI evaluation workflows · coding benchmark review · repository inspection
```

## Target roles

- Python SDET
- AI Evaluation Engineer
- Coding Benchmark QA Engineer
- Test Automation Engineer
- CI Reliability / Quality Engineering
- LLM Workflow Evaluation
- Repository Review and Validation

---

<p align="center">
  <img src="./assets/contact_panel.svg" alt="Contact panel" width="100%" />
</p>

- LinkedIn: **https://www.linkedin.com/in/devs69/**
- GitHub: **https://github.com/sherif69-sa**
- LeetCode: **https://leetcode.com/u/sherif69/**
- Email: **sherif.atef6300@gmail.com**
