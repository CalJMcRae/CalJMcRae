# GRC Portfolio Roadmap

**Callum McRae · GRC Analyst**
**Target Role:** GRC Analyst · **Focus:** Risk Management, Compliance & AI Governance

---

## Objective

This portfolio demonstrates applied GRC competency, not checkbox compliance, but defensible decision-making under realistic constraints. The goal is a collection of 3-5 high-quality projects that prove readiness for a GRC Analyst role, each showing how I think through risk, not just document it.

**Target audience:** Hiring managers and technical reviewers at organisations with structured GRC functions, particularly in private sector or federal-adjacent environments.

### What every project must demonstrate

- Defensible decisions backed by documented assumptions
- Clear trade-off analysis: what was accepted and why
- Residual risk acknowledgment
- Communication accessible to both technical and non-technical stakeholders

---

## Strategy

| Principle | Detail |
|---|---|
| Depth over breadth | 2-3 excellent projects outperform 6 shallow ones |
| Defensibility first | Every decision must survive audit-style scrutiny |
| Show the thinking | Assumptions, trade-offs, and residual risk are mandatory in every deliverable |
| Format standard | All deliverables in Markdown: Context → Analysis → Decision → Residual Risk |
| Audience test | Each document must be readable by a non-technical executive |

---

## Projects

Completed projects first, then in progress, then stretch goals.

---

### Phase 1: PCI DSS Scope Determination `Complete ✅`

> Simulated a scope determination and network segmentation review for an e-commerce environment handling cardholder data. The challenge is not just identifying gaps, it is defending your conclusions the way an auditor would challenge them.

| | |
|---|---|
| **Framework** | PCI DSS v4.0 |
| **Key skill** | Defending technical claims under audit pressure |
| **Why it matters** | Segmentation is one of the most contested areas in PCI assessments, and showing you can reason through it signals audit readiness |

#### Deliverables

- [PCI DSS Scope Determination] https://github.com/CalJMcRae/pci-dss-scope-project
- Assessed CDE boundaries, shared service dependencies, and segmentation gaps across eight findings with audit-ready QSA challenge preparation

#### Resume Bullet

> Conducted PCI DSS v4.0 scope determination and network segmentation review for a simulated e-commerce environment; identified CDE boundary gaps and produced audit-ready documentation with defensible conclusions.

#### Lessons Learned

This was my first hands-on project with the PCI DSS framework, so it was a 
learning experience from the start, which is exactly the point of this 
portfolio. Working through it pushed my understanding of PCI DSS beyond 
surface-level familiarity and gave me the vocabulary and reasoning process 
to meaningfully contribute to a real PCI DSS audit conversation in the 
future.

Beyond the framework itself, it reinforced why controls like segmentation, 
technology dependency mapping, and data privacy matter in practice, not 
just on paper. What surprised me most was how much of the difficulty was 
in defending a conclusion rather than reaching one: an auditor doesn't 
just want the right answer, they want to see the reasoning survive 
challenge.

If I revisited this project, I'd spend more time stress-testing my own 
assumptions before writing the final conclusion, rather than after. I 
don't consider this a finished or fully audit-grade piece of work yet, 
but it demonstrates the thing I think matters most at this stage: the 
ability to reason through a real compliance scenario, document that 
reasoning defensibly, and keep improving it as I learn.

---

### Phase 2: ISO 27001 Statement of Applicability `Complete ✅`

> Produced a Statement of Applicability for a simulated 85-person cloud-native SaaS 
> company. The hard part was not listing controls, it was justifying the exclusions 
> in a way that holds up to scrutiny.

| | |
|---|---|
| **Framework** | ISO 27001:2022 Annex A |
| **Key skill** | Risk-based decision making: inclusion AND exclusion rationale |
| **Why it matters** | Auditors spend more time challenging exclusions than inclusions. Showing you can defend an exclusion is a differentiator |

#### Deliverables

- [Repo: ISO 27001:2022 Statement of Applicability](https://github.com/CalJMcRae/ISO-27001-SoA-Project)
- All 93 Annex A controls assessed with risk-driven justifications
- 10 controls excluded, 5 with full auditor-challenge defense documentation
- Risk-to-control traceability matrix, alternative measures mapping, and evidence reference index completed

#### Resume Bullet

> Developed an ISO 27001:2022 Statement of Applicability for a simulated cloud-native SaaS organisation; assessed all 93 Annex A controls, documented risk-based inclusion and exclusion decisions, and produced full traceability and evidence documentation.

#### Tasks

- [x] Define company context: size, industry, data sensitivity, threat landscape
- [x] List all ISO 27001:2022 Annex A controls
- [x] For each control: include, exclude, or conditionally apply
- [x] Document risk reasoning for every exclusion
- [x] Flag controls where the decision is genuinely ambiguous
- [x] Write an executive summary accessible to a non-technical board

#### Lessons Learned

**What surprised me, and what kept the work honest.** Going in, I expected ISO 27001 to reward comprehensive coverage: include every control and claim everything is implemented. The standard's own guidance corrected that. A footnote made the point that certification is not about blanket compliance but about applying practical, relevant security controls, and that reframed the whole exercise. It kept me honest with the implementation status, 61 Implemented, 20 Partial, 2 Planned rather than a wall of green, and it made me ask "is this control actually relevant here?" for every Annex A control rather than defaulting to include.

**The exclusions were more straightforward than I expected, for a specific reason.** All five documented exclusions were relatively easy to defend because the company is cloud-native. The physical and premises controls, such as securing offices and the physical protection of confidential information, were the natural candidates. My first instinct was that some physical safeguards would still be needed wherever confidential information could be handled, but ISO 27001:2022 treats Annex A as a set of controls to consider against actual risk, and with endpoint management and an Acceptable Use Policy already addressing that risk, excluding the premises controls held up.

**What I would keep.** The risk-to-control traceability matrix was the most useful part as a learning tool. Mapping every applicable control back to a specific risk forced me to read all 93 controls and understand what each one is and why it exists, rather than skimming the familiar ones. That is the part of the process I would repeat on any future framework.

---

### Phase 3: Cloud Risk Assessment & Remediation Lab (AWS) `Complete ✅`

> An end-to-end GRC engagement on a real AWS environment built for a simulated healthtech
> startup (Meridian Health Analytics). Walks a finding from cloud misconfiguration through a
> risk register, NIST CSF 2.0 mapping, and prioritised remediation to a verified fix, and
> adds a mock vendor assessment and a SOC 2 Type II report review as independent workstreams.

| | |
|---|---|
| **Frameworks** | NIST SP 800-30 · NIST CSF 2.0 · AICPA SOC 2 Trust Services Criteria · SIG Lite |
| **Key skill** | Running the full risk lifecycle on live cloud infrastructure and closing the loop with evidence |
| **Why it matters** | Most entry-level portfolios stop at documentation. Building the environment, scanning it with a real open-source tool, and implementing verified fixes shows the work can actually be done, not just written about |

#### Deliverables

- [Repo: GRC-AWS-Project](https://github.com/CalJMcRae/GRC-AWS-Project)
- AWS lab (VPC, EC2, S3, IAM, CloudTrail, KMS) with 5 documented deliberate misconfigurations and a hardened contrast tier
- 16-risk register (2 critical, 4 high, 8 medium, 2 low): 5 by design, 11 surfaced by an independent Prowler scan and triaged with documented keep/exclude rationale
- NIST CSF 2.0 subcategory mapping with current-vs-target maturity ratings and a control heat map
- Mock third-party vendor assessment: 8-domain questionnaire, weighted scorecard, executive "approve-with-conditions" memo with contractual conditions and compensating controls
- SOC 2 Type II report review (scope, CUECs, exceptions, bridge letter), cross-checked against the vendor questionnaire
- Prioritised remediation roadmap (0-30 / 30-90 / 90+ day windows, effort and cost per item) with 2 fixes implemented and verified in the live environment (public S3 exposure closed; IMDSv2 enforced)

#### Resume Bullet

> Built a multi-service AWS environment and ran an independent Prowler scan; produced a 16-risk register scored with NIST SP 800-30, mapped every risk to NIST CSF 2.0 with maturity ratings, completed a mock vendor assessment and SOC 2 Type II review, and delivered a prioritised remediation roadmap with two verified fixes implemented in the live environment.

#### Lessons Learned

This is the most comprehensive and multifaceted project in my portfolio so far. It runs a full risk lifecycle (build, scan, register, framework mapping, remediation, verification) plus two independent workstreams (a vendor assessment and a SOC 2 review), and most of the lessons below come from that breadth.

**What I would do differently.** Set up broad read-only permissions for the scanning identity before starting the risk assessment rather than during it. I hit repeated access-denied walls mid-Phase-2 and could not read account-level Block Public Access, list buckets, or check KMS key rotation. I would also build a lightweight Terraform version alongside the console build. Building by hand meant no reproducible teardown, and every remediation had to be clicked and screenshotted rather than diffed. And I would run Prowler with the instances actually running, since the scan reported the SSH port as "no public IP" only because the box was stopped, which understated a real exposure.

**Assumptions that proved wrong.** I read Prowler's "critical" flag on the root account as "root has no MFA." It has virtual MFA, and only the hardware-MFA check failed. I rescored that risk from High to Medium once I checked the specific finding rather than the severity label. I assumed a genuine public sample SOC 2 report would be easy to find, but every one was a locked PDF, so I pivoted to the AICPA illustrative report. I also assumed that running a scanner would let me claim "GRC tools" on a resume. It does not. To a hiring manager that phrase means the dedicated platforms.

**What surprised me.** How much of the risk assessment was triage judgment rather than analysis. It went from 116 Prowler failures to 16 risks, and the defensible part was documenting why roughly 100 were excluded, not scoring the 16. How readily related findings collapse: about fourteen separate CloudWatch checks are really one "no monitoring" risk. And that the strongest piece of work was unplanned. The cross-check between the vendor questionnaire and the SOC 2 report surfaced a discrepancy, where the vendor claimed annual access reviews but the report tested quarterly, that only existed because I did both phases. The weakest link is the opposite: the vendor answers and the SOC 2 report are self-authored, so they show I know the structure, not that I have handled a real evasive vendor.

---

### Phase 4: Vendor Risk Management `In Progress`

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

- `vendor-risk-management.md`: full process documentation

#### Resume Bullet

> Developed a third-party vendor risk management process including intake questionnaire, risk tiering, control evaluation, and ongoing monitoring cadence.

---

### Phase 5: Risk Acceptance Documentation `Not Started`

> Document a formal risk acceptance for a realistic business scenario: an unpatched legacy system, a third-party integration, or a deferred control implementation. The goal is executive-level communication of a security decision.

| | |
|---|---|
| **Framework** | NIST SP 800-30 / general GRC practice |
| **Key skill** | Executive communication: translating technical risk into business language |
| **Why it matters** | Most GRC work involves getting sign-off from people who don't speak security. This project proves you can bridge that gap |

#### Tasks

- [ ] Define a realistic risk scenario with business context
- [ ] Quantify impact: financial, operational, reputational
- [ ] Articulate why the risk is being accepted (cost, timeline, compensating controls)
- [ ] Document compensating controls currently in place
- [ ] Set an acceptance duration and review trigger
- [ ] Write the memo for a non-technical executive audience

#### Deliverables

- `risk-acceptance.md`: formal risk acceptance memo

#### Resume Bullet

> Produced executive-level risk acceptance documentation for a simulated legacy system scenario; quantified business impact and communicated compensating controls and review cadence to a non-technical audience.

---

### Phase 6: AI Compliance Assessment (Eramba) `Complete ✅`

> Assess a simulated AWS-hosted clinical-risk ML model against the EU AI Act and the NIST AI RMF, and run the whole assessment inside a real GRC platform (Eramba Community). Scenario: Meridian Health Analytics deploys a model that scores partner-clinic patient cohorts for elevated ("rising") health risk and surfaces the scores to clinicians, trained on the de-identified data from the Phase 3 lab. The hard part is twofold: interpreting emerging AI regulation where the classification itself is genuinely contested, and operationalising that judgement as a control catalogue, risk register and treatment plan a reviewer could actually work from.

| | |
|---|---|
| **Frameworks** | EU AI Act (2024) · NIST AI RMF 1.0 · ISO/IEC 42001:2023 (overlay) |
| **Tool** | Eramba Community Edition, an open-source GRC platform self-hosted via Docker (free) |
| **Key skill** | Interpreting ambiguous AI regulation and operationalising it in a GRC platform, not just a document |
| **Why it matters** | AI governance is a fast-growing compliance area few entry-level candidates can demonstrate; doing it in a recognised GRC tool rather than a Word doc is a second differentiator |

#### Tasks

- [x] Stand up Eramba Community (Docker) and configure the organisation, framework and asset structure
- [x] Define the AI system: purpose, inputs, outputs, users, affected persons, lifecycle stage, hosting, third-party model components
- [x] Classify the system under the EU AI Act (prohibited / high-risk / limited / minimal); document the reasoning and the genuine ambiguity, clinical decision-support vs autonomous decision, and the medical-device (MDR) interplay
- [x] Map applicable EU AI Act obligations to the system (if high-risk: risk-management system, data governance, technical documentation, logging and record-keeping, transparency, human oversight, accuracy / robustness / cybersecurity, post-market monitoring)
- [x] Build a combined control catalogue in Eramba: EU AI Act obligations plus NIST AI RMF (Govern / Map / Measure / Manage) subcategories
- [x] Build the AI risk register in Eramba, bias and fairness, data quality, model drift, explainability, misuse, security, human-oversight failure, supply-chain (third-party model), with likelihood / impact scoring
- [x] Run the assessment in Eramba: control status, gaps, owners
- [x] Document a treatment plan for each gap, with residual risk stated
- [x] Build and evaluate a real minimal model on AWS (SageMaker), confirming one risk with measured evidence and surfacing a new one, then tear it down
- [x] Write the executive classification and gap-analysis report; state where the regulation is unclear and how the ambiguity was resolved

#### Deliverables

- `ai-compliance-assessment.md`: classification report, gap analysis, treatment plan, residual-risk sign-off
- Eramba exports / screenshots: AI control catalogue, risk register, assessment, treatment plans
- AI system data-flow diagram

#### Resume Bullet

> Assessed a clinical AI system against the EU AI Act and NIST AI RMF, classifying it as high-risk through a genuinely contested regulatory question; built the control catalogue, 10-risk register and gap analysis in Eramba (open-source GRC platform); then built and evaluated a real machine-learning model on AWS to test the assessment against actual evidence, confirming a critical fairness risk with measured data and surfacing a new finding a design-only review would have missed.

---

### Phase 7: GRC Control Automation Proposal `Stretch Goal`

> Design an automation approach for a manual GRC control: evidence collection, periodic review, or control testing. This bridges GRC and technical implementation, showing you understand both sides.

| | |
|---|---|
| **Framework** | Agnostic, applies to any standard |
| **Key skill** | Connecting compliance requirements to technical implementation |
| **Why it matters** | Employers increasingly want GRC professionals who can work with engineering teams, not just produce documentation |

#### Tasks

- [ ] Identify a specific manual control that is a good automation candidate
- [ ] Describe the current manual process and its weaknesses
- [ ] Design an automation approach (tools, logic, workflow)
- [ ] Identify trade-offs: what the automation gains and what it might miss
- [ ] Address limitations and failure modes

#### Deliverables

- `automation-proposal.md`: design document with trade-off analysis

#### Resume Bullet

> Designed a GRC control automation proposal for [control type]; documented current-state manual process, proposed automation architecture, and trade-offs including failure modes and coverage gaps.

---

### Phase 8: IAM & Access Control Audit `Complete ✅`

> Suggested by a mentor rather than part of the original seven-phase plan above, added here because it is a real, substantial project rather than left to sit outside the roadmap. An ITGC-style audit of identity and access management for Meridian Health Analytics (the same company as Phases 3 and 6, now grown to 210 employees), covering provisioning, deprovisioning, privileged access management, MFA enforcement, access reviews, joiner/mover/leaver, and change management on Microsoft 365 / Entra ID.

| | |
|---|---|
| **Framework** | ITGC methodology / general GRC practice |
| **Key skill** | Designing and executing a control test plan (pass/fail criteria and sampling method fixed before evidence is examined) and tracing findings back to a shared root cause |
| **Why it matters** | Identity and access management is one of the most commonly audited control domains in any organisation, and most entry-level portfolios do not show a full test-to-remediation-to-ticket lifecycle |

#### Tasks

- [x] Define the company scenario, identity environment, and Conditional Access policies
- [x] Build population data: 210 active and 25 terminated employees, a privileged account roster, and service accounts, with deliberately seeded control gaps
- [x] Define 14 testable controls across the 7 required areas, with pass/fail criteria and sampling method fixed before testing
- [x] Test every control area: full population where the data allowed it, a judgmental sample where it did not
- [x] Consolidate testing results into a findings register, scored with Likelihood x Impact
- [x] Build a phased remediation tracker, grouping findings that share a root cause
- [x] Convert the remediation plan into Jira-style tickets
- [x] Write the project README summarising scenario, approach, results, and limitations

#### Deliverables

- [Repo: IAM-Access-Control-Audit](https://github.com/CalJMcRae/IAM-Access-Control-Audit)
- 14-control test plan with pass/fail criteria and sampling methodology fixed before testing
- Full testing evidence across all 7 control areas (provisioning, deprovisioning, privileged access, MFA enforcement, access reviews, joiner/mover/leaver, change management)
- 17-finding register (5 critical, 5 high, 5 medium, 2 low), including 3 incidental findings outside the original control matrix
- Phased remediation tracker (13 items, 0-30/30-90 day windows) and 24 Jira-style tickets

#### Resume Bullet

> Conducted an ITGC-style audit of identity and access management for a simulated 210-person Microsoft 365 / Entra ID environment; designed a 14-control test plan with sampling methodology fixed before testing, produced a 17-finding register, traced multiple critical findings to a shared root cause in change management, and delivered a phased remediation plan converted into Jira-style tickets.

---

### Phase 9: Meridian Infrastructure Configuration Compliance (ServiceNow) `Complete ✅`

> Self-initiated after completing ServiceNow's "Configuration Compliance Essentials" course on LearnNow, to build baseline hands-on competency with ServiceNow's GRC application on its free Developer Instance. Models the same real infrastructure from Phase 3 (the AWS lab project) as CMDB configuration items, then builds an actual configuration compliance program around them: policy statements, compliance results, an exception, and remediation tracking, inside a real GRC platform rather than a document describing one.

| | |
|---|---|
| **Platform** | ServiceNow (GRC: Policy and Compliance Management, CMDB), Personal Developer Instance |
| **Framework** | NIST CSF 2.0 (reusing the AWS lab project's exact subcategory mappings for carried-over findings) |
| **Key skill** | Navigating a real enterprise GRC platform's actual object model (Authority Documents, Citations, Policies, Policy Statements, Entities, Controls, Issues), and adapting around genuine platform constraints rather than treating a clean build as a given |
| **Why it matters** | ServiceNow is one of the most widely deployed GRC platforms in industry; demonstrating baseline fluency in it, on top of Eramba from Phase 6, shows adaptability across tools rather than depth in only one |

#### Tasks

- [x] Model the AWS lab project's real infrastructure (`meridian-web`, `meridian-db`, the customer-reports S3 bucket) as ServiceNow CMDB configuration items
- [x] Create an Authority Document (NIST CSF 2.0) and Citations for the subcategories referenced
- [x] Build a Policy ("Meridian Infrastructure Configuration Standard") with 7 Policy Statements, 5 reusing known AWS lab project findings and 2 genuinely new to this project
- [x] Link each statement to the correct CMDB entity and assess compliance for all 8 resulting Controls
- [x] Document one risk-acceptance exception with a compensating control and review date
- [x] Track every non-compliant result as an Issue with a remediation recommendation and priority
- [x] Diagnose and work around two separate non-functional platform mechanisms (a stalled plugin install tied to an unrelated upgrade path, and a non-functional native attestation workflow), documenting both rather than hiding them
- [x] Write the project README summarising scenario, approach, results, and limitations

#### Deliverables

- [Repo: ServiceNow-Configuration-Compliance](https://github.com/CalJMcRae/ServiceNow-Configuration-Compliance)
- CMDB design and mapping back to the AWS lab project's real assets
- 7-statement compliance policy mapped to NIST CSF 2.0
- Compliance results for all 8 Controls (3 pass, 4 fail, 1 fail with a documented exception)
- One documented exception, a remediation tracker, and Issue records for every open finding

#### Resume Bullet

> Built a configuration compliance program in ServiceNow's GRC application, modeling real AWS infrastructure as configuration items, mapping 7 policy statements to NIST CSF 2.0, and tracking compliance assessments, an exception, and remediation issues; adapted the approach multiple times around real platform constraints rather than treating a clean path as a given.

---

## Timeline

| Project | Status |
|---|---|
| PCI DSS Scope Determination | Complete ✅ |
| ISO 27001:2022 Statement of Applicability | Complete ✅ |
| Cloud Risk Assessment & Remediation Lab (AWS) | Complete ✅ |
| AI Compliance Assessment (Eramba) | Complete ✅ |
| Vendor Risk Management | In progress |
| Risk Acceptance Documentation | Planned |
| GRC Control Automation | Stretch goal |
| IAM & Access Control Audit (mentor-assigned) | Complete ✅ |
| Meridian Infrastructure Configuration Compliance (ServiceNow) | Complete ✅ |

---

## Progress Tracker

### Projects
- [x] Phase 1: PCI DSS Scope Determination
- [x] Phase 2: ISO 27001 Statement of Applicability
- [x] Phase 3: Cloud Risk Assessment & Remediation Lab (AWS)
- [ ] Phase 4: Vendor Risk Management
- [ ] Phase 5: Risk Acceptance Documentation
- [x] Phase 6: AI Compliance Assessment (Eramba)
- [ ] Phase 7: GRC Control Automation *(stretch)*
- [x] Phase 8: IAM & Access Control Audit *(mentor-assigned)*
- [x] Phase 9: Meridian Infrastructure Configuration Compliance (ServiceNow) *(self-initiated)*

### Certifications
- [x] CompTIA Security+
- [x] CompTIA Network+
- [ ] AWS Solutions Architect Associate *(in progress)*
- [ ] CRISC *(next milestone)*
- [ ] CISM *(long-term)*
- [ ] CISSP *(long-term)*

---

## Quality Checklist

Run this against every deliverable before publishing.

- [ ] Have I justified every significant decision?
- [ ] Are all assumptions documented explicitly?
- [ ] Have I explained trade-offs: what I chose and what I gave up?
- [ ] Is residual risk acknowledged?
- [ ] Would this survive audit-style challenge?
- [ ] Can a non-technical executive understand the key points?
- [ ] Is there a lessons learned note at the end?

---

## End Goal

> *"I can make and defend real-world GRC decisions under uncertainty."*

A recruiter or hiring manager who reviews this portfolio should come away with three things:

- This person understands GRC frameworks at a working level, not just a conceptual one
- This person can communicate risk to both technical and non-technical audiences
- This person is actively building skills and shows the judgement to do the work
