# research-skills

Claude skills for academic research. The repository follows the *plugin marketplace* layout
(`.claude-plugin/marketplace.json`) and keeps each skill in `skills/<name>/`, so it can be imported
either as a marketplace or as a skills repository.

## Skills

| Skill | Description |
|---|---|
| [`design-science-research`](skills/design-science-research/SKILL.md) | Design Science Research expert: framing, research protocol, processes (DSRM, three cycles, ADR, Wieringa, Dresch et al.), requirements, design principles and theories, contribution positioning (Gregor & Hevner), evaluation (FEDS, EVAL1–4, Prat et al. criteria), paper and thesis structure, manuscript review, and responses to reviewers. |
| [`cs-phd-thesis-evaluation`](skills/cs-phd-thesis-evaluation/SKILL.md) | Expert examiner for computer science PhD theses: calibrated assessment against the doctoral standard, claims-to-evidence ledger, subfield checklists (theory, formal methods, systems, security and cryptography, ML/AI, software engineering, HCI, information systems), integrity checks, examiner and pre-defense reports, defense questions, corrections verification, and mock examinations, adapted to different examination systems and theses by publication. |

## How to import

### Claude (desktop or web app)
**Skills → Import from GitHub**, enter `rodrigodg1/research-skills`, and click **Preview**.

### Claude Code
```
/plugin marketplace add rodrigodg1/research-skills
/plugin install design-science-research@research-skills
/plugin install cs-phd-thesis-evaluation@research-skills
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
    └── cs-phd-thesis-evaluation/
        ├── SKILL.md
        └── references/
            ├── doctoral-standard.md
            ├── cs-subfields.md
            ├── examination-systems.md
            ├── integrity-and-verification.md
            ├── report-templates.md
            └── bibliography.md
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
     "skills": ["./skills/skill-name"]
   }
   ```
4. Update the skills table in this README.
