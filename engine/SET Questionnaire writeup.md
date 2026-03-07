# SET Framework Assessment Engine
### Technical Reference for Researchers & Field Practitioners

> **Version:** 1.0  
> **Status:** Active  
> **Application Domain:** Cybersecurity Program Strategy & Organizational Maturity Assessment  
> **Assessment Mode:** Qualitative, Weighted, Generative Output Classification

---

## Table of Contents

- [1. Overview](#1-overview)
- [2. Theoretical Basis](#2-theoretical-basis)
  - [2.1 Design Philosophy](#21-design-philosophy)
  - [2.2 Why Qualitative Scoring](#22-why-qualitative-scoring)
  - [2.3 Why Generative Output](#23-why-generative-output)
- [3. Framework Architecture](#3-framework-architecture)
  - [3.1 Structural Hierarchy](#31-structural-hierarchy)
  - [3.2 The Nine Dimensions](#32-the-nine-dimensions)
  - [3.3 Sub-Factor Inventory](#33-sub-factor-inventory)
- [4. Scoring Model](#4-scoring-model)
  - [4.1 Maturity Scale](#41-maturity-scale)
  - [4.2 Descriptive Anchors](#42-descriptive-anchors)
  - [4.3 Sub-Factor Scoring](#43-sub-factor-scoring)
  - [4.4 Dimension Score Computation](#44-dimension-score-computation)
  - [4.5 Dimension Weight Configuration](#45-dimension-weight-configuration)
  - [4.6 Composite Score Computation](#46-composite-score-computation)
  - [4.7 Pillar Averages](#47-pillar-averages)
  - [4.8 Full Expanded Formula](#48-full-expanded-formula)
- [5. Output Classification Engine](#5-output-classification-engine)
  - [5.1 Classification Philosophy](#51-classification-philosophy)
  - [5.2 Classical Archetype Reference Vectors](#52-classical-archetype-reference-vectors)
  - [5.3 Cosine Similarity Algorithm](#53-cosine-similarity-algorithm)
  - [5.4 Classification Threshold Logic](#54-classification-threshold-logic)
  - [5.5 Novel Model Naming Algorithm](#55-novel-model-naming-algorithm)
  - [5.6 Threat-Capability Gap Signal](#56-threat-capability-gap-signal)
  - [5.7 Priority Sequencing](#57-priority-sequencing)
- [6. Digital Implementation](#6-digital-implementation)
  - [6.1 Technology Stack](#61-technology-stack)
  - [6.2 Phase Architecture](#62-phase-architecture)
  - [6.3 State Model](#63-state-model)
  - [6.4 Data Structures](#64-data-structures)
  - [6.5 Component Breakdown](#65-component-breakdown)
  - [6.6 Computation Pipeline](#66-computation-pipeline)
- [7. Physical On-Site Adaptation](#7-physical-on-site-adaptation)
  - [7.1 Field Assessment Overview](#71-field-assessment-overview)
  - [7.2 Pre-Assessment Preparation](#72-pre-assessment-preparation)
  - [7.3 Weight Configuration Protocol](#73-weight-configuration-protocol)
  - [7.4 Interview & Survey Protocol](#74-interview--survey-protocol)
  - [7.5 Scoring Sheet Templates](#75-scoring-sheet-templates)
  - [7.6 Manual Computation Procedure](#76-manual-computation-procedure)
  - [7.7 Output Interpretation in the Field](#77-output-interpretation-in-the-field)
  - [7.8 Evidence Standards](#78-evidence-standards)
- [8. Assessor Guidance](#8-assessor-guidance)
  - [8.1 Stakeholder Mapping](#81-stakeholder-mapping)
  - [8.2 Interview Question Bank](#82-interview-question-bank)
  - [8.3 Common Scoring Errors](#83-common-scoring-errors)
  - [8.4 Inter-Rater Reliability](#84-inter-rater-reliability)
- [9. Validation & Calibration](#9-validation--calibration)
  - [9.1 Baseline Calibration Exercise](#91-baseline-calibration-exercise)
  - [9.2 Sensitivity Analysis](#92-sensitivity-analysis)
  - [9.3 Suggested Validation Studies](#93-suggested-validation-studies)
- [10. Extending the Framework](#10-extending-the-framework)
  - [10.1 Adding Dimensions](#101-adding-dimensions)
  - [10.2 Adding Archetypes](#102-adding-archetypes)
  - [10.3 Industry-Specific Presets](#103-industry-specific-presets)
  - [10.4 Longitudinal Tracking](#104-longitudinal-tracking)
- [11. Worked Example](#11-worked-example)
- [12. Limitations & Research Gaps](#12-limitations--research-gaps)
- [13. Glossary](#13-glossary)
- [14. Changelog](#14-changelog)

---

## 1. Overview

The **SET Framework Assessment Engine** is a structured, evidence-based methodology for profiling organizational cybersecurity posture across three interdependent pillars — **Socio**, **Econo**, and **Tech** — decomposed into nine weighted dimensions and twenty primary sub-factors.

The engine operates in three sequential phases:

1. **Configure** — The assessor assigns percentage weights to each of the nine dimensions, summing to exactly 100%, to reflect the assessed relevance of each dimension for the specific organizational context.
2. **Assess** — Each of the twenty sub-factors is scored 1–5 using descriptive behavioural anchors, producing a qualitative evidence-grounded rating.
3. **Output** — Scores are aggregated through a weighted computation model to produce a composite maturity score, a dimensional profile, and a generative strategic model classification.

The framework is designed to be **context-adaptive**: the weight configuration layer allows any two assessors evaluating different organizations — even within the same industry — to produce structurally different composite models that accurately reflect the unique conditions of each subject organization.

The output is **generative, not classificatory**: the framework does not pre-assign organizations to archetypes. Instead, it derives a strategic model from the dimensional data, then compares the result against classical reference vectors to determine whether the output resembles a known model, a hybrid of known models, or constitutes a novel configuration not previously defined in the field.

---

## 2. Theoretical Basis

### 2.1 Design Philosophy

Most existing cybersecurity maturity frameworks — CMMI, NIST CSF, ISO 27001 maturity mappings — are **prescriptive and conformance-oriented**: they measure how closely an organization matches a defined ideal state. This is useful for compliance tracking but insufficient for strategic program design, because organizations are not static entities moving toward a fixed target. They are structurally, economically, and technically differentiated organisms whose optimal security program architecture is a function of their specific conditions, not a generic best practice.

The SET Framework inverts this logic. Rather than asking *"how close is this organization to a defined ideal?"*, it asks *"given the complete dimensional profile of this organization, what is the most appropriate strategic program architecture for its specific conditions?"*

This shifts the framework from a **conformance model** to a **generative model**.

### 2.2 Why Qualitative Scoring

Cybersecurity organizational factors resist precise quantification. It is impossible to assign a numerically exact score to "executive sponsorship depth" or "career architecture maturity" without reducing complex, context-dependent organizational realities to numbers that carry false precision.

The 1–5 maturity scale with descriptive behavioural anchors addresses this by:

- Grounding each score in observable, describable organizational conditions rather than arbitrary numerical assignments.
- Enabling consistent scoring across different assessors through shared anchor language.
- Producing scores that are **ordinal** (rank-ordered) rather than **cardinal** (arithmetically precise), which is epistemologically honest about what organizational assessment can actually measure.

The use of weighted aggregation on ordinal scores introduces a known approximation — treating ordinal intervals as arithmetic. This is a deliberate and documented trade-off: the aggregation model sacrifices mathematical purity in order to produce a tractable composite output useful for decision-making. Assessors and researchers should be aware of this limitation. See [Section 12](#12-limitations--research-gaps).

### 2.3 Why Generative Output

Classical cybersecurity program archetypes — Compliance-Centric, Zero Trust, Threat-Informed Defense, etc. — were developed under specific industry conditions and organizational assumptions. They represent useful reference models but poor universal prescriptions.

Many organizations, when profiled honestly, do not fit cleanly into any classical archetype. Forcing a fit introduces strategic misalignment: the organization invests in program components designed for a different context, and under-invests in areas that its specific dimensional profile demands.

The SET output engine uses cosine similarity against classical reference vectors to determine fit. When fit is high (≥97.5%), the classical archetype is confirmed. When fit is partial (≥92%), a hybrid designation is used. When fit is low (<92%), the engine generates a novel model name derived directly from the dimensional signature — making the output a product of the data, not a lookup.

---

## 3. Framework Architecture

### 3.1 Structural Hierarchy

```
SET Framework
│
├── 3 Pillars  (Socio, Econo, Tech)
│   │
│   ├── 3 Dimensions per Pillar  (9 total: D1–D9)
│   │   │
│   │   └── 2–3 Sub-Factors per Dimension  (20 total)
│   │       │
│   │       └── 5 Descriptive Anchors per Sub-Factor
│
└── Output Layer
    ├── Composite Score  (weighted, 1–5)
    ├── Pillar Averages  (descriptive, 1–5)
    ├── Threat-Capability Gap  (D9 vs D7+D8 avg)
    ├── Priority Dimensions  (bottom 3 by score)
    └── Strategic Model Classification  (Classical / Hybrid / Novel)
```

### 3.2 The Nine Dimensions

| ID | Pillar | Dimension | Sub-Factors | Default Weight |
|:---|:---|:---|:---:|:---:|
| D1 | Socio | Business Mission | 3 | 12% |
| D2 | Socio | Gov / Regulatory | 2 | 10% |
| D3 | Socio | People | 2 | 10% |
| D4 | Econo | Capital Flow | 3 | 12% |
| D5 | Econo | Culture | 2 | 10% |
| D6 | Econo | Constraints | 2 | 10% |
| D7 | Tech | Process | 2 | 12% |
| D8 | Tech | Technical | 2 | 12% |
| D9 | Tech | Threat Landscape | 2 | 12% |
| | | **Total** | **20** | **100%** |

> **Default weights** are provided as a neutral starting point only. They carry no normative significance. The assessor must configure weights for each assessment engagement based on the subject organization's context.

### 3.3 Sub-Factor Inventory

#### D1 — Business Mission
| ID | Sub-Factor |
|:---|:---|
| 1a | Critical Revenue Dependency |
| 1b | Structural Org Topology |
| 1c | Strategic Competitive Risk Posture |

#### D2 — Gov / Regulatory
| ID | Sub-Factor |
|:---|:---|
| 2a | Statutory Compliance & Legal Rigidity |
| 2b | Geopolitical Data & People Sovereignty |

#### D3 — People
| ID | Sub-Factor |
|:---|:---|
| 3a | Technical vs. Managerial Career Architecture |
| 3b | Scarcity-Based Compensation Elasticity |

#### D4 — Capital Flow
| ID | Sub-Factor |
|:---|:---|
| 4a | Multi-Year Funding Logic |
| 4b | Specialized SME Labor Scarcity |
| 4c | Data Intensity & Telemetry Scale |

#### D5 — Culture
| ID | Sub-Factor |
|:---|:---|
| 5a | Product & Innovation Velocity |
| 5b | Enterprise-wide Cyber-Accountability |

#### D6 — Constraints
| ID | Sub-Factor |
|:---|:---|
| 6a | Executive Sponsorship & Influence Depth |
| 6b | M&A / Divestiture Frequency |

#### D7 — Process
| ID | Sub-Factor |
|:---|:---|
| 7a | Operational Workflow Maturity & Discipline |
| 7b | Critical Asset & Business Service Mapping |

#### D8 — Technical
| ID | Sub-Factor |
|:---|:---|
| 8a | Telemetry Cohesion & Interoperability |
| 8b | Org Engineering DNA & Automation Capability |

#### D9 — Threat Landscape
| ID | Sub-Factor |
|:---|:---|
| 9a | Adversary Sophistication & Intent |
| 9b | Attack Surface Structural Complexity |

---

## 4. Scoring Model

### 4.1 Maturity Scale

All sub-factors are scored on a five-point ordinal maturity scale:

| Score | Label | Interpretation |
|:---:|:---|:---|
| 1 | **Nascent** | No formal capability. Approach is entirely ad hoc, reactive, and undocumented. |
| 2 | **Developing** | Awareness and intent exist; initiatives are fragmented, inconsistent, or early-stage. |
| 3 | **Established** | Documented, repeatable capability in place; functional but meaningful gaps remain. |
| 4 | **Advanced** | Measured, proactive, well-integrated; approaching best-in-class for sector. |
| 5 | **Optimized** | Continuous improvement culture; industry-leading with sustained evidence of performance. |

### 4.2 Descriptive Anchors

Each sub-factor has five descriptive behavioural anchors — one per score level. Anchors describe concrete, observable organizational conditions at each maturity level for that specific factor. They serve three functions:

1. **Grounding** — Prevent score inflation or deflation by anchoring scores to described reality rather than assessor intuition.
2. **Consistency** — Enable different assessors to arrive at the same score for the same organization independently, supporting inter-rater reliability.
3. **Evidence linkage** — Provide a reference description that the assessor can match to gathered evidence (interview notes, documents, observations).

> **Field instruction:** During scoring, the assessor should select the anchor that most accurately describes the organization's *current operational state*, not its aspirational state, documented policy, or stated intent. What is practiced consistently and verifiably is what is scored.

### 4.3 Sub-Factor Scoring

Each of the 20 sub-factors receives a single integer score `s ∈ {1, 2, 3, 4, 5}`.

Sub-factors within a dimension carry **equal weight** — there is no sub-factor-level weighting. This is a deliberate design choice: differential sub-factor weighting introduces additional configuration complexity that would require domain expertise to calibrate reliably, and the marginal precision gain does not justify the added assessor burden for most applications.

Researchers wishing to implement sub-factor-level weighting can extend the model by introducing a secondary weight vector at the sub-factor level. See [Section 10.1](#101-adding-dimensions).

### 4.4 Dimension Score Computation

The dimension score is the arithmetic mean of all sub-factor scores within that dimension:

```
D_n = (1 / k) × Σ s_i     for i = 1 to k
```

Where:
- `D_n` = dimension score for dimension n
- `k` = number of sub-factors in dimension n
- `s_i` = score assigned to sub-factor i

**Example — D1 (Business Mission, 3 sub-factors):**
```
D1 = (s_1a + s_1b + s_1c) / 3
   = (4 + 3 + 4) / 3
   = 3.67
```

**Example — D2 (Gov / Regulatory, 2 sub-factors):**
```
D2 = (s_2a + s_2b) / 2
   = (5 + 4) / 2
   = 4.50
```

The dimension score is a continuous real number in the range `[1.00, 5.00]`.

### 4.5 Dimension Weight Configuration

Each of the nine dimensions is assigned a percentage weight `w_n` by the assessor, subject to the constraint:

```
Σ w_n = 100     for n = D1 to D9
```

Weights must sum to exactly 100%. No partial completion is permitted — the composite computation is undefined unless all nine weights are assigned and sum to 100%.

**Weight assignment principles:**
- Weights reflect the **relative strategic importance** of each dimension given the subject organization's context, industry, and regulatory environment.
- A dimension that is structurally irrelevant to the subject organization (e.g., D2 Gov/Regulatory for an unregulated startup) should receive a low weight, not be excluded — exclusion would require renormalization and changes the compositional logic.
- Weights encode the assessor's expert judgment about organizational context. They should be documented and justified in the assessment report.

### 4.6 Composite Score Computation

The composite score is the weighted sum of all dimension scores:

```
C = Σ (D_n × w_n / 100)     for n = D1 to D9
```

Where:
- `C` = composite score
- `D_n` = dimension score for dimension n
- `w_n` = assessor-assigned weight for dimension n (as a percentage)

The composite score is a continuous real number in the range `[1.00, 5.00]`.

**Composite score interpretation:**

| Range | Label | Strategic Implication |
|:---|:---|:---|
| 1.00 – 1.79 | Nascent | Foundational gaps across most dimensions. Program must build baseline capability before advanced investment. |
| 1.80 – 2.59 | Developing | Pockets of capability exist but are inconsistent. Prioritize anchor dimensions before expanding scope. |
| 2.60 – 3.39 | Established | Core foundations in place. Focus shifts to scaling and integrating existing capabilities. |
| 3.40 – 4.19 | Advanced | Strong proactive posture. Investment focus: resilience, automation, edge capability. |
| 4.20 – 5.00 | Optimized | Industry-leading maturity. Focus: continuous improvement and intelligence-led operations. |

### 4.7 Pillar Averages

Pillar averages are computed as unweighted arithmetic means of the dimension scores within each pillar. They are **descriptive signals only** — they do not contribute directly to the composite score computation.

```
Pillar_Socio = (D1 + D2 + D3) / 3
Pillar_Econo = (D4 + D5 + D6) / 3
Pillar_Tech  = (D7 + D8 + D9) / 3
```

Pillar averages are used in the output phase to:
- Identify structural imbalances between pillars (e.g., Tech advanced, Socio nascent).
- Label the dominant and deficient pillars for novel model naming.
- Support narrative interpretation of organizational posture.

### 4.8 Full Expanded Formula

```
C =   (((s_1a + s_1b + s_1c) / 3) × w_D1 / 100)
    + (((s_2a + s_2b)         / 2) × w_D2 / 100)
    + (((s_3a + s_3b)         / 2) × w_D3 / 100)
    + (((s_4a + s_4b + s_4c) / 3) × w_D4 / 100)
    + (((s_5a + s_5b)         / 2) × w_D5 / 100)
    + (((s_6a + s_6b)         / 2) × w_D6 / 100)
    + (((s_7a + s_7b)         / 2) × w_D7 / 100)
    + (((s_8a + s_8b)         / 2) × w_D8 / 100)
    + (((s_9a + s_9b)         / 2) × w_D9 / 100)
```

---

## 5. Output Classification Engine

### 5.1 Classification Philosophy

The classification engine operates on a single governing principle: **the output earns its label from the data**. Classical archetypes are reference vectors against which the dimensional profile is compared — they are not destinations to fit toward.

The classification process:
1. Compute the full dimensional score vector `[D1, D2, ..., D9]`.
2. Compute cosine similarity between this vector and each classical archetype reference vector.
3. Apply threshold logic to assign a classification type: Classical, Hybrid, or Novel.
4. If Novel, derive a model name algorithmically from the dimensional signature.

### 5.2 Classical Archetype Reference Vectors

Each classical archetype is defined as an ideal-state dimension score vector representing the theoretical profile of an organization that fully embodies that archetype:

| Archetype | Abbr | D1 | D2 | D3 | D4 | D5 | D6 | D7 | D8 | D9 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Compliance-Centric Program | CCP | 3 | 5 | 2 | 3 | 2 | 3 | 4 | 2 | 2 |
| Risk-Based Management Model | RBM | 4 | 3 | 3 | 4 | 3 | 4 | 4 | 3 | 3 |
| Threat-Informed Defense | TID | 4 | 2 | 4 | 4 | 4 | 4 | 4 | 5 | 5 |
| Zero Trust Architecture | ZTA | 4 | 3 | 3 | 4 | 4 | 5 | 5 | 5 | 4 |
| Resilience-Oriented Program | ROP | 5 | 3 | 3 | 4 | 3 | 4 | 5 | 4 | 3 |
| DevSecOps / Shift-Left Model | DSO | 3 | 2 | 5 | 3 | 5 | 3 | 4 | 5 | 3 |

> **Research note:** These reference vectors represent the initial calibration set. Researchers are encouraged to validate, refine, and extend this set through empirical engagement data. The vectors should be treated as working hypotheses, not ground truth.

### 5.3 Cosine Similarity Algorithm

Cosine similarity measures the angular distance between two vectors in n-dimensional space, normalized for magnitude. It is appropriate here because it captures the *shape* of the dimensional profile — the relative pattern of scores — rather than the absolute distance, which would penalize organizations that score uniformly high or low across all dimensions.

**Formula:**

```
cos_sim(A, B) = (A · B) / (||A|| × ||B||)
```

Where:
- `A` = subject organization's dimension score vector `[D1, D2, ..., D9]`
- `B` = archetype reference vector `[b_1, b_2, ..., b_9]`
- `A · B` = dot product: `Σ(A_i × B_i)`
- `||A||` = Euclidean magnitude: `√(Σ A_i²)`
- `||B||` = Euclidean magnitude: `√(Σ B_i²)`

**Result range:** `[0, 1]`  
**Interpretation:** 1.0 = identical directional profile; 0.0 = orthogonal profiles.

**Pseudocode:**
```python
def cosine_similarity(a: dict, b: dict) -> float:
    keys = list(a.keys())
    dot  = sum(a[k] * b[k] for k in keys)
    mag_a = sum(a[k] ** 2 for k in keys) ** 0.5
    mag_b = sum(b[k] ** 2 for k in keys) ** 0.5
    if mag_a == 0 or mag_b == 0:
        return 0.0
    return dot / (mag_a * mag_b)
```

All six archetype similarities are computed. The archetypes are ranked by descending similarity. The highest-similarity archetype is designated the closest classical reference.

### 5.4 Classification Threshold Logic

The classification type is determined by the cosine similarity of the closest-matching archetype:

```
if   top_sim >= 0.975  →  CLASSICAL
elif top_sim >= 0.920  →  HYBRID
else                   →  NOVEL
```

| Type | Threshold | Meaning |
|:---|:---|:---|
| **Classical** | ≥ 97.5% | The dimensional profile closely conforms to an established archetype. Strategic guidance from that archetype is directly applicable. |
| **Hybrid** | 92% – 97.4% | Partial alignment with the closest archetype, but meaningful deviation across multiple dimensions. The archetype is a reference frame, not a prescription. |
| **Novel** | < 92% | The profile does not conform to any established archetype. An original program architecture is required. Classical models serve as orientation only. |

> **Threshold calibration note:** The 97.5% and 92% thresholds are initial working values derived from the geometric properties of the 9-dimensional reference space. They should be empirically validated through repeated use across diverse organizations. Researchers who collect sufficient engagement data should re-derive these thresholds from empirical distributions of similarity scores. See [Section 9.3](#93-suggested-validation-studies).

### 5.5 Novel Model Naming Algorithm

When the output is classified as Novel, the model is named algorithmically from three components of the dimensional signature:

**Step 1 — Identify the top two dimensions by score:**
```python
sorted_dims = sorted(dim_scores.items(), key=lambda x: x[1], reverse=True)
top_dim_1 = sorted_dims[0][0]   # e.g., D8
top_dim_2 = sorted_dims[1][0]   # e.g., D1
```

**Step 2 — Map each top dimension to its "high score" driver label:**

| Dimension | High Driver Label |
|:---|:---|
| D1 | Mission-Critical |
| D2 | Sovereignty-Constrained |
| D3 | Talent-Optimized |
| D4 | Capital-Enabled |
| D5 | Velocity-Driven |
| D6 | Executive-Anchored |
| D7 | Process-Disciplined |
| D8 | Engineering-Native |
| D9 | Adversary-Calibrated |

**Step 3 — Compose model name:**
```
"{top_dim_1_driver} × {top_dim_2_driver} Model"
```

**Step 4 — Compose posture subtitle** from dominant and deficient pillar averages plus the lowest-scoring dimension's constraint label:
```
"{dominant_pillar_descriptor}, {deficient_pillar_descriptor} · primary constraint: {bottom_dim_label}"
```

**Example output:**
```
Model Name:  Engineering-Native × Mission-Critical Model
Posture:     Technically-Mature, Resource-Constrained · primary constraint: Sponsorship-Deficient
```

This produces a designation that is both human-readable and directly derived from the data — no lookup, no manual labeling.

### 5.6 Threat-Capability Gap Signal

The Threat-Capability Gap is a secondary diagnostic signal computed independently of the composite score:

```
TCG = D9 - ((D7 + D8) / 2)
```

Where:
- `D9` = Threat Landscape dimension score (adversary sophistication + attack surface)
- `D7` = Process dimension score
- `D8` = Technical dimension score

**Interpretation:**

| TCG Value | Signal | Action |
|:---|:---|:---|
| `TCG < -0.8` | **Critical gap** ⚠ | Threat intelligence maturity significantly exceeds technical and process capability. Highest-urgency remediation priority. The organization knows what threatens it but cannot detect or respond effectively. |
| `-0.8 ≤ TCG < 0` | **Moderate gap** | Some misalignment between threat awareness and execution capability. Monitor and close through D7/D8 investment. |
| `TCG ≥ 0` | **Aligned or surplus** | Technical capability is commensurate with or ahead of threat intelligence maturity. Maintain balance; avoid over-investing in tooling without corresponding threat intelligence development. |

### 5.7 Priority Sequencing

The three lowest-scoring dimensions are surfaced as remediation priorities, ranked in ascending order of their dimension score (lowest first = highest urgency):

```python
sorted_dims = sorted(dim_scores.items(), key=lambda x: x[1])
priorities = sorted_dims[:3]   # P1, P2, P3
```

The dimension weight is displayed alongside each priority to contextualize the investment impact: a low-scoring dimension with a high weight has a disproportionate drag on the composite score, and should be prioritized accordingly.

---

## 6. Digital Implementation

### 6.1 Technology Stack

| Layer | Technology |
|:---|:---|
| Framework | React 18 (functional components, hooks) |
| State management | `useState`, `useMemo` (no external state library) |
| Styling | Inline styles (no CSS framework dependency) |
| Typography | JetBrains Mono (monospace), Syne (sans-serif) via Google Fonts |
| Computation | Pure JavaScript — no external math library |
| Deployment target | Any React-capable environment (CRA, Vite, Next.js, CodeSandbox) |

### 6.2 Phase Architecture

The engine is structured as a single-page React application with three sequential phases managed by a `phase` state variable:

```
"configure"  →  "assess"  →  "output"
```

Phase progression is gated:
- `"configure"` → `"assess"`: Unlocked when dimension weights sum to exactly 100%.
- `"assess"` → `"output"`: Unlocked when all 20 sub-factors have been scored.
- Back-navigation is permitted at any phase without data loss.

### 6.3 State Model

```javascript
// Phase control
const [phase, setPhase] = useState("configure")

// Dimension weights (D1–D9, % values summing to 100)
const [dimWeights, setDimWeights] = useState({
  D1: 12, D2: 10, D3: 10,
  D4: 12, D5: 10, D6: 10,
  D7: 12, D8: 12, D9: 12
})

// Sub-factor scores (factor ID → integer 1–5, 0 = unscored)
const [scores, setScores] = useState({})

// Derived: dimension scores (computed via useMemo)
const dimScores = useMemo(() => { ... }, [scores])

// Derived: full output object (computed via useMemo when all scored)
const output = useMemo(() => { ... }, [allScored, dimScores, dimWeights])
```

### 6.4 Data Structures

#### Dimension Definition Object
```javascript
{
  id: "D1",                    // Dimension identifier
  pillar: "Socio",             // Parent pillar
  factor: "Business Mission",  // Dimension label
  defaultW: 12,                // Default weight (%)
  factors: [                   // Sub-factor array
    {
      id: "1a",                          // Sub-factor identifier
      label: "Critical Revenue Dependency",
      anchors: [                         // 5 descriptive anchors (index 0 = score 1)
        "No digital dependency...",      // Score 1 anchor
        "Digital assists revenue...",    // Score 2 anchor
        "Digital continuity...",         // Score 3 anchor
        "Revenue is highly...",          // Score 4 anchor
        "Revenue entirely contingent...",// Score 5 anchor
      ]
    },
    // ... additional sub-factors
  ]
}
```

#### Archetype Definition Object
```javascript
{
  name: "Threat-Informed Defense",
  abbr: "TID",
  sig: {                    // Reference dimension score vector
    D1: 4, D2: 2, D3: 4,
    D4: 4, D5: 4, D6: 4,
    D7: 4, D8: 5, D9: 5
  },
  desc: "Archetype description..."
}
```

#### Output Object (returned by `buildOutput`)
```javascript
{
  composite: 3.24,           // Weighted composite score
  pillar: {                  // Pillar averages
    Socio: 3.10,
    Econo: 2.90,
    Tech:  3.72
  },
  sims: [                    // Archetype similarities, sorted descending
    { name: "...", abbr: "TID", sim: 0.943, desc: "..." },
    // ...
  ],
  cls: {                     // Classification result
    type: "Hybrid",          // "Classical" | "Hybrid" | "Novel"
    typeColor: "#5BC8AF",
    headline: "Hybrid — TID-Influenced Configuration",
    sub: "94.3% similarity to Threat-Informed Defense",
    body: "...",
    closestRef: { ... }      // null if Classical
  },
  priorities: [              // Bottom 3 dimensions by score
    { id: "D5", score: 1.50, dim: { ... } },
    // ...
  ],
  threatGap: -1.25           // D9 - avg(D7, D8)
}
```

### 6.5 Component Breakdown

| Component | Responsibility |
|:---|:---|
| `SETEngine` | Root — phase state, data initialization, derived computation |
| `PhaseNav` | Navigation bar; phase gating logic |
| `ConfigurePhase` | Weight input grid; running total validation; equal-split utility |
| `AssessPhase` | Questionnaire; anchor hover/select; per-dimension progress |
| `OutputPhase` | Score display; classification block; archetype similarity panel |
| `Bar` | Reusable proportional bar (used in all phases) |
| `Tag` | Reusable pill label (dimension IDs, pillar tags) |

### 6.6 Computation Pipeline

```
User inputs sub-factor scores (s_1a … s_9b)
    │
    ▼
useMemo: dimScores
    For each dimension D_n:
        if all sub-factors scored:
            D_n = mean(s_i for i in D_n.factors)
        else:
            D_n = undefined
    │
    ▼
useMemo: output  (only when all 20 scored)
    │
    ├── composite = Σ(D_n × w_n / 100)
    ├── pillar averages = mean(D_n) per pillar
    ├── sims = [cosine_sim(dimScores, archetype.sig) for each archetype]
    │           sorted descending
    ├── cls = threshold(sims[0].sim) → Classical / Hybrid / Novel
    │         if Novel: name from top-2 dimension drivers
    ├── priorities = bottom 3 dimensions by D_n score
    └── threatGap = D9 - mean(D7, D8)
```

---

## 7. Physical On-Site Adaptation

### 7.1 Field Assessment Overview

The SET Framework is designed to function both as a digital tool and as a **physical assessment instrument** for in-person organizational engagements. The on-site adaptation converts the digital engine into a structured fieldwork protocol consisting of four activities:

1. **Pre-visit weight configuration** — Assessor establishes dimension weights before the engagement based on available background intelligence on the subject organization.
2. **Stakeholder interviews** — Semi-structured interviews with identified organizational stakeholders, using the sub-factor anchor framework as an interview guide.
3. **Document and artefact review** — Review of organizational documents to corroborate interview-derived scores.
4. **Manual score computation and output derivation** — Scoring sheets, computation worksheets, and classification lookup table.

A full on-site engagement typically requires **2–4 days** depending on organizational size and complexity.

### 7.2 Pre-Assessment Preparation

Before arriving on-site, the assessor should complete the following:

**Background intelligence gathering:**
- Review the organization's public regulatory filings, annual reports, press releases.
- Research sector threat intelligence reports relevant to the organization's industry.
- Identify the organization's known regulatory obligations (D2 input).
- Review public information on recent M&A activity (D6 input).
- Research the organization's engineering culture indicators: job listings, GitHub presence, conference presentations (D3, D8 input).

**Preliminary weight hypothesis:**
Based on background intelligence, draft a preliminary dimension weight configuration. This is a hypothesis — it will be validated and potentially revised during the engagement. Document the reasoning behind each weight assignment.

**Stakeholder list:**
Prepare a target stakeholder list covering the following functional domains:

| Domain | Relevant Dimensions | Target Roles |
|:---|:---|:---|
| Executive Leadership | D1, D6 | CEO, COO, CFO, Board member |
| Security Leadership | D1, D7, D8, D9 | CISO, VP Security, Security Director |
| Legal / Compliance | D2 | General Counsel, Chief Compliance Officer, DPO |
| HR / People | D3 | CHRO, Head of Talent, Compensation Lead |
| Finance | D4 | CFO, Head of FP&A, Budget Owner |
| Engineering / Product | D5, D8 | CTO, VP Engineering, Head of Product |
| IT / Operations | D7, D8 | CIO, Head of Infrastructure, ITIL Process Owner |
| Threat Intelligence | D9 | Head of Threat Intel, SOC Director |

### 7.3 Weight Configuration Protocol

**On-site weight configuration session (recommended: Day 1, 2 hours):**

Conduct a facilitated workshop with the CISO and 1–2 senior stakeholders to configure dimension weights collaboratively. Use the following prompt sequence:

1. *"For this organization specifically, which of these nine dimensions most directly determines whether a security program will succeed or fail?"*
2. *"If you could only address three dimensions in the next 12 months, which three would have the largest strategic impact?"*
3. *"Are there any dimensions that are structurally irrelevant or out of scope for this organization? Why?"*

Use responses to validate or revise the preliminary weight hypothesis. Document the rationale for each final weight assignment — this documentation is part of the assessment deliverable.

**Weight constraint:** Must sum to 100%. Use the field worksheet in [Section 7.5](#75-scoring-sheet-templates).

### 7.4 Interview & Survey Protocol

**Interview structure per stakeholder session (60–90 minutes):**

1. **Context framing (10 min):** Explain the purpose of the assessment, the SET Framework structure, and how the interview outputs will be used. Establish that scores reflect current observable state, not aspirations.

2. **Domain-specific questioning (40–60 min):** Use the interview question bank in [Section 8.2](#82-interview-question-bank) to guide the session. For each relevant sub-factor:
   - Ask the primary question.
   - Present the five anchor descriptions (verbally or on a card).
   - Ask the stakeholder to identify which anchor best describes current organizational reality.
   - Probe with follow-up questions if the response is ambiguous.
   - Record the preliminary score and supporting evidence notes.

3. **Document requests (10 min):** Identify and request documents that will corroborate interview scores. See [Section 7.8](#78-evidence-standards) for evidence standards by sub-factor.

4. **Score review (10 min):** At the end of the session, read back preliminary scores to the stakeholder for validation. Note any disagreements — these are important data points for inter-rater reconciliation.

**Survey alternative:**
For organizations where stakeholder access is limited, a written survey can substitute for interviews. The survey format presents each sub-factor's five anchor descriptions in writing and asks the respondent to select the one that best describes current organizational reality. Survey responses should be validated against available documents before finalization. Self-reported survey scores without corroboration should be clearly flagged in the assessment report.

### 7.5 Scoring Sheet Templates

#### Weight Configuration Worksheet

```
ORGANIZATION: _________________________________   DATE: ___________
ASSESSOR: ____________________________________   VERSION: ________

DIMENSION WEIGHT CONFIGURATION
─────────────────────────────────────────────────────────
SOCIO PILLAR
  D1  Business Mission        _______ %   Rationale: ________________
  D2  Gov / Regulatory        _______ %   Rationale: ________________
  D3  People                  _______ %   Rationale: ________________
                              ─────────
                 Socio subtotal  _______ %

ECONO PILLAR
  D4  Capital Flow            _______ %   Rationale: ________________
  D5  Culture                 _______ %   Rationale: ________________
  D6  Constraints             _______ %   Rationale: ________________
                              ─────────
                 Econo subtotal  _______ %

TECH PILLAR
  D7  Process                 _______ %   Rationale: ________________
  D8  Technical               _______ %   Rationale: ________________
  D9  Threat Landscape        _______ %   Rationale: ________________
                              ─────────
                  Tech subtotal  _______ %

─────────────────────────────────────────────────────────
                 TOTAL  [ must = 100% ]   _______ %
─────────────────────────────────────────────────────────
Approved by: _______________________   Signature: _________________
```

#### Sub-Factor Scoring Sheet

```
ORGANIZATION: _________________________________   DATE: ___________
ASSESSOR: ____________________________________   STAKEHOLDER: ______

SUB-FACTOR SCORES  (circle selected score; record evidence source)
─────────────────────────────────────────────────────────────────────
DIMENSION D1 — Business Mission
  1a  Critical Revenue Dependency          1  2  3  4  5
      Evidence: __________________________________________________
  1b  Structural Org Topology              1  2  3  4  5
      Evidence: __________________________________________________
  1c  Strategic Competitive Risk Posture   1  2  3  4  5
      Evidence: __________________________________________________
  D1 Score = (1a + 1b + 1c) / 3 = _____ / 3 = _______

DIMENSION D2 — Gov / Regulatory
  2a  Statutory Compliance & Legal Rigidity    1  2  3  4  5
      Evidence: __________________________________________________
  2b  Geopolitical Data & People Sovereignty  1  2  3  4  5
      Evidence: __________________________________________________
  D2 Score = (2a + 2b) / 2 = _____ / 2 = _______

DIMENSION D3 — People
  3a  Technical vs. Managerial Career Arch     1  2  3  4  5
      Evidence: __________________________________________________
  3b  Scarcity-Based Compensation Elasticity   1  2  3  4  5
      Evidence: __________________________________________________
  D3 Score = (3a + 3b) / 2 = _____ / 2 = _______

DIMENSION D4 — Capital Flow
  4a  Multi-Year Funding Logic            1  2  3  4  5
      Evidence: __________________________________________________
  4b  Specialized SME Labor Scarcity      1  2  3  4  5
      Evidence: __________________________________________________
  4c  Data Intensity & Telemetry Scale    1  2  3  4  5
      Evidence: __________________________________________________
  D4 Score = (4a + 4b + 4c) / 3 = _____ / 3 = _______

DIMENSION D5 — Culture
  5a  Product & Innovation Velocity           1  2  3  4  5
      Evidence: __________________________________________________
  5b  Enterprise-wide Cyber-Accountability    1  2  3  4  5
      Evidence: __________________________________________________
  D5 Score = (5a + 5b) / 2 = _____ / 2 = _______

DIMENSION D6 — Constraints
  6a  Executive Sponsorship & Influence Depth  1  2  3  4  5
      Evidence: __________________________________________________
  6b  M&A / Divestiture Frequency              1  2  3  4  5
      Evidence: __________________________________________________
  D6 Score = (6a + 6b) / 2 = _____ / 2 = _______

DIMENSION D7 — Process
  7a  Operational Workflow Maturity            1  2  3  4  5
      Evidence: __________________________________________________
  7b  Critical Asset & Business Service Mapping 1  2  3  4  5
      Evidence: __________________________________________________
  D7 Score = (7a + 7b) / 2 = _____ / 2 = _______

DIMENSION D8 — Technical
  8a  Telemetry Cohesion & Interoperability    1  2  3  4  5
      Evidence: __________________________________________________
  8b  Org Engineering DNA & Automation Cap.    1  2  3  4  5
      Evidence: __________________________________________________
  D8 Score = (8a + 8b) / 2 = _____ / 2 = _______

DIMENSION D9 — Threat Landscape
  9a  Adversary Sophistication & Intent        1  2  3  4  5
      Evidence: __________________________________________________
  9b  Attack Surface Structural Complexity     1  2  3  4  5
      Evidence: __________________________________________________
  D9 Score = (9a + 9b) / 2 = _____ / 2 = _______
─────────────────────────────────────────────────────────────────────
```

### 7.6 Manual Computation Procedure

After all sub-factor scores are finalized and weights are configured, compute the composite score using the following sequence:

**Step 1 — Compute dimension scores:**
```
D1 = (1a + 1b + 1c) / 3
D2 = (2a + 2b) / 2
D3 = (3a + 3b) / 2
D4 = (4a + 4b + 4c) / 3
D5 = (5a + 5b) / 2
D6 = (6a + 6b) / 2
D7 = (7a + 7b) / 2
D8 = (8a + 8b) / 2
D9 = (9a + 9b) / 2
```

**Step 2 — Multiply each dimension score by its weight:**
```
D1_weighted = D1 × (w_D1 / 100)
D2_weighted = D2 × (w_D2 / 100)
... etc.
```

**Step 3 — Sum weighted scores:**
```
Composite = D1_weighted + D2_weighted + ... + D9_weighted
```

**Step 4 — Compute pillar averages:**
```
Socio_avg = (D1 + D2 + D3) / 3
Econo_avg = (D4 + D5 + D6) / 3
Tech_avg  = (D7 + D8 + D9) / 3
```

**Step 5 — Compute Threat-Capability Gap:**
```
TCG = D9 - ((D7 + D8) / 2)
```

**Step 6 — Identify top-3 priority dimensions:**
Sort D1–D9 by dimension score, ascending. The three lowest are P1, P2, P3.

**Step 7 — Output classification (manual):**
For field use without digital tools, the assessor can approximate classification using the following heuristic lookup:

```
If the dimensional profile closely matches one of these patterns  →  use Classical
Otherwise, note the two highest-scoring dimensions and compose:  →  Novel
"[top_dim_driver] × [second_dim_driver] Model"
```

For full cosine similarity computation in the field, a pre-computed similarity table for common organizational profiles can be prepared in advance, or the digital tool should be used for the output phase even if field scoring is done on paper.

### 7.7 Output Interpretation in the Field

When presenting results to organizational leadership:

1. **Present the composite score first**, placed in context of the maturity scale. Avoid leading with the classification label — it can anchor the conversation prematurely.

2. **Walk through pillar averages** to identify structural imbalances. The narrative question: *"Is this organization's security posture structurally coherent, or is there a pillar where the program is materially ahead of or behind the others?"*

3. **Present the Threat-Capability Gap** as an urgency signal. For most organizations, this is the most immediately actionable finding.

4. **Present priority dimensions** with weight context: *"D5 Culture scores lowest at 1.5/5.0, and you've allocated 10% weight to it — this is dragging your composite by approximately 0.15 points and requires immediate attention."*

5. **Present the classification last**, with the archetype similarity table. Frame the result as the starting point for program design, not a final diagnosis. If Novel: *"Your organization's profile doesn't match any existing model — which means an original architecture is required. That is not a bad outcome; it means off-the-shelf frameworks won't fit, and forcing a fit would cost you."*

### 7.8 Evidence Standards

Each sub-factor score should be corroborated by at least one form of evidence. Recommended evidence types by dimension:

| Dimension | Primary Evidence Sources |
|:---|:---|
| D1 Business Mission | Annual reports; revenue model documentation; org charts; business continuity plans |
| D2 Gov / Regulatory | Compliance register; regulatory correspondence; legal opinions; DPA registrations |
| D3 People | Job architecture documentation; compensation bands; retention data; exit interview themes |
| D4 Capital Flow | Budget documentation; multi-year financial plans; procurement records; FTE cost data |
| D5 Culture | Deployment frequency metrics; incident post-mortems; RACI matrices; OKR/KPI documentation |
| D6 Constraints | Board minutes; CISO reporting line documentation; M&A transaction history |
| D7 Process | Process documentation library; change management records; asset inventory exports |
| D8 Technical | SIEM/XDR architecture diagrams; automation runbook library; tooling inventory |
| D9 Threat Landscape | CTI reports; threat model documentation; attack surface scan results; penetration test reports |

---

## 8. Assessor Guidance

### 8.1 Stakeholder Mapping

Not all stakeholders have equal visibility into all dimensions. Use this matrix to prioritize stakeholder selection per dimension:

| Dimension | Primary Stakeholder | Secondary Stakeholder |
|:---|:---|:---|
| D1 Business Mission | CEO / COO | CISO / CRO |
| D2 Gov / Regulatory | General Counsel / DPO | CCO / CISO |
| D3 People | CHRO | Head of Engineering, Compensation Lead |
| D4 Capital Flow | CFO | CISO / Head of FP&A |
| D5 Culture | CTO / VP Engineering | Head of Product / CISO |
| D6 Constraints | CEO / Board Member | CFO / CISO |
| D7 Process | CIO / Head of IT Ops | ITIL Process Owner / CISO |
| D8 Technical | CISO / Head of Security Engineering | SOC Director / CTO |
| D9 Threat Landscape | Head of Threat Intelligence | CISO / SOC Director |

### 8.2 Interview Question Bank

The following questions are designed to elicit observable, evidence-grounded responses for each sub-factor. They are probing questions — the assessor should not read anchor descriptions until after the stakeholder has answered freely, to avoid anchoring bias.

**D1 — Business Mission**

- *1a:* "If your primary customer-facing digital systems went offline for 24 hours, what would be the direct business impact in terms of revenue, customer trust, and operational continuity?"
- *1b:* "If a major security decision needed to be made tomorrow that would affect three different business units, how would that decision get made, and how long would it take?"
- *1c:* "If a material security incident became public knowledge, what would be the competitive consequence? Have you seen this happen to a direct competitor?"

**D2 — Gov / Regulatory**

- *2a:* "Which specific regulatory frameworks are you currently subject to? Which of these have direct financial or criminal penalty exposure?"
- *2b:* "Do you have data that must remain within specific geographic boundaries? Do you have staff or contractors in jurisdictions with government data access obligations?"

**D3 — People**

- *3a:* "Can a highly skilled security engineer grow to the equivalent of a VP-level role without ever managing a team? What does that career path look like here?"
- *3b:* "If you identified a candidate for a critical role who required 40% above your standard pay band, what would happen? How long would it take to resolve?"

**D4 — Capital Flow**

- *4a:* "Is your security program funded on an annual budget cycle, or do you have multi-year capital commitment? What happens to your program if there's a CFO change or a down quarter?"
- *4b:* "What are the hardest roles to fill on your security team right now? How long has your most critical open role been open?"
- *4c:* "How much data are you ingesting and processing for security monitoring today? Is that volume growing, and how does the cost scale?"

**D5 — Culture**

- *5a:* "How often does your engineering team ship new code or infrastructure changes to production? How much advance notice does security typically get before a major new capability is deployed?"
- *5b:* "When a business unit makes a decision that introduces security risk — like adopting a new SaaS tool without security review — what happens? Who is accountable?"

**D6 — Constraints**

- *6a:* "When you need a decision that requires a change in budget, behaviour, or organizational structure — what level of the organization do you need to engage? Has the CEO or Board ever personally sponsored a security initiative?"
- *6b:* "How many acquisitions or divestitures has this organization completed in the last three years? What is the current integration backlog?"

**D7 — Process**

- *7a:* "Walk me through your incident response process. Is it documented? Was it exercised in the last 12 months? What happened in the last real incident?"
- *7b:* "If I asked you right now to list every system that processes personally identifiable data, how long would it take to produce that list? How confident would you be in its completeness?"

**D8 — Technical**

- *8a:* "If a threat actor compromised a contractor's laptop and used it to move laterally into your cloud environment, how long would it take your team to detect it? What would trigger the alert?"
- *8b:* "Does your security team write code? Do your detection rules come from a vendor out of the box, or does your team build and tune custom detections?"

**D9 — Threat Landscape**

- *9a:* "Who is trying to attack you specifically — not generically, but by name or actor group? How do you know? Do you have a threat intelligence function?"
- *9b:* "How many externally facing assets does this organization have? How many third parties have access to your internal systems or data? When did you last audit that?"

### 8.3 Common Scoring Errors

| Error | Description | Mitigation |
|:---|:---|:---|
| **Optimism bias** | Stakeholders consistently describe aspirational state rather than current reality. | Probe with *"when did this last happen in practice?"* and request corroborating documentation. |
| **Policy/practice gap** | Documented policies score high; actual operational practice scores much lower. | Always ask for recent operational examples, not policy documents alone. |
| **Halo effect** | A high score on one visible sub-factor inflates adjacent sub-factor scores. | Score each sub-factor independently; review all scores together at the end for consistency. |
| **Recency bias** | A recent positive event (new tool purchase, recent audit pass) inflates scores. | Assess against sustained operational pattern over 12+ months, not recent events. |
| **Anchoring** | Assessor shares anchor descriptions before hearing the stakeholder's unprompted response, biasing the answer. | Always ask the question first; present anchors only when asking for a final score selection. |
| **Single-source scoring** | Scores derived entirely from a single stakeholder interview without corroboration. | Triangulate across at least two stakeholders per dimension and one documentary evidence source. |

### 8.4 Inter-Rater Reliability

When two assessors score the same organization independently, score variance across sub-factors is expected but should be managed. Recommended protocol for multi-assessor engagements:

1. Each assessor completes scoring independently after their respective stakeholder interviews.
2. Both assessors meet to compare scores for each sub-factor.
3. For any sub-factor where scores differ by more than 1 point, the assessors must present their evidence and reasoning.
4. Consensus is reached by evidence weight: the assessor with stronger corroborating documentation sets the score.
5. Where consensus cannot be reached, take the mean of the two scores (this should be rare — if it is common, the anchors need refinement).

Document all score reconciliations in the assessment record.

---

## 9. Validation & Calibration

### 9.1 Baseline Calibration Exercise

Before deploying the framework in a live engagement, assessors should complete a calibration exercise using a known reference organization (real or synthetic). The calibration exercise:

1. Score a reference organization independently using only the anchor descriptions and the interview question bank.
2. Compare results to a pre-scored reference answer key (to be developed by the framework maintainers as engagement data accumulates).
3. For any sub-factor where the assessor's score deviates by more than 1 point from the reference, review the anchor descriptions and evidence standards for that sub-factor.
4. Re-score until deviations are within ±1 on all sub-factors.

### 9.2 Sensitivity Analysis

Assessors should perform a sensitivity analysis on the composite score before finalizing any assessment report. Sensitivity analysis examines how much the composite score would change if individual sub-factor scores shifted by ±1:

```
For each sub-factor s_i:
  Δ_composite = (Δs_i / k_n) × (w_n / 100)
```

Where `k_n` is the number of sub-factors in dimension `n` and `w_n` is that dimension's weight.

A sub-factor where a ±1 score change produces a composite shift of more than 0.10 should be flagged for additional evidence gathering before the score is finalized.

The dimension with the highest sensitivity (highest weight × 1/k) is the dimension where scoring error has the most impact on the output.

### 9.3 Suggested Validation Studies

The following empirical studies would materially advance the scientific validity of the framework and are recommended for future researchers:

1. **Archetype vector validation** — Apply the framework to organizations with known, well-documented program architectures (e.g., organizations that have published detailed CISO case studies) and test whether the cosine similarity algorithm correctly classifies them.

2. **Threshold calibration** — Accumulate similarity score distributions across a diverse sample of organizations and derive empirical thresholds for Classical / Hybrid / Novel classification boundaries, replacing the current working values of 97.5% and 92%.

3. **Predictive validity** — Test whether composite scores and dimensional profiles predict meaningful organizational outcomes: breach frequency, breach impact, regulatory penalty incidence, program cost efficiency.

4. **Inter-rater reliability study** — Have multiple trained assessors independently score the same set of organizations and compute intraclass correlation coefficients (ICC) for each sub-factor and dimension.

5. **Longitudinal stability** — Re-assess the same organizations at 12-month intervals to test whether framework scores track organizational change as expected.

6. **Industry-specific anchor refinement** — Develop industry-specific variants of the descriptive anchors for high-prevalence sectors (financial services, healthcare, critical infrastructure, technology) where generic anchors may misrepresent sector-specific conditions.

---

## 10. Extending the Framework

### 10.1 Adding Dimensions

To add a new dimension to the framework:

1. Assign it to an existing pillar or define a new pillar.
2. Define 2–3 sub-factors, each with 5 descriptive behavioural anchors.
3. Add the dimension to the `DIMS` array in the implementation with a `defaultW` value.
4. Update the weight configuration logic: the total must still equal 100%. Adding a new dimension requires redistributing weights from existing dimensions.
5. Add a new archetype reference vector entry for each archetype in `ARCHETYPES` (the new dimension needs a reference score for the cosine similarity to remain valid).
6. Add the new dimension to `DIM_DRIVER` with high and low label descriptors for novel model naming.

> **Warning:** Adding dimensions without updating archetype reference vectors will corrupt the cosine similarity computation. All archetype vectors must be the same length as the dimension score vector.

To implement sub-factor-level weighting as an extension, introduce a secondary weight configuration step:

```javascript
// Sub-factor weights per dimension (must sum to 1.0 within each dimension)
const [sfWeights, setSfWeights] = useState({
  "1a": 0.40, "1b": 0.30, "1c": 0.30,
  "2a": 0.55, "2b": 0.45,
  // ... etc.
})

// Dimension score with sub-factor weighting:
D_n = Σ (s_i × sfWeights[i])   for i in D_n.factors
```

### 10.2 Adding Archetypes

To add a new archetype reference vector:

1. Define the archetype's ideal-state dimension score vector across all 9 (or n) dimensions.
2. Add to the `ARCHETYPES` array with `name`, `abbr`, `sig`, and `desc` fields.
3. No other code changes are required — the similarity loop iterates over all archetypes automatically.

Archetype reference vectors should be defined through one of two methods:
- **Expert elicitation:** Have multiple domain experts independently score the ideal-state organization for that archetype, then average.
- **Empirical derivation:** Average the dimension scores of multiple organizations that are verified instances of that archetype.

### 10.3 Industry-Specific Presets

The weight configuration layer supports the addition of industry preset profiles — pre-configured weight sets tailored to specific sectors. To implement:

```javascript
const INDUSTRY_PRESETS = {
  "Financial Services": {D1:15,D2:18,D3:8,D4:14,D5:8,D6:12,D7:10,D8:10,D9:5},
  "Healthcare":         {D1:12,D2:20,D3:10,D4:10,D5:6,D6:10,D7:12,D8:10,D9:10},
  "Critical Infrastructure": {D1:18,D2:12,D3:8,D4:14,D5:5,D6:14,D7:12,D8:10,D9:7},
  // ...
}
```

Expose preset selection in the Configure phase UI. Presets should be treated as **starting points that the assessor adjusts**, not fixed configurations.

### 10.4 Longitudinal Tracking

For organizations assessed at multiple points in time, extend the data model to support time-series storage:

```javascript
const assessmentRecord = {
  org_id: "ORG_001",
  assessments: [
    {
      date: "2025-01",
      weights: { D1: 12, D2: 10, ... },
      scores: { "1a": 3, "1b": 2, ... },
      composite: 2.84,
      classification: "Hybrid",
    },
    {
      date: "2026-01",
      // ...
      composite: 3.21,
      classification: "Hybrid",
    }
  ]
}
```

Delta analysis — comparing dimension scores across assessment periods — is the primary value of longitudinal tracking. Display score movement (Δ) alongside current scores in the output phase.

---

## 11. Worked Example

The following example demonstrates the complete scoring and computation procedure for a hypothetical mid-size financial services organization.

**Organization profile:** Mid-size regional bank. 2,400 employees. Publicly listed. Operations in 3 countries. Subject to PCI-DSS, local banking regulations, and GDPR for EU customers. No M&A activity in 5 years. Engineering team of ~150 developers. Security team of 12.

**Step 1 — Weight configuration (assessor judgment, financial services context):**

| Dim | Factor | Weight | Rationale |
|:---|:---|:---:|:---|
| D1 | Business Mission | 14% | Core banking uptime is existential; high competitive sensitivity |
| D2 | Gov / Regulatory | 18% | PCI-DSS, banking reg, GDPR — heaviest regulatory density |
| D3 | People | 8% | Talent market is constrained but not the primary risk driver |
| D4 | Capital Flow | 14% | Multi-year program funding is structurally important in banking |
| D5 | Culture | 7% | Moderate velocity; traditional banking culture |
| D6 | Constraints | 12% | Board-level engagement is a critical success factor |
| D7 | Process | 12% | Operational discipline is a regulatory requirement |
| D8 | Technical | 9% | Moderate engineering depth; not engineering-native |
| D9 | Threat Landscape | 6% | Sector CTI exists; threat profile well-understood |
| | **Total** | **100%** | |

**Step 2 — Sub-factor scores (post-interview, evidence-corroborated):**

| ID | Sub-Factor | Score | Evidence |
|:---|:---|:---:|:---|
| 1a | Critical Revenue Dependency | 5 | Core banking systems; any outage = immediate revenue and regulatory impact |
| 1b | Structural Org Topology | 3 | Hierarchical with regional matrix; moderate decision velocity |
| 1c | Strategic Competitive Risk Posture | 4 | Regional banking market; incident = meaningful customer attrition risk |
| 2a | Statutory Compliance & Legal Rigidity | 5 | PCI-DSS, banking reg, GDPR; active regulatory relationship |
| 2b | Geopolitical Data & People Sovereignty | 3 | 3-country ops; manageable sovereignty requirements; no high-risk jurisdictions |
| 3a | Technical vs. Managerial Career Architecture | 2 | No formal technical ladder; advancement requires management |
| 3b | Scarcity-Based Compensation Elasticity | 2 | Rigid pay bands; 6-week approval process for exceptions |
| 4a | Multi-Year Funding Logic | 4 | 3-year security programme budget approved by Board |
| 4b | Specialized SME Labor Scarcity | 3 | Open cloud security architect role; 4-month fill time |
| 4c | Data Intensity & Telemetry Scale | 3 | Enterprise SIEM; significant data volume; manageable cost |
| 5a | Product & Innovation Velocity | 2 | Quarterly releases; traditional change management |
| 5b | Enterprise-wide Cyber-Accountability | 2 | Security team owns risk; business units not formally accountable |
| 6a | Executive Sponsorship & Influence Depth | 4 | CISO reports to CEO; Board Risk Committee quarterly engagement |
| 6b | M&A / Divestiture Frequency | 1 | No M&A activity in 5 years; stable corporate structure |
| 7a | Operational Workflow Maturity | 4 | ITIL-aligned; documented incident response; regular exercises |
| 7b | Critical Asset & Business Service Mapping | 3 | Asset inventory exists; crown jewel mapping incomplete |
| 8a | Telemetry Cohesion & Interoperability | 3 | Centralized SIEM; partial cross-domain correlation |
| 8b | Org Engineering DNA & Automation | 2 | Limited detection engineering; primarily vendor-managed tooling |
| 9a | Adversary Sophistication & Intent | 3 | Sector CTI subscription; general threat profile; limited operationalization |
| 9b | Attack Surface Structural Complexity | 3 | Hybrid estate; known gaps in third-party inventory |

**Step 3 — Dimension score computation:**

```
D1 = (5 + 3 + 4) / 3 = 12 / 3 = 4.00
D2 = (5 + 3) / 2     = 8  / 2 = 4.00
D3 = (2 + 2) / 2     = 4  / 2 = 2.00
D4 = (4 + 3 + 3) / 3 = 10 / 3 = 3.33
D5 = (2 + 2) / 2     = 4  / 2 = 2.00
D6 = (4 + 1) / 2     = 5  / 2 = 2.50
D7 = (4 + 3) / 2     = 7  / 2 = 3.50
D8 = (3 + 2) / 2     = 5  / 2 = 2.50
D9 = (3 + 3) / 2     = 6  / 2 = 3.00
```

**Step 4 — Weighted composite:**

```
C = (4.00×0.14) + (4.00×0.18) + (2.00×0.08) +
    (3.33×0.14) + (2.00×0.07) + (2.50×0.12) +
    (3.50×0.12) + (2.50×0.09) + (3.00×0.06)

  = 0.560 + 0.720 + 0.160 +
    0.466 + 0.140 + 0.300 +
    0.420 + 0.225 + 0.180

  = 3.171   →   Established
```

**Step 5 — Pillar averages:**
```
Socio = (4.00 + 4.00 + 2.00) / 3 = 3.33
Econo = (3.33 + 2.00 + 2.50) / 3 = 2.61
Tech  = (3.50 + 2.50 + 3.00) / 3 = 3.00
```

**Step 6 — Threat-Capability Gap:**
```
TCG = D9 - ((D7 + D8) / 2) = 3.00 - ((3.50 + 2.50) / 2) = 3.00 - 3.00 = 0.00
```
*Aligned — no critical gap.*

**Step 7 — Priority dimensions (bottom 3):**
```
P1: D3 People       — 2.00 (8% weight)
P2: D5 Culture      — 2.00 (7% weight)
P3: D6 Constraints  — 2.50 (12% weight)
```

**Step 8 — Classification:**

Closest archetype by cosine similarity: **CCP (Compliance-Centric Program)** at approximately 91%.

Result: **Novel** (below 92% threshold).

Model name derived from top 2 dimensions by score: D1 (4.00) and D2 (4.00) — tied; use both:
```
Headline:  Sovereignty-Constrained × Mission-Critical Model
Posture:   Governance-Led, Resource-Constrained · primary constraint: Capability-Deficient
```

**Interpretation:** This organization has built strong compliance and mission-critical resilience foundations (D1, D2 strong) but has a material capability ceiling imposed by people architecture (D3), culture (D5), and executive constraint (D6). It is not a classical Compliance-Centric Program because its threat landscape and process maturity exceed the CCP signature, but it doesn't conform to any other archetype either. The strategic program architecture must address the D3/D5/D6 triad as foundational blockers before technical capability advancement (D8) can be sustained.

---

## 12. Limitations & Research Gaps

Researchers and practitioners should be aware of the following known limitations:

**1. Ordinal-to-cardinal conversion.** The scoring model treats 1–5 ordinal scores as if interval arithmetic is valid (adding and averaging scores). This produces tractable outputs at the cost of mathematical precision. Scores should not be interpreted as having ratio properties (a score of 4 is not "twice as good" as a score of 2).

**2. Cosine similarity is magnitude-insensitive.** Cosine similarity captures profile shape but not absolute maturity level. Two organizations with very different composite scores but similar dimensional profiles (one consistently high, one consistently low) will show high cosine similarity. Assessors should present cosine similarity alongside the composite score, not in isolation.

**3. Archetype reference vectors are theoretical.** The six classical archetype vectors were constructed through expert judgment, not empirical derivation. They represent hypotheses about what ideal-state organizational profiles look like for each archetype. Empirical validation through case-study research is required to establish their validity. See [Section 9.3](#93-suggested-validation-studies).

**4. Classification thresholds are uncalibrated.** The 97.5% and 92% similarity thresholds are working values, not empirically derived boundaries. They should be replaced with data-derived thresholds once sufficient engagement data is available.

**5. Weight configuration is subjective.** The assessment output is sensitive to weight configuration. Two assessors who configure different weights for the same organization will produce different composite scores. This is a feature (contextual adaptability) and a limitation (subjectivity and reproducibility). Weight configuration decisions must be documented and justified.

**6. Single-assessor reliability.** A solo assessor conducting all stakeholder interviews for an engagement introduces a systemic bias risk. Multi-assessor protocols with reconciliation are strongly recommended for high-stakes applications.

**7. Self-reported data risk.** Sub-factor scores derived primarily from stakeholder interviews are subject to social desirability bias. Documentary corroboration is required for each sub-factor per the evidence standards in [Section 7.8](#78-evidence-standards).

**8. Static snapshot limitation.** The framework produces a point-in-time assessment. Organizational maturity is dynamic. Findings from a single assessment should not be treated as stable characterizations — reassessment at regular intervals is required for longitudinal validity.

---

## 13. Glossary

| Term | Definition |
|:---|:---|
| **Anchor** | A descriptive behavioural statement associated with a specific score level (1–5) for a given sub-factor. |
| **Archetype** | A canonical cybersecurity program model representing a specific strategic orientation. Used as a reference vector in the classification engine. |
| **Classical (output type)** | A classification indicating the organizational profile closely conforms to an established archetype (cosine similarity ≥ 97.5%). |
| **Composite score** | The weighted sum of all nine dimension scores, producing a single organizational maturity score in the range [1.00, 5.00]. |
| **Cosine similarity** | A mathematical measure of the angular distance between two vectors; used to compare organizational profiles against archetype reference vectors. |
| **Dimension** | One of nine structured assessment areas, each belonging to a pillar and decomposed into 2–3 sub-factors. |
| **Dimension score** | The arithmetic mean of all sub-factor scores within a dimension. |
| **Dimension weight** | A percentage value assigned by the assessor to a dimension, expressing its relative importance in the composite computation. |
| **Hybrid (output type)** | A classification indicating partial alignment with the closest archetype (92% ≤ cosine similarity < 97.5%). |
| **Novel (output type)** | A classification indicating the organizational profile does not conform to any established archetype (cosine similarity < 92%). The model name is derived algorithmically from the dimensional signature. |
| **Pillar** | One of three top-level groupings (Socio, Econo, Tech) containing three dimensions each. |
| **Pillar average** | The unweighted mean of dimension scores within a pillar; a descriptive signal, not a composite input. |
| **Sub-factor** | One of twenty primary assessment factors, each assigned a 1–5 score using descriptive anchors. |
| **Threat-Capability Gap (TCG)** | A secondary diagnostic signal: D9 score minus the average of D7 and D8 scores. Negative values indicate technical and process capability is insufficient relative to threat intelligence maturity. |

---

## 14. Changelog

| Version | Date | Author | Notes |
|:---|:---|:---|:---|
| `v1.0` | 2026-03 | SET Framework Working Group | Initial framework definition. 3 pillars, 9 dimensions, 20 sub-factors, 6 archetype reference vectors. Weighted composite model. Cosine similarity classification engine. Physical field protocol. |

---

> **License:** Research Use — Attribution Required.  
> **Status:** `Active — v1.0`  
> **Maintainer:** SET Framework Working Group  
> **Contributions:** Researchers wishing to contribute empirical validation data, refined archetype vectors, or industry-specific anchor sets are encouraged to open an issue or submit a pull request.
