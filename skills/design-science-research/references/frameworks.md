# DSR processes and frameworks

Content paraphrased from the original sources. When writing academic text, cite the primary source
(see `bibliography.md`) and make any adaptation explicit.

## Contents
1. Foundations: sciences of the artificial and the design paradigm
2. Hevner et al. (2004): seven guidelines
3. Hevner (2007): three cycles; Drechsler & Hevner (2016): fourth cycle
4. Peffers et al. (2007): Design Science Research Methodology (DSRM)
5. Vaishnavi & Kuechler: general design cycle
6. Wieringa (2014): design cycle and engineering cycle
7. Action Design Research (Sein et al., 2011) and eADR (Mullarkey & Hevner, 2019)
8. Dresch, Lacerda & Antunes Jr. (2015)
9. Two DSR strategies (Iivari, 2015)
10. DSR in software engineering and computer science
11. How to choose and combine
12. Crosswalk table

---

## 1. Foundations

**Sciences of the artificial (Simon, 1996).** Natural sciences describe how things are; sciences of
the artificial deal with how things ought to be in order to attain goals. Designing is devising
courses of action that turn existing situations into preferred ones. An artifact is the interface
between an *inner environment* (its substance and organization) and an *outer environment* (the
surroundings in which it operates). For complex problems, one seeks a satisfactory solution
(*satisficing*), not necessarily an optimal one.

**Complementary paradigms (Hevner et al., 2004).** Behavioral science seeks truth: developing and
justifying theories that explain or predict phenomena. DSR seeks utility: building and evaluating
artifacts. The two feed each other: theories inform design, and artifacts in use create phenomena
to explain.

**Outputs and activities (March & Smith, 1995).** Four output types (constructs, models, methods,
instantiations) crossed with four activities (build, evaluate, theorize, justify). The first two
activities are typical of design science; the last two, of natural science. Details in
`contributions-and-theory.md` §1.

**Precursor in IS.** Nunamaker et al. (1990) argued for systems development as a research
methodology, anticipating many elements of DSR.

**Principles from the German memorandum (Österle et al., 2011).** Design-oriented research should
meet four principles: *abstraction* (applicable to a class of problems), *originality* (adds to the
body of knowledge), *justification* (can be validated in a comprehensible way), and *benefit*
(creates value for stakeholders, now or in the future).

**Epistemological stance.** DSR is commonly associated with pragmatism: valid knowledge is what
works to solve problems, and one learns by building and evaluating. State the stance in the
methodology only if the audience expects it (common in theses and in IS).

**Terminology.** Avoid using interchangeably *design science* (the paradigm and body of knowledge),
*design science research* (the research activity), and *design research* (which in some fields
means research about the design process). Dresch et al. (2015) explicitly distinguish design science
(the epistemological basis) from design science research (the method that operationalizes it).

---

## 2. Hevner et al. (2004): seven guidelines

The authors present the guidelines as support for the judgment of researchers, reviewers, and
editors, not as a mandatory checklist. Use them to *examine* a project, not to *declare*
compliance.

| # | Guideline | What it asks (paraphrase) | What to evidence | Typical failure |
|---|---|---|---|---|
| 1 | Design as an artifact | Produce a viable artifact: construct, model, method, or instantiation | Reproducible description; artifact actually built | Idea or sketch presented as an artifact |
| 2 | Problem relevance | Solutions to important and relevant problems | Stakeholders; data; cost of the problem; gap in current solutions | Problem invented to fit the solution |
| 3 | Design evaluation | Utility, quality, and efficacy demonstrated with well-executed methods | Strategy, criteria, metrics, baseline, results | Anecdotal evidence or demonstration only |
| 4 | Research contributions | Clear, verifiable contributions in the artifact, design foundations, or design methodologies | Contribution statement compared with the state of the art | "Contribution" = having built something |
| 5 | Research rigor | Rigorous methods in both construction and evaluation | Grounding in the knowledge base; appropriate evaluation methods | Rigor only in evaluation, arbitrary design |
| 6 | Design as a search process | Use available means to reach desired ends while satisfying laws of the environment | Alternatives, iterations, heuristics, trade-offs | Solution presented as obvious and unique |
| 7 | Communication of research | Present to technology-oriented and management-oriented audiences | Enough technical detail and practical implications | Text only technical or only managerial |

The evaluation methods proposed in the same paper are in `evaluation.md` §1.

---

## 3. Three cycles (Hevner, 2007) and a fourth cycle (Drechsler & Hevner, 2016)

**Relevance cycle.** Connects the application environment (people, organizational systems,
technical systems, problems and opportunities) to the research. Brings in requirements and
acceptance criteria; takes the artifact back into the environment for field testing. If field
testing reveals deficiencies, a new iteration begins.

**Rigor cycle.** Connects the research to the knowledge base. Brings in scientific theories and
methods, domain experience and expertise, and existing design artifacts and processes. Returns
extensions to theories and methods, new meta-artifacts (design products and processes), and
experience. Hevner stresses that the researcher must show the artifact is genuinely new, not a
routine application of known knowledge.

**Design cycle.** The core: rapid iteration between building and evaluating alternatives until a
satisfactory design is reached. Effort should be balanced between construction and evaluation; both
must be grounded in the other two cycles.

**How to use it in writing.** A table showing what each cycle brought into the project and what the
project gave back is a compact way to demonstrate relevance and rigor:

| Cycle | Inputs to the project | Outputs of the project |
|---|---|---|
| Relevance | Problem, stakeholders, requirements, acceptance criteria | Field-tested artifact; evidence of utility |
| Rigor | Kernel theories, methods, prior artifacts | Design principles, theory extensions, new methods |
| Design | Alternatives, prototypes, formative evaluations | Final artifact; iteration history |

**Fourth cycle — change and impact (Drechsler & Hevner, 2016).** Adds a cycle connecting the
immediate application context to a broader, dynamic environment. It captures the need for the
artifact to evolve as the environment changes, and the effects the artifact itself produces in the
organization, which trigger further design efforts. Useful for platforms, long-lived systems,
ecosystems, and volatile environments.

---

## 4. DSRM (Peffers et al., 2007)

A nominal process of six activities, with iterative loops from evaluation and communication back
to defining objectives and to design.

### Activity 1 — Problem identification and motivation
Define the specific research problem and justify the value of a solution. Breaking the problem down
conceptually helps the solution capture its complexity. Resources: knowledge of the state of the
problem and the importance of its solution.
**In a thesis:** introduction chapter and, if present, an exploratory study of the problem.

### Activity 2 — Define the objectives for a solution
Infer objectives from the problem definition and from knowledge of what is possible and feasible.
Objectives can be **quantitative** (in what terms the new solution would be better than current
ones) or **qualitative** (how the artifact will support solutions to problems not yet addressed).
Resources: knowledge of current solutions and their efficacy.
**In a thesis:** requirements and design objectives, with traceable sources.

### Activity 3 — Design and development
Create the artifact: determine its desired functionality and architecture, then build it.
Resources: theory that can be brought to bear on the solution.
**In a thesis:** the artifact chapter, with design decisions and their grounding.

### Activity 4 — Demonstration
Show the use of the artifact to solve one or more instances of the problem — through
experimentation, simulation, case study, proof, or another appropriate activity. Resources:
knowledge of how to use the artifact.

### Activity 5 — Evaluation
Observe and measure how well the artifact supports a solution, comparing objectives with observed
results. This may include comparing functionality with objectives, quantitative performance
measures, satisfaction surveys, client feedback, or simulations. At the end, decide whether to
iterate back to activity 2 or 3 or to move on to communication.

### Activity 6 — Communication
Communicate the problem and its importance, the artifact, its utility and novelty, the rigor of its
design, and its effectiveness to researchers and other relevant audiences, such as practitioners.
The authors suggest that the process structure can organize scholarly papers, just as the nominal
empirical process structures empirical papers.

### Entry points
| Entry point | Starts at | Typical situation |
|---|---|---|
| Problem-centered initiation | Activity 1 | Problem observed or suggested by prior research |
| Objective-centered solution | Activity 2 | Industry or research need that an artifact could address |
| Design and development-centered initiation | Activity 3 | Existing artifact not yet formally thought through as a solution for a problem domain |
| Client/context-initiated | Activity 4 | A practical solution that worked; researchers work backward to apply rigor |

When using an entry point other than activity 1, say so explicitly in the methodology. It is more
defensible than narrating a linear process that did not happen.

---

## 5. General design cycle (Vaishnavi & Kuechler)

Derived from design process models in engineering and adopted by Kuechler & Vaishnavi (2008) and
Vaishnavi & Kuechler (2015).

| Phase | Output |
|---|---|
| Awareness of problem | Proposal |
| Suggestion | Tentative design |
| Development | Artifact |
| Evaluation | Performance measures |
| Conclusion | Results |

**Knowledge flows.** When development or evaluation shows that the artifact does not behave as
expected, *circumscription* knowledge is generated: the constraints and limits of the theory become
better understood, and the cycle returns to awareness of the problem. *Operation and goal
knowledge* is also produced along the cycle.

**Emphasis.** This model highlights DSR as a generator and refiner of theory: Kuechler & Vaishnavi
(2008) show how a design project can extend a kernel theory, and Kuechler & Vaishnavi (2012) discuss
design theories and explanatory theories relevant to design. The conclusion phase also records
"loose ends" — unexplained behaviors that become a research agenda.

---

## 6. Wieringa (2014)

**Object.** Design science is the design and investigation of artifacts *in context*. An artifact
alone solves nothing; what produces effects is the artifact × context interaction (the
*treatment*).

**Two kinds of problems — keep them separate.**
- **Design problems** call for a change in the world; they have many possible solutions, evaluated
  by their utility for stakeholder goals.
- **Knowledge questions** ask for knowledge about the world; they have one answer (possibly
  uncertain), evaluated by truth.
A DSR project is a hierarchy of nested design problems and knowledge questions. Merging them into a
single "research question" creates confusion about what counts as an answer.

**Design problem template (paraphrase):**
> Improve <problem context>
> by <(re)designing an artifact>
> that satisfies <requirements>
> in order to <help stakeholders achieve goals>.

**Design cycle.**
1. *Problem investigation*: stakeholders, goals, phenomena, causes, mechanisms, effects; evaluation
   of the current situation.
2. *Treatment design*: specify requirements, examine available treatments, design new ones.
3. *Treatment validation*: predict the effects of the artifact in context before real-world
   implementation. Typical questions:
   - effect: artifact × context → what effects? Do they satisfy the requirements?
   - trade-off: alternative artifacts × context → effects?
   - sensitivity: artifact × alternative contexts → effects?

**Engineering cycle.** The design cycle plus *treatment implementation* (transfer to the real world)
and *implementation evaluation* (which works as a new problem investigation). Academic DSR usually
goes as far as validation; real implementation is often out of scope.

**Validation methods.**
| Method | Description | When to use |
|---|---|---|
| Expert opinion | Experts predict the artifact's effects in context | Early; cheap; does not replace testing |
| Single-case mechanism experiment | Prototype tested in a simulated context; behavior explained by mechanisms | Technical artifacts; software engineering |
| Technical action research (TAR) | Researcher uses the artifact to help a real client and learns from it | Transition from lab to practice |
| Statistical difference-making experiment | Groups with and without the treatment compared statistically | When sample size and control are sufficient |

In TAR (Wieringa & Moralı, 2012), the researcher holds several roles — designer of the artifact,
empirical researcher answering knowledge questions, and helper of the client — and must keep them
consciously separate.

**Generalization.** By analogy, based on architectural similarity between cases (same components and
mechanisms), and by gradually widening conditions: from the lab to increasingly realistic conditions
(*scaling up*).

**Terminology warning.** In Wieringa, *validation* happens before implementation and *evaluation*
concerns the real implementation. In Peffers et al. (2007), *evaluation* covers both. Define the
terms in the text.

---

## 7. Action Design Research

### ADR (Sein et al., 2011)
**Motivation.** IT artifacts are shaped by their organizational context during development and use.
Separating "build" and "evaluate" into watertight stages ignores this; ADR interweaves building,
intervention, and evaluation.

| Stage | Principles |
|---|---|
| 1. Problem formulation | P1 Practice-inspired research — field problems as knowledge-creation opportunities; P2 Theory-ingrained artifact — theories inform the artifact |
| 2. Building, intervention, and evaluation (BIE) | P3 Reciprocal shaping — artifact and organizational context shape each other; P4 Mutually influential roles — researchers and practitioners learn from each other; P5 Authentic and concurrent evaluation — ongoing evaluation, not a final stage |
| 3. Reflection and learning | P6 Guided emergence — the artifact reflects the initial design and its continuous shaping by use and evaluation |
| 4. Formalization of learning | P7 Generalized outcomes — generalize the problem instance to a class of problems and the solution instance to a class of solutions, and derive design principles |

**Stage 1 involves:** framing the research opportunity, formulating initial questions, casting the
problem as an instance of a class, identifying theoretical bases and prior technology advances,
securing long-term organizational commitment, and setting up roles.

**BIE schemas.**
- *IT-dominant*: technological innovation; alpha version with evaluation in a limited context, beta
  version in wider organizational use.
- *Organization-dominant*: innovation mainly in the organizational intervention.

**When to use.** The researcher has access to and an active role in an organization, the artifact
only makes sense in use, and practitioners take part in design. **When to avoid.** Purely technical
artifacts evaluated in the lab; there, ADR becomes a label.

**Cautions.** Document interventions (who decided what, when, and on what basis), manage the bias of
being both designer and evaluator, and record changes in the context.

### eADR (Mullarkey & Hevner, 2019)
Elaborates ADR into four stages — **diagnosis, design, implementation, and evolution** — each running
its own ADR cycle (problem formulation and planning, artifact creation, evaluation, reflection and
learning). It allows entering the process at any stage and recognizes that each stage can produce
its own artifacts and contributions, for example problem-diagnosis artifacts.

---

## 8. Dresch, Lacerda & Antunes Jr. (2015)

Widely used in Brazil, especially in production engineering and management (a Portuguese edition was
published by Bookman in 2015; see also Lacerda et al., 2013).

**Method steps:**
1. Problem identification
2. Problem awareness
3. Systematic literature review
4. Identification of artifacts and configuration of classes of problems
5. Proposal of artifacts to solve the specific problem
6. Design of the selected artifact
7. Development of the artifact
8. Evaluation of the artifact
9. Explicitation of learnings
10. Conclusions
11. Generalization to a class of problems
12. Communication of results

**Core concepts.**
- **Class of problems:** an organization of a set of problems, practical or theoretical, that
  contains artifacts useful for action. Configuring it early (step 4) guides the literature review
  and the generalization (step 11).
- The systematic review appears as an explicit step, reinforcing the rigor cycle.
- Learnings and generalization are steps in their own right, not appendices to the evaluation.

**When to use.** Committees in production engineering, management, and related fields that know the
method; projects that need a formal systematic review. It can be combined with FEDS to detail the
evaluation.

---

## 9. Two DSR strategies (Iivari, 2015)

| | Strategy 1 | Strategy 2 |
|---|---|---|
| Starting point | General solution concept (meta-artifact) for a class of problems | A specific client problem |
| Movement | From general to instances: build the meta-artifact, instantiate, and evaluate | From specific to general: build a concrete artifact in context, then distill prescriptive knowledge |
| Closest to | "Classic" lab and field DSR | ADR and action research |
| Generalization challenge | Show that it works in varied real contexts | Show that the learning holds beyond the client |

Declaring the strategy helps justify the evaluation design and the generality claims.

---

## 10. DSR in software engineering and computer science

**Problem–solution pair and technological rule.** Runeson et al. (2020) and Engström et al. (2020)
frame software engineering research as DSR: a problem instance and a solution instance, linked by
three activities — problem conceptualization, solution design, and empirical validation — and a
**technological rule** as the generalizable contribution:
> To achieve <effect> in <situation>, apply <intervention>.

**Visual abstract (Storey et al., 2017).** A one-page summary with the technological rule, the three
activities, and an assessment of the study through three lenses: **relevance** (does the rule matter
to practitioners?), **rigor** (does the validation support the rule?), and **novelty** (is the rule
new?). Engström et al. (2020) used these lenses to analyze software engineering papers.

**Computer science and security.** Systems, networking, and security papers often follow the DSR
logic without the name: motivation and threat model (problem), design goals (requirements),
architecture and protocol (artifact), security analysis or proofs (analytical evaluation),
implementation (instantiation), benchmarks against baselines (experimental evaluation). See
`writing-and-reviewing.md` §5 for the section mapping.

---

## 11. How to choose and combine

| Situation | Recommended process | Why |
|---|---|---|
| IT/IS artifact, Information Systems audience | DSRM + three cycles | Most recognized; clear activities; cycles make rigor and relevance explicit |
| Artifact built inside an organization with researcher intervention | ADR or eADR | Interweaves building, intervention, and evaluation in a real context |
| Software or systems engineering; focus on validating before deployment | Wieringa | Separates design problems from knowledge questions; detailed validation methods |
| Emphasis on building or refining design theory | Vaishnavi & Kuechler | Circumscription and conclusion make theoretical learning explicit |
| Production engineering or management in Brazil | Dresch et al. | Familiar to committees; explicit class of problems and systematic review |
| Computer science or security venues that do not use "DSR" | Wieringa or problem–solution pair with a technological rule, in the field's vocabulary | DSR rigor without jargon foreign to the community |
| Long-lived artifact in a volatile environment | Three cycles + change and impact cycle | Captures evolution and effects of the artifact |

**A frequent coherent stack:** DSRM for the process, the three cycles for relevance and rigor, FEDS
for the evaluation, and the Gregor & Hevner framework for the contribution. Each framework plays a
distinct role.

**Avoid "framework salad":** citing five models without saying what role each plays in the project.
For every framework cited, the methodology should say *what it organizes* and *where that shows up*
in the work.

**Adaptations** are legitimate when declared and justified (e.g., "the demonstration activity was
merged into the first evaluation episode because…").

---

## 12. Crosswalk table

Approximate correspondence; the models are not isomorphic.

| DSRM (Peffers) | Cycles (Hevner) | Vaishnavi & Kuechler | Wieringa | ADR (Sein et al.) | Dresch et al. |
|---|---|---|---|---|---|
| 1 Problem and motivation | Relevance | Awareness of problem | Problem investigation | Stage 1 (P1) | 1–3 |
| 2 Objectives of a solution | Relevance (requirements) and rigor | Suggestion | Treatment design (requirements) | Stage 1 (P2) | 4–5 |
| 3 Design and development | Design and rigor | Development | Treatment design | Stage 2 (P3, P4) | 6–7 |
| 4 Demonstration | Design | Development / evaluation | Treatment validation | Stage 2 | 7–8 |
| 5 Evaluation | Design (internal) and relevance (field) | Evaluation | Validation; implementation evaluation | Stage 2 (P5) | 8 |
| Iterative loops | Rigor (additions to the knowledge base) | Circumscription; conclusion | New cycle | Stage 3 (P6) | 9–11 |
| 6 Communication | Rigor | Conclusion | — | Stage 4 (P7) | 12 |
