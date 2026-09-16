# Writing, publishing, and reviewing DSR

## Contents
1. Publication schema (Gregor & Hevner, 2013)
2. Thesis, dissertation, and proposal structure
3. Research questions, objectives, and the Hevner & Chatterjee checklist
4. Title, abstract, and introduction
5. Venues and vocabulary by community
6. One-page summaries: DSR Grid and visual abstract
7. Review rubric for DSR manuscripts
8. Misattributions and frequent citation errors
9. Frequent reviewer criticisms and how to respond

---

## 1. Publication schema (Gregor & Hevner, 2013)

| Section | Expected content | Tips |
|---|---|---|
| **1. Introduction** | Problem and relevance; research question or objective; DSR approach; summary of contributions; outline | Name the artifact and the type of contribution early; readers should not reach section 4 without knowing what was built |
| **2. Literature review** | Knowledge about the problem (Ω); existing solutions and their limitations (Λ); kernel theories; gap | End with comparison criteria that reappear in the evaluation |
| **3. Method** | Why DSR; process and adaptations; iterations; evaluation strategy; data and participants; ethics | Justify choices; include a figure or table of the process actually followed |
| **4. Artifact description** | Requirements; architecture or structure; design decisions and grounding; alternatives; principles; search process | Enough detail to rebuild it; lengthy material in an appendix or repository |
| **5. Evaluation** | Episodes, methods, criteria, results, threats to validity | Organize by requirement or by episode, but keep the requirement → result link |
| **6. Discussion** | Interpretation; contribution to knowledge (quadrant, level, principles); implications for research and practice; generalization; limitations | This is where the artifact becomes knowledge |
| **7. Conclusions** | Answers to the questions; contributions; future work | No new results |

The order is flexible: in projects with several iterations, artifact description and evaluation can
alternate by cycle.

---

## 2. Thesis, dissertation, and proposal structure

### Option A — Traditional monograph
1. **Introduction** — context, problem, motivation, questions, objectives, contributions, outline.
2. **Theoretical background** — concepts and kernel theories (Ω).
3. **Related work** — state of the art of solutions (Λ), with a comparison table using criteria that
   will return in the evaluation.
4. **Methodology** — DSR and its justification; process and adaptations; map of *process steps ×
   chapters*; evaluation strategy; protocol; ethics; overview of iterations.
5. **Problem investigation and requirements** — when there is a dedicated study of the problem.
6. **Artifact** — design, decisions, alternatives, principles.
7. **Evaluation** — episodes and results.
8. **Discussion** — contributions (quadrant, levels), design principles, generalization,
   implications, limitations.
9. **Conclusion** — answers to the questions and future work.

### Option B — By iteration
After the methodology, one chapter per design cycle (problem refinement → design → evaluation →
learnings → changes), followed by a consolidated discussion. It shows the search process and the
artifact's evolution naturally; it takes discipline to avoid repetition.

### Option C — Thesis by publication
- An integrative introductory chapter presenting the complete DSR arc.
- A table positioning each paper: process activity, cycle, evaluation episode, contribution.
- Linking text between papers explaining what each one changed in the artifact.
- An integrated discussion of the overall contribution, which is not the sum of the papers.
- Papers published in computer science venues may not use DSR vocabulary; the integrative chapter
  translates.

### Proposal or qualifying exam
The committee expects: evidence of the problem; preliminary requirements with sources; an initial
design or prototype; an evaluation plan with strategy and episodes; a schedule by iteration; risks
and alternatives; ethical aspects. A DSR protocol (`templates.md` §1) covers these items.

---

## 3. Research questions, objectives, and checklist

### Main question (design problem)
- "How should [artifact or class of artifacts] be designed to [objective] in [context or class of
  contexts]?"
- "Which design principles guide [class of artifacts] to achieve [objective] in [class of
  contexts]?"

### Sub-questions (knowledge questions, following Wieringa, 2014)
| Purpose | Template |
|---|---|
| Problem investigation | "What are the causes and effects of [problem] in [context]?" |
| Requirements | "Which requirements must a [artifact] satisfy to [objective] according to [stakeholders or literature]?" |
| Effect | "What is the effect of [artifact] on [criterion] compared with [baseline] in [context]?" |
| Trade-off | "How do [design alternatives] compare on [criteria]?" |
| Sensitivity | "How does the effect of [artifact] vary with [context characteristic]?" |

Separate the design question (answer: an artifact) explicitly from the knowledge questions (answer:
facts or explanations).

### Objectives
- **General:** "Design and evaluate [artifact] to [objective] in [context]."
- **Specific**, phrased as outcomes and aligned with the process activities: "characterize
  [problem] in [context]"; "define requirements for [artifact]"; "design and instantiate
  [artifact]"; "evaluate [artifact] with respect to [criteria]"; "derive design principles for
  [class]".
- Avoid objectives that are tasks ("conduct a literature review," "study the topic").

### DSR checklist (Hevner & Chatterjee, 2010)
Use as a self-check for a proposal or manuscript:
1. What is the research question (design requirements)?
2. What is the artifact, and how is it represented?
3. What design processes (search heuristics) will be used to build it?
4. How are the artifact and design processes grounded in the knowledge base? Which theories support
   them?
5. What evaluations are performed during the internal design cycles, and what improvements do they
   produce?
6. How is the artifact introduced into the application environment and field-tested? What metrics
   show its utility and its improvement over previous artifacts?
7. What new knowledge is added to the knowledge base, and in what form?
8. Has the research question been satisfactorily addressed?

---

## 4. Title, abstract, and introduction

### Titles
- "[Artifact name]: A [artifact type] for [objective] in [context]"
- "Designing [class of artifact] for [objective]: Design principles and evaluation in [context]"
Avoid titles that name only the technology ("An X-based solution").

### Structured abstract
1. Context and problem (1–2 sentences, with a relevance figure if possible)
2. Gap in current solutions
3. Objective
4. Method: DSR, process, number of iterations
5. Artifact: what it is, in one sentence
6. Evaluation: strategy, methods, participants or data
7. Main results, with numbers
8. Contribution: design knowledge and implications

### Introduction moves
1. Why the problem matters (evidence).
2. What has been tried and why it is not enough.
3. What this work does (artifact and approach).
4. How it was evaluated and what was found.
5. A list of specific, verifiable contributions.
6. Outline.

---

## 5. Venues and vocabulary by community

Expectations vary a lot across communities. Always check the current calls and norms of the target
venue.

| Community | Example venues | Expectations |
|---|---|---|
| Information Systems | MIS Quarterly, ISR, JMIS, JAIS, EJIS, BISE; DESRIST, ICIS, ECIS, PACIS, AMCIS, HICSS | Explicit DSR vocabulary; abstraction (principles or theory); contribution discussion; canonical frameworks cited |
| Software engineering | ICSE, FSE, ESEM; EMSE, IST, JSS, TSE | Technological rules; rigorous empirical validation; threats to validity; available artifacts. The ACM SIGSOFT Empirical Standards include a standard for engineering (design science) research — check the current version |
| Computer science, systems, networking, security | The field's conferences and journals | Rarely use "DSR"; expect a threat or system model, design goals, analysis, implementation, and strong experimental evaluation against the state of the art |
| Management and production engineering | Operations and management journals; in Brazil, e.g., Gestão & Produção | Technological rules, CIMO, Dresch et al.; managerial relevance |
| Brazil — IS | SBSI; iSys — Brazilian Journal of Information Systems | DSR vocabulary well accepted; applied contributions |

### DSR in computer science and security papers
Keep the logic and switch the vocabulary:

| DSR element | Typical section | How to write it |
|---|---|---|
| Problem and relevance | Introduction, motivation | Concrete scenario, cost or impact, limitations of the state of the art |
| Knowledge base (Ω) | Background | Concepts and assumptions needed |
| Requirements | Threat or system model; design goals; non-goals | Numbered goals, referenced later in the evaluation |
| Artifact and decisions | Design or architecture; protocol | Each decision linked to a goal; alternatives in "design alternatives" or the discussion |
| Analytical evaluation | Security analysis; proofs | Properties under the threat model |
| Instantiation | Implementation | Enough detail for reproduction; code available |
| Empirical evaluation | Evaluation | Explicit evaluation questions; baselines; ablation |
| Design knowledge | Discussion, lessons learned | Generalizable lessons and the conditions under which they hold |
| State of the art of solutions (Λ) | Related work | Comparison along dimensions, not a list of papers |
| Limitations | Limitations, discussion | Assumptions, threats, out of scope |

In a thesis, the methodology chapter can make DSR explicit and map the papers onto the process, even
if the papers themselves do not use the term.

---

## 6. One-page summaries

### DSR Grid (vom Brocke & Maedche, 2019)
Six dimensions to plan and communicate a project on one page: **problem**, **input knowledge**,
**research process**, **key concepts**, **solution**, and **output knowledge**. Useful in proposals,
qualifying exams, posters, and for aligning with a supervisor. Template in `templates.md` §11.

### Visual abstract (Storey et al., 2017)
For software engineering: the technological rule at the center; the problem instance, problem
conceptualization, solution design, and empirical validation around it; and an assessment through
three lenses — relevance, rigor, and novelty.

---

## 7. Review rubric for DSR manuscripts

If a general peer-review rubric is also in use, this one complements it with DSR-specific
dimensions. For each dimension, record findings with location (section, figure, table) and severity.

**Severity:**
- **Critical** — undermines the existence of the contribution or the validity of the main
  conclusions (e.g., no evaluation, no novelty, claims without evidence).
- **Major** — significantly weakens the work but is fixable (weak baseline, requirements without
  sources, missing threats to validity).
- **Minor** — clarity, terminology, presentation.

| # | Dimension | Guiding questions |
|---|---|---|
| R1 | **Framing** | Is the question prescriptive? Is DSR the appropriate approach, and is that justified? Is the declared process the one followed? |
| R2 | **Problem and relevance** | Is there evidence of the problem? Are stakeholders identified? Is the class of problems defined? |
| R3 | **Knowledge base** | Is the state of the art of solutions mapped with criteria? Are kernel theories used in design decisions? |
| R4 | **Requirements** | Explicit, verifiable, and sourced? Defined before the evaluation? |
| R5 | **Artifact and search** | Description sufficient to rebuild it? Decisions justified? Alternatives and iterations reported? |
| R6 | **Evaluation** | Strategy justified by risks? Criteria linked to requirements? Methods appropriate to the artifact type? Adequate baseline? Formative and summative? Adequate participants and data? Ethics? |
| R7 | **Results vs. claims** | Are conclusions limited to what the evidence shows? Negative results reported? |
| R8 | **Contribution and novelty** | Plausible quadrant and level? Design knowledge explicit, beyond the artifact? |
| R9 | **Generalization and limits** | Boundary conditions stated? Instantiation validity discussed? Specific threats? |
| R10 | **Communication and reproducibility** | Clear structure for technical and managerial audiences? Artifact, instruments, and data available? DSR citations correct (§8)? |

**Recommendation summary:**
- No critical findings and few major ones → accept or minor revision.
- Major findings fixable within the scope of the study → major revision.
- A critical finding that requires a new study (e.g., no evaluation at all) → reject or resubmit as a
  new work.

Report structure in `templates.md` §13.

---

## 8. Misattributions and frequent citation errors

| Concept | Correct source | Common error |
|---|---|---|
| Seven DSR guidelines | Hevner, March, Park & Ram (2004), *MIS Quarterly* 28(1) | Attributing them to Peffers et al. or to Hevner (2007) |
| Three cycles (relevance, design, rigor) | Hevner (2007), *Scandinavian Journal of Information Systems* 19(2) | Attributing them to Hevner et al. (2004) |
| DSRM (six activities, entry points) | Peffers, Tuunanen, Rothenberger & Chatterjee (2007), *JMIS* 24(3) | "Hevner's DSRM" |
| Constructs, models, methods, instantiations | March & Smith (1995) | Citing only Hevner et al. (2004), who adopt the typology citing March & Smith |
| Improvement, invention, exaptation, routine design; levels 1–3 | Gregor & Hevner (2013) | Attributing them to Hevner et al. (2004) |
| FEDS and its four strategies | Venable, Pries-Heje & Baskerville (2016), *EJIS* 25(1) | Citing the 2012 framework or the 2008 strategies as FEDS |
| Ex ante / ex post; artificial / naturalistic | Pries-Heje, Baskerville & Venable (2008); Venable et al. (2012) | Attributing them to Hevner |
| ADR (stages and seven principles) | Sein, Henfridsson, Purao, Rossi & Lindgren (2011) | Attributing it to Hevner; confusing it with classic action research |
| eADR | Mullarkey & Hevner (2019) | — |
| Eight components of a design theory | Gregor & Jones (2007) | Confusing them with the ISDT of Walls et al. (1992) |
| Anatomy of a design principle | Gregor, Chandra Kruse & Seidel (2020) | — |
| Technological rule | van Aken (2004) | Attributing it to software engineering in general |
| CIMO | Denyer, Tranfield & van Aken (2008) | — |
| Design cycle and engineering cycle; design problems vs. knowledge questions | Wieringa (2014) | — |
| DSR Grid | vom Brocke & Maedche (2019) | — |
| *The Sciences of the Artificial* | Simon — 1st ed. 1969; 3rd ed. 1996 | Citing the year of one edition with the pagination of another |

Other checks: confirm pages, volume, and issue in `bibliography.md`; do not use a chapter DOI to cite
the whole book (or vice versa); state the edition used.

---

## 9. Frequent reviewer criticisms and how to respond

| Criticism | What usually lies behind it | How to respond (and what to change) |
|---|---|---|
| "This is just engineering or development" | Implicit design knowledge; novelty not positioned | Make principles or rules explicit; position in the Gregor & Hevner framework; compare with prior solutions |
| "The evaluation is weak" | Demonstration or perception only; no baseline | Add a summative episode; justify the FEDS strategy; include baseline and threats; if impossible, scale down the claims |
| "There is no theoretical contribution" | Venue expects abstraction | Abstract principles with justification; argue with Baskerville et al. (2018) when the artifact is the contribution; or change venue |
| "The results do not generalize" | Single context; vague class of problems | Boundary conditions; mechanism-based explanation; additional context if feasible; calibrated language |
| "Why DSR and not another method?" | Question not phrased as prescriptive | Rephrase the question; justify by the nature of the problem |
| "The requirements look arbitrary" | Sources not documented | Requirements table with sources; traceability matrix |
| "The researcher evaluated their own artifact" | Risk of bias | Report mitigation; independent evaluators; raw data; thresholds defined in advance |
| "The artifact is not described in enough detail" | Narrative description without specification | Specification, models, pseudocode, repository |
| "Frameworks cited but not used" | Framework salad | State what each framework organizes and where it appears; remove what is unused |

### Response letter
1. Brief thanks and a summary of the main changes.
2. For each comment: quote or summary of the comment → response → change made, with location
   (section, page, table).
3. When disagreeing: acknowledge the concern, present evidence or literature, and show what was
   adjusted to avoid the misunderstanding.
4. Do not promise changes that are not in the revised text.
