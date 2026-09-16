# Evaluation in DSR

Evaluation is where DSR projects most often lose credibility. A good evaluation answers three
questions: **does the artifact produce the intended effect?** (efficacy), **does it produce that
effect in real situations?** (effectiveness), and **why does it produce it?** (mechanism). It answers
them with criteria derived from the requirements and fixed before looking at the results.

## Contents
1. Evaluation methods from Hevner et al. (2004)
2. Observed method types (Peffers et al., 2012)
3. Ex ante and ex post; artificial and naturalistic
4. FEDS (Venable et al., 2016)
5. EVAL1–EVAL4 (Sonnenberg & vom Brocke, 2012)
6. Hierarchy of criteria (Prat et al., 2015)
7. From requirement to criterion and metric
8. Evaluation by artifact type
9. Method cards
10. Threats to validity
11. Ethics
12. Evaluation plan checklist

---

## 1. Evaluation methods from Hevner et al. (2004)

| Category | Method | Description (paraphrase) |
|---|---|---|
| Observational | Case study | Study the artifact in depth in the business environment |
| | Field study | Monitor use of the artifact in multiple projects |
| Analytical | Static analysis | Examine the artifact's structure for static qualities (e.g., complexity) |
| | Architecture analysis | Study the artifact's fit into the technical architecture |
| | Optimization | Demonstrate optimal properties or provide optimality bounds on behavior |
| | Dynamic analysis | Study the artifact in use for dynamic qualities (e.g., performance) |
| Experimental | Controlled experiment | Study the artifact in a controlled environment (e.g., usability) |
| | Simulation | Execute the artifact with artificial data |
| Testing | Functional (black box) | Execute the artifact's interfaces to discover failures |
| | Structural (white box) | Coverage testing of some metric of the implementation |
| Descriptive | Informed argument | Use the knowledge base to build a convincing argument for utility |
| | Scenarios | Build detailed scenarios around the artifact to demonstrate utility |

The authors reserve descriptive methods for especially innovative artifacts, when other forms of
evaluation are not feasible. In theses, descriptive methods alone are usually considered weak.

---

## 2. Observed method types (Peffers et al., 2012)

Analyzing DSR papers, Peffers et al. (2012) identified recurring evaluation types: logical argument,
expert evaluation, technical experiment, subject-based experiment, action research, prototype,
illustrative scenario, and case study. These types are associated with artifact types — for example,
algorithms tend toward technical experiments, and models and methods toward scenarios, cases, or
experts. Use the list to check whether the chosen method is usual for the artifact type and, if not,
to justify it.

---

## 3. Ex ante and ex post; artificial and naturalistic

Pries-Heje et al. (2008) and Venable et al. (2012) organize evaluation along two distinctions:

**When:**
- **Ex ante** — before building or instantiating: evaluates the design, specification, or
  requirements. Cheap; reduces risk early; does not show real performance.
- **Ex post** — after instantiating: evaluates the built artifact.

**Where:**
- **Artificial** — some element is not real (users, system, or problem): lab experiments,
  simulations, criteria-based analysis, theoretical arguments, proofs. High control and
  reproducibility; low realism.
- **Naturalistic** — real people, real systems, real problems: case studies, field studies, action
  research, surveys. High realism; high cost, risk, and confounds too.

| | Artificial | Naturalistic |
|---|---|---|
| **Ex ante** | Criteria-based evaluation of the specification; proof on the model; expert review in a lab setting | Focus group with practitioners on the design; design assessment by the target organization |
| **Ex post** | Benchmark; simulation; controlled experiment with a prototype | Pilot deployment; case study; action research |

Illustrative examples, not an official classification.

---

## 4. FEDS — Framework for Evaluation in Design Science (Venable et al., 2016)

### Two dimensions
- **Functional purpose:** *formative* (produce improvements; evaluation during design) → *summative*
  (judge the outcome; assign meaning to effects).
- **Paradigm:** *artificial* → *naturalistic*.

Each evaluation **episode** is a point in this plane. The sequence of episodes forms the evaluation
**trajectory**.

### Goals the evaluation design balances
1. **Rigor** — show that the improvement is due to the artifact (*efficacy*) and that it works in
   real situations (*effectiveness*).
2. **Uncertainty and risk reduction** — human and social risks (will it be used? accepted?) and
   technical risks (will it work? scale?).
3. **Ethics** — risks to people, organizations, and society, including during evaluation.
4. **Efficiency** — balance the goals above against available resources.

### Four strategies
| Strategy | Trajectory | When to choose |
|---|---|---|
| **Quick & Simple** | Few episodes; moves early to summative naturalistic | Small, simple design; low social and technical risk |
| **Human Risk & Effectiveness** | Early formative artificial; soon formative naturalistic; ends in summative naturalistic | Main risk is social or user-oriented; goal is to show utility holds in real situations and over time |
| **Technical Risk & Efficacy** | Formative artificial; summative artificial; naturalistic only at the end | Main risk is technical; evaluating with real users is too costly; goal is to show rigorously that the benefit comes from the artifact |
| **Purely Technical** | Summative artificial | Artifact without human users, or real use planned only far in the future |

### Four steps
1. **Explicate the goals of the evaluation** (rigor, risk, ethics, efficiency) and their priorities.
2. **Choose the strategy** (or a combination) according to risks and goals.
3. **Determine the properties to evaluate** — derived from requirements, objectives, and
   propositions.
4. **Design the individual episodes** — considering constraints of time, money, and access to people
   and organizations; deciding how many episodes, when, with which method, and with which data.

### Application in computer science and security
Technical artifacts (protocols, algorithms, architectures) usually follow **Technical Risk &
Efficacy** or **Purely Technical**: formal analysis and benchmarks first, and a study with operators
or a pilot deployment at the end, if the artifact has users. If success depends on people adopting or
trusting the artifact (tools for analysts, privacy interfaces), human risk dominates and the strategy
changes.

Plan template in `templates.md` §8.

---

## 5. EVAL1–EVAL4 (Sonnenberg & vom Brocke, 2012)

They propose evaluating throughout the process, not only at the end, with four episode types tied to
design activities. The criteria and methods below are typical examples.

| Episode | Timing | What it validates | Typical criteria | Typical methods |
|---|---|---|---|---|
| **EVAL1** | Ex ante, after problem identification | Justified problem statement and research gap | Importance, novelty, feasibility | Literature review, expert interviews, focus groups |
| **EVAL2** | Ex ante, after design | Validated design specification | Clarity, completeness, consistency, feasibility | Experts, focus groups, logical argument |
| **EVAL3** | Ex post, after construction | Instantiation validated in an artificial setting | Feasibility, efficacy, efficiency, ease of use | Prototype demonstration, experiment, simulation, benchmark |
| **EVAL4** | Ex post, after use | Artifact validated in naturalistic use | Applicability, effectiveness, impact, fit with context | Case study, field experiment, survey, interviews |

Useful to show a committee that evaluation started before the prototype.

---

## 6. Hierarchy of criteria (Prat et al., 2015)

Criteria organized by the dimensions of a system. Use it as a catalog so relevant criteria are not
forgotten, not as a list to evaluate exhaustively.

| Dimension | Criteria |
|---|---|
| **Goal** | Efficacy; validity (the artifact works correctly and does what it should); generality |
| **Environment — people** | Utility; understandability; ease of use; ethicality; side effects |
| **Environment — organization** | Utility; fit with organization; side effects |
| **Environment — technology** | Harmonization with other technologies; feasibility; side effects |
| **Structure** | Completeness; simplicity; clarity; style; homomorphism (correspondence with another model; fidelity to the modeled phenomenon); level of detail; consistency |
| **Activity** | Completeness; consistency; accuracy; performance; efficiency |
| **Evolution** | Robustness; learning capability |

---

## 7. From requirement to criterion and metric

For each requirement, define **before** the evaluation:

| Element | Question | Example |
|---|---|---|
| Requirement | What must the artifact ensure? | R2 — do not increase missed critical incidents |
| Criterion | Which property observes it? | Efficacy (Prat: goal) |
| Question | What do we want to know? | Does prioritization miss more critical incidents than the current process? |
| Metric | How is it measured? | Recall of critical incidents in the top-k |
| Data source | Where do the data come from? | Six months of labeled historical data |
| Comparator | Against what? | SIEM severity ordering (baseline) |
| Success threshold | What counts as meeting it? | Recall ≥ baseline, with confidence interval reported |
| Episode | Where is it measured? | E2 — artificial, summative |

Fixing thresholds and comparators in advance prevents adjusting criteria to results after the fact —
one of the most serious criticisms of DSR evaluations. If something changed during the project,
report the change and the reason.

---

## 8. Evaluation by artifact type

Guiding synthesis; adapt to the case.

| Artifact | Core criteria | Usual methods | Notes |
|---|---|---|---|
| **Construct** (taxonomy, ontology, concepts) | Completeness, clarity, consistency, usefulness for classifying or communicating | Experts; application to real cases; comparison with existing schemes; inter-rater agreement | Show that someone can use the constructs, not only that they are well defined |
| **Model** (reference, maturity, process) | Fidelity, completeness, level of detail, understandability, utility | Experts, focus groups, case studies, scenarios | Maturity models need validation of the progression between levels |
| **Method** (process, procedure, technique) | Efficacy, efficiency, operationality, ease of use, generality | Case study, user experiment, technical action research, comparison with the current method | Evaluate both the method's outcome and its execution |
| **Algorithm** | Correctness, complexity, performance, accuracy, robustness | Formal analysis, benchmarks with baselines, tests on real and synthetic data, ablation | Current, strong baselines; variance and statistical significance |
| **Protocol or security mechanism** | Security properties under the threat model, cost, performance, deployability | Proofs or formal verification, security analysis, implementation and benchmarks, deployment study | State assumptions and what is outside the threat model |
| **Architecture or system** | Satisfaction of quality attributes, feasibility, scalability, integration | Quality scenarios, prototype, performance and load tests, case study | Show the trade-offs of architectural decisions |
| **Tool or interface** | Task efficacy, efficiency, usability, acceptance | User experiment, usability tests, field study with logs | Combine task performance with perception |
| **Design principles** | Predicted effects, reuse, understandability, generality | Instantiation and evaluation; ablation; experts; multiple contexts | Check instantiation validity |
| **Design theory** | Confirmed testable propositions, explanatory power, scope | Multiple studies; varied instantiations | Cumulative evidence |

---

## 9. Method cards

### A. Informed argument and logical analysis
- **When:** ex ante; highly novel artifacts; as a complement to other methods.
- **Design:** explicit premises; argument tied to the knowledge base; consider counterarguments.
- **Pitfall:** using it as the only evaluation in a thesis or empirical paper.

### B. Formal proofs and verification
- **When:** protocols, algorithms, security mechanisms, critical systems.
- **Design:** define the model (threat, faults, assumptions) first; state what the proof covers and
  what it does not; for automated verification, make models and scripts available.
- **Report:** theorem or property, assumptions, proof sketch or tool, limits.

### C. Illustrative scenarios
- **When:** showing applicability to varied situations; complementing quantitative evaluation.
- **Design:** realistic scenarios, preferably based on real cases; include hard scenarios or ones
  where the artifact fails.
- **Pitfall:** scenarios chosen to favor the artifact.

### D. Expert evaluation
- **When:** ex ante (requirements, design) and ex post (models, methods, principles).
- **Selection:** explicit expertise criteria (years, role, domain); diversity of perspectives;
  independence from the researcher whenever possible.
- **Instrument:** questions tied to the criteria; rating scales accompanied by qualitative
  justifications; protocol published in an appendix.
- **Size:** there is no magic number. Justify by saturation of responses or by design (e.g., Delphi
  rounds until consensus).
- **Report:** expert profiles, instrument, analysis, disagreements, and what changed in the artifact.

### E. Focus groups (Tremblay et al., 2010)
- **Exploratory focus groups:** formative; incremental improvements to the design.
- **Confirmatory focus groups:** summative; demonstrate the artifact's utility in real use.
- **Design:** a moderator who does not advocate for the artifact; a script; recording and systematic
  analysis; report what changed between rounds.

### F. Technical experiments and benchmarks
- **When:** algorithms, systems, protocols, pipelines.
- **Design:**
  - strong, current baselines with a fair setup (same hardware, equivalent tuning);
  - workloads and data representative of the class of problems, real when possible;
  - repetitions, variance, confidence intervals, and appropriate statistical tests;
  - **ablation** to link each design decision or principle to its effect — very strong evidence in
    DSR, because it shows *why* the artifact works;
  - artifact, data, and scripts available for reproduction.
- **Pitfall:** comparing only against a previous version of one's own artifact.

### G. Simulation
- **When:** environments that are expensive, dangerous, or do not yet exist; scale.
- **Design:** validate the simulator or model; sensitivity analysis of parameters; discuss the gap
  between simulation and reality.

### H. User experiments
- **When:** the artifact's effect on people's performance or behavior.
- **Design:** hypotheses and measures defined in advance; control condition (no artifact or an
  alternative); between- or within-subjects design with counterbalancing; realistic tasks; sample
  size calculation or justification; manipulation checks.
- **Pitfalls:** labmates as participants; participants who know which condition is "the
  researcher's."

### I. Case study and field study
- **When:** naturalistic evaluation; effectiveness and fit with context.
- **Design:** case protocol; multiple sources of evidence (logs, interviews, documents, metrics);
  criteria defined in advance; report problems and unexpected uses.
- **Report:** rich context description (so readers can judge transferability), period, participants,
  data, analysis.

### J. Technical action research and ADR
- **When:** the artifact is used to solve a real client's problem, with the researcher involved.
- **Design:** separate the roles of designer, researcher, and helper (Wieringa & Moralı, 2012);
  intervention log; agreement with the organization; explicit reflection on bias.

### K. Perception questionnaires
- **When:** acceptance, usability, and perceived usefulness, as a complement.
- **Design:** instruments validated in the version and language used; report the full instrument; do
  not treat perception as proof of efficacy.
- **Pitfall:** an "evaluation" consisting only of a questionnaire given to a few people close to the
  researcher.

### L. Cost, feasibility, and adoption
- **When:** organizational artifacts; practical value arguments.
- **Design:** explicit cost assumptions; sensitivity analysis; include deployment and maintenance
  costs.

---

## 10. Threats to validity

| Type | Typical threat in DSR | Mitigations |
|---|---|---|
| **Instantiation** | The instance does not faithfully embody the principles; effects come from incidental details | Map principle → feature; multiple instantiations; ablation; hold incidental aspects constant |
| **Construct** | The metric does not measure the requirement (e.g., satisfaction instead of efficacy) | Derive metrics from requirements; multiple metrics; validated instruments |
| **Internal** | Researcher designs and evaluates; novelty effect; participants want to please; learning across tasks | Independent evaluators; thresholds set in advance; blinding; counterbalancing; control condition |
| **External** | Context, participants, or data do not represent the class of problems | State boundary conditions; varied contexts; rich description of context |
| **Conclusion** | Small sample; inappropriate tests; many comparisons; variance ignored in benchmarks | Statistical power; corrections for multiple comparisons; repetitions; effect sizes |
| **Ecological** | Artificial setting far from real use | FEDS trajectory toward naturalistic; discuss the gap |
| **Reproducibility** | Artifact, data, or configuration unavailable | Versioned repository; data or equivalent synthetic data; environment description |

Report the threats that actually apply, with the mitigation adopted and the residual risk. A generic
list unconnected to the study reads as a formality.

---

## 11. Ethics

### Ethical principles for DSR (Myers & Venable, 2014)
1. **Public interest** — consider whether the artifact and its use benefit or harm stakeholders and
   society.
2. **Informed consent** — from those who take part in design and evaluation.
3. **Privacy** — protection of personal data used or collected.
4. **Honesty and accuracy** — report results, limitations, and authorship correctly.
5. **Property** — rights over the artifact and intellectual property, agreed with the parties.
6. **Quality of the artifact** — care that the artifact does not cause harm through defects.

### Approvals and data protection
- Research with human participants: approval by the relevant ethics board (IRB, REC). In Brazil:
  Research Ethics Committee (CEP) via Plataforma Brasil, under CNS Resolutions No. 466/2012 and
  No. 510/2016 (the latter for human and social sciences). Check with the institution's board which
  evaluation steps require review.
- Personal data: the applicable law (e.g., GDPR in the EU, LGPD — Law No. 13,709/2018 — in Brazil):
  legal basis, minimization, anonymization.

### Security and dual use
- Test only systems with explicit authorization.
- Responsible disclosure of vulnerabilities found.
- Discussion of misuse risks of the artifact and their mitigations.

---

## 12. Evaluation plan checklist

- [ ] Evaluation goals explicit and prioritized (rigor, risk, ethics, efficiency)
- [ ] Strategy chosen and justified by the project's risks
- [ ] Each requirement linked to a criterion, metric, comparator, and threshold defined in advance
- [ ] Episodes spread across the project (formative and summative)
- [ ] At least one summative episode appropriate to the artifact type and to the claims made
- [ ] Relevant, current baseline or comparator
- [ ] Participants, data, and contexts described and justified
- [ ] Bias of whoever designs and evaluates mitigated
- [ ] Specific threats to validity and mitigations
- [ ] Ethics approval and data protection where applicable
- [ ] Artifact, instruments, and data available for reproduction where possible
- [ ] Negative results and artifact changes recorded in the iteration log
