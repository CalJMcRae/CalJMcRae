# GRC Portfolio Roadmap

**Callum McRae · Aspiring GRC Analyst**
**Target Role:** GRC Analyst · **Focus:** Risk Management, Compliance & AI Governance

---

## Objective

This portfolio demonstrates applied GRC competency — not checkbox compliance, but defensible decision-making under realistic constraints. The goal is a collection of 3–5 high-quality projects that prove readiness for a GRC Analyst role, each showing how I think through risk, not just document it.

**Target audience:** Hiring managers and technical reviewers at organisations with structured GRC functions, particularly in private sector or federal-adjacent environments.

### What every project must demonstrate

- Defensible decisions backed by documented assumptions
- Clear trade-off analysis — what was accepted and why
- Residual risk acknowledgment
- Communication accessible to both technical and non-technical stakeholders

---

## Strategy

| Principle | Detail |
|---|---|
| Depth over breadth | 2–3 excellent projects outperform 6 shallow ones |
| Defensibility first | Every decision must survive audit-style scrutiny |
| Show the thinking | Assumptions, trade-offs, and residual risk are mandatory in every deliverable |
| Format standard | All deliverables in Markdown: Context → Analysis → Decision → Residual Risk |
| Audience test | Each document must be readable by a non-technical executive |

---

## Projects

---

### Phase 1 — PCI DSS Scope Determination `Complete ✅`

> Simulated a scope determination and network segmentation review for an e-commerce environment handling cardholder data. The challenge is not just identifying gaps — it is defending your conclusions the way an auditor would challenge them.

| | |
|---|---|
| **Framework** | PCI DSS v4.0 |
| **Key skill** | Defending technical claims under audit pressure |
| **Why it matters** | Segmentation is one of the most contested areas in PCI assessments — showing you can reason through it signals audit readiness |

#### Deliverables

- [Repo: PCI DSS Scope Determination](https://github.com/CalJMcRae/pci-dss-scope-project)
- Assessed CDE boundaries, shared service dependencies, and segmentation gaps across eight findings with audit-ready QSA challenge preparation

#### Resume Bullet

> Conducted PCI DSS v4.0 scope determination and network segmentation review for a simulated e-commerce environment; identified CDE boundary gaps and produced audit-ready documentation with defensible conclusions.

#### Lessons Learned


This was my first hands-on project with the PCI DSS framework, so it was a 
learning experience from the start — which is exactly the point of this 
portfolio. Working through it pushed my understanding of PCI DSS beyond 
surface-level familiarity and gave me the vocabulary and reasoning process 
to meaningfully contribute to a real PCI DSS audit conversation in the 
future.

Beyond the framework itself, it reinforced why controls like segmentation, 
technology dependency mapping, and data privacy matter in practice, not 
just on paper. What surprised me most was how much of the difficulty was 
in defending a conclusion rather than reaching one — an auditor doesn't 
just want the right answer, they want to see the reasoning survive 
challenge.

If I revisited this project, I'd spend more time stress-testing my own 
assumptions before writing the final conclusion, rather than after. I 
don't consider this a finished or fully audit-grade piece of work yet — 
but it demonstrates the thing I think matters most at this stage: the 
ability to reason through a real compliance scenario, document that 
reasoning defensibly, and keep improving it as I learn.

---

### Phase 2 — Risk Assessment Lab `In Progress`

> Walks through a structured risk assessment using NIST SP 800-30 methodology, including asset identification, threat modelling, likelihood/impact scoring, and treatment options.

| | |
|---|---|
| **Framework** | NIST SP 800-30 |
| **Key skill** | Structured risk analysis and treatment recommendation |
| **Why it matters** | NIST SP 800-30 is a foundational federal risk methodology — demonstrating fluency here signals readiness for structured, defensible risk work |

#### Tasks

- [ ] Define scenario and scope
- [ ] Identify assets and their business value
- [ ] Identify threats and vulnerabilities
- [ ] Score likelihood and impact for each risk
- [ ] Recommend treatment options (mitigate, accept, transfer, avoid)
- [ ] Document assumptions and residual risk

#### Deliverables

- `risk-assessment-lab.md` — full assessment with scoring and treatment plan
- 3–5 min Loom walkthrough explaining your reasoning

#### Resume Bullet

> Conducted a structured risk assessment using NIST SP 800-30 methodology; performed asset identification, threat modelling, and likelihood/impact scoring, and recommended defensible risk treatment options.

#### Lessons Learned

*What would you do differently? What assumptions proved wrong? What surprised you?*

---

### Phase 3 — Vendor Risk Management `In Progress`

> Develops a third-party risk management process: intake questionnaire, risk tiering, control evaluation, and ongoing monitoring cadence.

| | |
|---|---|
| **Framework** | General GRC practice / NIST CSF |
| **Key skill** | Third-party risk evaluation and lifecycle management |
| **Why it matters** | Vendor risk is one of the most common real-world GRC responsibilities, especially for lean or micro organisations relying on third-party tools |

#### Tasks

- [ ] Design vendor intake questionnaire
- [ ] Define risk tiering criteria (critical, high, medium, low)
- [ ] Build a control evaluation checklist per tier
- [ ] Define ongoing monitoring cadence and review triggers
- [ ] Document escalation path for high-risk vendors

#### Deliverables

- `vendor-risk-management.md` — full process documentation
- 3–5 min Loom walkthrough

#### Resume Bullet

> Developed a third-party vendor risk management process including intake questionnaire, risk tiering, control evaluation, and ongoing monitoring cadence.

#### Lessons Learned

*What would you do differently? What assumptions proved wrong? What surprised you?*

---

### Phase 4 — ISO 27001 Statement of Applicability `Not Started`

> Produce a Statement of Applicability for a fictional mid-size company. The hard part is not listing controls — it is justifying the exclusions in a way that holds up to scrutiny.

| | |
|---|---|
| **Framework** | ISO 27001:2022 Annex A |
| **Key skill** | Risk-based decision making — inclusion AND exclusion rationale |
| **Why it matters** | Auditors spend more time challenging exclusions than inclusions. Showing you can defend an exclusion is a differentiator |

#### Tasks

- [ ] Define company context: size, industry, data sensitivity, threat landscape
- [ ] List all ISO 27001:2022 Annex A controls
- [ ] For each control: include, exclude, or conditionally apply
- [ ] Document risk reasoning for every exclusion
- [ ] Flag controls where the decision is genuinely ambiguous
- [ ] Write an executive summary accessible to a non-technical board

#### Deliverables

- `soa.md` — full Statement of Applicability with justifications
- 3–5 min Loom walkthrough focusing on your exclusion rationale

#### Resume Bullet

> Developed an ISO 27001:2022 Statement of Applicability for a simulated mid-size organisation; documented risk-based inclusion and exclusion decisions for all Annex A controls with board-level executive summary.

#### Lessons Learned

*What was harder than expected? Any controls where the right call was genuinely unclear?*

---

### Phase 5 — Risk Acceptance Documentation `Not Started`

> Document a formal risk acceptance for a realistic business scenario — an unpatched legacy system, a third-party integration, or a deferred control implementation. The goal is executive-level communication of a security decision.

| | |
|---|---|
| **Framework** | NIST SP 800-30 / general GRC practice |
| **Key skill** | Executive communication — translating technical risk into business language |
| **Why it matters** | Most GRC work involves getting sign-off from people who don't speak security. This project proves you can bridge that gap |

#### Tasks

- [ ] Define a realistic risk scenario with business context
- [ ] Quantify impact: financial, operational, reputational
- [ ] Articulate why the risk is being accepted (cost, timeline, compensating controls)
- [ ] Document compensating controls currently in place
- [ ] Set an acceptance duration and review trigger
- [ ] Write the memo for a non-technical executive audience

#### Deliverables

- `risk-acceptance.md` — formal risk acceptance memo
- 3–5 min Loom walkthrough explaining the business context and your reasoning

#### Resume Bullet

> Produced executive-level risk acceptance documentation for a simulated legacy system scenario; quantified business impact and communicated compensating controls and review cadence to a non-technical audience.

#### Lessons Learned

*Was the business case for acceptance convincing? What would change your recommendation?*

---

### Phase 6 — EU AI Act Compliance Assessment `Stretch Goal`

> Assess a fictional AI system against the EU AI Act risk classification framework. This project directly supports an interest in AI governance and is a strong differentiator — few entry-level candidates can demonstrate it.

| | |
|---|---|
| **Framework** | EU AI Act (2024) |
| **Key skill** | Interpreting emerging regulation with genuine ambiguity |
| **Why it matters** | AI governance is a fast-growing compliance area. Early demonstrable knowledge is a real career advantage |

#### Tasks

- [ ] Define the AI system: purpose, inputs, outputs, affected parties
- [ ] Apply EU AI Act risk classification (unacceptable, high, limited, minimal)
- [ ] Map applicable requirements to the system's operations
- [ ] Identify compliance gaps
- [ ] Highlight areas of genuine regulatory ambiguity and how you resolved them
- [ ] Note where the regulation is unclear and what further guidance would be needed

#### Deliverables

- `ai-act-assessment.md` — classification report with gap analysis
- 3–5 min Loom walkthrough

#### Resume Bullet

> Completed EU AI Act risk classification and gap analysis for a simulated AI system; identified applicable requirements and documented areas of regulatory ambiguity with recommended interpretations.

---

### Phase 7 — GRC Control Automation Proposal `Stretch Goal`

> Design an automation approach for a manual GRC control — evidence collection, periodic review, or control testing. This bridges GRC and technical implementation, showing you understand both sides.

| | |
|---|---|
| **Framework** | Agnostic — applies to any standard |
| **Key skill** | Connecting compliance requirements to technical implementation |
| **Why it matters** | Employers increasingly want GRC professionals who can work with engineering teams, not just produce documentation |

#### Tasks

- [ ] Identify a specific manual control that is a good automation candidate
- [ ] Describe the current manual process and its weaknesses
- [ ] Design an automation approach (tools, logic, workflow)
- [ ] Identify trade-offs: what the automation gains and what it might miss
- [ ] Address limitations and failure modes

#### Deliverables

- `automation-proposal.md` — design document with trade-off analysis

#### Resume Bullet

> Designed a GRC control automation proposal for [control type]; documented current-state manual process, proposed automation architecture, and trade-offs including failure modes and coverage gaps.

---

## Portfolio Presentation Standards

The Loom walkthroughs are not optional extras — they are a core part of this portfolio. A document proves you can write. A walkthrough proves you can communicate. For an entry-level GRC role, being able to explain your reasoning out loud is exactly the skill being tested.

**For each completed project:**

- Record a 3–5 minute Loom walkthrough
- Lead with the scenario and what made it challenging
- Walk through your key decisions — not the whole document
- Explicitly call out the trade-offs you faced
- End with what you would do differently or what you are still uncertain about
- Add the Loom link to the project README

---

## Timeline

| Period | Focus | Status |
|---|---|---|
| Month 1 | Risk Assessment Lab + Vendor Risk Management | In Progress |
| Month 2 | ISO 27001 Statement of Applicability | Not Started |
| Month 3 | Risk Acceptance Documentation | Not Started |
| Month 4+ | EU AI Act Assessment (stretch) | Stretch Goal |
| Month 5+ | GRC Control Automation (stretch) | Stretch Goal |

---

## Progress Tracker

### Projects
- [x] Phase 1 — PCI DSS Scope Determination
- [ ] Phase 2 — Risk Assessment Lab
- [ ] Phase 3 — Vendor Risk Management
- [ ] Phase 4 — ISO 27001 Statement of Applicability
- [ ] Phase 5 — Risk Acceptance Documentation
- [ ] Phase 6 — EU AI Act Assessment *(stretch)*
- [ ] Phase 7 — GRC Control Automation *(stretch)*

### Certifications
- [x] CompTIA Security+
- [ ] ISC2 CGRC *(in progress)*
- [ ] CRISC *(next milestone)*
- [ ] CISM *(long-term)*
- [ ] CISSP *(long-term)*

---

## Quality Checklist

Run this against every deliverable before publishing.

- [ ] Have I justified every significant decision?
- [ ] Are all assumptions documented explicitly?
- [ ] Have I explained trade-offs — what I chose and what I gave up?
- [ ] Is residual risk acknowledged?
- [ ] Would this survive audit-style challenge?
- [ ] Can a non-technical executive understand the key points?
- [ ] Is the Loom walkthrough recorded and linked?
- [ ] Is there a lessons learned note at the end?

---

## End Goal

> *"I can make and defend real-world GRC decisions under uncertainty."*

A recruiter or hiring manager who reviews this portfolio should come away with three things:

- This person understands GRC frameworks at a working level, not just a conceptual one
- This person can communicate risk to both technical and non-technical audiences
- This person is actively building skills and shows the judgement to do the work