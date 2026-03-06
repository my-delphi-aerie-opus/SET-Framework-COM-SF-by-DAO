# SET Framework

> **Socio · Econo · Tech** — A multi-dimensional organizational assessment framework for evaluating structural, economic, and technical maturity across complex enterprises.

---

## Table of Contents

- [Overview](#overview)
- [Framework Architecture](#framework-architecture)
- [Pillar I — Socio](#pillar-i--socio)
  - [D1 · Business Mission](#d1--business-mission)
  - [D2 · Gov / Regulatory](#d2--gov--regulatory)
  - [D3 · People](#d3--people)
- [Pillar II — Econo](#pillar-ii--econo)
  - [D4 · Capital Flow](#d4--capital-flow)
  - [D5 · Culture](#d5--culture)
  - [D6 · Constraints](#d6--constraints)
- [Pillar III — Tech](#pillar-iii--tech)
  - [D7 · Process](#d7--process)
  - [D8 · Technical](#d8--technical)
  - [D9 · Threat Landscape](#d9--threat-landscape)
- [Scoring Logic](#scoring-logic)
  - [Maturity Scale](#maturity-scale)
  - [Factor Weight Distribution](#factor-weight-distribution)
  - [Score Aggregation Model](#score-aggregation-model)
- [Composite Scoring](#composite-scoring)
- [Interpretation Guide](#interpretation-guide)
- [Usage by Organizations](#usage-by-organizations)
- [Changelog](#changelog)

---

## Overview

The **SET Framework** is a structured organizational assessment model designed to evaluate how an organization is positioned across three interdependent pillars: **Socio**, **Econo**, and **Tech**. It provides a systematic, weighted scoring methodology that enables practitioners to derive a dimensional profile of any enterprise — surfacing strengths, gaps, and risk concentrations.

The framework is built for use in:

- Security program scoping and maturity baselining
- Organizational capability gap analysis
- Strategic investment prioritization
- M&A due diligence and post-merger integration planning
- Regulatory compliance readiness assessment

Each pillar contains three **Dimensional Factors**, each decomposed into **Primary Factors** with defined selection logic and weighted contribution scores.

---

## Framework Architecture

```
SET Framework
├── Pillar I: Socio
│   ├── D1 · Business Mission
│   │   ├── Critical Revenue Dependency           [40%]
│   │   ├── Structural Org Topology               [30%]
│   │   └── Strategic Competitive Risk Posture    [30%]
│   ├── D2 · Gov / Regulatory
│   │   ├── Statutory Compliance & Legal Rigidity [55%]
│   │   └── Geopolitical Data & People Sovereignty[45%]
│   └── D3 · People
│       ├── Technical vs. Managerial Career Arch  [50%]
│       └── Scarcity-Based Compensation Elasticity[50%]
│
├── Pillar II: Econo
│   ├── D4 · Capital Flow
│   │   ├── Multi-Year Funding Logic              [35%]
│   │   ├── Specialized SME Labor Scarcity        [35%]
│   │   └── Data Intensity & Telemetry Scale      [30%]
│   ├── D5 · Culture
│   │   ├── Product & Innovation Velocity         [50%]
│   │   └── Enterprise-wide Cyber-Accountability  [50%]
│   └── D6 · Constraints
│       ├── Executive Sponsorship & Influence Depth[55%]
│       └── M&A / Divestiture Frequency           [45%]
│
└── Pillar III: Tech
    ├── D7 · Process
    │   ├── Operational Workflow Maturity & Discipline [50%]
    │   └── Critical Asset & Business Service Mapping  [50%]
    ├── D8 · Technical
    │   ├── Telemetry Cohesion & Interoperability      [50%]
    │   └── Org Engineering DNA & Automation Capability[50%]
    └── D9 · Threat Landscape
        ├── Adversary Sophistication & Intent          [55%]
        └── Attack Surface Structural Complexity       [45%]
```

---

## Pillar I — Socio

The **Socio** pillar captures the human, structural, and governance dimensions of an organization. It evaluates how mission-criticality, regulatory context, and people architecture shape the conditions under which any program must operate.

---

### D1 · Business Mission

> How deeply embedded is the organization's mission in digital continuity, structural complexity, and competitive risk sensitivity?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `1a` | Critical Revenue Dependency | 40% | Degree to which core revenue streams depend on digital continuity and operational uptime. High dependency = elevated consequence of disruption. |
| `1b` | Structural Org Topology | 30% | Complexity of org structure — federated, hierarchical, matrixed — affecting decision velocity, accountability diffusion, and program alignment difficulty. |
| `1c` | Strategic Competitive Risk Posture | 30% | How competitive positioning amplifies or dampens the consequence of risk events. Organizations in hyper-competitive sectors face greater reputational and operational exposure. |

**Dimension Score Formula:**

```
D1 = (1a × 0.40) + (1b × 0.30) + (1c × 0.30)
```

**Practitioner Notes:**
- `1a` is the primary driver. Revenue dependency directly determines the blast radius of any operational disruption.
- `1b` should be assessed against the org chart but also informally — shadow hierarchies and informal power structures matter as much as reporting lines.
- `1c` is industry-contextual. A regulated monopoly carries different competitive risk than a venture-backed SaaS challenger.

---

### D2 · Gov / Regulatory

> What is the density and rigidity of the compliance and sovereignty obligations binding the organization?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `2a` | Statutory Compliance & Legal Rigidity | 55% | Binding regulatory obligations — GDPR, HIPAA, PCI-DSS, SOX, NIS2, etc. — that constrain architectural and operational choices and introduce legal liability. |
| `2b` | Geopolitical Data & People Sovereignty | 45% | Cross-border data residency requirements, workforce nationality constraints, and exposure to state-level interference, sanctions, or data access demands. |

**Dimension Score Formula:**

```
D2 = (2a × 0.55) + (2b × 0.45)
```

**Practitioner Notes:**
- `2a` is weighted higher because statutory obligations are typically non-negotiable and carry direct financial and criminal penalties.
- `2b` is increasingly relevant as organizations operate across jurisdictions with conflicting data sovereignty laws (e.g., EU GDPR vs. US CLOUD Act).
- Sector examples with high D2 scores: financial services, healthcare, critical national infrastructure, defense contractors.

---

### D3 · People

> How does career architecture and compensation structure shape the organization's ability to attract, retain, and leverage critical human capital?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `3a` | Technical vs. Managerial Career Architecture | 50% | Whether career paths reward deep technical mastery or default to management tracks, shaping retention of critical individual contributors and specialized talent. |
| `3b` | Scarcity-Based Compensation Elasticity | 50% | The organization's ability to dynamically compensate for skills in short supply (e.g., threat intelligence, OT security, ML engineering) without triggering structural pay band friction. |

**Dimension Score Formula:**

```
D3 = (3a × 0.50) + (3b × 0.50)
```

**Practitioner Notes:**
- `3a` is a structural indicator. Organizations with engineering-track career ladders (e.g., Staff/Principal/Distinguished Engineer titles) score higher — they retain deep expertise longer.
- `3b` is an economic-cultural signal. HR systems with rigid compensation bands in high-scarcity skill markets will consistently underperform in talent acquisition and retention.
- D3 has strong interdependency with D4 (`Capital Flow`) and D5 (`Culture`).

---

## Pillar II — Econo

The **Econo** pillar evaluates the financial, cultural, and structural economic forces that govern how an organization funds, prioritizes, and sustains capability. It captures the economic logic of investment — and the constraints that shape it.

---

### D4 · Capital Flow

> How does the organization's funding model, labor economics, and data infrastructure investment posture shape program sustainability?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `4a` | Multi-Year Funding Logic | 35% | Stability and predictability of capital allocation cycles — CapEx vs. OpEx orientation, annual budget cycles vs. multi-year program investment, and resilience of funding under leadership change. |
| `4b` | Specialized SME Labor Scarcity | 35% | Market scarcity and fully-loaded cost-to-acquire for niche subject matter experts driving total program cost. Relevant for roles in OT/ICS, red teaming, cloud security architecture, and AI safety. |
| `4c` | Data Intensity & Telemetry Scale | 30% | Volume, velocity, and variety of data instrumentation required to operate the program, impacting storage, processing, and tooling cost trajectory at scale. |

**Dimension Score Formula:**

```
D4 = (4a × 0.35) + (4b × 0.35) + (4c × 0.30)
```

**Practitioner Notes:**
- `4a` and `4b` are equally weighted as co-primary drivers. Unstable funding and unaffordable talent are the two most common program killers.
- `4c` should be evaluated against current telemetry architecture. Organizations running SIEM/XDR/UEBA at enterprise scale will have significantly higher data cost curves.
- CapEx-dominant organizations (e.g., utilities, manufacturing) often score lower on `4a` due to long budget cycles and limited OpEx flexibility.

---

### D5 · Culture

> Does the organization's cultural velocity and accountability model accelerate or resist program adoption?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `5a` | Product & Innovation Velocity | 50% | Speed at which the organization ships new capability — a proxy for how rapidly the risk surface changes and how quickly security must adapt, integrate, and respond. |
| `5b` | Enterprise-wide Cyber-Accountability | 50% | Whether risk ownership is diffused across business functions or siloed in a single team. Distinguishes organizations with genuine shared accountability from those where security is a penalty center. |

**Dimension Score Formula:**

```
D5 = (5a × 0.50) + (5b × 0.50)
```

**Practitioner Notes:**
- `5a` is not just a development speed metric — it is a signal of how rapidly new attack surface is introduced and whether security can keep pace without becoming a bottleneck.
- `5b` is the most culturally sensitive factor in the framework. Low scores here often indicate that security is perceived as compliance overhead rather than business enablement.
- Organizations with high `5a` and low `5b` represent the highest-risk cultural profile: fast-moving but accountability-diffused.

---

### D6 · Constraints

> What structural and organizational ceiling limits exist on program ambition and execution authority?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `6a` | Executive Sponsorship & Influence Depth | 55% | How high and how wide executive mandate extends for security investment, behavioral change, and org-level prioritization. CISO reporting line and C-suite alignment are key signals. |
| `6b` | M&A / Divestiture Frequency | 45% | Rate of corporate restructuring events — acquisitions, spin-offs, carve-outs, mergers — that introduce integration complexity, inherited risk, and attack surface volatility. |

**Dimension Score Formula:**

```
D6 = (6a × 0.55) + (6b × 0.45)
```

**Practitioner Notes:**
- `6a` is the single highest-weighted primary factor in the Econo pillar. Programs without genuine executive sponsorship at CEO/Board level rarely sustain transformational investment.
- `6b` is directional — high M&A frequency is not inherently bad, but it represents a consistent injection of uncontrolled variables into the program's scope and risk surface.
- Note that `6b` scoring is **inverse**: a higher frequency of M&A activity corresponds to a lower organizational maturity score on this factor, as it signals structural instability and integration debt.

---

## Pillar III — Tech

The **Tech** pillar evaluates the operational, engineering, and adversarial dimensions of the organization's technical estate. It captures process discipline, technical capability, and threat exposure as a unified technical maturity signal.

---

### D7 · Process

> How mature are the organization's operational workflows, and how well does it understand the relationship between its technology and business services?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `7a` | Operational Workflow Maturity & Discipline | 50% | Consistency, documentation, and enforcement of core operational processes — incident response, change management, access governance — as a signal of control quality and change management capability. |
| `7b` | Critical Asset & Business Service Mapping | 50% | Quality, currency, and completeness of asset inventory and the mapping between technology components and the business services they underpin. |

**Dimension Score Formula:**

```
D7 = (7a × 0.50) + (7b × 0.50)
```

**Practitioner Notes:**
- `7a` and `7b` are equally weighted because they are interdependent. Process discipline without asset visibility is theater; asset mapping without operational discipline is an unmaintained spreadsheet.
- `7b` is often an organization's most honest signal of operational maturity. Organizations that cannot credibly answer "what are your crown jewels and where do they live?" score 1–2 here regardless of tooling investment.
- High D7 scores are a prerequisite for meaningful D8 and D9 performance. Poor process foundations undermine technical capability.

---

### D8 · Technical

> How cohesive is the organization's telemetry architecture and how deeply embedded is engineering culture in its security operations?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `8a` | Telemetry Cohesion & Interoperability | 50% | Degree to which monitoring signals across endpoints, network, cloud, identity, and application layers are unified, correlated, normalized, and actionable in real time. |
| `8b` | Organizational Engineering DNA & Automation Capability | 50% | Depth of software engineering culture within security and operations functions — enabling automation of detection logic, response playbooks, and operational toil reduction at scale. |

**Dimension Score Formula:**

```
D8 = (8a × 0.50) + (8b × 0.50)
```

**Practitioner Notes:**
- `8a` is a direct proxy for detection fidelity. Fragmented telemetry — siloed SIEMs, disconnected EDR, incomplete cloud logging — produces blind spots that adversaries will exploit.
- `8b` distinguishes organizations that "use security tools" from organizations that "build security capability." High scorers have security engineers writing detection-as-code, automating triage, and building internal tooling.
- The `8a`/`8b` combination is a strong predictor of mean-time-to-detect (MTTD) and mean-time-to-respond (MTTR) performance.

---

### D9 · Threat Landscape

> What is the sophistication and structural complexity of the threat environment the organization operates within?

| ID | Primary Factor | Weight | Selection Logic |
|:---|:---|:---:|:---|
| `9a` | Adversary Sophistication & Intent | 55% | Profile of threat actors targeting the organization — nation-state APTs, organized eCrime, hacktivists — and their demonstrated operational maturity, tooling, and persistence. |
| `9b` | Attack Surface Structural Complexity | 45% | Breadth, depth, and interconnectedness of the digital estate: cloud sprawl, legacy technology debt, third-party supply chain exposure, OT/IT convergence, and shadow IT prevalence. |

**Dimension Score Formula:**

```
D9 = (9a × 0.55) + (9b × 0.45)
```

**Practitioner Notes:**
- `9a` should be informed by threat intelligence specific to the organization's sector, geography, and profile. Generic scores are not useful here — input from a CTI function or sector ISAC is recommended.
- `9b` is partially within the organization's control (attack surface reduction) but is also a function of business decisions (cloud adoption, third-party integrations, M&A). Evaluate as a current-state snapshot.
- D9 acts as a **risk multiplier** in composite scoring interpretation. High D9 scores in organizations with low D7 and D8 scores represent the highest-urgency remediation priority profile.
- Note: `9a` scoring is **directional** — higher adversary sophistication means a worse organizational position, not a better one. Scoring convention: `1 = Optimized` (low threat), `5 = Nascent` (extreme threat exposure). Invert for composite aggregation.

---

## Scoring Logic

### Maturity Scale

All primary factors are scored on a **1–5 integer scale**:

| Score | Label | Definition |
|:---:|:---|:---|
| **1** | Nascent | No formal capability exists. Approach is entirely ad hoc, reactive, and undocumented. |
| **2** | Developing | Awareness and intent exist; initiatives are fragmented, inconsistent, or in early stages. |
| **3** | Established | Documented, repeatable processes are in place; capability is functional but meaningful gaps remain. |
| **4** | Advanced | Measured, proactive, and well-integrated capability; approaching best-in-class. |
| **5** | Optimized | Continuous improvement culture; industry-leading maturity with evidence of sustained performance. |

> **Note:** For factors where higher real-world values represent a worse organizational posture (e.g., `6b` M&A Frequency, `9a` Adversary Sophistication), scores must be **inverted** before aggregation. See [Score Aggregation Model](#score-aggregation-model).

---

### Factor Weight Distribution

Weights within each dimension reflect the relative influence of each primary factor on the dimension's overall signal. All weights within a dimension sum to `1.00`.

| Dim | Factor ID | Factor Label | Weight |
|:---|:---|:---|:---:|
| D1 | `1a` | Critical Revenue Dependency | 0.40 |
| D1 | `1b` | Structural Org Topology | 0.30 |
| D1 | `1c` | Strategic Competitive Risk Posture | 0.30 |
| D2 | `2a` | Statutory Compliance & Legal Rigidity | 0.55 |
| D2 | `2b` | Geopolitical Data & People Sovereignty | 0.45 |
| D3 | `3a` | Technical vs. Managerial Career Architecture | 0.50 |
| D3 | `3b` | Scarcity-Based Compensation Elasticity | 0.50 |
| D4 | `4a` | Multi-Year Funding Logic | 0.35 |
| D4 | `4b` | Specialized SME Labor Scarcity | 0.35 |
| D4 | `4c` | Data Intensity & Telemetry Scale | 0.30 |
| D5 | `5a` | Product & Innovation Velocity | 0.50 |
| D5 | `5b` | Enterprise-wide Cyber-Accountability | 0.50 |
| D6 | `6a` | Executive Sponsorship & Influence Depth | 0.55 |
| D6 | `6b` | M&A / Divestiture Frequency | 0.45 |
| D7 | `7a` | Operational Workflow Maturity & Discipline | 0.50 |
| D7 | `7b` | Critical Asset & Business Service Mapping | 0.50 |
| D8 | `8a` | Telemetry Cohesion & Interoperability | 0.50 |
| D8 | `8b` | Org Engineering DNA & Automation Capability | 0.50 |
| D9 | `9a` | Adversary Sophistication & Intent | 0.55 |
| D9 | `9b` | Attack Surface Structural Complexity | 0.45 |

---

### Score Aggregation Model

Scores aggregate bottom-up through three levels: **Factor → Dimension → Pillar → Composite**.

#### Level 1 — Dimension Score

Each dimension score is the weighted sum of its primary factor scores:

```
Dₙ = Σ (factor_score × factor_weight)
```

Example — D1:
```
D1 = (score_1a × 0.40) + (score_1b × 0.30) + (score_1c × 0.30)
```

#### Level 2 — Pillar Score

Each pillar score is the unweighted arithmetic mean of its three dimension scores:

```
Pillar_Score = (Dₓ + Dᵧ + D_z) / 3
```

Example — Socio:
```
Socio = (D1 + D2 + D3) / 3
```

#### Level 3 — Composite Score

The composite organizational score is the unweighted arithmetic mean of the three pillar scores:

```
Composite = (Socio + Econo + Tech) / 3
```

The composite score falls on the same 1–5 scale and maps to the [Maturity Scale](#maturity-scale) labels.

#### Full Expanded Formula

```
Composite =
  [
    ((1a×0.40 + 1b×0.30 + 1c×0.30) +
     (2a×0.55 + 2b×0.45) +
     (3a×0.50 + 3b×0.50)) / 3   ← Socio
    +
    ((4a×0.35 + 4b×0.35 + 4c×0.30) +
     (5a×0.50 + 5b×0.50) +
     (6a×0.55 + 6b×0.45)) / 3   ← Econo
    +
    ((7a×0.50 + 7b×0.50) +
     (8a×0.50 + 8b×0.50) +
     (9a×0.55 + 9b×0.45)) / 3   ← Tech
  ] / 3
```

---

## Composite Scoring

| Composite Range | Label | Organizational Profile |
|:---|:---|:---|
| `1.00 – 1.79` | **Nascent** | Foundational gaps across most pillars. High urgency for baseline capability investment before any advanced program work. |
| `1.80 – 2.59` | **Developing** | Pockets of capability exist but are inconsistent. Program investment should prioritize anchor dimensions before expanding scope. |
| `2.60 – 3.39` | **Established** | Core foundations in place. Focus shifts from building to scaling and integrating existing capabilities more cohesively. |
| `3.40 – 4.19` | **Advanced** | Strong, proactive posture. Investment focus should be on resilience, automation, and expanding to edge capability areas. |
| `4.20 – 5.00` | **Optimized** | Industry-leading maturity. Program focus is on continuous improvement, threat intelligence operationalization, and innovation. |

---

## Interpretation Guide

### Reading a Dimensional Profile

A single composite score is a starting point, not a conclusion. The diagnostic value of the SET Framework lies in the **shape** of the dimensional profile — the pattern of scores across all nine dimensions and three pillars.

**Key interpretive patterns:**

**Pillar Imbalance** — A significant spread between pillar scores (e.g., Tech = 4.2, Socio = 1.8) indicates that technical capability is being built on an unstable organizational and human foundation. This is a fragility signal.

**Anchor Deficits** — A low score on D7 (Process) with high scores on D8 (Technical) and D9 (Threat Landscape) indicates an organization investing in advanced tooling without the operational discipline to use it effectively.

**Constraint Ceilings** — A low D6 (Constraints) score — particularly `6a` Executive Sponsorship — acts as a ceiling on all other dimensions. No dimension can sustainably score above the organization's executive will to support it.

**Threat-Capability Gap** — The spread between D9 (Threat Landscape) and the average of D7 + D8 is the most operationally critical signal in the framework. A large gap here indicates the organization is materially outpaced by its adversaries.

### Priority Sequencing Logic

When scores across dimensions vary significantly, use the following sequencing heuristic:

```
Priority 1  →  Any dimension scoring 1.0 – 1.5  (Critical baseline gap)
Priority 2  →  D6 (Constraints) if < 2.5        (Ceiling effect — blocks all others)
Priority 3  →  D7 (Process) if < 3.0            (Foundation required for D8 benefit)
Priority 4  →  Largest Threat-Capability Gap     (D9 score minus D7/D8 average)
Priority 5  →  Lowest Pillar average             (Structural imbalance correction)
```

---

## Usage by Organizations

The SET Framework is designed to be applied at the **enterprise program level** by practitioners performing organizational assessment, strategy development, or investment scoping. Below are the primary use cases.

### Security Program Scoping

Organizations use the SET Framework to determine the appropriate scale, pace, and composition of a security program before committing capital. The dimensional profile reveals which pillars require foundational investment versus which are ready for capability advancement.

**Who applies it:** CISOs, security architects, program directors
**Inputs required:** Stakeholder interviews, documentation review, threat intelligence briefing
**Output:** Dimensional scorecard, priority sequencing recommendation, program scope boundaries

---

### Organizational Baseline Assessment

A structured baseline engagement captures a point-in-time score across all nine dimensions. This creates an evidence-backed maturity snapshot that can be used to track program progress over time, benchmark against peer organizations, or support board-level reporting.

**Recommended cadence:** Annually (full assessment) + semi-annually (delta review on Priority 1–3 dimensions)

---

### Strategic Investment Prioritization

When competing for limited capital, the framework provides a structured rationale for investment sequencing. Dimensions with low scores and high weight contributions to the composite drive the largest improvement per dollar spent.

**Investment efficiency heuristic:**

```
ΔComposite per investment unit = (Target_Score - Current_Score) × Dimension_Weight_in_Composite
```

---

### M&A Due Diligence

Prior to acquisition close, applying the SET Framework to the target organization produces a structured risk profile that informs integration planning, deal pricing adjustments, and Day 1 remediation priorities.

**Focus dimensions in M&A context:** D1 (Business Mission), D2 (Gov/Regulatory), D6 (Constraints), D9 (Threat Landscape)

---

### Regulatory Readiness Assessment

The framework's D2 dimension, combined with D7 (Process) and D8 (Technical), provides a structured lens for evaluating readiness against specific regulatory frameworks (NIS2, DORA, ISO 27001, SOC 2, NIST CSF). Dimension scores map to control domain maturity levels.

---

### Vendor & Third-Party Risk Profiling

A condensed version of the framework can be applied to critical third-party suppliers and managed service providers to produce a comparable risk profile, enabling like-for-like comparison across the supply chain.

**Recommended condensed set for third-party use:** D2, D7, D8, D9

---

## Changelog

| Version | Date | Notes |
|:---|:---|:---|
| `v1.0` | 2026-03 | Initial framework definition. 3 pillars, 9 dimensions, 20 primary factors. Weighted aggregation model established. |

---

> **Framework Author:** SET Framework Working Group
> **License:** Internal Use — Not for redistribution without attribution.
> **Status:** `Active — v1.0`
