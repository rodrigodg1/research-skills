# research-skills

Skills do Claude para pesquisa acadêmica. O repositório segue o layout de *plugin marketplace*
(`.claude-plugin/marketplace.json`) e mantém cada skill em `skills/<nome>/`, então pode ser
importado tanto como marketplace quanto como repositório de skills.

## Skills

| Skill | Descrição |
|---|---|
| [`design-science-research`](skills/design-science-research/SKILL.md) | Especialista em Design Science Research: enquadramento, protocolo, processos (DSRM, três ciclos, ADR, Wieringa, Dresch et al.), requisitos, princípios e teorias de design, contribuição (Gregor & Hevner), avaliação (FEDS, EVAL1–4, critérios de Prat et al.), estrutura de artigos e teses, revisão de manuscritos e resposta a revisores. |

## Como importar

### Claude (app desktop ou web)
**Skills → Import from GitHub**, informe `rodrigodg1/research-skills` e clique em **Preview**.

### Claude Code
```
/plugin marketplace add rodrigodg1/research-skills
/plugin install design-science-research@research-skills
```

## Estrutura

```
research-skills/
├── .claude-plugin/
│   └── marketplace.json          # catálogo de plugins (um por skill)
└── skills/
    └── design-science-research/
        ├── SKILL.md              # instruções principais (carregadas quando a skill é acionada)
        └── references/           # material detalhado, lido sob demanda
            ├── frameworks.md
            ├── contributions-and-theory.md
            ├── evaluation.md
            ├── writing-and-reviewing.md
            ├── templates.md
            ├── bibliography.md
            └── glossary.md
```

## Como adicionar uma nova skill

1. Crie `skills/<nome-da-skill>/SKILL.md` com frontmatter YAML:
   ```yaml
   ---
   name: nome-da-skill          # minúsculas e hífens; igual ao nome da pasta
   description: O que a skill faz e quando deve ser usada.
   ---
   ```
2. Coloque material extenso em `skills/<nome-da-skill>/references/` e aponte para ele no `SKILL.md`.
3. Adicione uma entrada em `.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "nome-da-skill",
     "description": "…",
     "source": "./",
     "strict": false,
     "skills": ["./skills/nome-da-skill"]
   }
   ```
4. Atualize a tabela de skills deste README.
