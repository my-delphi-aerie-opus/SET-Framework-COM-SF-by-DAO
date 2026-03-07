# SET Framework Assessment Engine
### Comprehensive Technical Reference for Global Cybersecurity Practitioners & Researchers

> **Version:** 2.0  
> **Status:** Active  
> **Application Domain:** Cybersecurity Program Strategy & Organizational Maturity Assessment  
> **Assessment Mode:** Qualitative, Weighted, Generative Output Classification  
> **Scope:** Global — applicable across all industries, organization sizes, and regulatory jurisdictions

---

## Table of Contents

- [1. Overview](#1-overview)
- [2. Theoretical Basis](#2-theoretical-basis)
- [3. Framework Architecture](#3-framework-architecture)
- [4. Pillar I — Socio](#4-pillar-i--socio)
  - [D1 · Business Mission](#d1--business-mission)
  - [D2 · Gov / Regulatory](#d2--gov--regulatory)
  - [D3 · People](#d3--people)
- [5. Pillar II — Econo](#5-pillar-ii--econo)
  - [D4 · Capital Flow](#d4--capital-flow)
  - [D5 · Culture](#d5--culture)
  - [D6 · Constraints](#d6--constraints)
- [6. Pillar III — Tech](#6-pillar-iii--tech)
  - [D7 · Process](#d7--process)
  - [D8 · Technical](#d8--technical)
  - [D9 · Threat Landscape](#d9--threat-landscape)
- [7. Scoring Model](#7-scoring-model)
- [8. Output Classification Engine](#8-output-classification-engine)
- [9. Digital Implementation](#9-digital-implementation)
- [10. Physical On-Site Adaptation](#10-physical-on-site-adaptation)
- [11. Assessor Guidance](#11-assessor-guidance)
- [12. Global Context & Regional Applicability](#12-global-context--regional-applicability)
- [13. Validation & Calibration](#13-validation--calibration)
- [14. Extending the Framework](#14-extending-the-framework)
- [15. Worked Example](#15-worked-example)
- [16. Limitations & Research Gaps](#16-limitations--research-gaps)
- [17. Glossary](#17-glossary)
- [18. Changelog](#18-changelog)

---

## 1. Overview

The **SET Framework Assessment Engine** is a structured, evidence-based methodology for profiling organizational cybersecurity posture across three interdependent pillars — **Socio**, **Econo**, and **Tech** — decomposed into nine weighted dimensions and forty-two primary sub-factors.

The engine is built to operate across organizational contexts of all types: publicly listed corporations and private enterprises, government agencies and non-profit institutions, multinational conglomerates and regional operators, technology-native companies and traditional industrials. Its architecture is deliberately context-adaptive — the weight configuration layer allows any two assessors evaluating different organizations to produce structurally different outputs that accurately reflect the unique conditions of each subject, regardless of geography, sector, size, or regulatory jurisdiction.

The engine operates in three sequential phases:

1. **Configure** — The assessor assigns percentage weights to each of the nine dimensions, summing to exactly 100%, to reflect the assessed relevance of each dimension for the specific organizational and environmental context.
2. **Assess** — Each of the forty-two sub-factors is scored 1–5 using descriptive behavioural anchors calibrated to globally recognizable organizational conditions.
3. **Output** — Scores are aggregated through a weighted computation model to produce a composite maturity score, a dimensional profile, and a generative strategic model classification.

The output is **generative, not classificatory**: the framework does not pre-assign organizations to archetypes. It derives a strategic model from the dimensional data, then uses cosine similarity against classical reference vectors to determine whether the output resembles a known model, a hybrid configuration, or something entirely novel to the field.

---

## 2. Theoretical Basis

### 2.1 Design Philosophy

Most existing cybersecurity maturity frameworks — CMMI for Security, NIST CSF, ISO 27001 maturity mappings, C2M2, CIS Controls implementation tiers — are **prescriptive and conformance-oriented**: they measure how closely an organization matches a defined ideal state. This is useful for compliance tracking but strategically insufficient, because organizations are not static entities converging on a single universal ideal. They are differentiated organisms shaped by their history, economics, people, markets, regulatory environments, and threat contexts. The optimal security program architecture for any given organization is a function of those specific conditions — not a generic best practice imported from an industry report.

The SET Framework inverts this logic. Rather than asking *"how close is this organization to a defined ideal?"*, it asks *"given the complete dimensional profile of this organization, what is the most appropriate strategic architecture for its specific conditions?"*

This shifts the framework from a **conformance model** to a **generative model**.

### 2.2 Global Applicability

Cybersecurity frameworks developed primarily in North American or Western European contexts carry embedded assumptions about regulatory environments, talent markets, organizational structures, and threat landscapes that do not universally apply. An organization operating in Southeast Asia, sub-Saharan Africa, Latin America, or the Middle East faces structurally different conditions across nearly every dimension.

The SET Framework addresses this through three design choices:

1. **Weight configurability** — Dimensions that are structurally irrelevant in one context (e.g., D2 Gov/Regulatory for an informal-sector cooperative) can receive low weights without distorting the composite output.
2. **Anchor universality** — Descriptive anchors are written to describe observable organizational behaviours rather than named frameworks or technologies, making them interpretable across contexts where NIST, GDPR, or SOC 2 may be unknown.
3. **Geopolitical sub-factors** — Dimensions D2 and D9 explicitly incorporate geopolitical and sovereignty factors that are acutely relevant to organizations operating in contested, sanctioned, or digitally sovereign jurisdictions.

### 2.3 Why Qualitative Scoring

Cybersecurity organizational factors resist precise quantification. It is epistemologically dishonest to assign a numerically exact score to "executive sponsorship depth" or "organizational change fatigue" as if these were measurable physical quantities. The 1–5 maturity scale with descriptive behavioural anchors addresses this by:

- Grounding each score in **observable, describable organizational conditions** rather than arbitrary numerical assignments.
- Enabling consistent scoring across different assessors through shared anchor language — a form of inter-rater calibration embedded in the instrument itself.
- Producing scores that are **ordinal** (rank-ordered) rather than **cardinal** (arithmetically precise), which is the correct epistemic category for organizational assessment data.

The use of weighted aggregation on ordinal scores introduces a known approximation — treating ordinal intervals as arithmetic. This is a deliberate and documented trade-off: the aggregation model sacrifices mathematical purity to produce a tractable composite output that is useful for strategic decision-making. This limitation is documented in full in [Section 16](#16-limitations--research-gaps).

### 2.4 Why Generative Output

Classical cybersecurity program archetypes were developed under specific industry conditions and organizational assumptions. Many organizations, when profiled honestly against their actual conditions rather than their aspirations, do not fit cleanly into any classical archetype. Forcing a fit introduces strategic misalignment: the organization invests in program components designed for a different context and under-invests in areas that its specific dimensional signature demands.

The SET output engine uses cosine similarity against classical reference vectors as a **diagnostic orientation tool**, not a prescriptive assignment. When fit is high (≥97.5%), the classical archetype is confirmed as a valid strategic reference. When fit is partial (≥92%), a hybrid designation signals that selective borrowing from the closest archetype is appropriate. When fit is low (<92%), the engine generates a novel model designation derived directly from the dimensional data — making the output a product of the evidence, not a lookup.

This approach is consistent with complexity science perspectives on organizations as adaptive systems, and with the cybersecurity field's increasing recognition that no two organizations are identical in their risk, resource, and operational context.

---

## 3. Framework Architecture

### 3.1 Structural Hierarchy

```
SET Framework  (v2.0)
│
├── Pillar I: SOCIO
│   ├── D1 · Business Mission          (5 sub-factors)
│   ├── D2 · Gov / Regulatory          (5 sub-factors)
│   └── D3 · People                    (5 sub-factors)
│
├── Pillar II: ECONO
│   ├── D4 · Capital Flow              (4 sub-factors)
│   ├── D5 · Culture                   (4 sub-factors)
│   └── D6 · Constraints               (4 sub-factors)
│
└── Pillar III: TECH
    ├── D7 · Process                   (5 sub-factors)
    ├── D8 · Technical                 (5 sub-factors)
    └── D9 · Threat Landscape          (5 sub-factors)

TOTAL: 9 Dimensions · 42 Sub-Factors · 210 Descriptive Anchors
```

### 3.2 Dimension Summary Table

| ID | Pillar | Dimension | Sub-Factors | Default Weight |
|:---|:---|:---|:---:|:---:|
| D1 | Socio | Business Mission | 5 | 12% |
| D2 | Socio | Gov / Regulatory | 5 | 10% |
| D3 | Socio | People | 5 | 10% |
| D4 | Econo | Capital Flow | 4 | 12% |
| D5 | Econo | Culture | 4 | 10% |
| D6 | Econo | Constraints | 4 | 10% |
| D7 | Tech | Process | 5 | 12% |
| D8 | Tech | Technical | 5 | 12% |
| D9 | Tech | Threat Landscape | 5 | 12% |
| | | **Total** | **42** | **100%** |

> **Default weights** are provided as a neutral baseline. They carry no normative significance and must be reconfigured by the assessor for every engagement to reflect the subject organization's specific context.

---

## 4. Pillar I — Socio

The **Socio** pillar captures the human, structural, and governance dimensions of an organization. It evaluates how mission-criticality, regulatory environment, and people architecture shape the conditions under which any cybersecurity program must operate. Socio factors are frequently underweighted in technical assessments — yet they represent the most consequential long-term determinants of program sustainability.

---

### D1 · Business Mission

> **Core question:** How deeply is the organization's mission embedded in digital continuity, structural complexity, competitive exposure, digital transformation risk, and supply chain dependency?

This dimension evaluates the degree to which organizational survival and performance are contingent on digital systems, and how the organization's structural and competitive characteristics amplify or dampen the consequence of security events. It is the primary driver of **impact sizing** — how badly things go wrong when they go wrong.

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `1a` | Critical Revenue Dependency | Degree to which core revenue streams depend on digital continuity and operational uptime. High dependency elevates the blast radius of any disruption. |
| `1b` | Structural Org Topology | Complexity of org structure — federated, hierarchical, matrixed, consortium — affecting decision velocity, accountability diffusion, and program alignment difficulty. |
| `1c` | Strategic Competitive Risk Posture | How competitive positioning amplifies or dampens the consequence of security events. Organizations in trust-dependent or hyper-competitive sectors face greater reputational and operational exposure. |
| `1d` | Digital Transformation Dependency | Extent to which ongoing digital transformation programmes introduce security risk as an operational byproduct — cloud migration, OT/IT convergence, AI integration, platform modernisation. |
| `1e` | Third-Party & Supply Chain Mission Criticality | Degree to which the organization's mission delivery is dependent on third-party providers, outsourced services, or supply chain partners whose compromise would directly impair operations. |

#### Descriptive Anchors — D1

**1a — Critical Revenue Dependency**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No meaningful digital dependency. Revenue operations remain fully viable through manual or offline processes indefinitely. |
| 2 | Developing | Digital systems support but do not drive revenue. Manual fallback exists for most critical processes; disruptions are inconvenient but tolerable. |
| 3 | Established | Digital continuity is operationally important. Disruptions are tolerable for 24–72 hours before meaningful revenue impact is felt. |
| 4 | Advanced | Revenue is highly uptime-dependent. Any unplanned disruption causes measurable, quantifiable hourly revenue and customer trust loss. |
| 5 | Optimized | Revenue is entirely contingent on digital continuity. Any outage — regardless of duration — produces immediate, catastrophic financial and operational impact. |

**1b — Structural Org Topology**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Simple flat hierarchy with single clear authority. Security decisions can be made and implemented rapidly with minimal coordination. |
| 2 | Developing | Moderate organizational depth with some functional separation. Security decisions require involvement of 2–3 stakeholders; manageable coordination overhead. |
| 3 | Established | Multi-layered structure with partial federation. Significant cross-functional coordination required for most security decisions; some accountability diffusion. |
| 4 | Advanced | Complex federated or matrixed structure. Security governance spans multiple business units, regions, or legal entities with competing priorities. |
| 5 | Optimized | Global conglomerate, holding company, or multi-entity consortium. Accountability for security outcomes is severely diffused; no single authority can enforce enterprise-wide decisions. |

**1c — Strategic Competitive Risk Posture**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Monopoly or state-protected market position. Security incidents carry minimal competitive consequence; market position is structurally insulated. |
| 2 | Developing | Stable oligopolistic market. Incidents cause limited, temporary reputational impact; customer inertia is high and competitive alternatives are limited. |
| 3 | Established | Competitive but stable market. Incidents cause meaningful customer impact and media attention; some market share movement is plausible. |
| 4 | Advanced | Highly competitive sector with low customer switching cost. Incidents cause rapid customer attrition, partner concern, and measurable market share damage. |
| 5 | Optimized | Hyper-competitive or trust-is-the-product sector (e.g. fintech, healthtech, legal, consulting). Any material incident threatens market position, valuation, and licence to operate. |

**1d — Digital Transformation Dependency**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No active digital transformation. Technology environment is stable, mature, and predominantly on-premise with minimal change velocity. |
| 2 | Developing | Isolated transformation projects underway (e.g. single cloud workload migration, basic SaaS adoption). Security risk from transformation activity is contained and manageable. |
| 3 | Established | Broad transformation programme active across multiple domains. Cloud migration, platform modernisation, and/or OT/IT convergence introduces ongoing, manageable security complexity. |
| 4 | Advanced | Aggressive multi-stream transformation underway (cloud-first, AI integration, digital product development). Security must continuously adapt to a rapidly changing risk surface. |
| 5 | Optimized | The organisation is in a state of near-continuous transformation. The boundary between "building new capability" and "operating existing capability" is permanently blurred; security risk is structurally embedded in the transformation engine itself. |

**1e — Third-Party & Supply Chain Mission Criticality**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Minimal third-party dependency. Core mission delivery relies on internally managed systems and staff with no single critical external dependency. |
| 2 | Developing | Some third-party services in use. External dependencies are present but redundant; loss of any single provider would not impair mission delivery. |
| 3 | Established | Significant third-party dependency across multiple service categories. Loss of one or more critical providers would cause material operational disruption. |
| 4 | Advanced | Deep supply chain integration. Mission delivery is co-dependent with external partners; several single points of failure exist in the supplier ecosystem. |
| 5 | Optimized | Entire mission is underpinned by a complex third-party and supply chain ecosystem. Any compromise of a tier-1 supplier immediately propagates to the organisation's core operations. |

---

### D2 · Gov / Regulatory

> **Core question:** What is the density, rigidity, jurisdictional complexity, and reporting obligations of the compliance and sovereignty framework the organization operates within?

This dimension evaluates the external legal and regulatory environment. It is not a measure of the organization's compliance performance — that is captured in D7 (Process). D2 measures the **weight and complexity of the regulatory burden** itself as a structural input to program design.

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `2a` | Statutory Compliance & Legal Rigidity | Binding regulatory obligations that constrain architectural and operational choices and carry direct financial, operational, or criminal liability. |
| `2b` | Geopolitical Data & People Sovereignty | Cross-border data residency requirements, workforce nationality constraints, and exposure to state-level interference, data access demands, or sanctions regimes. |
| `2c` | Incident Reporting & Notification Obligations | Mandatory timelines and scope of breach notification obligations to regulators, affected individuals, stock exchanges, and sector bodies. |
| `2d` | Cross-Sector Regulatory Overlap | Degree to which the organisation operates across multiple regulated sectors, each with distinct and potentially conflicting cybersecurity requirements. |
| `2e` | International Standards & Framework Alignment Pressure | External pressure — from customers, investors, supply chain, or regulators — to demonstrate alignment with internationally recognised cybersecurity standards. |

#### Descriptive Anchors — D2

**2a — Statutory Compliance & Legal Rigidity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No binding cybersecurity regulations apply. The organization operates under voluntary standards only, with no regulatory penalty exposure. |
| 2 | Developing | Light-touch sector guidance or soft-law obligations. Regulatory requirements are principles-based, flexible in implementation, and carry low penalty exposure. |
| 3 | Established | Moderate statutory obligations under one or two frameworks (e.g. national data protection law, sector cybersecurity guidance). Defined compliance timelines and financial penalties apply. |
| 4 | Advanced | Stringent multi-framework obligations (e.g. GDPR + PCI-DSS, or national CNI regulation + sector licensing requirements). Significant financial penalties and regulatory intervention powers apply. |
| 5 | Optimized | Maximum regulatory density. Subject to multiple overlapping mandatory frameworks (e.g. GDPR, HIPAA, PCI-DSS, NIS2/DORA, SOX, NERC CIP, or equivalent national critical infrastructure regulations). Criminal liability for senior officers is possible. |

**2b — Geopolitical Data & People Sovereignty**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Single-jurisdiction operations. No cross-border data flows, no foreign workforce, and no exposure to geopolitical data access demands. |
| 2 | Developing | Limited cross-border operations in politically aligned jurisdictions. Data residency requirements are present but straightforward to implement. |
| 3 | Established | Multi-jurisdiction operations including some jurisdictions with active data sovereignty requirements (e.g. EU GDPR data transfer restrictions, China PIPL, India DPDP Act, Russia localisation requirements). |
| 4 | Advanced | Significant cross-border exposure with conflicting sovereignty requirements. Active management required for data residency, workforce nationality obligations, and foreign government data access requests. |
| 5 | Optimized | Global operations with structurally conflicting sovereignty laws (e.g. EU GDPR vs. US CLOUD Act, China DSL vs. EU SCCs). Active exposure to state-level surveillance demands, sanctions regimes, or contested digital jurisdiction. |

**2c — Incident Reporting & Notification Obligations**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No mandatory incident reporting obligations. Disclosure is entirely voluntary and at organizational discretion. |
| 2 | Developing | Voluntary or loosely defined reporting guidance from sector bodies. No enforceable timelines or penalties for non-disclosure. |
| 3 | Established | Mandatory breach notification obligations under one jurisdiction (e.g. 72-hour GDPR notification, US state breach laws). Defined scope and timeline for regulator and individual notification. |
| 4 | Advanced | Multi-jurisdiction mandatory reporting with different timelines and scope requirements (e.g. SEC material incident disclosure + GDPR + NIS2 significant incident reporting + sector-specific CERT notification). |
| 5 | Optimized | Complex multi-regulator, multi-timeline reporting obligations. Simultaneous notification required to financial regulators, data protection authorities, national CERTs, stock exchanges, and affected individuals across multiple jurisdictions — often with conflicting requirements. |

**2d — Cross-Sector Regulatory Overlap**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Single-sector operation with one clear regulatory regime. No cross-sector complexity. |
| 2 | Developing | Primarily single-sector with minor secondary activities (e.g. financial services firm with a small insurance subsidiary). Regulatory overlap is limited and manageable. |
| 3 | Established | Dual-sector operation (e.g. a healthcare organisation that also processes payment data). Two distinct cybersecurity regulatory regimes apply with partial overlap in requirements. |
| 4 | Advanced | Multi-sector conglomerate subject to 3+ distinct regulatory frameworks with different control requirements, audit rights, and penalty structures. |
| 5 | Optimized | Complex ecosystem of sector-spanning obligations (e.g. a systemically important financial institution that also operates critical infrastructure, cross-sector platform services, and health data processing under different regulatory regimes globally). |

**2e — International Standards & Framework Alignment Pressure**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No external pressure to demonstrate alignment with any international cybersecurity standard. No customer, investor, or regulatory expectation of certification. |
| 2 | Developing | Informal customer or partner preference for standards alignment. Some commercial advantage from certification but not a contractual or regulatory requirement. |
| 3 | Established | Contractual or procurement requirements for alignment with one or more standards (e.g. ISO 27001, SOC 2, NIST CSF, CSA STAR). Certification is a business enabler and some contracts require it. |
| 4 | Advanced | Formal certification requirements from multiple customer segments, regulators, or supply chain partners. Certification audits are a recurring operational activity. |
| 5 | Optimized | International standards alignment is a licence-to-operate requirement. Entry into major markets, contracts with critical customers, or access to regulated sectors is contingent on maintaining multiple concurrent certifications. |

---

### D3 · People

> **Core question:** How do career architecture, compensation systems, security culture, insider risk, and workforce diversity shape the organization's human capital foundation for cybersecurity?

This dimension evaluates the human infrastructure of the organization's security posture. People are simultaneously a primary asset and a primary vulnerability in any security program. D3 captures both dimensions.

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `3a` | Technical vs. Managerial Career Architecture | Whether career paths reward deep technical mastery or default entirely to management tracks, shaping long-term retention of critical technical expertise. |
| `3b` | Scarcity-Based Compensation Elasticity | The organization's structural ability to compete for skills in short supply without triggering pay band friction or prolonged approval delays. |
| `3c` | Security Awareness & Human Risk Culture | The breadth, depth, and effectiveness of security awareness across the workforce as a measurable reduction in human-factor risk. |
| `3d` | Insider Threat Risk Profile | The structural likelihood of malicious or negligent insider activity, based on access concentration, workforce profile, and monitoring capability. |
| `3e` | Workforce Distribution & Remote Security Posture | The security implications of geographic workforce distribution, remote and hybrid working patterns, and contractor/third-party staff integration. |

#### Descriptive Anchors — D3

**3a — Technical vs. Managerial Career Architecture**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | All career advancement requires transition to people management. Technical depth is not formally valued or rewarded. Senior technical staff must move to management or leave to progress. |
| 2 | Developing | Informal technical recognition exists but no structured parallel track. Individual contributors may receive ad hoc recognition but lack formal career progression pathways or compensation parity. |
| 3 | Established | An emerging technical career track exists with defined senior individual contributor roles. Compensation parity with management is partial; recognition is improving but the management track remains culturally dominant. |
| 4 | Advanced | Formal dual-track architecture with Staff/Principal/Senior Principal levels. Technical career paths are clearly defined, publicly communicated, and approach compensation parity with equivalent management levels. |
| 5 | Optimized | Mature engineering ladder with Distinguished Engineer/Fellow/Technical Director equivalents. Full compensation parity with executive management. Deep technical expertise is organizationally prized and institutional knowledge is actively retained. |

**3b — Scarcity-Based Compensation Elasticity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Rigid, non-negotiable pay bands enforced uniformly. No mechanism exists to compensate above band for any role, regardless of skill scarcity or market conditions. |
| 2 | Developing | Exceptions are theoretically possible but require escalation through multiple layers of HR and finance approval, taking weeks to months and often failing. |
| 3 | Established | Defined exceptions process exists with moderate friction. Compensation adjustments for scarce skills are achievable within 2–4 weeks with manager and HR director approval. |
| 4 | Advanced | Market-rate adjustments available through a streamlined approval workflow. Regular compensation benchmarking against cybersecurity-specific talent markets informs band-setting. |
| 5 | Optimized | Real-time compensation elasticity. The organization operates skill-market-driven pricing for critical security roles, responds rapidly to talent supply shifts, and competes effectively in any cybersecurity labor market globally. |

**3c — Security Awareness & Human Risk Culture**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No formal security awareness programme. Staff have no structured exposure to security practices, phishing risks, or incident reporting expectations. |
| 2 | Developing | Annual mandatory security awareness training exists, primarily for compliance purposes. Content is generic, not role-specific, and has no measurable impact on human-factor risk. |
| 3 | Established | Regular, structured awareness programme with phishing simulation, role-based training, and basic metrics (click rates, completion rates). Some evidence of behavioural improvement. |
| 4 | Advanced | Targeted, behaviour-focused awareness programme with tiered content by role and risk profile. Metrics-driven continuous improvement; measurable reduction in human-factor incidents over time. |
| 5 | Optimized | Human risk management is treated as an operational discipline. The organisation measures human risk by individual, role, and team; delivers just-in-time training; and has embedded security-conscious behaviour as a demonstrable cultural norm. |

**3d — Insider Threat Risk Profile**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | High insider threat exposure with no mitigation: broad privileged access, no activity monitoring, low staff loyalty indicators, and no formal insider threat programme. |
| 2 | Developing | Basic access controls exist but are not regularly reviewed. Some awareness of insider risk but no formal programme, behavioural monitoring, or defined response capability. |
| 3 | Established | Defined insider threat policy and access governance. Privileged access is controlled and reviewed. Basic user activity monitoring exists; HR and security coordinate on high-risk individual processes. |
| 4 | Advanced | Mature insider threat programme with behavioural analytics, defined risk indicators, formal investigation procedures, and cross-functional oversight (security, HR, legal). |
| 5 | Optimized | Comprehensive insider threat management: continuous behavioural monitoring, automated anomaly detection, regular access recertification, active intelligence programme, and demonstrated incident response capability for insider events. |

**3e — Workforce Distribution & Remote Security Posture**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Highly distributed workforce (remote/hybrid/contractor-heavy/multi-country) with no security controls adapted for distributed access. Endpoint security, network access, and remote work policies are absent or unenforced. |
| 2 | Developing | Basic remote access controls (VPN) exist but are inconsistently applied. Contractor and third-party staff are managed under the same or weaker security standards than employees. |
| 3 | Established | Defined remote work security policy with standard endpoint controls deployed across the workforce. Contractor integration is managed but third-party access controls have gaps. |
| 4 | Advanced | Mature distributed work security architecture. Endpoint management, secure access, and identity controls are consistently applied across employees, contractors, and partners regardless of location. |
| 5 | Optimized | Zero-trust access model applied across a fully distributed workforce. Location, device, and contractor status are irrelevant to security policy enforcement. Workforce security posture is continuously monitored regardless of geography. |

---

## 5. Pillar II — Econo

The **Econo** pillar evaluates the financial, cultural, and structural economic forces that govern how an organization funds, prioritizes, and sustains security capability. Economic factors determine what is *possible* in program design — independent of what is technically desirable. A program architecture that exceeds its economic conditions will not be sustained.

---

### D4 · Capital Flow

> **Core question:** How does the organization's funding model, labor economics, data infrastructure investment, and risk transfer strategy shape program sustainability and economic resilience?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `4a` | Multi-Year Funding Logic | Stability and predictability of capital allocation cycles — CapEx vs. OpEx orientation, annual budget cycles vs. multi-year programme commitments. |
| `4b` | Specialized SME Labor Scarcity | Market scarcity and fully-loaded cost-to-acquire for niche subject matter experts driving total programme labour cost. |
| `4c` | Data Intensity & Telemetry Scale | Volume, velocity, and variety of data instrumentation required, impacting storage, processing, and tooling cost trajectory at scale. |
| `4d` | Cyber Insurance & Risk Transfer Maturity | The organization's sophistication in using financial risk transfer instruments — cyber insurance, contractual indemnification, captive structures — to manage residual cyber risk economically. |

#### Descriptive Anchors — D4

**4a — Multi-Year Funding Logic**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Security funding is entirely project-by-project or ad hoc. No dedicated security budget line exists; funding competes annually against all other organizational priorities with no assurance of continuity. |
| 2 | Developing | Annual security budget exists but resets to zero each cycle. Significant year-end funding risk; programme continuity is contingent on re-approval every budget cycle. |
| 3 | Established | Annual budget with some informal multi-year commitment for major programme components. Some capital continuity assurance but dependence on annual approval remains. |
| 4 | Advanced | Formal 3-year security programme budget approved by board or executive committee. Defined milestones and spending envelopes provide reliable programme capital trajectory. |
| 5 | Optimized | Long-cycle capital commitment (5+ years) or endowed security capability that is structurally insulated from annual budget cycles, leadership change, and short-term financial pressures. |

**4b — Specialized SME Labor Scarcity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | All required security skills are widely available in the local labor market at standard rates. No meaningful scarcity premium applies to any required role. |
| 2 | Developing | Moderate scarcity for 1–2 role categories. Typical cost premium of 10–20% above general IT market rates; time-to-hire is extended but manageable. |
| 3 | Established | Significant scarcity for multiple role categories (e.g. cloud security architect, OT/ICS specialist, threat intelligence analyst). 20–50% cost premium with 2–4 month fill times. |
| 4 | Advanced | Severe scarcity in most critical security roles. 50–100% cost premium over general IT market; roles routinely take 4–8 months to fill. Reliance on contractors or consultants to fill permanent gaps. |
| 5 | Optimized | Extreme scarcity across the board. Critical roles (e.g. ICS security architect, red team lead, AI security researcher) take 6–18 months to fill; custom compensation structures required. The labor market cannot reliably supply required expertise at any price in local geographies. |

**4c — Data Intensity & Telemetry Scale**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Minimal telemetry. Low data volume environment with basic system logging only. No meaningful security data infrastructure cost. |
| 2 | Developing | Moderate instrumentation. Standard SIEM in place with conventional log management. Data volumes are manageable within standard licensing and infrastructure budgets. |
| 3 | | Established | High-volume telemetry across multiple domains (endpoint, network, cloud, application). Significant and growing storage, processing, and pipeline cost. Data architecture complexity is increasing. |
| 4 | Advanced | Enterprise-scale multi-source telemetry with complex data engineering requirements. SIEM/XDR/UEBA at scale; data management is a dedicated operational function with material cost. |
| 5 | Optimized | Petabyte-scale real-time telemetry. AI/ML processing required for analysis at volume. Data infrastructure is a major cost centre; scaling decisions have direct programme budget implications. |

**4d — Cyber Insurance & Risk Transfer Maturity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No cyber insurance. No formal contractual indemnification structures. Financial exposure from cyber events is entirely retained by the organisation with no risk transfer mechanism. |
| 2 | Developing | Basic cyber insurance policy exists but coverage terms are poorly understood. Policy was procured as a compliance exercise; coverage limits, exclusions, and conditions have not been systematically evaluated. |
| 3 | Established | Cyber insurance is actively managed with understood coverage terms, exclusions, and premium drivers. Annual policy review is conducted; some alignment between security controls and policy conditions. |
| 4 | Advanced | Sophisticated cyber insurance programme with tailored coverage, understood sub-limits, and active premium optimisation through security control improvement. Risk quantification informs coverage decisions. |
| 5 | Optimized | Mature risk transfer strategy integrating cyber insurance, captive structures, contractual risk allocation, and financial hedging. Insurance is one component of a quantified cyber risk management programme. Coverage decisions are driven by quantitative risk models (e.g. FAIR). |

---

### D5 · Culture

> **Core question:** How do organisational velocity, shared accountability, psychological safety, and the perceived role of security shape the cultural operating environment for a security programme?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `5a` | Product & Innovation Velocity | Speed at which the organisation ships new capability — a proxy for how rapidly the risk surface changes and how quickly security must adapt. |
| `5b` | Enterprise-wide Cyber-Accountability | Whether risk ownership is diffused across business functions or concentrated in a single team; distinguishes shared-accountability from siloed-penalty models. |
| `5c` | Psychological Safety & Incident Reporting Culture | Whether the organizational culture rewards early disclosure of security incidents, near-misses, and vulnerabilities — or punishes reporters and suppresses signals. |
| `5d` | Security-as-Enabler vs. Security-as-Blocker Perception | How the wider organization perceives the security function: as a business enabler and strategic partner, or as a bureaucratic obstacle and compliance cost. |

#### Descriptive Anchors — D5

**5a — Product & Innovation Velocity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Waterfall development or annual system release cycles. Change is infrequent, heavily governed, and highly predictable. Security review can be conducted as a discrete periodic activity. |
| 2 | Developing | Quarterly release cadence. Some agile adoption. Moderate change frequency; security involvement is episodic and typically occurs near release gates. |
| 3 | Established | Monthly releases. Agile methodology broadly adopted. Security is involved in development cycles but integration is incomplete; some security review backlog exists. |
| 4 | Advanced | Weekly releases across most development teams. CI/CD pipeline adopted. Security tooling is partially integrated into delivery pipelines; shifting left is in progress. |
| 5 | Optimized | Continuous deployment with multiple daily releases. Security is natively integrated into the development platform; automated security gates are embedded in every deployment pipeline. Human security review occurs only at risk-threshold events. |

**5b — Enterprise-wide Cyber-Accountability**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Security is entirely siloed. All accountability for cyber outcomes is assigned to the security team. Business units have no formal security obligations, no risk ownership, and no performance measures related to security. |
| 2 | Developing | Broad awareness of security importance exists at business unit level but no formal accountability structures. Business units support security initiatives when convenient but are not held to account for outcomes. |
| 3 | Established | Risk ownership is formally assigned to business units in some domains. Risk acceptance processes exist. Accountability is documented but enforcement is inconsistent. |
| 4 | Advanced | Business units hold measurable accountability for cyber risk in their domain. Security is treated as a shared function; risk owners engage with the security team as partners rather than service consumers. |
| 5 | Optimized | Cyber accountability is embedded in enterprise performance frameworks: business unit leaders have security-related KPIs/OKRs, security outcomes influence compensation, and the board receives regular enterprise-wide accountability reporting. |

**5c — Psychological Safety & Incident Reporting Culture**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Punitive culture around security failures. Staff fear consequences for reporting incidents, near-misses, or vulnerabilities. Incidents are concealed; the organisation has no reliable view of its actual security event landscape. |
| 2 | Developing | Incident reporting is nominally encouraged but fear of blame or consequence suppresses early disclosure. Reports tend to arrive late and incomplete; near-miss reporting is rare. |
| 3 | Established | Blameless reporting is formally stated policy. Incident reporting channels exist and are used. Some residual fear of consequence persists in practice; reporting is improving but not yet a cultural norm. |
| 4 | Advanced | Psychological safety around security reporting is well established. Staff actively report near-misses; the organisation treats early disclosure as a positive signal and acts on reports constructively. |
| 5 | Optimized | Security reporting is a deeply embedded cultural behaviour. The organisation systematically collects, analyses, and learns from near-miss and precursor signals. Security incident reports are treated as intelligence inputs that improve organisational resilience. |

**5d — Security-as-Enabler vs. Security-as-Blocker Perception**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Security is universally perceived as an obstacle to business operations. Business leaders actively route around security processes. Security function has no credibility or influence outside of compliance-mandated activities. |
| 2 | Developing | Security is tolerated as a compliance necessity. Business leaders engage with security reluctantly and only when required. No positive perception of security as a business enabler exists. |
| 3 | Established | Mixed perception. Some business leaders view security as a partner; others view it as overhead. The security team is working to build credibility but has not yet achieved broad business sponsorship. |
| 4 | Advanced | Security is broadly perceived as a business enabler. Business leaders proactively engage with the security team; security input is sought early in business decisions. The CISO has a strategic voice in business discussions. |
| 5 | Optimized | Security is a recognized business differentiator. The organisation uses its security posture as a competitive advantage (e.g. in procurement, customer trust, investor relations, and market positioning). Security is institutionally valued at all levels. |

---

### D6 · Constraints

> **Core question:** What structural ceilings — executive authority limitations, corporate restructuring complexity, vendor dependency, and organizational change fatigue — limit the ambition and execution capacity of the security programme?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `6a` | Executive Sponsorship & Influence Depth | How high and how wide executive mandate extends for security investment, behavioural change, and organisational priority-setting. |
| `6b` | M&A / Divestiture Frequency | Rate of corporate restructuring events that introduce integration complexity, inherited risk, and attack surface volatility. |
| `6c` | Vendor & Third-Party Dependency Lock-in | Degree to which strategic technology vendor lock-in constrains security architecture decisions and limits the organisation's ability to implement optimal security controls. |
| `6d` | Organisational Change Fatigue & Reform Tolerance | The workforce's capacity to absorb further security-driven behavioural, process, and technology changes without reform exhaustion. |

#### Descriptive Anchors — D6

**6a — Executive Sponsorship & Influence Depth**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No meaningful executive sponsor. Security decisions are made at operational or middle-management level. Security has no budget authority and no pathway to executive escalation. |
| 2 | Developing | VP-level or equivalent sponsor exists with limited budget authority and narrow organisational reach. Security is visible to leadership but not a strategic priority. |
| 3 | Established | C-suite awareness and engagement. CISO or equivalent has a seat at the senior leadership table and regular access to the CEO. Security is considered in major business decisions. |
| 4 | Advanced | CEO and Board-level engagement. Security is explicitly framed as enterprise risk and receives board-level oversight. The CISO has direct escalation to the CEO and board risk committee. |
| 5 | Optimized | Board-mandated security accountability. Individual board members have personal accountability for cyber risk oversight. Executive team performance measures include security outcomes. Security is treated as a strategic enterprise capability at the highest organisational level. |

**6b — M&A / Divestiture Frequency**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No M&A or divestiture activity. Corporate structure is stable with no integration complexity and no inherited security risk from acquisitions. |
| 2 | Developing | Rare transactions (fewer than 1 per 5 years). When transactions occur, integration scope is manageable and security implications are limited. |
| 3 | Established | Occasional transactions (1–2 per 3 years). Active integration work exists; inherited security debt from recent acquisitions is being addressed. |
| 4 | Advanced | Regular M&A activity (1–2 transactions per year). Persistent integration backlog; acquired organisations routinely introduce new attack surface, technology debt, and regulatory obligations. |
| 5 | Optimized | Continuous M&A and/or divestiture activity. Corporate structure is in a near-permanent state of change; security programme must continuously accommodate new entities, systems, and risk profiles. Integration complexity dominates available security capacity. |

**6c — Vendor & Third-Party Dependency Lock-in**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No significant vendor lock-in. Technology stack is modular and portable; the organisation can change security tooling and providers with minimal switching cost. |
| 2 | Developing | Some platform dependency exists but alternatives are available. Transitioning primary security tools would be costly but feasible within a 12-month programme. |
| 3 | Established | Material vendor lock-in in 1–2 platform categories. Security architecture decisions are partially constrained by existing contracts, integrations, or proprietary data formats. |
| 4 | Advanced | Deep lock-in across multiple strategic platforms (cloud hyperscaler, ERP, security tooling). Switching costs are prohibitive for most major components; security decisions must work within existing vendor constraints. |
| 5 | Optimized | Profound ecosystem lock-in. Core business operations and security architecture are fundamentally inseparable from a small number of strategic vendors. Independent security architecture decisions are structurally impossible in most domains. |

**6d — Organisational Change Fatigue & Reform Tolerance**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Workforce is highly resistant to change. The organisation has recently undergone multiple major transformation programmes; staff are exhausted and cynical. Any further security-driven change faces structural resistance. |
| 2 | Developing | Moderate change fatigue present. Staff are willing to participate in security initiatives but discretionary effort is limited; adoption of new controls and behaviours is slower than expected. |
| 3 | Established | Neutral change tolerance. The workforce is neither resistant nor proactively engaged with security-driven change. Security initiatives succeed when well-managed and resourced; fail when poorly communicated or resourced. |
| 4 | Advanced | Good change absorption capacity. The organisation has effective change management capability; security-driven transformation programmes are supported with appropriate communication, training, and reinforcement. |
| 5 | Optimized | High reform tolerance and organisational agility. The workforce actively embraces security improvements; change management is a core organisational capability; security transformation initiatives are adopted rapidly and sustainably. |

---

## 6. Pillar III — Tech

The **Tech** pillar evaluates the operational, engineering, and adversarial dimensions of the organisation's technical estate. It captures process discipline, technical capability, and threat exposure as a unified technical maturity signal. Tech factors are most susceptible to over-investment without Socio and Econo foundations — advanced tooling in an immature process environment produces marginal security improvement at high cost.

---

### D7 · Process

> **Core question:** How mature are the organisation's operational workflows, asset understanding, incident response capability, supply chain risk processes, and change management discipline?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `7a` | Operational Workflow Maturity & Discipline | Consistency, documentation, and enforcement of core operational processes as a signal of control quality and repeatability. |
| `7b` | Critical Asset & Business Service Mapping | Quality and currency of asset inventory and the mapping between technology components and the business services they underpin. |
| `7c` | Incident Response Lifecycle Maturity | The organisation's structured capability to detect, contain, eradicate, recover from, and learn from security incidents. |
| `7d` | Third-Party & Supply Chain Risk Process | Formal capability to assess, monitor, and manage the security posture of third-party providers and supply chain partners. |
| `7e` | Change Management & Configuration Control | Rigour of processes governing technology changes and configuration management as a control against unintended security degradation. |

#### Descriptive Anchors — D7

**7a — Operational Workflow Maturity & Discipline**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No documented security processes. Responses to security events are entirely ad hoc; outcomes depend on the individual responding rather than a defined process. |
| 2 | Developing | Some documentation exists but processes are inconsistently followed. Significant variance in how security tasks are performed across teams and individuals. |
| 3 | Established | Core security processes are documented and generally followed. Significant gaps remain in some areas; process compliance is enforced inconsistently across the organisation. |
| 4 | Advanced | Standardised, measured security processes are in place across primary operational domains. Regular process review cycles occur; continuous improvement is embedded in operational rhythm. |
| 5 | Optimized | Process excellence with automated enforcement, continuous performance monitoring, full audit trails, and documented evidence of process-driven outcome improvement. The organisation can demonstrate that its security operations quality is process-driven, not people-dependent. |

**7b — Critical Asset & Business Service Mapping**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No asset inventory exists. The organisation cannot identify its critical systems, data stores, or the technology supporting its most important business services. |
| 2 | Developing | Partial inventory exists for some technology categories. Critical assets (crown jewels) have not been formally identified, classified, or mapped to the business services they support. |
| 3 | Established | Asset inventory maintained across major technology categories. Business service dependency mapping is incomplete; gaps exist in cloud, third-party, and OT/IoT domains. |
| 4 | Advanced | Comprehensive asset inventory with formal crown jewel identification and business service mapping, regularly updated through defined review cycles. Dependencies are documented and understood. |
| 5 | Optimized | Real-time asset intelligence with automated discovery, continuous enrichment, and full mapping between technology components and the business services they underpin — including cloud workloads, containers, APIs, shadow IT, and third-party integrations. |

**7c — Incident Response Lifecycle Maturity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No incident response plan. When incidents occur, response is improvised; there is no defined team, no communication structure, and no recovery procedure. |
| 2 | Developing | Basic incident response procedure exists on paper. The plan has not been tested; roles are loosely defined; communication protocols are unclear. Response effectiveness depends on individual initiative. |
| 3 | Established | Documented incident response plan with defined roles and escalation procedures. The plan has been tested at least annually through tabletop exercises. Post-incident reviews occur but lessons learned are inconsistently applied. |
| 4 | Advanced | Mature incident response capability with defined playbooks for high-probability incident types, regular simulation exercises (including technical exercises), and a demonstrated post-incident improvement cycle. Metrics track mean-time-to-detect and mean-time-to-respond. |
| 5 | Optimized | World-class incident response capability with continuously rehearsed playbooks, automated detection-to-response workflows, a dedicated incident response team or retainer, and a documented track record of effective incident containment and recovery across multiple significant events. |

**7d — Third-Party & Supply Chain Risk Process**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No third-party security assessment process. Suppliers and partners are granted access to systems and data without any formal security evaluation. |
| 2 | Developing | Basic questionnaire-based supplier assessment exists for new high-risk vendors. Assessments are point-in-time, not reassessed, and outcomes do not systematically influence contracting decisions. |
| 3 | Established | Formal third-party risk management programme covering new vendor onboarding. Tiered assessment approach based on risk. Some contractual security obligations in supplier contracts. Ongoing monitoring is limited. |
| 4 | Advanced | Mature TPRM programme with risk-tiered assessments, contractual security requirements, periodic reassessment, and defined remediation tracking. Concentration risk in critical suppliers is monitored. |
| 5 | Optimized | Comprehensive supply chain security programme covering suppliers, sub-processors, and nth-party dependencies. Continuous monitoring, real-time risk scoring, contractual audit rights exercised, and incident response integration across the supply chain. |

**7e — Change Management & Configuration Control**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No formal change management process. Technology changes are made without review, documentation, or approval. Security configurations frequently change without awareness or oversight. |
| 2 | Developing | Basic change management process exists for major changes but is not consistently applied. Emergency changes routinely bypass the process. Security review is not a standard step in the change process. |
| 3 | Established | Formal change management process with security review as a defined gate for significant changes. Emergency change process exists and is documented. Configuration baselines are established for major systems but drift occurs. |
| 4 | Advanced | Mature change and configuration management. Security review is integrated into all change types. Configuration drift is regularly detected and remediated. Change-related security incidents are tracked and drive process improvement. |
| 5 | Optimized | Change management and configuration control are fully integrated with security operations. Automated configuration enforcement prevents drift in real time; all changes are security-reviewed and tracked. Security impact assessment is embedded in the change approval workflow. |

---

### D8 · Technical

> **Core question:** How cohesive is the organisation's telemetry architecture, how deep is its engineering culture, how mature is its identity security, how well-designed is its cloud security architecture, and how effective is its vulnerability management lifecycle?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `8a` | Telemetry Cohesion & Interoperability | Degree to which monitoring signals across all domains are unified, correlated, normalized, and actionable. |
| `8b` | Organisational Engineering DNA & Automation Capability | Depth of software engineering culture enabling automation of detection, response, and security operations. |
| `8c` | Identity & Access Management Maturity | Sophistication of the organisation's approach to identity as the primary security control plane — particularly in distributed, cloud, and hybrid environments. |
| `8d` | Cloud Security Architecture Maturity | The rigour, coherence, and enforcement capability of security controls across cloud environments. |
| `8e` | Vulnerability Management Lifecycle | The organisation's ability to systematically discover, prioritise, remediate, and track vulnerabilities across its entire technology estate. |

#### Descriptive Anchors — D8

**8a — Telemetry Cohesion & Interoperability**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Siloed, disconnected logging across systems. No correlation capability. Security teams have no unified view of activity across the estate; investigations require manual log collection from multiple disconnected sources. |
| 2 | Developing | Partial SIEM adoption with some log aggregation. Significant blind spots exist in cloud, OT, or application layers. Correlation capability is limited; analyst work is predominantly manual. |
| 3 | Established | Centralised SIEM with moderate cross-domain correlation. Coverage across endpoint and network is solid; cloud and identity coverage is partial. Alerting exists but signal-to-noise ratio is high. |
| 4 | Advanced | High-fidelity normalized telemetry across endpoint, network, cloud, identity, and application layers. XDR or equivalent correlation capability reduces analyst burden. Detection logic is curated and regularly tuned. |
| 5 | Optimized | Unified real-time telemetry fabric spanning all technology domains including OT/IoT and supply chain integration points. ML-driven automated enrichment and correlation. Detection-as-code governs alert logic. Mean-time-to-detect for high-priority threat scenarios is measured in minutes. |

**8b — Organisational Engineering DNA & Automation Capability**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No engineering culture in the security function. Security tools are operated as black boxes; vendor defaults are used without customisation. No automation capability exists. |
| 2 | Developing | Limited scripting capability for basic task automation (log parsing, report generation). Security team relies on vendor tooling; no internally developed detection logic or automation. |
| 3 | Established | Moderate automation capability. Some detection-as-code and playbook automation implemented. A subset of the security team has software engineering skills and builds lightweight internal tooling. |
| 4 | Advanced | Strong engineering culture within the security function. Detection logic is built and maintained as code. Significant operational tasks are automated via SOAR or custom tooling. Internal security tools are developed and maintained. |
| 5 | Optimized | Engineering-first security operations. The security team operates as a software engineering organisation that produces security capability. Detection-as-code, infrastructure-as-code, and full pipeline automation are standard practice. The security team contributes to open-source security tooling and drives industry capability. |

**8c — Identity & Access Management Maturity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No formal IAM programme. User accounts are created and removed ad hoc; privileged access is unmanaged; shared accounts are common; no Multi-Factor Authentication enforced. |
| 2 | Developing | Basic IAM processes exist: user onboarding/offboarding is defined, MFA is deployed for some systems. Access reviews are infrequent or absent. Privileged access management is manual and inconsistent. |
| 3 | Established | Formal IAM programme with defined lifecycle management, MFA broadly enforced, and Privileged Access Management tooling in place for critical systems. Access reviews occur on an annual cycle. Role-based access control is partially implemented. |
| 4 | Advanced | Mature IAM capability with just-in-time privileged access, regular access recertification, strong authentication enforced universally, and identity governance tooling providing visibility and control across the user population. |
| 5 | Optimized | Identity is operated as the primary security control plane. Zero-standing-privilege architecture for administrative access, continuous access review, risk-adaptive authentication, non-human identity management (service accounts, API keys, machine identities), and full identity lifecycle automation. |

**8d — Cloud Security Architecture Maturity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Cloud environments exist but have no security architecture. Workloads are deployed without security review; no cloud security policy, tooling, or governance exists. |
| 2 | Developing | Basic cloud security controls in place for major workloads (e.g. some network segmentation, storage encryption defaults). Cloud security governance is informal; shadow cloud usage is prevalent and untracked. |
| 3 | Established | Defined cloud security architecture with enforced baseline controls (CSPM deployed, network segmentation designed, encryption-at-rest enforced). Cloud security is integrated into architecture review. Multi-cloud or hybrid complexity is managed with some gaps. |
| 4 | Advanced | Mature cloud security programme with Cloud Security Posture Management, Cloud Workload Protection, and defined Landing Zone architecture. Security-by-default is enforced through Infrastructure-as-Code policies. Cloud security incidents are detected and responded to with acceptable MTTD/MTTR. |
| 5 | Optimized | Cloud security is a differentiating organisational capability. Policy-as-code enforces security standards in real time across all cloud environments. Automated remediation, developer-embedded security guardrails, and continuous compliance monitoring eliminate security drift. Cloud security architecture is regularly reviewed against emerging threat vectors. |

**8e — Vulnerability Management Lifecycle**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No formal vulnerability management programme. Known vulnerabilities are not systematically tracked; patching is reactive and uncoordinated. |
| 2 | Developing | Periodic vulnerability scanning exists for some systems. Results are reviewed but remediation is inconsistent; no formal SLA for vulnerability remediation; critical patches are routinely delayed. |
| 3 | Established | Formal vulnerability management programme with defined scanning cadence, risk-based prioritisation, and remediation SLAs for critical and high vulnerabilities. Compliance with SLAs is tracked but not consistently achieved. |
| 4 | Advanced | Mature vulnerability management with continuous scanning, risk-based prioritisation informed by threat intelligence and asset criticality, defined and enforced remediation SLAs, and formal exception management for accepted risks. |
| 5 | Optimized | Comprehensive vulnerability management encompassing traditional CVEs, cloud misconfigurations, container vulnerabilities, open-source dependency risks, and API security. Exposure management extends across the full attack surface. CISA KEV and threat-intelligence-informed prioritisation drives remediation sequencing. Mean-time-to-remediate for critical vulnerabilities is measured and meets or exceeds industry benchmarks. |

---

### D9 · Threat Landscape

> **Core question:** What is the sophistication and targeting intent of adversaries, the structural complexity of the attack surface, supply chain compromise risk, geopolitical threat exposure, and insider threat probability?

| ID | Sub-Factor | Selection Logic |
|:---|:---|:---|
| `9a` | Adversary Sophistication & Intent | Profile of threat actors targeting the organisation — nation-state APTs, organised eCrime, hacktivists — and their operational maturity, tooling, and targeting persistence. |
| `9b` | Attack Surface Structural Complexity | Breadth and interconnectedness of the digital estate: cloud sprawl, legacy technology debt, third-party exposure, OT/IT convergence, and shadow IT prevalence. |
| `9c` | Supply Chain & Third-Party Compromise Risk | Exposure to adversaries who use supply chain and third-party access as an attack vector against the organisation — distinct from operational dependency risk captured in D1. |
| `9d` | Geopolitical & Nation-State Threat Exposure | Degree to which the organisation is targeted or likely to be targeted by nation-state actors motivated by geopolitical, economic espionage, or critical infrastructure disruption objectives. |
| `9e` | Insider Threat Probability & Detection Capability | Combined assessment of the probability that an insider event will occur and the organisation's current capability to detect it before significant damage occurs. |

#### Descriptive Anchors — D9

**9a — Adversary Sophistication & Intent**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No threat intelligence function. Adversary profile is entirely unknown. The organisation has no structured understanding of who targets organisations in its sector or what techniques they use. |
| 2 | Developing | General sector threat awareness based on public reports. No adversary-specific intelligence. The organisation is aware that threats exist at a sector level but has no operationalised intelligence. |
| 3 | Established | Sector-level threat intelligence maintained through ISAC membership, commercial feeds, or national CERT subscriptions. General adversary profiles are understood; intelligence is not fully operationalised into detection design. |
| 4 | Advanced | Targeted CTI programme with named adversary tracking, TTP-level intelligence, and integration into detection engineering. The organisation understands which actors are likely targeting it and can attribute incidents to known groups. |
| 5 | Optimized | Mature, intelligence-led security operations. Real-time adversary tracking with organic and partner-sourced collection. All detection logic, threat hunting, and incident response prioritisation is informed by current, organisation-specific threat intelligence. |

**9b — Attack Surface Structural Complexity**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | Minimal attack surface. Simple, monolithic environment with limited external exposure, no cloud footprint, no OT/IoT, and a small, well-understood perimeter. |
| 2 | Developing | Moderate complexity. Some cloud adoption and third-party connectivity; perimeter is expanding but primary exposure points are known and manageable. |
| 3 | Established | Significant complexity. Hybrid estate with multi-cloud, legacy systems, third-party integrations, and some OT or IoT components. Known gaps in attack surface visibility exist. |
| 4 | Advanced | High complexity. Distributed multi-cloud, legacy debt, active digital transformation, extensive third-party connectivity, and OT/IT convergence. Attack surface is difficult to fully enumerate; continuous attack surface management is required. |
| 5 | Optimized | Extreme structural complexity. Attack surface spans global cloud infrastructure, OT/critical systems, mobile, APIs, supply chain integration points, and an unknown volume of shadow IT. The organisation operates in a permanent state of incomplete attack surface visibility despite active management efforts. |

**9c — Supply Chain & Third-Party Compromise Risk**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No meaningful supply chain attack surface. The organisation has minimal third-party technology dependencies and no exposure to software supply chain risk. |
| 2 | Developing | Limited supply chain exposure. Some commercial off-the-shelf software and SaaS services in use. Software supply chain risk is present but not formally assessed. |
| 3 | Established | Moderate supply chain risk. Multiple commercial SaaS platforms, open-source dependencies, and managed service providers create known supply chain exposure. Some supply chain compromise scenarios have been risk-assessed. |
| 4 | Advanced | High supply chain risk. The organisation depends on complex, multi-tier software supply chains, critical managed service providers, and open-source ecosystems. Known supply chain attack scenarios are actively monitored. |
| 5 | Optimized | Extreme supply chain exposure. The organisation is a high-value target for supply chain compromise due to its position as a platform or critical infrastructure provider whose compromise would cascade to downstream organisations. Nation-state and eCrime actors have demonstrated interest in supply chain attack vectors against this sector. |

**9d — Geopolitical & Nation-State Threat Exposure**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | No meaningful geopolitical threat exposure. The organisation operates in a single non-contested jurisdiction with no state-sensitive data, no critical infrastructure role, and no profile that would attract state-sponsored adversary attention. |
| 2 | Developing | Low-level geopolitical exposure. The organisation operates in a jurisdiction that experiences some state-sponsored cyber activity but is not itself a likely primary target. |
| 3 | Established | Moderate geopolitical exposure. The organisation operates in a sector (finance, energy, healthcare, technology, defence supply chain) that nation-state actors are known to target for economic espionage or pre-positioning. |
| 4 | Advanced | High geopolitical exposure. The organisation has been identified as a likely target of nation-state actors through CTI reporting, peer sector incidents, or government advisories. Operations span jurisdictions with active adversarial cyber programmes. |
| 5 | Optimized | Extreme geopolitical exposure. The organisation is a confirmed or highly probable target of nation-state cyber operations. It operates critical national infrastructure, holds state-sensitive data, or has a strategic profile that makes it a priority target in active geopolitical conflicts. |

**9e — Insider Threat Probability & Detection Capability**

| Score | Label | Anchor |
|:---:|:---|:---|
| 1 | Nascent | High insider threat probability with no detection capability: broad standing privileged access, no activity monitoring, no behavioural analytics, no formal insider threat programme, and no history of insider event detection. |
| 2 | Developing | Basic access controls reduce the insider threat attack surface marginally. Some after-the-fact log review capability exists but no proactive detection. The organisation would likely discover an insider event only after significant damage occurred. |
| 3 | Established | Defined insider threat risk reduction programme. Privileged access is controlled; basic user activity monitoring is in place. Some capacity to detect anomalous behaviour exists; insider events would likely be detected within days to weeks. |
| 4 | Advanced | Mature insider threat programme with behavioural analytics, defined risk indicators, and a cross-functional oversight model (security, HR, legal). The organisation has demonstrated capability to detect and respond to insider events before catastrophic data loss. |
| 5 | Optimized | Comprehensive insider threat management: continuous behavioural monitoring, automated anomaly detection integrated with HR and access management systems, active intelligence programme for high-risk individuals, and a documented track record of successful early insider event detection and containment. |

---

## 7. Scoring Model

### 7.1 Maturity Scale

All sub-factors are scored on a five-point ordinal maturity scale:

| Score | Label | Definition |
|:---:|:---|:---|
| **1** | **Nascent** | No formal capability. Approach is entirely ad hoc, reactive, and undocumented. The organisation cannot reliably describe what it does in this area. |
| **2** | **Developing** | Awareness and intent exist. Initiatives are fragmented, inconsistent, or in early stages. Progress is visible but outcomes are not yet reliable or repeatable. |
| **3** | **Established** | Documented, repeatable capability is in place. Core function is operational with meaningful gaps remaining. Performance is consistent but not yet measured or continuously improved. |
| **4** | **Advanced** | Measured, proactive, and well-integrated capability. Approaching best-in-class for the sector. Evidence of sustained performance exists; improvement is driven by data. |
| **5** | **Optimized** | Continuous improvement culture with evidence of industry-leading performance. The organisation can demonstrate consistent outcomes, lessons-learned integration, and capability growth over time. |

> **Critical instruction for assessors:** Scores represent the organisation's **current, consistently practised operational reality** — not its documented policy, stated intent, or aspirational state. The question is always: *"What does this organisation reliably do today?"* not *"What does its policy say it should do?"*

### 7.2 Sub-Factor Scoring

Each of the 42 sub-factors receives a single integer score `s ∈ {1, 2, 3, 4, 5}`. Fractional scores are not permitted in the standard model — the assessor must commit to the anchor that most accurately describes the current organisational state.

When two adjacent anchors both partially apply, the lower score should be selected unless the higher anchor is demonstrably true for the majority of the organisation. The principle of **conservative scoring** prevents systematic upward bias and produces more actionable output by clearly identifying gaps.

### 7.3 Dimension Score Computation

The dimension score is the arithmetic mean of all sub-factor scores within that dimension:

```
D_n = (1/k) × Σ s_i     for i = 1 to k
```

Where `k` = number of sub-factors in dimension n, and `s_i` = score for sub-factor i.

All sub-factors within a dimension carry equal weight. This design choice prioritises assessment tractability and consistency over marginal computational precision.

### 7.4 Dimension Weight Configuration

Each of the nine dimensions is assigned a percentage weight `w_n` by the assessor, subject to the constraint:

```
Σ w_n = 100     for n = D1 to D9
```

Weights encode the assessor's expert judgement about the **relative strategic importance** of each dimension for the specific organisation, context, and assessment purpose. They must be:

1. **Justified** — Each weight assignment should be documented with a rationale in the assessment record.
2. **Organisation-specific** — Weights that are appropriate for a financial services firm may be entirely inappropriate for a manufacturing company or a government agency.
3. **Stable within an engagement** — Weights should be set before scoring begins and not changed post-hoc to influence the composite output.

### 7.5 Composite Score Computation

```
C = Σ (D_n × w_n / 100)     for n = D1 to D9
```

**Composite score interpretation bands:**

| Range | Label | Implication |
|:---|:---|:---|
| 1.00 – 1.79 | **Nascent** | Foundational gaps across most dimensions. Baseline capability investment is required before any advanced programme work. |
| 1.80 – 2.59 | **Developing** | Pockets of capability exist but inconsistently. Anchor dimensions must be established before scope expansion. |
| 2.60 – 3.39 | **Established** | Core foundations in place. Programme focus shifts from building to scaling and integrating. |
| 3.40 – 4.19 | **Advanced** | Strong proactive posture. Investment focus: resilience, automation, and edge capability areas. |
| 4.20 – 5.00 | **Optimized** | Industry-leading maturity. Programme focus: continuous improvement and intelligence-led operations. |

### 7.6 Full Expanded Formula (v2.0 — 42 Sub-Factors)

```
C =   (((s_1a + s_1b + s_1c + s_1d + s_1e) / 5) × w_D1 / 100)
    + (((s_2a + s_2b + s_2c + s_2d + s_2e) / 5) × w_D2 / 100)
    + (((s_3a + s_3b + s_3c + s_3d + s_3e) / 5) × w_D3 / 100)
    + (((s_4a + s_4b + s_4c + s_4d)         / 4) × w_D4 / 100)
    + (((s_5a + s_5b + s_5c + s_5d)         / 4) × w_D5 / 100)
    + (((s_6a + s_6b + s_6c + s_6d)         / 4) × w_D6 / 100)
    + (((s_7a + s_7b + s_7c + s_7d + s_7e) / 5) × w_D7 / 100)
    + (((s_8a + s_8b + s_8c + s_8d + s_8e) / 5) × w_D8 / 100)
    + (((s_9a + s_9b + s_9c + s_9d + s_9e) / 5) × w_D9 / 100)
```

---

## 8. Output Classification Engine

### 8.1 Classification Philosophy

The classification engine operates on a single governing principle: **the output earns its label from the data.** Classical archetypes are reference vectors against which the dimensional profile is compared — they are not destinations that organizations are directed toward. This distinction is the single most important design principle in the SET Framework.

The classification process:
1. Compute the full dimensional score vector `V = [D1, D2, D3, D4, D5, D6, D7, D8, D9]`
2. Compute cosine similarity between V and each classical archetype reference vector
3. Apply threshold logic to assign: **Classical**, **Hybrid**, or **Novel**
4. If Novel: derive a model name algorithmically from the dimensional signature
5. Present classical archetypes as a ranked reference table — orientation, not prescription

### 8.2 Classical Archetype Reference Vectors (v2.0)

Reference vectors represent the theoretical ideal-state dimensional profile of an organisation that fully embodies each archetype. They are expressed on the same 1–5 scale as the assessment instrument.

| Archetype | Abbr | D1 | D2 | D3 | D4 | D5 | D6 | D7 | D8 | D9 |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Compliance-Centric Program | CCP | 3 | 5 | 2 | 3 | 2 | 3 | 4 | 2 | 2 |
| Risk-Based Management Model | RBM | 4 | 3 | 3 | 4 | 3 | 4 | 4 | 3 | 3 |
| Threat-Informed Defense | TID | 4 | 2 | 4 | 4 | 4 | 4 | 4 | 5 | 5 |
| Zero Trust Architecture | ZTA | 4 | 3 | 3 | 4 | 4 | 5 | 5 | 5 | 4 |
| Resilience-Oriented Program | ROP | 5 | 3 | 3 | 4 | 3 | 4 | 5 | 4 | 3 |
| DevSecOps / Shift-Left Model | DSO | 3 | 2 | 5 | 3 | 5 | 3 | 4 | 5 | 3 |

**Archetype descriptions:**

**CCP — Compliance-Centric Program**
Security investment driven primarily by regulatory obligation. Programme scope and budget are proportional to penalty risk rather than threat reality. Common in heavily regulated industries at early-to-mid maturity stages where the regulatory driver is more powerful than the operational risk driver. The programme can achieve significant maturity in D2 and D7 while remaining underdeveloped in D3, D5, and D8.

**RBM — Risk-Based Management Model**
Quantified risk as the primary decision framework. Investment is sequenced by expected loss reduction rather than regulatory requirement or threat sophistication. Balanced profile across all three pillars; structured around a documented risk appetite and tolerance framework. Common in mature, well-governed organisations where the board expects risk management language.

**TID — Threat-Informed Defense**
Adversary behaviour as the primary design input. CTI-led, MITRE ATT&CK-aligned, detection-engineering-first posture. Requires high D8 (Technical) and D9 (Threat Landscape) scores as prerequisites; depends on strong D3 (People) for engineering depth. Common in high-threat-profile sectors (financial services, critical infrastructure, technology) with sophisticated security teams.

**ZTA — Zero Trust Architecture**
Identity and micro-segmentation as the control plane. Perimeter-less, verify-always design philosophy. Requires strong D7 (Process), D8 (Technical), and D6 (Constraints — specifically executive mandate) as prerequisites. Common in cloud-native organisations and those with highly distributed workforces where perimeter-based security is architecturally impossible.

**ROP — Resilience-Oriented Program**
Business continuity and rapid recovery as the primary security objective. Assume-breach, minimise-impact posture. Driven by high D1 (Business Mission) scores indicating that operational continuity is existentially important. Common in critical national infrastructure, healthcare, and manufacturing where operational downtime is the primary risk consequence.

**DSO — DevSecOps / Shift-Left Model**
Security embedded natively in the development lifecycle. Velocity-aligned, engineering-native capability. Driven by high D3 (People) and D5 (Culture) scores indicating deep engineering culture and high development velocity. Common in technology product companies and cloud-native organisations where the product is the security surface.

### 8.3 Cosine Similarity Algorithm

Cosine similarity measures the angular distance between two vectors in n-dimensional space, independent of magnitude. It is appropriate for the SET classification engine because it captures the **shape** of the dimensional profile — the relative pattern of scores — rather than absolute distance, which would unfairly penalise organisations that score uniformly high or low.

```
cos_sim(A, B) = (A · B) / (||A|| × ||B||)
             = Σ(A_i × B_i) / (√(Σ A_i²) × √(Σ B_i²))
```

**Pseudocode implementation:**
```python
def cosine_similarity(subject: dict, archetype: dict) -> float:
    dims = list(subject.keys())
    dot_product   = sum(subject[d] * archetype[d] for d in dims)
    mag_subject   = sum(subject[d] ** 2 for d in dims) ** 0.5
    mag_archetype = sum(archetype[d] ** 2 for d in dims) ** 0.5
    if mag_subject == 0 or mag_archetype == 0:
        return 0.0
    return dot_product / (mag_subject * mag_archetype)

# Compute and rank all archetypes
similarities = [
    {"archetype": a, "score": cosine_similarity(dim_scores, a["sig"])}
    for a in ARCHETYPES
]
similarities.sort(key=lambda x: x["score"], reverse=True)
top_match = similarities[0]
```

### 8.4 Classification Threshold Logic

```
if   top_match.score >= 0.975  →  CLASSICAL
elif top_match.score >= 0.920  →  HYBRID
else                           →  NOVEL
```

| Type | Threshold | Strategic Implication |
|:---|:---|:---|
| **Classical** | ≥ 97.5% | The dimensional profile closely conforms to a known archetype. Established guidance, frameworks, and toolkits for that archetype are directly applicable. |
| **Hybrid** | 92% – 97.4% | Meaningful alignment with the closest archetype but significant deviation across multiple dimensions. Selective borrowing from the archetype is appropriate; wholesale adoption is not. |
| **Novel** | < 92% | No established archetype fits the profile. An original programme architecture is required, derived from the organisation's specific dimensional signature. |

### 8.5 Novel Model Naming Algorithm

When the output is Novel, the model is named from the dimensional signature using the following procedure:

```python
# Step 1: Sort dimensions by score, descending
sorted_dims = sorted(dim_scores.items(), key=lambda x: x[1], reverse=True)
top_dim_1 = sorted_dims[0][0]
top_dim_2 = sorted_dims[1][0]
bottom_dim = sorted_dims[-1][0]

# Step 2: Map to driver labels
DIM_HIGH_LABELS = {
    "D1": "Mission-Critical",       "D2": "Sovereignty-Constrained",
    "D3": "Talent-Optimized",       "D4": "Capital-Enabled",
    "D5": "Velocity-Driven",        "D6": "Executive-Anchored",
    "D7": "Process-Disciplined",    "D8": "Engineering-Native",
    "D9": "Adversary-Calibrated"
}

DIM_LOW_LABELS = {
    "D1": "Mission-Agnostic",       "D2": "Regulation-Light",
    "D3": "Capability-Deficient",   "D4": "Capital-Sparse",
    "D5": "Inertia-Bound",          "D6": "Sponsorship-Deficient",
    "D7": "Process-Deficient",      "D8": "Tool-Dependent",
    "D9": "Intelligence-Dark"
}

# Step 3: Compose model name and posture
model_name = f"{DIM_HIGH_LABELS[top_dim_1]} × {DIM_HIGH_LABELS[top_dim_2]} Model"
posture = f"{PILLAR_HIGH[dominant_pillar]}, {PILLAR_LOW[deficient_pillar]} · primary constraint: {DIM_LOW_LABELS[bottom_dim]}"
```

This produces a designation that is simultaneously human-readable, data-derived, and directly traceable to the dimensional evidence — with no subjective labelling or lookup.

### 8.6 Threat-Capability Gap Signal

```
TCG = D9 - ((D7 + D8) / 2)
```

| TCG | Signal | Recommended Action |
|:---|:---|:---|
| `< -0.8` | **Critical** ⚠ | Threat intelligence maturity materially exceeds detection and process capability. D7 and D8 investment is the highest-urgency programme priority. |
| `-0.8 to 0` | **Moderate** | Some misalignment. Monitor and close through targeted D7/D8 investment. |
| `0 to +0.8` | **Aligned** | Technical capability is commensurate with threat awareness. Maintain balance. |
| `> +0.8` | **Surplus** | Technical investment may be ahead of threat intelligence capability. Ensure D9 investment keeps pace with D8 advancement. |

---

## 9. Digital Implementation

### 9.1 Technology Stack

| Layer | Technology | Notes |
|:---|:---|:---|
| Framework | React 18 | Functional components with hooks |
| State | `useState`, `useMemo` | No external state library required |
| Styling | Inline styles | No CSS framework dependency; maximises portability |
| Typography | JetBrains Mono + Syne | Google Fonts CDN |
| Computation | Pure JavaScript | No external math library |
| Deployment | Any React environment | CRA, Vite, Next.js, CodeSandbox, Claude Artifacts |

### 9.2 Phase Architecture

```
"configure" ──(weights valid)──► "assess" ──(all scored)──► "output"
     ▲                               │                          │
     └───────────────────────────────┴──────────────────────────┘
                          (back-navigation permitted)
```

### 9.3 Core State Model

```javascript
// Phase control
const [phase, setPhase]           = useState("configure")

// Nine dimension weights (%, must sum to 100)
const [dimWeights, setDimWeights] = useState({
  D1:12, D2:10, D3:10, D4:12, D5:10, D6:10, D7:12, D8:12, D9:12
})

// 42 sub-factor scores (factorId → 1–5, 0 = unscored)
const [scores, setScores]         = useState({})

// Derived states (via useMemo — recomputed on score/weight change)
const dimScores = useMemo(() => {
  const ds = {}
  DIMS.forEach(d => {
    if (d.factors.every(f => scores[f.id] > 0)) {
      ds[d.id] = d.factors.reduce((s, f) => s + scores[f.id], 0) / d.factors.length
    }
  })
  return ds
}, [scores])

const allScored = DIMS.every(d => d.factors.every(f => scores[f.id] > 0))

const output = useMemo(() =>
  allScored ? buildOutput(dimScores, dimWeights) : null,
  [allScored, dimScores, dimWeights]
)
```

### 9.4 Key Data Structures

```javascript
// Dimension definition
{
  id:       "D1",
  pillar:   "Socio",
  factor:   "Business Mission",
  defaultW: 12,             // default weight %
  factors: [
    {
      id:      "1a",
      label:   "Critical Revenue Dependency",
      anchors: [             // index 0 = score 1, index 4 = score 5
        "Score 1 anchor text...",
        "Score 2 anchor text...",
        "Score 3 anchor text...",
        "Score 4 anchor text...",
        "Score 5 anchor text...",
      ]
    },
    // ... additional sub-factors
  ]
}

// Output object (returned by buildOutput)
{
  composite:  3.24,
  pillar:     { Socio: 3.10, Econo: 2.90, Tech: 3.50 },
  sims:       [ { name, abbr, sim, desc }, ... ],   // sorted by sim desc
  cls: {
    type:       "Novel",           // "Classical" | "Hybrid" | "Novel"
    typeColor:  "#7B9FE0",
    headline:   "Engineering-Native × Mission-Critical Model",
    sub:        "Technically-Mature, Resource-Constrained ...",
    body:       "...",
    closestRef: { name, abbr, sim } | null
  },
  priorities:  [ { id, score, dim }, ... ],   // bottom 3 by score
  threatGap:   -1.25
}
```

### 9.5 Computation Pipeline

```
 scores{} + dimWeights{}
         │
         ▼
 dimScores (useMemo)
   D_n = mean(scores for sub-factors in D_n)
   [only computed when all sub-factors in D_n are scored]
         │
         ▼
 buildOutput() [only runs when all 42 scored]
   │
   ├─ composite = Σ(D_n × w_n / 100)
   ├─ pillar averages = mean(D_n) per pillar
   ├─ sims[] = cosine_sim(dimScores, archetype.sig) for each archetype
   ├─ classification = threshold(sims[0].sim)
   │   ├─ Classical: confirm archetype
   │   ├─ Hybrid: closest archetype + deviation signal
   │   └─ Novel: name from top-2 dim drivers + pillar posture
   ├─ priorities = bottom 3 dimensions by D_n
   └─ threatGap = D9 - mean(D7, D8)
```

---

## 10. Physical On-Site Adaptation

### 10.1 Field Assessment Overview

The SET Framework is designed to operate as both a digital instrument and a **physical field assessment protocol** for in-person organizational engagements. The physical adaptation is essential for assessments where:
- Digital tools are unavailable or inappropriate (classified environments, air-gapped facilities, early-stage organisations without IT infrastructure)
- Multi-assessor team engagements require synchronized paper scoring before digital consolidation
- The assessed organisation requires a paper record as part of the engagement deliverable

A standard on-site engagement using the physical protocol typically requires **2–5 working days** depending on organisational size, complexity, and number of stakeholders.

### 10.2 Pre-Assessment Preparation

**Background intelligence review (complete before site visit):**

| Source | Dimensions Informed | What to Look For |
|:---|:---|:---|
| Annual reports / financial filings | D1, D4, D6 | Revenue dependency on digital, capital allocation patterns, M&A history |
| Regulatory filings and public enforcement actions | D2 | Applicable regulations, recent enforcement, notification history |
| LinkedIn / careers pages | D3, D5, D8 | Career architecture signals, engineering culture indicators, open security roles and seniority levels |
| News archives and press releases | D1, D6, D9 | M&A activity, incident history, geopolitical exposure |
| Sector threat intelligence reports | D9 | Active threat actors, recent sector incidents, vulnerability trends |
| Glassdoor / employer review sites | D3, D5, D6 | Culture signals, change fatigue indicators, leadership credibility |
| GitHub / technical blog / conference presentations | D5, D8 | Engineering culture depth, open-source participation, security engineering maturity |
| CERT / NCSC / sector body advisories | D2, D9 | Specific regulatory guidance, sector threat landscape |

**Preliminary weight hypothesis:**
Draft initial dimension weights based on background intelligence. Treat as a hypothesis to be validated in the on-site weight configuration session. Document the reasoning for each weight assignment.

### 10.3 Weight Configuration Protocol

**Recommended: Facilitated workshop, Day 1, 60–90 minutes**
**Participants:** CISO (or equivalent) + 1–2 senior stakeholders

Facilitator prompt sequence:

1. *"For this organisation specifically, which of these nine dimensions most directly determines whether a security programme will succeed or fail over the next 3 years?"*
2. *"Which dimensions represent conditions that are structurally fixed for this organisation — things you cannot change regardless of investment — versus conditions that are actively malleable?"*
3. *"If your security programme fails in 18 months, which dimension failure would be the most likely cause?"*
4. *"Are there any dimensions that are structurally irrelevant to this organisation's context? What makes them less important here?"*

Distribute the printed Weight Configuration Worksheet. Collect weight assignments. Review that weights sum to 100%. Document rationale. Finalise and lock weights before beginning the questionnaire phase.

### 10.4 Interview & Survey Protocol

**Interview structure (60–90 minutes per session):**

1. **Framing (10 min):** Explain the framework structure, scoring approach, and how results will be used. Establish that scores reflect current practised reality, not policy or aspiration.

2. **Free response questioning (40–60 min):** Use the Interview Question Bank in [Section 11.2](#112-interview-question-bank). For each relevant sub-factor: ask the primary question first without reference to anchors; listen to the free response; only then present the anchor descriptions for score selection.

3. **Document request (10 min):** Identify corroborating documents for each scored sub-factor. Record document reference and availability.

4. **Score read-back (10 min):** Read preliminary scores back to the stakeholder. Note any disagreements. Disagreements are data — record them separately.

**Written survey alternative:**
Present each sub-factor's five anchor descriptions in written form. Ask respondents to select the anchor that most accurately describes current reality. Survey responses should always be validated against documentary evidence before finalisation. Flag self-reported survey scores without corroboration clearly in the assessment report.

### 10.5 Scoring Sheet Templates

#### Weight Configuration Worksheet

```
ORGANISATION:  ______________________________   DATE:  ___________
ASSESSOR(S):   ______________________________   VERSION:  ________

DIMENSION WEIGHT CONFIGURATION
═══════════════════════════════════════════════════════════════════
SOCIO PILLAR
  D1  Business Mission        _____% │ Rationale: _________________
  D2  Gov / Regulatory        _____% │ Rationale: _________________
  D3  People                  _____% │ Rationale: _________________
                              ──────   Socio sub-total: _________ %

ECONO PILLAR
  D4  Capital Flow            _____% │ Rationale: _________________
  D5  Culture                 _____% │ Rationale: _________________
  D6  Constraints             _____% │ Rationale: _________________
                              ──────   Econo sub-total: _________ %

TECH PILLAR
  D7  Process                 _____% │ Rationale: _________________
  D8  Technical               _____% │ Rationale: _________________
  D9  Threat Landscape        _____% │ Rationale: _________________
                              ──────   Tech sub-total:  _________ %

═══════════════════════════════════════════════════════════════════
               TOTAL (MUST EQUAL 100%):  _________ %
═══════════════════════════════════════════════════════════════════
Approved by: ________________________   Signature: _______________
Date approved: ______________________
```

#### Sub-Factor Scoring Sheet (Full 42-Factor)

```
ORGANISATION: ______________________________   DATE: ___________
ASSESSOR:     ______________________________   STAKEHOLDER: _____

SCORING KEY: 1=Nascent  2=Developing  3=Established  4=Advanced  5=Optimized

═══ D1 — BUSINESS MISSION  (weight: ______%) ═══════════════════════
1a  Critical Revenue Dependency               1   2   3   4   5
    Evidence: ___________________________________________________
1b  Structural Org Topology                   1   2   3   4   5
    Evidence: ___________________________________________________
1c  Strategic Competitive Risk Posture        1   2   3   4   5
    Evidence: ___________________________________________________
1d  Digital Transformation Dependency         1   2   3   4   5
    Evidence: ___________________________________________________
1e  Third-Party & Supply Chain Mission Crit.  1   2   3   4   5
    Evidence: ___________________________________________________
D1 Score = (1a+1b+1c+1d+1e) / 5 = ______ / 5 = ________

═══ D2 — GOV / REGULATORY  (weight: ______%) ════════════════════════
2a  Statutory Compliance & Legal Rigidity     1   2   3   4   5
    Evidence: ___________________________________________________
2b  Geopolitical Data & People Sovereignty    1   2   3   4   5
    Evidence: ___________________________________________________
2c  Incident Reporting & Notification Oblig.  1   2   3   4   5
    Evidence: ___________________________________________________
2d  Cross-Sector Regulatory Overlap           1   2   3   4   5
    Evidence: ___________________________________________________
2e  Intl Standards & Framework Alignment      1   2   3   4   5
    Evidence: ___________________________________________________
D2 Score = (2a+2b+2c+2d+2e) / 5 = ______ / 5 = ________

═══ D3 — PEOPLE  (weight: ______%) ══════════════════════════════════
3a  Technical vs. Managerial Career Arch.     1   2   3   4   5
    Evidence: ___________________________________________________
3b  Scarcity-Based Compensation Elasticity    1   2   3   4   5
    Evidence: ___________________________________________________
3c  Security Awareness & Human Risk Culture   1   2   3   4   5
    Evidence: ___________________________________________________
3d  Insider Threat Risk Profile               1   2   3   4   5
    Evidence: ___________________________________________________
3e  Workforce Distribution & Remote Posture   1   2   3   4   5
    Evidence: ___________________________________________________
D3 Score = (3a+3b+3c+3d+3e) / 5 = ______ / 5 = ________

═══ D4 — CAPITAL FLOW  (weight: ______%) ════════════════════════════
4a  Multi-Year Funding Logic                  1   2   3   4   5
    Evidence: ___________________________________________________
4b  Specialized SME Labor Scarcity            1   2   3   4   5
    Evidence: ___________________________________________________
4c  Data Intensity & Telemetry Scale          1   2   3   4   5
    Evidence: ___________________________________________________
4d  Cyber Insurance & Risk Transfer Maturity  1   2   3   4   5
    Evidence: ___________________________________________________
D4 Score = (4a+4b+4c+4d) / 4 = ______ / 4 = ________

═══ D5 — CULTURE  (weight: ______%) ═════════════════════════════════
5a  Product & Innovation Velocity             1   2   3   4   5
    Evidence: ___________________________________________________
5b  Enterprise-wide Cyber-Accountability      1   2   3   4   5
    Evidence: ___________________________________________________
5c  Psychological Safety & Reporting Culture  1   2   3   4   5
    Evidence: ___________________________________________________
5d  Security-as-Enabler vs. Blocker           1   2   3   4   5
    Evidence: ___________________________________________________
D5 Score = (5a+5b+5c+5d) / 4 = ______ / 4 = ________

═══ D6 — CONSTRAINTS  (weight: ______%) ═════════════════════════════
6a  Executive Sponsorship & Influence Depth   1   2   3   4   5
    Evidence: ___________________________________________________
6b  M&A / Divestiture Frequency               1   2   3   4   5
    Evidence: ___________________________________________________
6c  Vendor & Third-Party Dependency Lock-in   1   2   3   4   5
    Evidence: ___________________________________________________
6d  Org Change Fatigue & Reform Tolerance     1   2   3   4   5
    Evidence: ___________________________________________________
D6 Score = (6a+6b+6c+6d) / 4 = ______ / 4 = ________

═══ D7 — PROCESS  (weight: ______%) ═════════════════════════════════
7a  Operational Workflow Maturity             1   2   3   4   5
    Evidence: ___________________________________________________
7b  Critical Asset & Business Service Mapping 1   2   3   4   5
    Evidence: ___________________________________________________
7c  Incident Response Lifecycle Maturity      1   2   3   4   5
    Evidence: ___________________________________________________
7d  Third-Party & Supply Chain Risk Process   1   2   3   4   5
    Evidence: ___________________________________________________
7e  Change Management & Configuration Control 1   2   3   4   5
    Evidence: ___________________________________________________
D7 Score = (7a+7b+7c+7d+7e) / 5 = ______ / 5 = ________

═══ D8 — TECHNICAL  (weight: ______%) ═══════════════════════════════
8a  Telemetry Cohesion & Interoperability     1   2   3   4   5
    Evidence: ___________________________________________________
8b  Org Engineering DNA & Automation          1   2   3   4   5
    Evidence: ___________________________________________________
8c  Identity & Access Management Maturity     1   2   3   4   5
    Evidence: ___________________________________________________
8d  Cloud Security Architecture Maturity      1   2   3   4   5
    Evidence: ___________________________________________________
8e  Vulnerability Management Lifecycle        1   2   3   4   5
    Evidence: ___________________________________________________
D8 Score = (8a+8b+8c+8d+8e) / 5 = ______ / 5 = ________

═══ D9 — THREAT LANDSCAPE  (weight: ______%) ════════════════════════
9a  Adversary Sophistication & Intent         1   2   3   4   5
    Evidence: ___________________________________________________
9b  Attack Surface Structural Complexity      1   2   3   4   5
    Evidence: ___________________________________________________
9c  Supply Chain & Third-Party Compromise     1   2   3   4   5
    Evidence: ___________________________________________________
9d  Geopolitical & Nation-State Exposure      1   2   3   4   5
    Evidence: ___________________________________________________
9e  Insider Threat Probability & Detection    1   2   3   4   5
    Evidence: ___________________________________________________
D9 Score = (9a+9b+9c+9d+9e) / 5 = ______ / 5 = ________

═══════════════════════════════════════════════════════════════════
COMPOSITE COMPUTATION
  D1(____) × ____% = ______
  D2(____) × ____% = ______
  D3(____) × ____% = ______
  D4(____) × ____% = ______
  D5(____) × ____% = ______
  D6(____) × ____% = ______
  D7(____) × ____% = ______
  D8(____) × ____% = ______
  D9(____) × ____% = ______
               TOTAL = ______   LABEL: _________________

PILLAR AVERAGES
  Socio: (D1 + D2 + D3) / 3 = ________
  Econo: (D4 + D5 + D6) / 3 = ________
  Tech:  (D7 + D8 + D9) / 3 = ________

THREAT-CAPABILITY GAP
  TCG = D9 - ((D7 + D8) / 2) = ________

PRIORITY DIMENSIONS (lowest 3 by score)
  P1: _____ (score: ______)
  P2: _____ (score: ______)
  P3: _____ (score: ______)
═══════════════════════════════════════════════════════════════════
```

### 10.6 Evidence Standards by Dimension

Each sub-factor score should be corroborated by at least one form of documentary or observational evidence. The following table specifies recommended evidence types by dimension:

| Dim | Sub-Factor | Primary Evidence Sources |
|:---|:---|:---|
| D1 | Revenue dependency | Business continuity plans; revenue model documentation; disaster recovery RTO/RPO |
| D1 | Org topology | Org chart; RACI matrix; governance frameworks |
| D1 | Competitive risk | Competitive landscape analysis; sector research; customer retention data |
| D1 | Digital transformation | Programme governance documents; cloud migration roadmap; digital strategy |
| D1 | Supply chain criticality | Vendor dependency register; business impact analysis; TPRM documentation |
| D2 | Statutory compliance | Compliance register; regulatory correspondence; audit reports |
| D2 | Data sovereignty | Data flow maps; data residency policy; DPIA documentation |
| D2 | Incident reporting | Incident notification procedure; past notification records; regulatory guidance |
| D2 | Regulatory overlap | Legal entity structure; sector licence documentation |
| D2 | Standards alignment | Certification certificates; audit scope documentation; customer contract requirements |
| D3 | Career architecture | Job architecture documentation; HR career framework; job descriptions |
| D3 | Compensation elasticity | Compensation policy; recent exception approvals; salary benchmarking reports |
| D3 | Security awareness | Training completion reports; phishing simulation results; awareness programme documentation |
| D3 | Insider threat | Insider threat policy; PAM configuration; user activity monitoring scope |
| D3 | Workforce distribution | Workforce demographics; remote work policy; endpoint management scope |
| D4 | Funding logic | Board-approved security budget; multi-year programme financial plan |
| D4 | Labor scarcity | Open role listings; time-to-fill data; compensation bands for security roles |
| D4 | Data intensity | SIEM/SIEM data volume metrics; telemetry architecture diagram; licensing costs |
| D4 | Cyber insurance | Insurance policy document; coverage review records; broker assessment reports |
| D5 | Innovation velocity | Deployment frequency metrics; sprint cadence data; CI/CD pipeline documentation |
| D5 | Cyber accountability | RACI for security; risk ownership documentation; business unit security KPIs |
| D5 | Psychological safety | Near-miss reporting statistics; incident communication records; post-incident review culture |
| D5 | Security perception | Business leader interviews; CISO engagement records; security council attendance |
| D6 | Executive sponsorship | CISO reporting line documentation; board minutes; security governance charter |
| D6 | M&A frequency | M&A transaction history; integration backlog register |
| D6 | Vendor lock-in | Strategic vendor contracts; technology roadmap; architectural dependency analysis |
| D6 | Change fatigue | Recent transformation programme inventory; staff survey results; adoption metrics |
| D7 | Workflow maturity | Process documentation library; audit findings; process compliance metrics |
| D7 | Asset mapping | Asset inventory exports; CMDB records; crown jewel classification register |
| D7 | Incident response | IR plan documentation; exercise records; post-incident reviews |
| D7 | TPRM process | TPRM programme documentation; vendor assessment records; supplier security requirements |
| D7 | Change management | Change management policy; CAB records; configuration baseline documentation |
| D8 | Telemetry cohesion | SIEM/XDR architecture diagram; log source inventory; detection coverage map |
| D8 | Engineering DNA | Detection-as-code repository; automation runbook library; security tooling inventory |
| D8 | IAM maturity | IAM architecture documentation; PAM tool configuration; access review records |
| D8 | Cloud security | Cloud security architecture diagram; CSPM tool configuration; cloud security policy |
| D8 | Vulnerability management | Vulnerability management policy; SLA performance data; scanner scope documentation |
| D9 | Adversary profile | CTI reports; threat model documentation; sector ISAC intelligence |
| D9 | Attack surface | Attack surface management tool output; external asset scan; shadow IT discovery results |
| D9 | Supply chain risk | Software bill of materials; third-party compromise scenarios; supply chain assessment reports |
| D9 | Geopolitical exposure | Government threat advisories; sector CERT guidance; geopolitical risk analysis |
| D9 | Insider threat | Insider event history; behavioural analytics tool coverage; insider programme documentation |

---

## 11. Assessor Guidance

### 11.1 Stakeholder Mapping

| Dimension | Primary Stakeholder | Secondary Stakeholder |
|:---|:---|:---|
| D1 Business Mission | CEO / COO | CISO / CRO / Head of Strategy |
| D2 Gov / Regulatory | General Counsel / DPO | CCO / CISO / Regional Legal Counsel |
| D3 People | CHRO / CPO | Head of Engineering / Compensation Lead / Head of Talent Acquisition |
| D4 Capital Flow | CFO / Head of FP&A | CISO / CIO / Budget Controller |
| D5 Culture | CTO / VP Engineering | Head of Product / CISO / COO |
| D6 Constraints | CEO / Board Member | CFO / CISO / Head of Corporate Development |
| D7 Process | CIO / Head of IT Operations | ITIL Process Owner / Change Manager / CISO |
| D8 Technical | CISO / Head of Security Engineering | SOC Director / CTO / Head of Infrastructure |
| D9 Threat Landscape | Head of Threat Intelligence | SOC Director / CISO / Head of Security Operations |

### 11.2 Interview Question Bank

#### D1 — Business Mission

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 1a | Revenue Dependency | *"If your primary customer-facing digital systems went offline for 24 hours — no manual workaround — what would be the direct financial and operational impact?"* |
| 1b | Org Topology | *"If a major security decision needed to be made urgently that would affect three different business units, how would that decision get made? Who has the final authority and how long would it take?"* |
| 1c | Competitive Risk | *"If a material security incident became public tomorrow, what would your competitors do within the next 48 hours? Have you seen this happen to a direct peer?"* |
| 1d | Digital Transformation | *"What major technology transformation programmes are currently active? How many months until the next major migration or platform change? How mature is security involvement in those programmes?"* |
| 1e | Supply Chain Criticality | *"If your three most critical third-party technology providers simultaneously became unavailable, what would happen to your core operations? When did you last assess that scenario?"* |

#### D2 — Gov / Regulatory

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 2a | Statutory Compliance | *"List the cybersecurity regulations you are currently subject to. Which of those carry direct financial or criminal penalty for non-compliance? What is the largest fine you could face?"* |
| 2b | Data Sovereignty | *"Do you have data that must stay within specific national boundaries? Do you have staff or contractors in jurisdictions where government authorities could legally compel access to your data?"* |
| 2c | Incident Reporting | *"If you discovered a material breach today, what notification obligations would be triggered, to which authorities, and within what timelines? When was this procedure last rehearsed?"* |
| 2d | Regulatory Overlap | *"How many distinct regulatory frameworks apply to your security programme? Are any of them in direct conflict with each other?"* |
| 2e | Standards Alignment | *"Which internationally recognised security certifications do you hold? Which are contractually required by customers or regulators? Which are you working toward?"* |

#### D3 — People

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 3a | Career Architecture | *"Can a highly skilled security engineer in this organisation grow to a VP-equivalent role without ever managing a team? What does that path look like, and does it pay the same?"* |
| 3b | Compensation Elasticity | *"If you identified a candidate for your most critical open security role who needed 40% above your standard pay band, what would happen? Walk me through the process from decision to offer letter."* |
| 3c | Security Awareness | *"What evidence do you have that your security awareness programme changes actual employee behaviour? What metrics do you track, and what have they shown over the last 12 months?"* |
| 3d | Insider Threat | *"If a trusted employee with broad access decided to exfiltrate your most sensitive data, how long would it take you to detect it? What would trigger the detection?"* |
| 3e | Workforce Distribution | *"What percentage of your workforce works remotely or in hybrid arrangements? How are contractor and third-party staff integrated into your security controls? What's the single weakest point in your distributed work security model?"* |

#### D4 — Capital Flow

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 4a | Funding Logic | *"Is your security programme funded on an annual budget cycle or a multi-year commitment? What happens to your programme if the CFO changes or you have a poor financial quarter?"* |
| 4b | Labor Scarcity | *"What are the hardest security roles to fill right now? How long has your most critical unfilled security position been open? What have you paid in contracting or consulting to cover gaps?"* |
| 4c | Data Intensity | *"How much data are you currently ingesting for security monitoring? Is that volume growing? What does that cost, and how does cost scale as your environment grows?"* |
| 4d | Cyber Insurance | *"Do you have cyber insurance? Do you understand your policy's sub-limits, exclusions, and notification conditions? Has your broker ever challenged a claim based on your security controls?"* |

#### D5 — Culture

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 5a | Innovation Velocity | *"How often does your engineering team deploy to production? How much advance notice does the security team typically receive before a major new capability or platform is deployed?"* |
| 5b | Cyber Accountability | *"When a business unit makes a decision that introduces security risk without security review — what actually happens? Can you give me a recent example?"* |
| 5c | Psychological Safety | *"In the last year, how many near-miss security events were reported to the security team that did not become full incidents? What happened to the people who reported them?"* |
| 5d | Security Perception | *"When business leaders think about the security team, do they call them first or last? Can you give me an example of a business initiative where security was involved at the strategy stage, not just the approval gate?"* |

#### D6 — Constraints

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 6a | Executive Sponsorship | *"When you need a decision that requires cross-organisational behaviour change or significant new budget — how high do you need to go, and does it actually happen? Has the Board ever personally debated a security architecture decision?"* |
| 6b | M&A Frequency | *"How many acquisitions or divestitures has this organisation completed in the last three years? How many of those are still in active security integration? What's in the backlog?"* |
| 6c | Vendor Lock-in | *"Which of your current strategic technology vendors would it be most costly to replace? How much of your security architecture is constrained by that relationship?"* |
| 6d | Change Fatigue | *"How many major organisational transformation programmes have staff experienced in the last 24 months? If you asked them tomorrow to adopt a significant new security behaviour, what would the resistance level look like?"* |

#### D7 — Process

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 7a | Workflow Maturity | *"Walk me through your security operations process on a typical day. Is it the same regardless of who is working? Can you show me where it is documented?"* |
| 7b | Asset Mapping | *"If I asked you right now to produce a complete list of every system that processes personally identifiable data, how long would that take and how confident would you be in its completeness?"* |
| 7c | Incident Response | *"Walk me through the last significant security incident you experienced. What triggered detection? How were decisions made? What changed after the incident?"* |
| 7d | Third-Party Risk | *"How do you assess the security posture of a critical new technology supplier before they are onboarded? How frequently do you reassess existing critical suppliers?"* |
| 7e | Change Management | *"In the last 12 months, how many security misconfigurations were introduced through the change management process? How did you detect them?"* |

#### D8 — Technical

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 8a | Telemetry Cohesion | *"If a threat actor compromised a contractor's device and used it to access your cloud environment, how quickly would you detect it and through what signal?"* |
| 8b | Engineering DNA | *"Does your security team write and maintain code? Show me an example of a detection rule or automation script your team built internally. How is it tested and deployed?"* |
| 8c | IAM Maturity | *"How is privileged access managed for your most sensitive systems? Can any administrator access your most critical systems without a time-limited approval? When was access last comprehensively reviewed?"* |
| 8d | Cloud Security | *"How do you prevent a developer from deploying a misconfigured cloud resource that creates a public-facing security exposure? Can you demonstrate it in your environment?"* |
| 8e | Vulnerability Management | *"What is your SLA for patching a critical vulnerability in an internet-facing system? What percentage of critical vulnerabilities are patched within that SLA? What is your current count of critical unpatched vulnerabilities?"* |

#### D9 — Threat Landscape

| ID | Sub-Factor | Primary Interview Question |
|:---|:---|:---|
| 9a | Adversary Profile | *"Name the three threat actors most likely targeting your organisation right now. How do you know? What are their primary techniques and what have you done specifically to counter them?"* |
| 9b | Attack Surface | *"How many externally facing assets does this organisation have? How many third parties have access to your internal systems or data? When was the last external attack surface review conducted?"* |
| 9c | Supply Chain Risk | *"Which of your technology suppliers, if compromised, could be used as a vector to attack your organisation? Has a supplier's compromise ever resulted in a security event for your organisation?"* |
| 9d | Geopolitical Exposure | *"Has your organisation been the subject of a government-issued threat advisory or warning? What state-sponsored threat groups are known to target your sector or country of operation?"* |
| 9e | Insider Probability | *"Who in your organisation could cause the most damage with the access they currently hold? Could you detect and stop them within 24 hours if they decided to act maliciously today?"* |

### 11.3 Common Scoring Errors

| Error | Description | Detection & Mitigation |
|:---|:---|:---|
| **Optimism bias** | Stakeholders describe aspirational or policy state rather than operational reality. | Probe with *"when did this last happen in practice?"* — request operational examples, not documentation. |
| **Policy/practice gap** | Documented policies score high; actual daily operational practice scores much lower. | Ask for recent operational examples; schedule process observation where possible. |
| **Halo effect** | High visibility in one sub-factor inflates adjacent scores within the same dimension. | Score each sub-factor independently; reconcile all scores at the end of the session. |
| **Recency bias** | A recent positive event (new tool deployed, recent audit pass) inflates scores beyond sustained reality. | Assess against a 12-month operational pattern, not the last quarter. |
| **Anchor contamination** | Assessor reads anchor descriptions before the stakeholder answers, anchoring the response. | Always ask the free-response question first; present anchors only for final score confirmation. |
| **Single-source dependency** | All scores derived from a single stakeholder without corroboration. | Triangulate across at least two stakeholders per dimension and one documentary source. |
| **Seniority inflation** | Senior executives consistently over-score operational realities they are not close to. | Balance executive interview data with operational-level stakeholder interviews and documentary evidence. |
| **Conservative deflation** | Assessors default to lower scores when uncertain, producing systematic underscoring. | When genuinely uncertain between two adjacent scores, use the lower — but resolve uncertainty through additional evidence gathering rather than defaulting. |

### 11.4 Inter-Rater Reliability Protocol

When two or more assessors score the same organisation independently:

1. Each assessor completes scoring independently after their respective stakeholder sessions.
2. Assessors compare all 42 sub-factor scores without discussion first — record all variances.
3. For sub-factors where scores differ by **1 point**: review evidence together; the assessor with stronger corroborating documentation sets the score.
4. For sub-factors where scores differ by **2+ points**: this indicates a substantive evidence gap or anchor interpretation disagreement — additional evidence gathering is required before finalisation.
5. Document all reconciliations in the assessment record, including the evidence that resolved the variance.
6. Where consensus genuinely cannot be reached after additional evidence gathering, take the mean of the two scores and document the disagreement.

---

## 12. Global Context & Regional Applicability

### 12.1 Framework Use Across Geographies

The SET Framework is designed for global application. The following guidance helps assessors calibrate dimension weights and anchor interpretation across different regional operating environments.

**Regulatory density by region (D2 calibration reference):**

| Region | High-Impact Regulatory Frameworks | D2 Weight Implication |
|:---|:---|:---|
| European Union | GDPR, NIS2, DORA, eIDAS, sector-specific financial/health regs | High D2 weight appropriate (12–20%) |
| United States | HIPAA, GLBA, CCPA/CPRA, SEC cybersecurity disclosure, NERC CIP, CMMC, FedRAMP | High D2 weight; multi-framework complexity |
| United Kingdom | UK GDPR, NIS Regulations, FCA/PRA cybersecurity requirements, CNI sector regs | High D2 weight post-Brexit divergence |
| China | Cybersecurity Law (CSL), Data Security Law (DSL), PIPL, MLPS 2.0, Critical Information Infrastructure regulations | Extremely high D2 weight; geopolitical sub-factor (2b) critical |
| India | DPDP Act 2023, RBI/SEBI cybersecurity circulars, CERT-In reporting obligations | Increasing D2 weight; reporting obligations (2c) elevated |
| Singapore | PDPA, MAS Technology Risk Management Guidelines, CSA cybersecurity framework | Moderate-high D2 weight; standards alignment (2e) elevated |
| Australia | Privacy Act, ASD Essential Eight, APRA CPS 234, Critical Infrastructure Act | Moderate-high D2 weight; standards alignment (2e) high |
| Middle East (UAE/Saudi) | UAE Data Protection Law, SAMA Cybersecurity Framework, NCA ECC, ADHICS | Moderate-high; rapid regulatory development trajectory |
| Africa | Variable; South Africa POPIA most mature. Many jurisdictions: voluntary standards only | Low-moderate D2 weight in most sub-Saharan contexts |
| Latin America | Brazil LGPD, Mexico LFPDPPP, Chile Cybersecurity Bill, sectoral banking regs | Moderate and growing; LGPD elevates Brazil significantly |
| ASEAN (ex-Singapore) | Variable national frameworks; Thailand PDPA, Philippines DPA, Malaysia PDPA | Low-moderate and developing |

**Threat landscape calibration by sector (D9 reference):**

| Sector | Primary Adversary Types | Key D9 Sub-Factors |
|:---|:---|:---|
| Financial Services | eCrime (Lazarus, FIN groups), nation-state (financial theft, sanctions evasion), insider fraud | 9a, 9b, 9e |
| Critical Infrastructure (Energy/Water/Transport) | Nation-state pre-positioning (APT40, Sandworm, Volt Typhoon), ransomware | 9a, 9d |
| Healthcare | Ransomware (high disruption value), data theft, nation-state (research theft) | 9a, 9b, 9c |
| Technology / Software | Supply chain attackers (SolarWinds-type), IP theft, nation-state | 9a, 9c, 9d |
| Defence / Government | Nation-state espionage (APT28, APT41), insider threat | 9a, 9d, 9e |
| Retail / Consumer | eCrime (PCI data theft), ransomware, phishing at scale | 9a, 9b |
| Manufacturing / OT | Ransomware (operational disruption), nation-state (critical infrastructure) | 9a, 9b, 9d |
| Education / Research | Nation-state (IP theft, research data), ransomware | 9a, 9d |
| Non-Profit / NGO | Nation-state (activist targeting), reputational attacks, limited resources | 9a, 9d |

### 12.2 Organisation Size Calibration

The framework applies to organisations of all sizes. The following guidance helps calibrate anchor interpretation and weight configuration for different organisational scales:

**Large Enterprise (5,000+ employees, multi-national):**
- D1e (Supply Chain), D2a/D2b (Regulatory), D6b (M&A), D9b (Attack Surface) tend to score higher due to structural complexity.
- D5c (Psychological Safety) and D5d (Security Perception) are harder to achieve at scale and often score lower than expected.
- Default weights are broadly applicable; adjust based on sector.

**Mid-Market (500–5,000 employees):**
- Greatest diversity of profiles — cannot generalise. Weight configuration is most important for mid-market organisations.
- D4a (Funding Logic) and D6a (Executive Sponsorship) are high-variance dimensions at this scale.
- D3b (Compensation Elasticity) is often a significant constraint.

**Small Organisation (<500 employees):**
- D8 (Technical) sub-factors may be scored lower by structural necessity rather than poor capability — a 50-person organisation operating a simple environment may score low on 8a not from negligence but from genuine simplicity.
- D2 (Regulatory) may be disproportionately high if the organisation operates in a regulated sector regardless of size.
- D4b (Labor Scarcity) is structurally acute: a small organisation competing for scarce talent has no economies of scale.
- Consider increasing D3 weight to reflect that people are the primary security capability at small scale.

**Government / Public Sector:**
- D4a (Funding Logic) may score higher (long budget cycles are common) or lower (annual appropriations are uncertain) depending on jurisdiction.
- D6a (Executive Sponsorship) is often structurally complex — political authority vs. operational authority distinction requires careful anchor interpretation.
- D3b (Compensation Elasticity) typically scores 1–2 due to civil service pay constraints. Weight D3 accordingly.
- D2 (Regulatory) may be extremely high for defence or intelligence-adjacent agencies, or lower for non-regulated public services.

---

## 13. Validation & Calibration

### 13.1 Baseline Calibration Exercise

Before conducting a live engagement, assessors should complete a calibration exercise:

1. Score a reference organisation (synthetic or published case study) using only the anchor descriptions and the interview question bank.
2. Compare results against the assessor cohort's consensus score (to be developed as engagement data accumulates).
3. For any sub-factor where the individual assessor's score deviates by more than 1 point from consensus, review the anchor and evidence standard.
4. Re-score until deviations on all sub-factors are within ±1 of consensus.

### 13.2 Sensitivity Analysis

For each sub-factor, the sensitivity of the composite score to a ±1 score change is:

```
Δ_composite = ±(1 / k_n) × (w_n / 100)
```

Where `k_n` is the number of sub-factors in dimension n and `w_n` is that dimension's weight.

Any sub-factor where `Δ_composite > 0.05` should be flagged for additional evidence gathering before finalisation. The highest-sensitivity sub-factor in any engagement is the one where the risk of scoring error most directly impacts the output.

### 13.3 Suggested Validation Studies

| Study | Purpose | Method |
|:---|:---|:---|
| **Archetype vector validation** | Test whether the cosine similarity algorithm correctly classifies organisations with documented, well-known programme architectures | Apply to public CISO case studies; compare output classification to known archetype |
| **Threshold calibration** | Replace working thresholds (97.5%, 92%) with empirically derived boundaries | Accumulate similarity score distributions across 100+ organisations; derive empirical cut-points |
| **Predictive validity** | Test whether SET scores predict real security outcomes | Longitudinal correlation of SET composite scores with breach incidence, regulatory penalty, and programme cost efficiency |
| **Inter-rater reliability** | Quantify assessor agreement | Compute Intraclass Correlation Coefficients (ICC) for all sub-factors across paired assessments of the same organisation |
| **Longitudinal stability** | Validate that framework scores track organisational change | Re-assess same organisations at 12-month intervals; correlate score changes with documented programme investments |
| **Anchor reliability** | Test that anchor language produces consistent scores across cultures and languages | Multi-national parallel assessments; score variance analysis by assessor geography |
| **Industry-specific validation** | Test anchor calibration in specific sectors | Sector-cohort assessments with sector expert review panels |

---

## 14. Extending the Framework

### 14.1 Adding Sub-Factors to Existing Dimensions

To add a sub-factor to an existing dimension:

1. Define the sub-factor ID (e.g. `1f` for a sixth sub-factor in D1)
2. Write the label, selection logic, and five behavioural anchors following the anchor writing guidelines below
3. Add to the relevant dimension object in the `DIMS` array
4. The dimension score formula automatically adjusts: `D_n = mean(all sub-factors in D_n)`
5. Add an interview question to the question bank
6. Add an evidence standard to the evidence table
7. Update the full expanded formula in this documentation

**Anchor writing guidelines:**
- Anchors must describe **observable, verifiable organisational behaviours** — not abstract qualities
- Each anchor should be **self-contained** and independently interpretable — an assessor should not need to have read the other four anchors to understand what score 3 means
- Anchors should progress monotonically from weakest (1) to strongest (5) without ambiguity at adjacent levels
- Avoid regulatory or technology-specific references that may not translate across geographies — use functional descriptions instead

### 14.2 Adding New Dimensions

To add a new dimension to the framework:

1. Assign to an existing pillar or define a new pillar
2. Define the dimension ID, factor name, and pillar assignment
3. Define 2–5 sub-factors with anchors, following the guidelines above
4. Set a default weight
5. Update all nine archetype reference vectors to include the new dimension (vectors must remain the same length as the dimension score vector for cosine similarity to function)
6. Add dimension to `DIM_DRIVER` map for novel model naming
7. Revise the total weight constraint: if adding a 10th dimension, weights must still sum to 100%

### 14.3 Industry-Specific Presets

Weight presets for common industry contexts:

```javascript
const INDUSTRY_PRESETS = {
  "Financial Services":         {D1:14,D2:18,D3:8, D4:14,D5:7, D6:12,D7:10,D8:9, D9:8},
  "Healthcare":                 {D1:12,D2:20,D3:10,D4:10,D5:6, D6:10,D7:12,D8:10,D9:10},
  "Critical Infrastructure":    {D1:18,D2:12,D3:8, D4:14,D5:5, D6:14,D7:12,D8:10,D9:7},
  "Technology / SaaS":          {D1:10,D2:8, D3:14,D4:10,D5:14,D6:10,D7:8, D8:16,D9:10},
  "Government / Public Sector": {D1:12,D2:18,D3:10,D4:12,D5:8, D6:14,D7:12,D8:8, D9:6},
  "Manufacturing / OT":         {D1:16,D2:10,D3:8, D4:14,D5:6, D6:12,D7:14,D8:10,D9:10},
  "Retail / Consumer":          {D1:12,D2:12,D3:10,D4:12,D5:10,D6:10,D7:12,D8:10,D9:12},
  "Education / Research":       {D1:10,D2:10,D3:14,D4:10,D5:10,D6:10,D7:12,D8:12,D9:12},
  "SME (<500 employees)":       {D1:12,D2:14,D3:16,D4:14,D5:8, D6:12,D7:10,D8:8, D9:6},
};
```

> **Critical instruction:** All presets are starting hypotheses, not fixed configurations. Every engagement requires the assessor to review and adjust preset weights based on the specific organisation's context.

### 14.4 Longitudinal Tracking

For organisations assessed across multiple time periods:

```javascript
const assessmentRecord = {
  org_id:   "ORG_001",
  org_name: "Example Organisation",
  sector:   "Financial Services",
  region:   "EMEA",
  assessments: [
    {
      date:           "2025-Q1",
      assessor:       "Assessor A",
      weights:        { D1:14, D2:18, ... },
      scores:         { "1a":3, "1b":3, ... },
      dim_scores:     { D1:3.40, D2:4.20, ... },
      composite:      3.17,
      classification: "Hybrid",
      closest_arch:   "CCP",
      closest_sim:    0.934,
      threat_gap:     -0.25,
      priorities:     ["D5", "D3", "D6"]
    },
    {
      date:           "2026-Q1",
      // ... updated scores
      composite:      3.54,
      classification: "Hybrid",
      // delta analysis: +0.37 composite improvement
    }
  ]
}
```

Delta analysis — computing score movement (Δ) between periods — is the primary value of longitudinal tracking and the mechanism through which programme effectiveness is demonstrated.

---

## 15. Worked Example

**Organisation:** A mid-size regional telecommunications operator. 8,000 employees. Listed on a national stock exchange. Operations spanning 4 countries. Subject to national telecommunications regulations, data protection law, and sector-specific security obligations. Recent acquisition of a smaller provider 14 months ago. Engineering team of ~400 developers. Dedicated security team of 18.

### Step 1 — Weight Configuration

| Dim | Factor | Weight | Rationale |
|:---|:---|:---:|:---|
| D1 | Business Mission | 15% | Telecom uptime is foundational to customer and regulatory trust; digital service criticality is extreme |
| D2 | Gov / Regulatory | 14% | Telecom sector is heavily regulated with multi-jurisdiction obligations and incident reporting |
| D3 | People | 9% | Talent market is constrained; remote workforce adds complexity |
| D4 | Capital Flow | 12% | Infrastructure-heavy CapEx model; labour scarcity for niche roles is significant |
| D5 | Culture | 8% | Culture change is in progress; accountability model is maturing |
| D6 | Constraints | 10% | Recent M&A integration is active; executive sponsorship is strong |
| D7 | Process | 12% | Operational maturity is central to service quality; asset mapping is strategically critical |
| D8 | Technical | 11% | Strong technical investment but engineering culture gap |
| D9 | Threat Landscape | 9% | Sector is targeted by nation-state (infrastructure pre-positioning) and eCrime |
| | **Total** | **100%** | |

### Step 2 — Sub-Factor Scores

| ID | Sub-Factor | Score | Notes |
|:---|:---|:---:|:---|
| 1a | Revenue Dependency | 5 | Any outage triggers immediate customer churn and regulatory response |
| 1b | Org Topology | 3 | Regional matrix structure; moderate decision velocity |
| 1c | Competitive Risk | 4 | Competitive market; incident = material customer attrition |
| 1d | Digital Transformation | 4 | Active network modernisation, cloud migration, and 5G rollout simultaneously |
| 1e | Supply Chain Criticality | 4 | Critical dependencies on network equipment vendors and NOC providers |
| 2a | Statutory Compliance | 4 | National telecom regulations, data protection law, sector security obligations |
| 2b | Data Sovereignty | 3 | 4-country operations with manageable sovereignty requirements |
| 2c | Incident Reporting | 4 | 24-hour regulatory notification obligation; stock exchange disclosure obligations |
| 2d | Regulatory Overlap | 3 | Telecom + data protection + financial services (payments subsidiary) |
| 2e | Standards Alignment | 3 | ISO 27001 certified for core scope; customer security questionnaire pressure |
| 3a | Career Architecture | 2 | No formal technical track; management-only advancement |
| 3b | Compensation Elasticity | 2 | Rigid band structure; long approval cycle for exceptions |
| 3c | Security Awareness | 3 | Annual programme with phishing simulation; some metrics; moderate effectiveness |
| 3d | Insider Threat | 3 | Access governance in place; basic monitoring; no formal insider threat programme |
| 3e | Workforce Distribution | 3 | Hybrid workforce policy in place; some endpoint management gaps for field technicians |
| 4a | Funding Logic | 3 | Annual budget with multi-year programme envelope; some year-end uncertainty |
| 4b | Labor Scarcity | 3 | Open cloud security architect and OT/network security specialist roles |
| 4c | Data Intensity | 4 | High telemetry volume from network infrastructure; significant SIEM cost |
| 4d | Cyber Insurance | 3 | Policy exists; terms understood; sub-limits not fully optimised |
| 5a | Innovation Velocity | 3 | Monthly release cadence; agile adopted in product teams; security integration incomplete |
| 5b | Cyber Accountability | 2 | Security team owns risk; business units are not formally accountable |
| 5c | Psychological Safety | 3 | Reporting policy exists; near-miss culture developing but not yet embedded |
| 5d | Security Perception | 3 | Mixed; some business leaders are engaged; others view security as overhead |
| 6a | Executive Sponsorship | 4 | CISO reports to CEO; board risk committee quarterly engagement |
| 6b | M&A Frequency | 3 | One acquisition 14 months ago; active integration backlog |
| 6c | Vendor Lock-in | 3 | Significant telecom equipment vendor dependency; partial security constraint |
| 6d | Change Fatigue | 2 | Staff are fatigued from merger integration; low discretionary reform tolerance |
| 7a | Workflow Maturity | 3 | Core processes documented; inconsistent enforcement across regions |
| 7b | Asset Mapping | 2 | Partial inventory; acquired network assets not fully integrated |
| 7c | Incident Response | 3 | IR plan documented and tested annually; post-incident reviews occur |
| 7d | TPRM Process | 2 | Basic supplier questionnaire; no ongoing monitoring; critical vendor gaps |
| 7e | Change Management | 3 | CAB process exists; security review is a gate for major changes; emergency change gaps |
| 8a | Telemetry Cohesion | 3 | Centralised SIEM; partial correlation; OT/network telemetry integration incomplete |
| 8b | Engineering DNA | 2 | Vendor-managed tooling; limited internal detection engineering capability |
| 8c | IAM Maturity | 3 | PAM deployed for critical systems; access reviews annual; some privileged access gaps |
| 8d | Cloud Security | 3 | CSPM deployed; cloud security architecture defined; enforcement gaps in dev environments |
| 8e | Vulnerability Management | 3 | Formal VM programme; SLAs defined; compliance ~75% for critical vulnerabilities |
| 9a | Adversary Profile | 3 | Sector CTI subscription; general telecom threat profile understood; limited operationalisation |
| 9b | Attack Surface | 4 | Large, complex estate: network infrastructure, cloud, OT, acquired assets, field devices |
| 9c | Supply Chain Risk | 3 | Equipment vendor risk understood; software supply chain risk partially assessed |
| 9d | Geopolitical Exposure | 3 | Telecom infrastructure is a known nation-state target; government advisories received |
| 9e | Insider Threat | 2 | High access concentration in NOC/field; limited monitoring; no formal programme |

### Step 3 — Dimension Score Computation

```
D1 = (5+3+4+4+4) / 5 = 20/5 = 4.00
D2 = (4+3+4+3+3) / 5 = 17/5 = 3.40
D3 = (2+2+3+3+3) / 5 = 13/5 = 2.60
D4 = (3+3+4+3)   / 4 = 13/4 = 3.25
D5 = (3+2+3+3)   / 4 = 11/4 = 2.75
D6 = (4+3+3+2)   / 4 = 12/4 = 3.00
D7 = (3+2+3+2+3) / 5 = 13/5 = 2.60
D8 = (3+2+3+3+3) / 5 = 14/5 = 2.80
D9 = (3+4+3+3+2) / 5 = 15/5 = 3.00
```

### Step 4 — Composite Score

```
C = (4.00×0.15) + (3.40×0.14) + (2.60×0.09) +
    (3.25×0.12) + (2.75×0.08) + (3.00×0.10) +
    (2.60×0.12) + (2.80×0.11) + (3.00×0.09)

  = 0.600 + 0.476 + 0.234 +
    0.390 + 0.220 + 0.300 +
    0.312 + 0.308 + 0.270

  = 3.110  →  Established
```

### Step 5 — Pillar Averages

```
Socio = (4.00 + 3.40 + 2.60) / 3 = 3.33
Econo = (3.25 + 2.75 + 3.00) / 3 = 3.00
Tech  = (2.60 + 2.80 + 3.00) / 3 = 2.80
```

### Step 6 — Threat-Capability Gap

```
TCG = D9 - ((D7 + D8) / 2) = 3.00 - ((2.60 + 2.80) / 2) = 3.00 - 2.70 = +0.30
```
*Aligned — slight technical surplus.*

### Step 7 — Priority Dimensions (lowest 3)

```
P1: D7 Process    — 2.60  (12% weight — high impact on composite)
P2: D3 People     — 2.60  (9% weight)
P3: D5 Culture    — 2.75  (8% weight)
```

### Step 8 — Classification

Closest classical archetype: **RBM (Risk-Based Management Model)** — approximate cosine similarity ~88%.

Result: **Novel** (below 92% threshold)

```
Top 2 dimensions by score: D1 (4.00), D2 (3.40)
Model name: Mission-Critical × Sovereignty-Constrained Model
Posture:    Governance-Led, Technically-Nascent · primary constraint: Process-Deficient
```

**Interpretation:** This organisation has built a strong mission and regulatory foundation (D1 and D2 both above 3.0) but is materially constrained by process immaturity, particularly following the acquisition (D7 at 2.60 with critical asset mapping gaps). The Tech pillar average of 2.80 lags behind Socio at 3.33, indicating an organisation that understands its risk environment and regulatory obligations but has not yet built the operational and technical capability to fully respond to them. The immediate programme priority is closing the D7/D3 gap before advancing D8 further — technical investment without process foundations and talent infrastructure produces diminishing returns. This is not a classical archetype because no established model accounts for the combination of high mission criticality, strong regulatory awareness, and simultaneously constrained process, people, and technical capability. An original programme architecture is required.

---

## 16. Limitations & Research Gaps

| # | Limitation | Impact | Mitigation |
|:---|:---|:---|:---|
| 1 | **Ordinal-to-cardinal conversion** | 1–5 ordinal scores treated as interval arithmetic in aggregation. Scores do not have ratio properties. | Document clearly; interpret composite scores as directional indicators, not precise measurements. |
| 2 | **Cosine similarity is magnitude-insensitive** | Two organisations with identical score patterns but different absolute levels appear equally similar to archetypes. | Present composite score alongside similarity table; never present similarity in isolation. |
| 3 | **Archetype vectors are theoretical** | Reference vectors were constructed through expert judgment, not empirical derivation. | Treat as working hypotheses. Empirical validation is a required future study. |
| 4 | **Classification thresholds are uncalibrated** | 97.5% and 92% thresholds are working values with no empirical basis. | Replace with data-derived thresholds once 100+ engagement similarity distributions are available. |
| 5 | **Weight subjectivity** | Two assessors may configure different weights for the same organisation, producing different composite scores. | Require documented weight rationale; multi-assessor weight consensus protocol for high-stakes engagements. |
| 6 | **Single-assessor reliability** | Solo assessors introduce systemic bias risk. | Multi-assessor protocol with reconciliation required for consequential assessments. |
| 7 | **Self-reported data risk** | Stakeholder interviews are subject to social desirability bias, particularly from senior leaders. | Mandatory documentary corroboration for all sub-factor scores. |
| 8 | **Static snapshot** | Framework produces a point-in-time assessment. Organisational maturity is dynamic. | Reassess at defined intervals (annually recommended); use delta analysis for longitudinal insight. |
| 9 | **Cultural translation** | Anchor language was developed in an English-language context; translation may alter nuance. | Field-test translated anchor language with native speakers; adapt culturally specific phrasing. |
| 10 | **Small organisation calibration** | Some sub-factors may produce artificially low scores for small organisations due to structural simplicity rather than poor capability. | Assessors should annotate scores where low scores reflect appropriate structural simplicity rather than genuine maturity gaps. |

---

## 17. Glossary

| Term | Definition |
|:---|:---|
| **Anchor** | A descriptive behavioural statement associated with a specific score level (1–5) for a given sub-factor. Used to calibrate assessor judgment across engagements. |
| **Archetype** | A canonical cybersecurity programme model representing a specific strategic orientation. Used as a reference vector in the classification engine; not a target to fit toward. |
| **Classical (output type)** | Classification indicating the dimensional profile closely conforms to an established archetype (cosine similarity ≥ 97.5%). |
| **Composite score** | The weighted sum of all nine dimension scores; a single organisational maturity indicator in the range [1.00, 5.00]. |
| **Cosine similarity** | A mathematical measure of the angular distance between two vectors in n-dimensional space; used to compare the shape of organisational profiles against archetype reference vectors. |
| **Dimension** | One of nine structured assessment areas (D1–D9), each belonging to a pillar and decomposed into 2–5 sub-factors. |
| **Dimension score** | The arithmetic mean of all sub-factor scores within a dimension. Falls in the range [1.00, 5.00]. |
| **Dimension weight** | A percentage value assigned by the assessor to a dimension, expressing its relative importance in the composite computation. All nine weights must sum to 100%. |
| **Generative output** | An output derived algorithmically from assessment data rather than selected from a predefined list. The SET Framework's Novel model designation is generative. |
| **Hybrid (output type)** | Classification indicating partial alignment with the closest archetype (92% ≤ cosine similarity < 97.5%). |
| **Novel (output type)** | Classification indicating the dimensional profile does not conform to any established archetype (cosine similarity < 92%). Model name is derived algorithmically from the dimensional signature. |
| **Pillar** | One of three top-level groupings — Socio, Econo, Tech — each containing three dimensions. |
| **Pillar average** | The unweighted arithmetic mean of dimension scores within a pillar. Descriptive signal only; not a direct input to the composite computation. |
| **Reference vector** | A nine-dimensional ideal-state dimension score vector representing a theoretical organisation that fully embodies a specific classical archetype. |
| **Sub-factor** | One of 42 primary assessment factors, each assigned a 1–5 score using five descriptive behavioural anchors. |
| **Threat-Capability Gap (TCG)** | D9 score minus the mean of D7 and D8 scores. Negative values indicate technical and process capability is insufficient relative to threat landscape maturity. |
| **Weight configuration** | The process of assigning percentage weights to each of the nine dimensions before scoring begins, reflecting the assessor's expert judgment about the organisational context. |

---

## 18. Changelog

| Version | Date | Notes |
|:---|:---|:---|
| `v1.0` | 2026-03 | Initial framework definition. 3 pillars, 9 dimensions, 20 sub-factors, 6 archetype reference vectors. Weighted composite model. Cosine similarity classification engine. Physical field protocol. |
| `v2.0` | 2026-03 | Major expansion to 42 sub-factors (5-5-5 for D1/D2/D3/D7/D8/D9; 4-4-4 for D4/D5/D6). New sub-factors: 1d Digital Transformation Dependency, 1e Supply Chain Mission Criticality, 2c Incident Reporting Obligations, 2d Cross-Sector Regulatory Overlap, 2e International Standards Alignment, 3c Security Awareness Culture, 3d Insider Threat Risk Profile, 3e Workforce Distribution, 4d Cyber Insurance Maturity, 5c Psychological Safety, 5d Security Perception, 6c Vendor Lock-in, 6d Change Fatigue, 7c Incident Response Maturity, 7d TPRM Process, 7e Change Management, 8c IAM Maturity, 8d Cloud Security Architecture, 8e Vulnerability Management, 9c Supply Chain Compromise Risk, 9d Geopolitical Exposure, 9e Insider Threat Probability. Added global regulatory context section, sector-specific threat calibration, organisation size guidance, and extended interview question bank. |

---

> **License:** Research Use — Attribution Required.  
> **Status:** `Active — v2.0`  
> **Framework Maintainer:** SET Framework Working Group  
> **Contributions:** Researchers wishing to contribute empirical validation data, refined archetype vectors, industry-specific anchor sets, or translated anchor language are encouraged to open an issue or submit a pull request.  
> **Citation:** SET Framework Working Group. (2026). *SET Framework Assessment Engine: Technical Reference v2.0.* GitHub.
