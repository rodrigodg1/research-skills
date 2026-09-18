# research-skills

Claude skills for academic research and autoresearch. The repository follows the *plugin marketplace* layout
(`.claude-plugin/marketplace.json`) and keeps each skill in `skills/<name>/`, so it can be imported
either as a marketplace or as a skills repository.

## Skills

### Academic Research & Methodology

| Skill | Description |
|---|---|
| [`design-science-research`](skills/design-science-research/SKILL.md) | Design Science Research expert: framing, research protocol, processes (DSRM, three cycles, ADR, Wieringa, Dresch et al.), requirements, design principles and theories, contribution positioning (Gregor & Hevner), evaluation (FEDS, EVAL1–4, Prat et al. criteria), paper and thesis structure, manuscript review, and responses to reviewers. |
| [`cs-phd-thesis-evaluation`](skills/cs-phd-thesis-evaluation/SKILL.md) | Expert examiner for computer science PhD theses: calibrated assessment against the doctoral standard, claims-to-evidence ledger, subfield checklists (theory, formal methods, systems, security and cryptography, ML/AI, software engineering, HCI, information systems), integrity checks, examiner and pre-defense reports, defense questions, corrections verification, and mock examinations, adapted to different examination systems and theses by publication. |

### OpenResearch Autoresearch & CLI (`orx`)

| Skill | Description |
|---|---|
| [`openresearch-cli`](skills/openresearch-cli/SKILL.md) | Overview and operating manual for driving local OpenResearch projects from a terminal via `orx` — project lifecycle, cardinal rules, and command quick-reference. |
| [`orx-agent-delegation`](skills/orx-agent-delegation/SKILL.md) | Delegate independent research work to helper agent sessions with `orx agent spawn`: task selection, self-contained briefs, branch ownership, compute authorization, and concurrency constraints. |
| [`orx-compute`](skills/orx-compute/SKILL.md) | Launch and monitor experiment runs across local and remote compute backends: Hugging Face Jobs, Modal, Kubernetes, SSH, Slurm, Ray, OpenResearch, and Tinker. |
| [`orx-create`](skills/orx-create/SKILL.md) | Initialize projects with `orx up` and create experiment nodes with `orx create-experiment` for baselines, parent nodes, and fixed run contracts. |
| [`orx-customize`](skills/orx-customize/SKILL.md) | Save reusable skills and LaTeX templates with `orx skills add` and `orx templates add` for cross-project reuse. |
| [`orx-evidence`](skills/orx-evidence/SKILL.md) | Prepare, inspect, and validate experiment run evidence: stdout metrics, summary formatting, and reading persisted results via `orx logs`. |
| [`orx-experiment-tree`](skills/orx-experiment-tree/SKILL.md) | Plan and navigate the experiment tree: baseline setup, frozen answered nodes, downward tree growth, variant branching, and turn summaries. |
| [`orx-figures`](skills/orx-figures/SKILL.md) | Publication-quality scientific figures in matplotlib and TikZ: learning curves, scaling laws, benchmark comparisons, Pareto frontiers, heatmaps, and method diagrams. |
| [`orx-git`](skills/orx-git/SKILL.md) | Coordinate Git worktrees, inspect diffs, edit experiment code, and preserve frozen branch history across nodes. |
| [`orx-instances`](skills/orx-instances/SKILL.md) | Provision standalone cloud and remote GPU compute instances with `orx instance create` for interactive exploration. |
| [`orx-lit-review`](skills/orx-lit-review/SKILL.md) | Multi-hop literature search and retrieval across alphaXiv, OpenAlex, and bioRxiv discovery endpoints. |
| [`orx-paper`](skills/orx-paper/SKILL.md) | Draft academic papers and preprints as compilable LaTeX directly in the project tree with live PDF rendering. |
| [`orx-reports`](skills/orx-reports/SKILL.md) | Structure and generate durable research artifacts, summaries, comparisons, and technical reports. |

## How to import

### Claude (desktop or web app)
**Skills → Import from GitHub**, enter `rodrigodg1/research-skills`, and click **Preview**.

### Claude Code
```sh
# Add the marketplace
/plugin marketplace add rodrigodg1/research-skills

# Install academic research skills
/plugin install design-science-research@research-skills
/plugin install cs-phd-thesis-evaluation@research-skills

# Install OpenResearch autoresearch skills
/plugin install openresearch-cli@research-skills
/plugin install orx-lit-review@research-skills
/plugin install orx-paper@research-skills
/plugin install orx-figures@research-skills
/plugin install orx-compute@research-skills
/plugin install orx-experiment-tree@research-skills
/plugin install orx-evidence@research-skills
/plugin install orx-reports@research-skills
/plugin install orx-git@research-skills
/plugin install orx-agent-delegation@research-skills
/plugin install orx-create@research-skills
/plugin install orx-customize@research-skills
/plugin install orx-instances@research-skills
```

## Structure

```
research-skills/
├── .claude-plugin/
│   └── marketplace.json          # plugin catalog (one plugin per skill)
└── skills/
    ├── design-science-research/
    │   ├── SKILL.md              # main instructions (loaded when the skill triggers)
    │   └── references/           # detailed material, read on demand
    │       ├── frameworks.md
    │       ├── contributions-and-theory.md
    │       ├── evaluation.md
    │       ├── writing-and-reviewing.md
    │       ├── templates.md
    │       ├── bibliography.md
    │       └── glossary.md
    ├── cs-phd-thesis-evaluation/
    │   ├── SKILL.md
    │   └── references/
    │       ├── doctoral-standard.md
    │       ├── cs-subfields.md
    │       ├── examination-systems.md
    │       ├── integrity-and-verification.md
    │       ├── report-templates.md
    │       └── bibliography.md
    ├── openresearch-cli/
    │   └── SKILL.md
    ├── orx-agent-delegation/
    │   └── SKILL.md
    ├── orx-compute/
    │   ├── SKILL.md
    │   └── references/
    │       ├── hf.md
    │       ├── k8s.md
    │       ├── local.md
    │       ├── modal.md
    │       ├── openresearch.md
    │       ├── ray.md
    │       ├── slurm.md
    │       ├── ssh.md
    │       └── tinker.md
    ├── orx-create/
    │   └── SKILL.md
    ├── orx-customize/
    │   └── SKILL.md
    ├── orx-evidence/
    │   └── SKILL.md
    ├── orx-experiment-tree/
    │   └── SKILL.md
    ├── orx-figures/
    │   ├── SKILL.md
    │   ├── assets/
    │   │   ├── orx_figstyle.py
    │   │   └── orx-tikz-preamble.tex
    │   └── references/
    │       ├── comparison.md
    │       ├── curves.md
    │       ├── diagram.md
    │       ├── matrix.md
    │       ├── pareto.md
    │       └── scaling.md
    ├── orx-git/
    │   └── SKILL.md
    ├── orx-instances/
    │   └── SKILL.md
    ├── orx-lit-review/
    │   └── SKILL.md
    ├── orx-paper/
    │   └── SKILL.md
    └── orx-reports/
        └── SKILL.md
```

## Adding a new skill

1. Create `skills/<skill-name>/SKILL.md` with YAML frontmatter:
   ```yaml
   ---
   name: skill-name             # lowercase and hyphens; same as the folder name
   description: What the skill does and when it should be used.
   ---
   ```
2. Put lengthy material in `skills/<skill-name>/references/` and point to it from `SKILL.md`.
3. Add an entry to `.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "skill-name",
     "description": "…",
     "source": "./",
     "strict": false,
     "version": "1.0.0",
     "category": "research",
     "keywords": ["..."],
     "skills": ["./skills/skill-name"]
   }
   ```
4. Update the skills table in this README.
