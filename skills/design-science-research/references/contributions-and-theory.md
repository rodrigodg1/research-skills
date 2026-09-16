# Artifacts, contribution, and theory in DSR

## Contents
1. Artifact types
2. Descriptive (Ω) and prescriptive (Λ) knowledge
3. Contribution framework and levels (Gregor & Hevner, 2013)
4. Balancing artifact and theory (Baskerville et al., 2018)
5. Design theory: Walls et al. (1992), Gregor & Jones (2007), Gregor (2006)
6. Kernel theories, requirements, and meta-requirements
7. Design principles
8. Technological rules and CIMO logic
9. Generalization, abstraction, and instantiation validity
10. Contribution statement

---

## 1. Artifact types

### March & Smith (1995)
| Type | Definition (paraphrase) | Examples in computing, security, and management | Typical representation |
|---|---|---|---|
| **Construct** | Vocabulary and symbols to define and communicate problems and solutions | Attack taxonomy; consent ontology; modeling notation; concepts of a policy language | Definitions, metamodel, formal glossary |
| **Model** | Propositions relating constructs; represent the problem and solution space | Maturity model; reference architecture; process model; formal threat model | Diagrams, specifications, formal models |
| **Method** | A set of steps (algorithm or guideline) to perform a task | Algorithm; risk assessment method; audit procedure; development process | Pseudocode, flows, step-by-step guides |
| **Instantiation** | Realization of the artifact in its environment; operationalizes constructs, models, and methods and demonstrates feasibility | Prototype; deployed system; protocol implementation; tool | Code, running system, deployment |

Activities crossed with these types: **build** (show the artifact can be made for a purpose),
**evaluate** (define criteria and measure performance), **theorize** (explain why and how the
artifact works in its environment), and **justify** (gather evidence that tests that explanation).

### Types observed in the IS literature (Offermann et al., 2010)
System design, method, language or notation, algorithm, guideline, requirements, pattern, and
metric. Useful when the March & Smith classification is too coarse — for example, "metric" and
"pattern" are legitimate artifacts that would fit poorly otherwise.

### More abstract artifacts
Gregor & Hevner (2013) and Gregor & Jones (2007) treat **design principles** and **design theories**
as DSR outputs at a higher level of abstraction (see §3 and §5).

### Practical notes
- A project usually produces several types at once (e.g., a method and an instantiation that
  implements it). Declare which is the **main** artifact — that is the one the evaluation must
  support.
- DSR artifacts can be sociotechnical (processes, policies, organizational structures), not only
  software.
- An instantiation alone is rarely enough as a scientific contribution; what makes it research is
  the knowledge it allows one to test or extract.

---

## 2. Descriptive (Ω) and prescriptive (Λ) knowledge

Gregor & Hevner (2013) distinguish two kinds of knowledge that interact in DSR:

| | Ω — descriptive (what, how, why) | Λ — prescriptive (how to) |
|---|---|---|
| Content | Phenomena (observations, classifications, measurements) and sense-making (laws, regularities, principles, patterns, theories) | Constructs, models, methods, instantiations, and design theories |
| Role in DSR | Grounds design decisions (kernel theories); explains why the artifact works | State of the art of solutions; what DSR mainly contributes to |

**Applying it to the literature review:** organize it into (a) what is known about the problem and
its mechanisms (Ω) and (b) what solutions exist and how well they work (Λ). The DSR gap is usually in
(b), justified by (a). DSR can also contribute to Ω — for instance, by explaining why the artifact
produced the observed effect.

---

## 3. Contribution framework and levels (Gregor & Hevner, 2013)

### DSR Knowledge Contribution Framework
Axes: **application domain maturity** (is the problem known and well understood?) and **solution
maturity** (do known, adequate solutions exist?).

| | **Low** solution maturity | **High** solution maturity |
|---|---|---|
| **High domain maturity** (known problem) | **Improvement** — new solution for a known problem | **Routine design** — known solution for a known problem |
| **Low domain maturity** (new problem) | **Invention** — new solution for a new problem | **Exaptation** — known solution extended to a new problem |

| Quadrant | What must be demonstrated | Common pitfall |
|---|---|---|
| Improvement | A well-mapped state of the art of solutions; comparative evaluation showing the new artifact is better on relevant criteria | Comparing against a weak or outdated baseline |
| Invention | That the problem is genuinely new and important; feasibility and initial utility of the artifact | Calling an improvement an invention; ignoring related work in other fields |
| Exaptation | That the transfer is non-trivial: adaptations required, why it was not obvious, what is learned about the new domain | Direct application of a known technique presented as a contribution |
| Routine design | Normally not a research contribution; it becomes research only if it reveals unexpected results leading to another quadrant | An entire thesis in this quadrant dressed in DSR jargon |

**Use in supervision:** ask the user for evidence on each axis. Domain maturity is shown with
literature and data about the problem; solution maturity, with a map of existing solutions and their
limitations.

### Contribution levels
| Level | Type | Examples | Expected evidence |
|---|---|---|---|
| **3** | Well-developed design theory about embedded phenomena | Mid-range or grand theories | Multiple studies, contexts, and instantiations; consolidated explanation |
| **2** | Nascent design theory — knowledge as operational principles or architecture | Constructs, methods, models, design principles, technological rules | Evaluated artifact and justified abstraction; boundary conditions stated |
| **1** | Situated implementation of an artifact | Instantiations: software, implemented processes | Working artifact evaluated in context |

- A project can contribute at more than one level; typical theses and papers combine levels 1 and 2.
- The claimed level must be proportional to the evidence. Claiming level 3 from a single study is a
  guaranteed criticism.
- Gregor & Hevner (2013) also propose a publication schema for DSR (see
  `writing-and-reviewing.md` §1).

---

## 4. Balancing artifact and theory (Baskerville et al., 2018)

There is tension, especially in IS journals, between demanding theory and valuing artifacts.
Baskerville et al. (2018) argue for balance: novel and useful artifacts are themselves valuable
knowledge, and theoretical abstraction should be proportional to the study's aim and the available
evidence.

**Practical guidance:**
- State explicitly where the weight of the contribution lies: in the artifact, in the abstracted
  design knowledge, or in both.
- High-impact IS journals tend to expect abstraction (principles or theory). Computer science venues
  tend to value the artifact and its evaluation. Adjust to the target audience.
- Do not fabricate theory: well-grounded, evaluated design principles are already a level 2
  contribution.

---

## 5. Design theory

### Types of theory in IS (Gregor, 2006)
Five types: I analysis; II explanation; III prediction; IV explanation and prediction; **V design and
action** — says how to do something, with explicit prescriptions. Design theories in DSR are type V
and usually rest on types I–IV as kernel theories.

### Information Systems Design Theory — ISDT (Walls et al., 1992)
| Aspect | Component | Description (paraphrase) |
|---|---|---|
| Product | Meta-requirements | The class of goals to which the theory applies |
| | Meta-design | The class of artifacts hypothesized to meet the meta-requirements |
| | Kernel theories | Natural or social science theories governing design requirements |
| | Testable design product hypotheses | Test whether the meta-design satisfies the meta-requirements |
| Process | Design method | Procedures for building the artifact |
| | Kernel theories | Theories governing the design process |
| | Testable design process hypotheses | Verify whether the method yields an artifact consistent with the meta-design |

### The anatomy of a design theory (Gregor & Jones, 2007)
| # | Component | Guiding question |
|---|---|---|
| 1 | Purpose and scope | What is the artifact for? Which meta-requirements does it meet? Within what limits? |
| 2 | Constructs | Which entities of interest does the theory use and how are they defined? |
| 3 | Principles of form and function | What is the "abstract blueprint": structure, architecture, functions? |
| 4 | Artifact mutability | What state changes or adaptations of the artifact does the theory anticipate? |
| 5 | Testable propositions | If the artifact follows the principles, what observable outcomes are expected? |
| 6 | Justificatory knowledge | What theories or knowledge explain why the design should work? |
| 7 | Principles of implementation* | How should the artifact be implemented in specific contexts? |
| 8 | Expository instantiation* | What concrete implementation illustrates the theory and allows it to be tested? |

\* Additional components; the first six are the core. Canvas in `templates.md` §12.

**Use:** the framework serves both to *build* a theory (fill in each component) and to *review*
theoretical claims (empty components show what is missing). If several components remain empty, the
contribution is probably at level 1 or 2, and the text should say so.

---

## 6. Kernel theories, requirements, and meta-requirements

### What counts as justificatory knowledge
- Social and behavioral science theories (cognitive load, trust in automation, agency theory,
  learning).
- Formal and mathematical theories (queueing theory, computational complexity, game theory,
  cryptographic assumptions).
- Design knowledge: patterns, reference architectures, prior artifacts.
- Established empirical findings and technical or regulatory standards.
- Domain experience and expertise — Hevner's (2007) knowledge base includes these.

When the design rests on engineering knowledge rather than behavioral theory, say so clearly. It is
more honest and more defensible than forcing a theory.

### Derivation chain
```
Kernel theory proposition
  → meta-requirement (for the class of problems)
    → design principle
      → artifact feature (instance)
        → testable proposition
          → evaluation criterion and episode
```
Example: *kernel theory* — users calibrate trust in automated systems when they understand the
system's reasoning → *meta-requirement* — the system must let users assess the basis of each
recommendation → *principle* — provide a readable justification for every recommendation →
*feature* — a panel showing the three factors that weighed most → *proposition* — users who see the
justification accept fewer wrong recommendations than users who do not → *evaluation* — an
experiment comparing both conditions.

### Good requirements
- **Specific and verifiable:** "reduce triage time relative to the current process" instead of "be
  efficient."
- **Traceable:** each requirement names its source (interview, data, literature, regulation,
  theory).
- **Classified:** functional and quality (performance, security, usability); priority.
- **Solution-independent:** describe what is needed, not how the artifact does it.
- **At class level when the contribution is abstract:** meta-requirements.

**Elicitation sources:** systematic review, interviews and focus groups with stakeholders, analysis
of documents and incidents, standards and regulations (e.g., GDPR, LGPD, ISO), threat modeling for
security requirements, observation of actual work.

### Design theories and explanatory theories
Kuechler & Vaishnavi (2012) distinguish design theories (prescriptive) from explanatory or predictive
theories relevant to design, which explain why an artifact works and can bridge kernel theory and
design theory.

### Common failures
- Theories listed in the background and never used in the design.
- A theory fitted after the artifact was finished, with no real influence on decisions. If that
  happened, it is better to present the theory as an *explanation* of the results than as the
  *foundation* of the design.

---

## 7. Design principles

**What they are.** Prescriptive statements that capture design knowledge transferable to a class of
problems. They are the most common form of level 2 contribution.

### Chandra, Seidel & Gregor (2015) template
Principles should articulate **materiality** (properties of the artifact), **action** (what users
can do), and **boundary conditions**. Adapted template:
> Provide the system with **[material property, in terms of form and function]** so that
> **[users or group]** can **[action or activity]**, given that **[boundary conditions: user
> characteristics or implementation setting]**.

### Anatomy by Gregor, Chandra Kruse & Seidel (2020)
Components: **aim**, **actors** — implementer, user, and enactor —, **context**, **mechanism**
(actions, activities, processes, or material properties), and **rationale** (based on theory or
evidence). Adapted template:
> For **implementer I** to achieve or allow **aim A** for **user U** in **context C**, employ
> **mechanisms M1, M2…**, enacted by **E1, E2…**, because of **[rationale R]**.

### Qualities of a good principle
- Prescriptive and action-oriented.
- Addressed to a class of situations, not to one instance.
- Independent of a specific technology — "use blockchain" is a feature; "ensure tamper-evident
  records verifiable by parties who do not trust each other" is a principle.
- Justified (theory or evidence) and with boundary conditions.
- Testable: it implies observable effects.
- Understandable and reusable by practitioners.

### Weak vs. strong
- **Weak:** "The system should be easy to use."
- **Strong:** "Provide the triage tool with a readable justification of the factors behind each
  priority, so that analysts can challenge incorrect priorities before acting, given that they work
  under high alert load and remain accountable for the final decision."

### Where principles come from
- **A priori:** derived from meta-requirements and kernel theories before building; tested in the
  evaluation.
- **A posteriori:** extracted by reflecting on the artifact and evaluation results; they need further
  evaluation to gain strength.
State which case applies. A posteriori principles presented as if they had guided the design from
the start are an integrity problem.

### How to evaluate principles
Instantiate them and measure the predicted effects; check instantiation validity (§9); compare
instantiations with and without the mechanism (ablation); ask experts about understandability and
reuse; test in more than one context.

---

## 8. Technological rules and CIMO logic

### Technological rule (van Aken, 2004)
> If you want to achieve **Y** in situation **Z**, then something like action **X** will help.

- "Something like" signals a **heuristic** prescription that must be adapted to context, as opposed
  to **algorithmic** prescriptions followed to the letter.
- Strong rules are **field-tested** (in practice) and **grounded** (explained by mechanisms or
  theory).
- In software engineering, the technological rule is the usual form of contribution
  (`frameworks.md` §10).

### CIMO logic (Denyer et al., 2008)
Design propositions with four elements:
- **C**ontext: the class of problematic situations;
- **I**ntervention: the type of intervention;
- **M**echanism: the generative mechanism the intervention triggers — *why* it works;
- **O**utcome: the results produced.
> In contexts of type **C**, use interventions of type **I** to trigger mechanisms **M** and produce
> outcomes **O**.

The mechanism is the link to kernel theory; CIMO without a mechanism is just a recommendation.

### Which format to use
| Audience | Preferred format |
|---|---|
| Information Systems | Design principles (Gregor et al., 2020) |
| Management and production engineering | Technological rules or CIMO |
| Software engineering | Technological rules |
| Computer science and security | Design goals and principles in technical language; generalizable lessons |

---

## 9. Generalization, abstraction, and instantiation validity

**The problem.** Evaluation happens on instances; contribution claims are about classes. That leap
must be argued.

**Types of generalization (Lee & Baskerville, 2003).** They distinguish generalizing from empirical
data to empirical data, from empirical data to theory, from theory to empirical data, and from
theory to theory. A DSR evaluation in one context usually supports generalization to *theory*
(principles and mechanisms), not statistical generalization to a population. Applying the principles
in a new context requires checking that the conditions still hold.

**Strategies to strengthen generalization:**
1. Explicitly define the class of problems and the boundary conditions.
2. Explain *why* the artifact works (mechanisms): where the mechanism operates, the effect should
   recur — this is Wieringa's (2014) reasoning by architectural similarity.
3. Instantiate and evaluate in more than one context, or in deliberately varied contexts.
4. Widen conditions gradually (lab → pilot → field).
5. Ask experts about transferability.
6. Abstract the knowledge into principles or rules, and state what was left out.

**Instantiation validity (Lukyanenko et al., 2014).** The extent to which the built instance actually
represents the abstract artifact or design principles. Implementation details (interface,
performance, incidental choices) can cause the observed effects instead of the principles.
Mitigations: document the principle → feature mapping; multiple instantiations; manipulation checks;
ablation studies; hold incidental aspects constant across conditions.

**Calibrated language:**
- Avoid: "the artifact solves the problem of X."
- Prefer: "in the evaluated context, the artifact reduced Y relative to Z; mechanisms M suggest the
  effect should recur in contexts with characteristics C1 and C2."

---

## 10. Contribution statement

A good statement answers:
1. **Which artifact?** Type and form.
2. **What is new?** Relative to which prior solutions, and in what respect.
3. **For which class of problems?** With boundary conditions.
4. **With what evidence?** Evaluation strategy and main results.
5. **What design knowledge?** Principles, rules, understanding of the problem.
6. **For whom?** Implications for research and for practice.
7. **Where in the framework?** Quadrant and level.

**Example structure (adapt):**
> This work contributes [artifact], a [type] for [class of problems]. Unlike [prior solutions],
> which [limitation], the artifact [essential difference]. The evaluation [strategy:
> artificial/naturalistic; formative/summative] showed [main result relative to the baseline]. From
> this experience we derive [n] design principles that [purpose] in contexts with [conditions]. In
> the Gregor & Hevner (2013) framework, this is an [quadrant] contribution at levels [1 and 2].

Full template in `templates.md` §10.
