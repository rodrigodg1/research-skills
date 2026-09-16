# Fillable DSR templates

Fill in what is already known about the project and mark gaps as **[to be defined]**, so it is clear
what is missing. Adapt field names to the language and venue.

## Contents
1. DSR research protocol
2. Problem statement and class of problems
3. Research questions
4. Requirements table
5. Traceability matrix
6. Design principles
7. Technological rule and CIMO proposition
8. Evaluation plan (FEDS)
9. Iteration log
10. Contribution statement
11. DSR Grid
12. Design theory canvas
13. DSR review report
14. Complete worked example

---

## 1. DSR research protocol

```markdown
# DSR protocol — [working title]

## 1. Identification
- Researcher / supervisor:
- Field and target venue(s):
- Version and date:

## 2. Problem
- Statement (see §2):
- Evidence of relevance (source → evidence):
- Stakeholders and interests:
- Known or hypothesized causes:
- Class of problems and boundary conditions:

## 3. Questions and objectives
- Design question:
- Knowledge questions:
- General objective:
- Specific objectives (as outcomes):

## 4. Knowledge base
- Knowledge about the problem (Ω):
- Existing solutions and limitations (Λ), with comparison criteria:
- Kernel theories and how they will be used in the design:

## 5. Methodological approach
- Justification for DSR:
- Process adopted (DSRM, ADR, Wieringa, Dresch et al....) and adaptations:
- Entry point:
- DSR strategy (Iivari: general → instance or instance → general):
- Mapping of process steps × deliverables × chapters or papers:

## 6. Requirements (see §4)

## 7. Artifact
- Type(s) and main artifact:
- Form of representation:
- Anticipated design decisions and alternatives to explore:
- A priori design principles (if any):

## 8. Evaluation (see §8)
- Evaluation goals and priorities:
- FEDS strategy and justification:
- Planned episodes:
- Criteria, metrics, comparators, and thresholds:
- Threats to validity and mitigation:

## 9. Expected contribution
- Quadrant (Gregor & Hevner) and justification:
- Level(s):
- Expected design knowledge:

## 10. Ethics and data
- Human participants? Ethics review required (IRB/REC/CEP)?
- Personal data and applicable law (GDPR, LGPD, ...):
- Dual-use risks:
- Agreements with organizations:

## 11. Schedule by iteration
| Iteration | Period | Focus | Evaluation episodes | Deliverables |
|---|---|---|---|---|

## 12. Project risks
| Risk | Likelihood | Impact | Mitigation or fallback plan |
|---|---|---|---|
```

---

## 2. Problem statement and class of problems

**Design problem (adapted from Wieringa, 2014):**
> Improve **[problem context]**
> by **[(re)designing an artifact]**
> that satisfies **[main requirements]**
> in order to **[help stakeholders achieve goals]**.

**Narrative statement:**
> In **[context]**, **[stakeholders]** face **[problem]**, as evidenced by **[data or sources]**. This
> causes **[consequences]**. Current solutions, such as **[solutions]**, fall short because
> **[limitations]**. What is missing is **[gap]**.

**Class of problems:**
> This problem is an instance of the class **[class name]**: situations in which **[shared essential
> characteristics]**. Situations in which **[exclusions]** are outside the class.

---

## 3. Research questions

```markdown
RQ (design):          How should [artifact] be designed to [objective] in [context]?
  KQ1 (problem):      What are the causes of [problem] in [context]?
  KQ2 (requirements): Which requirements must [artifact] satisfy according to [sources]?
  KQ3 (effect):       What is the effect of [artifact] on [criterion] compared with [baseline]?
  KQ4 (sensitivity):  How does that effect vary with [context characteristic]?
```

---

## 4. Requirements table

| ID | Requirement | Type | Source | Justification or kernel theory | Priority | Verification criterion |
|---|---|---|---|---|---|---|
| R1 | | Functional / quality | Interview I3; Author (year); standard X | | High / medium / low | |

For abstract contributions, add a **Meta-requirement** column (class-level version).

---

## 5. Traceability matrix

| Problem aspect | Requirement | Design principle or decision | Artifact component | Criterion | Episode and method | Evidence | Met? |
|---|---|---|---|---|---|---|---|
| P1 | R1 | DP1 | C2 | Efficacy | E2 — benchmark | Table 5 | Yes / partly / no |

Rows with empty cells point to gaps to address before writing up the results.

---

## 6. Design principles

**Full form (adapted from Gregor, Chandra Kruse & Seidel, 2020):**
> **DP[n] — [short name].** For **[implementer]** to achieve **[aim]** for **[users]** in
> **[context]**, employ **[mechanisms]**, enacted by **[people or components]**, because
> **[rationale: theory or evidence]**.

**Compact form (adapted from Chandra, Seidel & Gregor, 2015):**
> **DP[n].** Provide the system with **[material property]** so that **[users]** can **[action]**,
> given that **[boundary conditions]**.

**Card for each principle:**
| Field | Content |
|---|---|
| Origin | A priori (requirements and theory) or a posteriori (reflection on evaluation) |
| Meta-requirements addressed | |
| Rationale | |
| Instantiation (features that embody it) | |
| Testable proposition | |
| Evidence obtained | |
| Boundary conditions | |

---

## 7. Technological rule and CIMO proposition

**Technological rule (adapted from van Aken, 2004):**
> To achieve **[effect Y]** in **[situation Z]**, apply something like **[intervention X]**.

**CIMO proposition (adapted from Denyer et al., 2008):**
> In contexts **[C]**, use interventions **[I]** to trigger mechanisms **[M]** and produce outcomes
> **[O]**.

---

## 8. Evaluation plan (FEDS)

```markdown
## Evaluation goals
- Rigor (efficacy / effectiveness):
- Main risks (human/social | technical):
- Ethics:
- Resource constraints:

## Strategy
- FEDS strategy: [Quick & Simple | Human Risk & Effectiveness | Technical Risk & Efficacy | Purely Technical]
- Justification:

## Episodes
```

| # | Timing | Purpose | Paradigm | Evaluand | Criteria | Method | Participants or data | Comparator | Success threshold | Iteration |
|---|---|---|---|---|---|---|---|---|---|---|
| E1 | Ex ante | Formative | Artificial | Requirements and design | Completeness, feasibility | Experts | 5 external experts | — | Criticisms addressed | 1 |
| E2 | Ex post | Summative | Artificial | Prototype | Efficacy | Benchmark | Historical data | Baseline X | ≥ baseline | 2 |

Then describe each episode: procedure, instruments, analysis, threats, and mitigation.

---

## 9. Iteration log

| Iteration | Dates | What was built or changed | Episode(s) | Main findings | Decisions and changes | Knowledge generated |
|---|---|---|---|---|---|---|
| 1 | | | | | | |

Keep the log during the project; reconstructing it afterwards tends to erase exactly the discarded
alternatives and negative results that demonstrate the search process.

---

## 10. Contribution statement

```markdown
Main artifact: [name] — [type]
Class of problems: [class] — boundary conditions: [conditions]
Novelty: relative to [solutions], the artifact [essential difference]
Evidence: [strategy] — [main result vs. baseline]
Design knowledge: [principles, rules, understanding of the problem]
Positioning: [quadrant], because the domain is [mature/immature: evidence] and the solution is [mature/immature: evidence]
Levels: [1 / 2 / 3] — [what corresponds to each level]
Implications for research:
Implications for practice:
```

---

## 11. DSR Grid (vom Brocke & Maedche, 2019)

| Problem | Input knowledge | Research process |
|---|---|---|
| Which problem, for whom, with what evidence? | Which theories, methods, and artifacts were used? | Which activities and iterations, with which methods? |
| **Key concepts** | **Solution** | **Output knowledge** |
| Which concepts define the problem and solution space? | What artifact was built and how does it work? | What design knowledge and evidence were produced? |

---

## 12. Design theory canvas (Gregor & Jones, 2007)

| Component | Content |
|---|---|
| 1. Purpose and scope | |
| 2. Constructs | |
| 3. Principles of form and function | |
| 4. Artifact mutability | |
| 5. Testable propositions | |
| 6. Justificatory knowledge | |
| 7. Principles of implementation (optional) | |
| 8. Expository instantiation (optional) | |

---

## 13. DSR review report

```markdown
# Review — [manuscript title]

## 1. Summary of the work
Problem, artifact, approach, evaluation, and claimed contribution, in 5–8 lines and in the reviewer's own words.

## 2. DSR framing
Is the work DSR? Does the declared process match the one followed?

## 3. Strengths

## 4. Assessment by dimension (R1–R10)
For each dimension: a short assessment and findings with locations.

## 5. Critical findings
[C1] Description — location — why it is critical — what would be needed

## 6. Major findings
[M1] ...

## 7. Minor findings
[m1] ...

## 8. DSR citation check
Incorrect attributions or inconsistent metadata.

## 9. Recommendation
Accept | Minor revision | Major revision | Reject — with a justification tied to the findings.

## 10. Constructive suggestions
Concrete, prioritized ways to strengthen the work.
```

---

## 14. Complete worked example (illustrative)

A fictitious example showing the full chain; numbers and results are illustrative. In real work,
every kernel theory cited needs a verified reference.

**Context.** Mid-sized security operations centers (SOCs) receive thousands of alerts per day;
analysts spend most of their shift on triage, and critical incidents get lost among false positives.

**Design problem.** Improve alert triage in mid-sized SOCs by means of an explainable prioritization
method and a tool implementing it, which reduces triage time without increasing missed critical
incidents, in order to help analysts and managers focus effort on relevant alerts.

**Class of problems.** Triage of large volumes of heterogeneous alerts by small teams, with humans
accountable for the final decision. Outside the class: fully automated response.

**Questions.**
- RQ: How should an alert prioritization method be designed to reduce triage effort without
  increasing missed critical incidents in mid-sized SOCs?
- KQ1: Which factors lead to missed critical incidents in current triage?
- KQ3: What is the method's effect on triage time and on recall of critical incidents compared with
  SIEM severity ordering?

**Requirements.**
| ID | Requirement | Source |
|---|---|---|
| R1 | Reduce mean triage time relative to the current process | Manager interviews; SOC metrics |
| R2 | Do not reduce recall of critical incidents | Interviews; SOC policy |
| R3 | Let analysts understand and challenge each priority | Interviews; literature on trust in automation |
| R4 | Integrate with the existing SIEM without replacing it | Organizational constraint |

**Design principles.**
- **DP1 — Contestable justification.** Provide the tool with a readable justification of the factors
  behind each priority, so that analysts can challenge incorrect priorities before acting, given that
  they remain accountable for the final decision under high load.
- **DP2 — Aggregated context.** Group correlated alerts on the same asset into a single triage item,
  so that analysts assess incidents rather than isolated events, given that attacks generate multiple
  related alerts.

**Evaluation strategy.** Human Risk & Effectiveness: the biggest risk is that analysts neither trust
nor use the prioritization.

| # | Timing | Purpose | Paradigm | Method | Comparator | Threshold |
|---|---|---|---|---|---|---|
| E1 | Ex ante | Formative | Artificial | Review of requirements and principles by 5 external experts | — | Criticisms incorporated |
| E2 | Ex post | Formative and summative | Artificial | Replay of 6 months of labeled alerts; ablation of DP2 | SIEM ordering | Recall ≥ baseline; lower estimated time |
| E3 | Ex post | Formative | Naturalistic | 2-week pilot with 4 analysts; logs and interviews | — | Usage problems identified and addressed |
| E4 | Ex post | Summative | Naturalistic | 8 weeks of use; before and after; interviews | Prior period | Lower time; no increase in missed critical incidents |

**Traceability (excerpt).**
| Problem | Requirement | Principle | Component | Criterion | Episode | Evidence |
|---|---|---|---|---|---|---|
| Critical incidents lost in noise | R2 | DP2 | Alert grouper | Efficacy (recall) | E2, E4 | Results tables |
| Distrust of automation | R3 | DP1 | Justification panel | Understandability; use | E3, E4 | Challenge logs; interviews |

**Contribution.** Improvement (a known, well-documented problem; a new solution in combining
explainable prioritization with per-asset aggregation), with a level 1 contribution (evaluated tool)
and a level 2 contribution (DP1 and DP2 with boundary conditions).

**Main threats.** Instantiation validity (effects due to the interface rather than the principles —
mitigated by the ablation in E2); designer-researcher bias (metrics extracted from logs and thresholds
fixed in advance); external validity (a single SOC — addressed through boundary conditions and a
mechanism-based explanation).
