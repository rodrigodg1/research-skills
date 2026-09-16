# Report templates

Adapt to the institution's form when one exists: keep its headings and fill them with the content
below. Mark anything not yet assessed as **[not assessed]**.

## Contents
1. Chapter notes
2. Claims ledger
3. Examiner report
4. Criteria scorecard
5. Preliminary (pre-defense) report
6. Defense question bank
7. Corrections verification
8. Mock examination report
9. Consolidated committee report
10. Calibrated phrasing

---

## 1. Chapter notes

```markdown
## Chapter [n] — [title] (pp. [x–y])
Research type: [theory | systems | security | ML | SE | HCI | DSR | ...]
Purpose: [what the chapter is for; which RQ and contribution it serves]
Derived from: [publication(s), co-authors, candidate's stated role]

Claims:
- [claim] — [location]

Evidence:
- [proof / experiment / study / argument] — [location] — [adequacy]

Findings:
| ID | Location | Severity | Finding | Why it matters | Required action |
|---|---|---|---|---|---|
| 4.1 | §4.3, Eq. 7 | Major | ... | ... | ... |

Strengths:
- ...

Questions for the defense:
- ...

Editorial:
- p. [x]: ...
```

---

## 2. Claims ledger

| # | Claim | Where claimed | Where supported | Evidence type | Verdict | Notes |
|---|---|---|---|---|---|---|
| 1 | | | | | Supported / Partially / Unsupported / Contradicted | |

---

## 3. Examiner report

```markdown
# Examiner's report

**Candidate:** [name]
**Thesis title:** [title]
**Program / institution:** [ ]
**Examiner:** [name, affiliation, role]
**Date:** [ ]
**Declaration of conflicts of interest:** [none / details]

## 1. Summary of the thesis
[One or two paragraphs in the examiner's own words: problem, research questions, approach, main
results, claimed contributions, and structure. For theses by publication, list the papers and their
status.]

## 2. Overall assessment
[One or two paragraphs: does the thesis meet the doctoral standard? Main reasons, referring to the
criteria. State the recommendation here briefly.]

## 3. Contributions and strengths
[Specific strengths with locations: original results, rigorous evaluations, significant artifacts,
clarity.]

## 4. Assessment against the criteria
[Short paragraph or the scorecard in §4 for C1–C10, each with its level and justification.]

## 5. Required corrections
### 5.1 Critical issues
[C1] **[Short title]** — [location]
- Issue: ...
- Why it matters: ...
- Required action and what counts as resolved: ...

### 5.2 Major issues
[M1] ...

### 5.3 Minor issues
[m1] ...

## 6. Suggestions (optional)
[S1] ...

## 7. Questions for the oral examination
[Grouped by topic; each linked to findings where relevant.]

## 8. Recommendation
[Institution's category.] [Justification tied to the findings. If conditional on the defense or on
resolution of an integrity concern, say so.]

## Appendix A — Editorial corrections
- p. [x], line [y]: ...

## Appendix B — Confidential comments to the committee (if permitted)
[Integrity concerns or sensitive remarks, per institutional rules.]
```

---

## 4. Criteria scorecard

| # | Criterion | Level | Justification (with locations) |
|---|---|---|---|
| C1 | Problem and research questions | Exceeds / Meets / Partially meets / Does not meet | |
| C2 | Command of the literature | | |
| C3 | Originality | | |
| C4 | Technical correctness | | |
| C5 | Methodological rigor and reproducibility | | |
| C6 | Claims supported by evidence | | |
| C7 | Significance | | |
| C8 | Coherence and integration | | |
| C9 | Candidate's own contribution and independence | | |
| C10 | Presentation and scholarly apparatus | | |
| — | Integrity and ethics (gate) | Clear / Concern raised | |

---

## 5. Preliminary (pre-defense) report

For systems where a report decides whether the defense may proceed.

```markdown
# Preliminary report — [thesis title]

## Recommendation on proceeding to defense
[Proceed | Proceed, with issues to be addressed at the defense | Do not proceed until revised]

## Summary of the thesis
[Short paragraph.]

## Main contributions
- ...

## Issues that must be resolved before the defense (if any)
- [location] — [issue] — [required action]

## Issues to be discussed at the defense
- ...

## Additional corrections for the final version
- ...
```

---

## 6. Defense question bank

Annotate each question with its **purpose** (clarify / probe / extend) and **what a good answer
includes**, so the committee can judge the response.

### Opening
- Summarize the thesis in a few minutes: the problem, your main contributions, and why they matter.
- What is the single most important result, and why?
- If you started the doctorate again today, what would you do differently?

### Problem and positioning
- Why is this problem important now, and for whom?
- Which prior work is closest to yours, and what precisely distinguishes your contribution?
- How would [competing approach or community] view your contribution?

### Contributions (repeat per contribution)
- What was the key insight that made [contribution] possible?
- Which alternatives did you consider, and why did you reject them?
- Where does [contribution] stop working?

### Theory and correctness
- Walk us through the key idea of the proof of [theorem].
- Which assumption in [theorem] is strongest, and what happens if it is relaxed?
- Is the bound tight? What prevents a better result?

### Methodology and evaluation
- Why these baselines, datasets, workloads, or participants?
- How did you make sure the comparison with [baseline] was fair?
- How confident are you that the difference in [result] is not noise?
- Which result surprised you, and how did you investigate it?
- What would it take to reproduce [main result] from your artifacts?

### Validity and limitations
- What is the biggest threat to the validity of [study]?
- In which settings would you not recommend using your approach?
- What negative results did you obtain that are not in the thesis?

### Ownership (especially for co-authored work)
- What was your personal contribution to [paper or chapter]?
- Which design decision in [chapter] was hardest, and how did you reach it?
- What went wrong during this part of the work, and how did you fix it?

### Significance and future work
- How has the community responded to your published work?
- What is the most promising direction your thesis opens?
- How might your results change practice?

### Closing
- Is there anything in the thesis you would now state differently?
- Is there a question you expected that we did not ask?

**Escalation:** start with an open question; follow with a probe on a specific weakness; if needed,
present the concrete counterexample or issue from the report and ask how the candidate would resolve
it.

---

## 7. Corrections verification

| ID | Required correction (from report) | Resolution criterion | Candidate's response (location) | Status | Evidence / comment |
|---|---|---|---|---|---|
| M1 | | | | Resolved / Partially resolved / Unresolved | |

**Summary:** [all resolved | outstanding items listed] — [recommendation: accept final version / return
for further corrections]. New problems introduced by the revision are listed separately and flagged as
such.

---

## 8. Mock examination report

For candidates or supervisors before submission or defense. Keep it constructive and prioritized.

```markdown
# Mock examination — [thesis title]

## Readiness
[Ready to submit | Ready after the fixes below | Needs substantial work] — [one-paragraph reason]

## Likely examiner perception
[How an external examiner would probably summarize the thesis and its main weaknesses.]

## Priority fixes before submission
| Priority | Location | Issue | Why an examiner will care | Suggested fix | Effort |
|---|---|---|---|---|---|
| 1 | | | | | Small / Medium / Large |

## Quick wins
- ...

## Questions to prepare for
| Question | Why it will be asked | Points a strong answer should cover |
|---|---|---|

## Strengths to foreground
- ...
```

---

## 9. Consolidated committee report

```markdown
# Consolidated report — [thesis title]

## Committee
[Names, roles]

## Summary and joint assessment
[Agreed summary; points of consensus.]

## Divergences between examiners
[Issue — positions — resolution reached.]

## Required corrections (reconciled, deduplicated, numbered)
[ID] — [location] — [issue] — [resolution criterion] — [raised by]

## Suggestions
- ...

## Outcome
[Category and justification; deadline for corrections; who verifies them.]
```

---

## 10. Calibrated phrasing

**Strengths**
- "Chapter 4 makes a clear and significant contribution: [specific result], which improves on [prior
  work] by [how]."
- "The evaluation in Chapter 5 is particularly careful: [baselines, repetitions, ablation]."

**Concerns**
- "The claim in §1.3 that [claim] is broader than the evidence in §5.4, which covers only [scope].
  Either additional experiments on [settings] or a narrower claim is needed."
- "The proof of Lemma 3.2 does not address the case [case]; this case appears necessary for Theorem
  3.5."
- "Related work does not discuss [work], which addresses the same problem using [approach]. The
  novelty of [contribution] should be established against it."
- "It is not clear from the thesis which parts of [paper] were the candidate's own contribution.
  Please add a contribution statement."

**Required corrections**
- "Required: report variance over at least [n] runs for Tables 5.2–5.4 and state whether the
  differences are statistically significant."
- "Required: revise the abstract and §7.1 so that the claims match the results in Chapter 6."

**Suggestions**
- "Optional: a short discussion of [topic] would help readers connect Chapters 3 and 4."

**Avoid**
- Vague judgments without location ("the evaluation is weak").
- Sarcasm or rhetorical questions in place of findings.
- Demands for a different thesis ("the candidate should have studied X instead").
