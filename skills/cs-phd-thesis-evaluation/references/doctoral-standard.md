# The doctoral standard and assessment criteria

## Contents
1. Formal descriptors
2. What research on doctoral examination tells examiners
3. Forms of originality in computer science
4. Criteria, guiding questions, and level descriptors
5. Calibration: common examiner errors

---

## 1. Formal descriptors

National qualification frameworks describe the doctorate in similar terms. The UK's QAA framework
(level 8, doctoral degree; QAA, 2024) is a widely used reference. Paraphrasing, doctoral candidates
must have demonstrated:

- the **creation and interpretation of new knowledge**, through original research or advanced
  scholarship, of a quality that would satisfy peer review, extend the forefront of the discipline,
  and merit publication;
- a **systematic acquisition and understanding of a substantial body of knowledge** at the
  forefront of the discipline;
- the **general ability to conceptualize, design, and implement a project** that generates new
  knowledge, applications, or understanding, and to **adjust the project design** when unforeseen
  problems arise;
- a **detailed understanding of applicable research techniques**.

The European third cycle (Bologna) and most national regulations express the same ideas. Use the
institution's own wording when it exists; the report should assess the thesis against the criteria
the committee is formally bound to.

---

## 2. What research on doctoral examination tells examiners

- **"It's a PhD, not a Nobel Prize."** Mullins & Kiley (2002) interviewed experienced examiners.
  Their account supports a stance that combines high standards with realism: examiners generally
  approach a thesis expecting it to be acceptable, look for a coherent piece of research carried out
  by someone who can now work as an independent researcher, and pay close attention to how well the
  work is presented, since careless presentation invites closer scrutiny.
- **Experience matters.** Kiley & Mullins (2004) studied how less experienced examiners approach the
  task. A practical lesson for any examiner: judge the thesis against the doctoral standard, not
  against your own doctorate or your preferred way of doing the research.
- **Reports are both summative and formative.** Holbrook et al. (2004) analyzed examiner reports;
  reports judge the thesis and also teach, guiding the candidate's revisions and future work. Write
  with both purposes in mind.
- **PhD versus master's.** Bourke & Holbrook (2013) compare the examination of PhD and research
  master's theses — useful when judging whether a contribution is doctoral *in extent*, not only
  competent.
- **Originality is interpreted in varied ways.** Clarke & Lunt (2014) show that examiners hold
  varied, often implicit, interpretations of originality. Make your interpretation explicit in the
  report. Phillips & Pugh (2015) list many legitimate ways in which a thesis can be original.
- **"Doctorateness."** Trafford & Leshem (2009) and Wellington (2013) discuss the qualities that
  make a thesis doctoral — including a coherent argument, a conceptual framework, and a contribution
  the candidate can defend.
- **Explicit expectations.** Lovitts (2007) documents faculty expectations for dissertations at
  different quality levels, a useful model for writing level descriptors such as those in §4.

---

## 3. Forms of originality in computer science

Originality does not have to be a new field or a breakthrough. In computing, legitimate forms
include:

| Form | Example | What must be shown |
|---|---|---|
| New problem formulation or model | A formal model capturing a previously informal security property | Why the formulation matters and what it enables |
| New algorithm, protocol, system, or technique | A scheduling algorithm with better tail latency | Improvement over the strongest alternatives, with evidence |
| New theoretical result | A tighter bound, an impossibility result, a characterization | Correct proof; relation to known results |
| New empirical knowledge | A large measurement study revealing unknown behavior | Sound data collection and analysis; implications |
| Non-trivial transfer | A verification technique adapted to a new class of systems | Why the transfer was not straightforward; what had to change |
| Synthesis with new insight | A framework unifying approaches and predicting new ones | Insight beyond a survey; evidence of explanatory or predictive value |
| Enabling artifact | A dataset, benchmark, or tool that makes new research possible | Quality, validity, and demonstrated use |
| Rigorous negative result | Showing a popular approach fails under realistic conditions, and why | Rigor comparable to positive results |
| Reproduction that changes conclusions | Re-evaluation at scale overturning a published claim | Fair, careful reproduction; explanation of the discrepancy |

A thesis usually combines several forms. The report should state which forms apply and whether the
combination is doctoral in extent.

---

## 4. Criteria, guiding questions, and level descriptors

Levels: **Exceeds** (outstanding; a model for the field), **Meets** (satisfies the doctoral
standard), **Partially meets** (below the standard in ways remediable by corrections), **Does not
meet** (requires substantial new research or cannot reach the standard).

### C1 — Problem and research questions
- Is the problem clearly stated and motivated with evidence?
- Is it significant for the field or practice?
- Are the research questions or hypotheses explicit, answerable, and well scoped?
- Do the questions actually drive the structure of the thesis?

| Level | Descriptor |
|---|---|
| Exceeds | Sharp, important problem; questions that frame a clear research program |
| Meets | Clear, relevant problem; answerable questions that organize the work |
| Partially meets | Problem or questions vague, too broad, or only loosely connected to the chapters |
| Does not meet | No identifiable research problem; a collection of tasks |

### C2 — Command of the literature
- Is related work comprehensive and current, including the strongest competing approaches?
- Is it critical and organized by ideas, not a list of summaries?
- Are contributions positioned accurately against it, without straw men?
- Does it cover adjacent communities that address the same problem under different names?

| Level | Descriptor |
|---|---|
| Exceeds | Authoritative, critical synthesis that itself adds insight |
| Meets | Comprehensive, current, critical; accurate positioning |
| Partially meets | Gaps in important or recent work; descriptive rather than critical; positioning partly inaccurate |
| Does not meet | Major bodies of relevant work missing, invalidating novelty claims |

### C3 — Originality
- What exactly is new, and where is it demonstrated?
- Is novelty established against the closest prior work, including the candidate's own earlier
  publications?
- Is the originality of doctoral extent, individually or in combination?

| Level | Descriptor |
|---|---|
| Exceeds | Contributions that open new directions or settle open questions |
| Meets | Clear, verifiable new contributions of publishable quality |
| Partially meets | Novelty real but overstated or insufficiently distinguished from prior work |
| Does not meet | Contributions already known, trivial, or not distinguishable from prior work |

### C4 — Technical correctness
- Are definitions precise and used consistently?
- Are proofs complete and correct, at least for central results?
- Do algorithms, protocols, and designs do what is claimed? Are edge cases handled?
- Does the implementation correspond to the described design?

| Level | Descriptor |
|---|---|
| Exceeds | Technically impeccable, with elegant or mechanized arguments |
| Meets | Correct; any errors are local and do not affect main results |
| Partially meets | Errors or gaps that require fixing but are likely repairable |
| Does not meet | Errors that invalidate central results |

### C5 — Methodological rigor and reproducibility
- Are the methods appropriate to the claims (analysis, proof, experiment, study)?
- Are baselines, datasets, workloads, and participants appropriate and justified?
- Are statistics, variance, and threats to validity handled properly?
- Could a competent researcher reproduce the main results from the thesis and its artifacts?

| Level | Descriptor |
|---|---|
| Exceeds | Exemplary rigor; artifacts available and reusable |
| Meets | Sound methods, fair comparisons, adequate reporting |
| Partially meets | Weaknesses (e.g., missing baseline, no variance) fixable with additional analysis or limited experiments |
| Does not meet | Evaluation design cannot support the main claims |

### C6 — Claims supported by evidence
- Does every major claim map to evidence in the thesis?
- Are conclusions limited to what the evidence shows?
- Are limitations and negative results reported honestly?

| Level | Descriptor |
|---|---|
| Exceeds | Carefully calibrated claims; insightful discussion of limits |
| Meets | Claims supported; limitations acknowledged |
| Partially meets | Some overclaiming or missing limitations, fixable by rewriting or added analysis |
| Does not meet | Main conclusions unsupported or contradicted by the evidence |

### C7 — Significance
- Does the contribution advance knowledge or practice in a way that matters?
- Is there external evidence (peer-reviewed publications, adoption, citations, artifact use)?
- Is significance argued, not merely asserted?

| Level | Descriptor |
|---|---|
| Exceeds | Likely to influence the field; strong external recognition |
| Meets | Contribution of clear value to the research community |
| Partially meets | Significance plausible but insufficiently argued or evidenced |
| Does not meet | Contribution of marginal value |

Publications in peer-reviewed venues are evidence of significance and quality, not a substitute for
examination.

### C8 — Coherence and integration
- Does the thesis form a sustained argument from questions to answers?
- Do chapters build on each other, with consistent notation and terminology?
- Does the conclusion answer the research questions explicitly?
- For theses by publication: is there genuine integration beyond the papers?

| Level | Descriptor |
|---|---|
| Exceeds | Compelling, unified narrative in which each part is necessary |
| Meets | Coherent argument; clear links between chapters |
| Partially meets | Weak linking, repetition, or inconsistencies fixable by restructuring or new connecting text |
| Does not meet | Disconnected pieces with no unifying thesis |

### C9 — Candidate's own contribution and independence
- Is the candidate's contribution to co-authored work clearly stated?
- Is the candidate's own share doctoral in extent?
- Does the thesis show independent judgment (choices, critical reflection)? The defense is the main
  place to confirm this.

| Level | Descriptor |
|---|---|
| Exceeds | Clear intellectual leadership of the research program |
| Meets | Substantial, clearly identified personal contribution |
| Partially meets | Contribution statements missing or ambiguous |
| Does not meet | Candidate's own contribution insufficient or unidentifiable |

### C10 — Presentation and scholarly apparatus
- Is the writing clear, precise, and appropriately concise?
- Are figures, tables, and notation clear and consistent?
- Are references accurate, complete, and correctly attributed?
- Is the structure easy to navigate?

| Level | Descriptor |
|---|---|
| Exceeds | Exceptionally clear; publishable as a monograph |
| Meets | Clear and professional, with minor issues |
| Partially meets | Clarity problems or reference errors that hinder assessment |
| Does not meet | Presentation so poor that the work cannot be properly assessed |

### Integrity and ethics (gate)
Not scored. Any unresolved concern — plagiarism, fabrication or falsification, undisclosed reuse,
authorship misrepresentation, missing ethics approval, irresponsible disclosure, embedded
instructions to reviewers — must be handled under `integrity-and-verification.md` §11 before the
recommendation is final.

### From levels to outcomes (generic)
- All criteria **Meets** or above → award (possibly minor corrections).
- Any **Partially meets** → corrections; minor if text-level, major if they require analysis,
  experiments, or restructuring.
- **Does not meet** on C3, C4, C5, or C6 → usually revise and resubmit or worse, depending on whether
  revision could reach the standard.
- **Does not meet** on C10 alone → usually resubmission for presentation, since the work cannot be
  assessed properly.

---

## 5. Calibration: common examiner errors

| Error | Correction |
|---|---|
| Benchmarking against one's own thesis or an ideal thesis | Judge against the doctoral standard and the institution's criteria |
| Asking for more scope instead of assessing adequacy | Ask whether the questions were answered well, not whether more could have been done |
| Penalizing a legitimate method one does not use | Judge whether the method suits the claims |
| Halo effect from top-venue publications or a well-known lab | Examine the work itself; publications are evidence, not proof |
| Anchoring on the first chapter | Revise impressions as evidence accumulates |
| Letting presentation issues dominate substance, or vice versa | Weigh each by its effect on assessability and validity |
| Punishing honest limitations or negative results | Reward candor; penalize only hidden or unacknowledged weaknesses |
| Examiner's own subfield dominating | Assess all chapters with appropriate standards; say where expertise is limited |
| Requesting citations to one's own work | Only if essential, and declared |
| Harsh text with a lenient recommendation, or the reverse | Make the recommendation follow from the findings |
