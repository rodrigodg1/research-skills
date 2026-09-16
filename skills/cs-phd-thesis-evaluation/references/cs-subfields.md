# Checklists by research type in computer science

Apply the generic checks (§0) to every technical chapter, then the checklist for the chapter's
research type. Many theses mix types — e.g., a systems chapter with a security analysis and a user
study — so apply several. Checklists guide attention; they are not a scoring sheet, and a thesis can
be excellent without ticking every item.

## Contents
0. Generic checks for any technical chapter
1. Theory and algorithms
2. Formal methods and programming languages
3. Systems, networking, distributed systems, HPC, and databases
4. Security, privacy, and cryptography
5. Machine learning, AI, NLP, computer vision, and data science
6. Software engineering
7. Human-computer interaction and user studies
8. Information systems and design science research
9. Interdisciplinary and applied computing

---

## 0. Generic checks for any technical chapter

- **Claim:** What does the chapter claim, precisely? Is it stated up front?
- **Link:** Which research question and contribution does it serve?
- **Novelty:** What is new relative to the closest prior work, including the candidate's earlier
  papers?
- **Assumptions:** Are they explicit, justified, and realistic for the claimed setting?
- **Evidence type:** Is it appropriate to the claim (proof for guarantees, experiments for performance,
  studies for human effects)?
- **Comparison:** Against what? Is the comparison fair and current?
- **Reproducibility:** Could someone rebuild the result from the text and artifacts?
- **Limitations:** Stated honestly, including where the approach does not work?
- **Consistency:** Do definitions, notation, and numbers match other chapters?

---

## 1. Theory and algorithms

**Key questions**
- Are models of computation, input assumptions, and cost measures explicit?
- Are definitions precise and the theorems stated unambiguously?
- Are proofs complete for central results? Are "it is easy to see" steps actually easy?
- How do results compare with known upper and lower bounds? Is tightness discussed?
- Are dependencies on conjectures or hardness assumptions stated?
- If practical relevance is claimed, is there implementation or experimental evidence, and are
  hidden constants discussed?

**Common weaknesses**
- Central results supported only by proof sketches.
- Improvements that hold only in narrow parameter regimes presented as general.
- Missing comparison with results from adjacent communities (e.g., operations research, statistics).

**Strong evidence looks like**
- Complete proofs, possibly mechanized; clear relation to the landscape of known results; honest
  discussion of open gaps.

---

## 2. Formal methods and programming languages

**Key questions**
- Are syntax, semantics, and the properties proved (soundness, completeness, decidability,
  complexity) precisely defined?
- Are proofs mechanized (e.g., in Coq/Rocq, Isabelle, Lean)? If so, what is the trusted base, and do
  the formal definitions match the paper definitions?
- For tools: which benchmarks, and are they representative? How do precision, scalability, and false
  positives compare with existing tools?
- Is expressiveness traded against tractability consciously and explained?
- For type systems or analyses: are real programs handled, and what is excluded?

**Common weaknesses**
- Gaps between the formalized model and the real language or system.
- Benchmarks chosen to favor the tool; no comparison with state-of-the-art tools.
- Unsupported language features silently excluded.

**Strong evidence looks like**
- Mechanized proofs with a clear correspondence argument; evaluation on established benchmark suites
  and real code; artifacts available.

---

## 3. Systems, networking, distributed systems, HPC, and databases

**Key questions**
- Is the problem shown to matter in real deployments (traces, measurements, operator reports)?
- Are design goals and non-goals explicit, and does each design decision map to a goal?
- Are workloads realistic and representative? Are traces or benchmarks justified?
- Are baselines the current best systems, configured and tuned fairly?
- Is performance reported with variance, repeated runs, and appropriate statistics? Are tail metrics
  reported where they matter?
- Is overhead measured (CPU, memory, energy, cost), not just the benefit?
- Does the evaluation isolate the contribution of each design component (ablation)?
- Is scale realistic? If simulation or emulation is used, is its fidelity justified?
- Are failure modes, correctness under faults, and consistency guarantees addressed where relevant?

**Common weaknesses** (see Hoefler & Belli, 2015; van der Kouwe et al., 2019)
- Selective benchmarks or subsets without justification.
- Relative speedups without absolute numbers, or against weak baselines.
- Missing variance and unreported experimental environment.
- Results on a single hardware configuration generalized broadly.

**Strong evidence looks like**
- Full disclosure of setup; fair baselines; ablation; realistic scale; artifacts enabling repetition
  (see Collberg & Proebsting, 2016, on repeatability).

---

## 4. Security, privacy, and cryptography

**Key questions**
- Is the **threat model** explicit and realistic: attacker capabilities, goals, trust assumptions,
  what is out of scope?
- Are security and privacy goals defined precisely (formal definitions where appropriate)?
- For cryptographic constructions: are definitions standard or justified, reductions correct and
  tight enough, assumptions standard and stated, and parameters concrete?
- For systems defenses: is security argued against adaptive attackers who know the defense, not only
  against existing attacks?
- For attacks: is real-world impact demonstrated, and were vulnerabilities disclosed responsibly?
- Is the cost of security (performance, usability, deployability) measured?
- For measurement studies: are data collection ethical and legal, and are biases discussed?
- For ML in security: are the pitfalls identified by Arp et al. (2024) avoided — e.g., sampling bias,
  label inaccuracy, data snooping, inappropriate baselines, lab-only evaluation?

**Common weaknesses**
- Security by assertion; threat model implicit or tailored to the defense.
- Evaluation only against known attacks.
- Benchmarking flaws in security systems evaluation (van der Kouwe et al., 2019).
- Unclear distinction between what is proven and what is argued informally.

**Strong evidence looks like**
- Precise definitions and proofs for guarantees; adaptive-attacker analysis; realistic deployment
  cost; responsible disclosure; discussion of the evidence standards of security research (Herley &
  van Oorschot, 2017).

---

## 5. Machine learning, AI, NLP, computer vision, and data science

**Key questions**
- Are data sources, collection, licensing, preprocessing, and splits documented?
- Is there any **leakage** between training and test data (duplicates, temporal leakage, feature
  leakage, preprocessing fit on all data)? Kapoor & Narayanan (2023) document how pervasive leakage
  is in ML-based science.
- Were hyperparameters tuned on validation data only, with equal tuning effort for baselines?
- Are results reported over multiple seeds with variance, and are statistical tests appropriate
  (e.g., Demšar, 2006; Dror et al., 2018)?
- Are baselines strong and current, including simple baselines that sometimes win?
- Are ablations used to show which components matter?
- Does evaluation go beyond a single benchmark: out-of-distribution, robustness, real-world data?
- Are metrics valid for the claimed capability? Are qualitative examples cherry-picked?
- For large language models and foundation models: benchmark contamination; prompt sensitivity;
  model versions and dates for API-based models; cost and compute reporting; reproducibility when
  models change or are withdrawn.
- For human evaluation: protocol, annotator expertise, agreement, compensation, ethics approval.
- Are compute budgets, energy, and fairness or societal impacts discussed where relevant?
- Is code, data, and model release adequate for reproduction (see Pineau et al., 2021)?

**Common weaknesses** (see Lipton & Steinhardt, 2019)
- Explanations of gains not backed by ablation or analysis; speculation presented as explanation.
- Mathiness: notation that obscures rather than clarifies.
- Language that overstates capabilities ("understands," "reasons").
- Improvements within noise presented as significant.

**Strong evidence looks like**
- Leakage-free protocol; multiple seeds and statistics; strong baselines tuned fairly; ablations;
  evaluation across settings; full release of code and data.

---

## 6. Software engineering

**Key questions**
- Does each empirical study follow the standard expected for its method (experiment, case study,
  survey, mining software repositories, qualitative study, engineering research)? The ACM SIGSOFT
  Empirical Standards (Ralph et al., 2020) give method-specific checklists.
- For experiments: design, subjects, tasks, and threats to validity (Wohlin et al., 2012; Kitchenham
  et al., 2002).
- For repository mining: data cleaning (bots, forks, duplicates), sampling, time windows, and
  generalization across ecosystems.
- For tools and techniques: realistic subject programs, comparison with state-of-the-art tools,
  and practitioner relevance.
- For qualitative work: sampling rationale, analysis procedure, saturation or sufficiency, and
  researcher reflexivity.
- Is a replication package provided?

**Common weaknesses**
- Student participants generalized to professionals without discussion.
- Threats to validity listed generically, unconnected to the study.
- Evaluation on a small or convenient set of projects.

**Strong evidence looks like**
- Method-appropriate design and reporting; realistic subjects; replication package; practitioner
  validation where relevant.

---

## 7. Human-computer interaction and user studies

**Key questions**
- Are research questions and hypotheses defined before the study?
- Is the study design appropriate (controlled experiment, field study, interviews, diary study,
  participatory design)?
- Participants: recruitment, sample size justification, representativeness of target users,
  compensation, ethics approval, informed consent.
- Measures: validated instruments, objective measures where claims concern performance, task
  realism.
- Analysis: appropriate statistics and effect sizes; for qualitative work, a clear analysis method and
  how themes were derived.
- Ecological validity: does the lab setting reflect real use? Novelty effects?
- Accessibility and inclusion considered where relevant?

**Common weaknesses**
- Small convenience samples (e.g., labmates) generalized to the population.
- Only self-reported satisfaction for claims about effectiveness.
- Many statistical tests without correction; p-values without effect sizes.

**Strong evidence looks like**
- Pre-specified hypotheses; justified samples; mixed measures; transparent analysis; triangulation.

---

## 8. Information systems and design science research

For theses that build and evaluate artifacts under a design science research framing:
- Is the research question prescriptive, and is DSR justified as the approach?
- Are requirements sourced and traceable to evaluation criteria?
- Are design decisions grounded in kernel theories or prior knowledge?
- Does the evaluation strategy fit the artifact's risks, with a summative episode supporting the
  main claims?
- Is design knowledge (principles, technological rules) made explicit, with boundary conditions?
- Is the contribution positioned (e.g., improvement, invention, exaptation) and at an appropriate
  level of abstraction?

If a design science research skill is available, use it for a detailed assessment of these chapters.

---

## 9. Interdisciplinary and applied computing

(E.g., bioinformatics, computational science, health informatics, computational social science,
digital humanities.)

**Key questions**
- Is the thesis assessed against both computing standards and the standards of the application
  field?
- Are domain assumptions validated with domain experts or domain literature?
- Is success measured by domain-meaningful outcomes, not only computational metrics?
- Are data governance, consent, and domain-specific ethics addressed?
- Is the computing contribution genuine, or is the thesis mainly the application of existing tools?

**Common weaknesses**
- Computational novelty overstated when the main contribution is domain application, or domain
  validity ignored when the contribution is computational.

**Strong evidence looks like**
- Clear articulation of the contribution to each field; validation by domain experts or outcomes;
  collaboration acknowledged and the candidate's role clear.
