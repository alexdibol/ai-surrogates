# AI Surrogates in Finance — Constrained Surrogacy Under Governance

Governance-first · auditable · reproducible · human-accountable  
Built for **MBA / Master of Finance cohorts** and **professional finance / trading / research practitioners** who need mechanism clarity under constraint.

---

## What this repository is

This repository is the governed home of **AI Surrogates in Finance**: a synthetic-first, reviewable laboratory for designing **surrogate decision systems** in finance under explicit constraints.

The objective is not “a smarter model.”  
The objective is **a defensible controller**: a surrogate that behaves like a contract—explicit state, explicit constraints, explicit termination, explicit artifacts—so an independent reviewer can answer:

- what happened
- why it happened
- which constraints were active
- how close the system ran to boundaries
- what is fact vs assumption vs open item
- what required human escalation

This repo is intentionally explicit about limits:

- it does **not** promise alpha discovery
- it does **not** treat backtests as evidence
- it does **not** claim production readiness by default
- it does **not** claim correctness of external facts

**Core premise:**  
**Capability ↑ ⇒ Risk ↑ ⇒ Controls ↑**

---

## Repository structure (as in this repo)

- **/book/**
  The book source. The book is the governing spec: definitions, mechanisms, failure modes, acceptance gates.

- **/notebooks/**
  The governed laboratories that operationalize the book with synthetic data, diagnostics, and mandatory artifacts.


---

## The book structure (3 chapters)

This repository is organized to match the book exactly.  
Each chapter has a corresponding set of governed notebooks.

### Chapter 1 — Why Surrogacy Needs Governance
Surrogates are proxies. Proxies take actions (or drive decisions).  
Once a model becomes a proxy for a decision, “accuracy” is not the main question. The main question is whether the proxy is **reviewable under constraint**.

Chapter 1 formalizes:
- surrogacy as a **proxy contract** (what the surrogate may and may not claim)
- “generation ≠ verification” as a non-negotiable discipline
- facts vs assumptions vs open items as a first-class output requirement
- the baseline failure modes: overconfidence, silent constraint drift, boundary collapse, and irreproducible results

Deliverable expectation:
- a reviewer can reconstruct the logic from artifacts, not from persuasion

### Chapter 2 — Mechanisms: Constrained Surrogate Controllers
A surrogate worthy of use in finance must be designed like a controller:
- explicit **state**
- explicit **constraints**
- explicit **routing**
- explicit **termination rules**
- explicit **escalation paths**
- measurable **constraint margins** (distribution, not point estimates)

Chapter 2 operationalizes:
- constraint encoding (risk, leverage, turnover, liquidity, drawdown, exposure)
- bounded loops (no infinite retries)
- stage-gated decisions (advance / revise / reject)
- stress tests for structural breaks and regime shifts

Deliverable expectation:
- the system can explain *why* it stopped and *why* it escalated

### Chapter 3 — Evaluation & Acceptance: Reproducible Stage Gates
This repo is not a leaderboard. It is an acceptance framework.

Chapter 3 defines:
- acceptance criteria based on **compliance distributions**
- generalization across seeds and structural breaks
- boundary-time targets and constraint margins
- comparative baselines (conservative + robust references)
- exportable “advance / do-not-advance” decisions

Deliverable expectation:
- promotion is earned via artifacts and gates, not vibes

---

## Notebooks (how they map to the 3 chapters)

The notebooks are not “examples.” They are the operational proof of the book.

- **Chapter 1 notebooks** focus on:
  - proxy contract discipline
  - fact/assumption/open separation
  - reproducible synthetic setups
  - early termination and escalation posture

- **Chapter 2 notebooks** focus on:
  - constrained control loops
  - explicit state machines and routing
  - constraint enforcement + margin tracking
  - bounded retries and safe failure

- **Chapter 3 notebooks** focus on:
  - evaluation harnesses
  - compliance distributions across seeds
  - structural break stress testing
  - stage-gate promotion artifacts

(Notebook names and exact numbering live in **/notebooks/** and should be read as the lab companion to the corresponding book chapter.)

---

## What every notebook enforces (non-negotiable)

This repository follows a strict laboratory contract. Every notebook must:

- run **synthetic-first** (deterministic under seed)
- define explicit **state** (TypedDict or equivalent)
- implement **bounded loops** (no unbounded retries)
- implement **termination reasons** (stop is a feature, not a bug)
- enforce **facts vs assumptions vs open items** separation
- export review artifacts **every run**, including at minimum:
  - `run_manifest.json` (seed, versions, config hash, environment fingerprint)
  - `final_state.json` (what the system believed at the end)
  - `decision.json` (advance / revise / reject + reasons)
  - `risk_log.json` (risks triggered + controls applied)
  - `artifacts/` folder for any generated deliverables

This is not extra process.  
This is what makes surrogacy *reviewable*.

---

## How to use this repository

Recommended posture:

1) Read the relevant **chapter** in **/book/** (mechanism + acceptance rules).
2) Run the corresponding **notebook(s)** in **/notebooks/** as-is (no edits).
3) Inspect artifacts: termination reason, constraint margins, open items.
4) Stress structurally: change regimes, tighten constraints, reduce evidence.
5) Record failures as artifacts (don’t hand-wave them away).
6) Modify **one mechanism at a time**, then re-run and compare artifacts.

Operating rule:
If the system “works” only when you ignore gates, constraints, or termination logic, then it does not work.

---

## Shared governance spine (applies across this repo)

- **Generation ≠ verification**  
  Outputs are **Not verified** until qualified humans validate them.

- **Facts vs assumptions discipline**  
  Facts provided, assumptions made, and open questions are separated explicitly.

- **Scope and boundary control**  
  Clear stop-if rules, escalation paths, and refusal posture where required.

- **Auditability by design**  
  Artifacts enable reconstruction, supervision, and review.

- **Human accountability**  
  Responsibility never leaves the human professional.

---

## IMPORTANT DISCLAIMERS (read before use)

### Educational / Non-Reliance
All materials are provided **for educational and research purposes only**.  
Nothing in this repository constitutes investment, trading, legal, tax, accounting, audit, or compliance advice.

### Not verified
Unless explicitly stated otherwise in a specific artifact, treat all outputs, claims, calculations, citations, and conclusions as **Not verified**.

### Confidentiality and data hygiene
Do not paste confidential, proprietary, regulated, or personally identifying information into external systems.  
Use anonymization/redaction and **minimum-necessary** inputs by default.

### No fabricated sources or claims
Zero tolerance for invented citations, performance claims, fees, terms, or consequences.  
When evidence is missing, the correct output is a **verification task list**, not persuasive narrative.

---

## License (MIT)

This project is released under the **MIT License**.

**Copyright (c) 2026 Alejandro Reynoso**

---

## Contact

Alejandro Reynoso  
Email: areynoso@yahoo.com  
GitHub: https://github.com/alexdibol
