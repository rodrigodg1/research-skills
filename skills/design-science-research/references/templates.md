# Modelos preenchíveis para DSR

Preencha com o que já se sabe do projeto e marque lacunas como **[a definir]**, para ficar claro o
que falta. Adapte nomes de campos ao idioma e à venue.

## Sumário
1. Protocolo de pesquisa DSR
2. Enunciado do problema e classe de problemas
3. Questões de pesquisa
4. Tabela de requisitos
5. Matriz de rastreabilidade
6. Princípios de design
7. Regra tecnológica e proposição CIMO
8. Plano de avaliação (FEDS)
9. Registro de iterações
10. Declaração de contribuição
11. DSR Grid
12. Canvas de teoria de design
13. Parecer de revisão DSR
14. Exemplo completo

---

## 1. Protocolo de pesquisa DSR

```markdown
# Protocolo DSR — [título provisório]

## 1. Identificação
- Pesquisador(a) / orientador(a):
- Área e venue(s)-alvo:
- Versão e data:

## 2. Problema
- Enunciado (ver §2):
- Evidências de relevância (fonte → evidência):
- Stakeholders e interesses:
- Causas conhecidas ou hipotéticas:
- Classe de problemas e condições de contorno:

## 3. Questões e objetivos
- Questão de design:
- Questões de conhecimento:
- Objetivo geral:
- Objetivos específicos (como resultados):

## 4. Base de conhecimento
- Conhecimento sobre o problema (Ω):
- Soluções existentes e limitações (Λ), com critérios de comparação:
- Teorias de base e como serão usadas no design:

## 5. Abordagem metodológica
- Justificativa para DSR:
- Processo adotado (DSRM, ADR, Wieringa, Dresch et al....) e adaptações:
- Ponto de entrada:
- Estratégia de DSR (Iivari: geral → instância ou instância → geral):
- Mapeamento etapas do processo × entregas × capítulos ou artigos:

## 6. Requisitos (ver §4)

## 7. Artefato
- Tipo(s) e artefato principal:
- Forma de representação:
- Decisões de design previstas e alternativas a explorar:
- Princípios de design a priori (se houver):

## 8. Avaliação (ver §8)
- Objetivos da avaliação e prioridades:
- Estratégia FEDS e justificativa:
- Episódios planejados:
- Critérios, métricas, comparadores e limiares:
- Ameaças à validade e mitigação:

## 9. Contribuição esperada
- Quadrante (Gregor & Hevner) e justificativa:
- Nível(is):
- Conhecimento de design esperado:

## 10. Ética e dados
- Participantes humanos? Apreciação por CEP necessária?
- Dados pessoais e LGPD:
- Riscos de uso dual:
- Acordos com organizações:

## 11. Cronograma por iterações
| Iteração | Período | Foco | Episódios de avaliação | Entregas |
|---|---|---|---|---|

## 12. Riscos do projeto
| Risco | Probabilidade | Impacto | Mitigação ou plano alternativo |
|---|---|---|---|
```

---

## 2. Enunciado do problema e classe de problemas

**Problema de design (adaptado de Wieringa, 2014):**
> Melhorar **[contexto do problema]**
> por meio de **[(re)projeto de um artefato]**
> que satisfaça **[requisitos principais]**
> a fim de **[ajudar stakeholders a alcançar objetivos]**.

**Enunciado narrativo:**
> Em **[contexto]**, **[stakeholders]** enfrentam **[problema]**, evidenciado por **[dados ou
> fontes]**. Isso causa **[consequências]**. As soluções atuais, como **[soluções]**, não resolvem
> porque **[limitações]**. Falta **[o que falta]**.

**Classe de problemas:**
> Este problema é uma instância da classe **[nome da classe]**: situações em que **[características
> essenciais compartilhadas]**. Estão fora da classe as situações em que **[exclusões]**.

---

## 3. Questões de pesquisa

```markdown
QP (design): Como projetar [artefato] para [objetivo] em [contexto]?
  QC1 (problema):     Quais são as causas de [problema] em [contexto]?
  QC2 (requisitos):   Que requisitos [artefato] deve satisfazer segundo [fontes]?
  QC3 (efeito):       Qual o efeito de [artefato] sobre [critério] comparado a [baseline]?
  QC4 (sensibilidade): Como esse efeito varia com [característica do contexto]?
```

---

## 4. Tabela de requisitos

| ID | Requisito | Tipo | Origem (fonte) | Justificativa ou teoria de base | Prioridade | Critério de verificação |
|---|---|---|---|---|---|---|
| R1 | | Funcional / qualidade | Entrevista E3; Autor (ano); norma X | | Alta / média / baixa | |

Para contribuições abstratas, acrescente uma coluna **Meta-requisito** (versão em nível de classe).

---

## 5. Matriz de rastreabilidade

| Aspecto do problema | Requisito | Princípio ou decisão de design | Componente do artefato | Critério | Episódio e método | Evidência | Atendido? |
|---|---|---|---|---|---|---|---|
| P1 | R1 | DP1 | C2 | Eficácia | E2 — benchmark | Tabela 5 | Sim / parcial / não |

Linhas com células vazias indicam lacunas a tratar antes de escrever os resultados.

---

## 6. Princípios de design

**Forma completa (adaptada de Gregor, Chandra Kruse & Seidel, 2020):**
> **DP[n] — [nome curto].** Para que **[implementador]** alcance **[objetivo]** para **[usuários]**
> em **[contexto]**, empregue **[mecanismos]**, executados por **[pessoas ou componentes]**, porque
> **[justificativa: teoria ou evidência]**.

**Forma compacta (adaptada de Chandra, Seidel & Gregor, 2015):**
> **DP[n].** Forneça ao sistema **[propriedade material]** para que **[usuários]** possam **[ação]**,
> dado que **[condições de contorno]**.

**Ficha de cada princípio:**
| Campo | Conteúdo |
|---|---|
| Origem | A priori (requisitos e teoria) ou a posteriori (reflexão sobre avaliação) |
| Meta-requisitos atendidos | |
| Justificativa | |
| Instanciação (características que o materializam) | |
| Proposição testável | |
| Evidência obtida | |
| Condições de contorno | |

---

## 7. Regra tecnológica e proposição CIMO

**Regra tecnológica (adaptada de van Aken, 2004):**
> Para alcançar **[efeito Y]** em **[situação Z]**, aplique algo como **[intervenção X]**.

**Proposição CIMO (adaptada de Denyer et al., 2008):**
> Em contextos **[C]**, use intervenções **[I]** para acionar os mecanismos **[M]** e produzir os
> resultados **[O]**.

---

## 8. Plano de avaliação (FEDS)

```markdown
## Objetivos da avaliação
- Rigor (eficácia / efetividade):
- Riscos principais (humanos/sociais | técnicos):
- Ética:
- Restrições de recursos:

## Estratégia
- Estratégia FEDS: [rápida e simples | risco humano e efetividade | risco técnico e eficácia | puramente técnica]
- Justificativa:

## Episódios
```

| # | Momento | Propósito | Paradigma | Objeto avaliado | Critérios | Método | Participantes ou dados | Comparador | Limiar de sucesso | Iteração |
|---|---|---|---|---|---|---|---|---|---|---|
| E1 | Ex ante | Formativo | Artificial | Requisitos e design | Completude, viabilidade | Especialistas | 5 especialistas externos | — | Críticas tratadas | 1 |
| E2 | Ex post | Somativo | Artificial | Protótipo | Eficácia | Benchmark | Base histórica | Baseline X | ≥ baseline | 2 |

Depois, descreva cada episódio: procedimento, instrumentos, análise, ameaças e mitigação.

---

## 9. Registro de iterações

| Iteração | Datas | O que foi construído ou alterado | Episódio(s) | Principais achados | Decisões e mudanças | Conhecimento gerado |
|---|---|---|---|---|---|---|
| 1 | | | | | | |

Mantenha o registro durante o projeto; reconstruí-lo depois tende a apagar exatamente as
alternativas descartadas e os resultados negativos que demonstram a busca.

---

## 10. Declaração de contribuição

```markdown
Artefato principal: [nome] — [tipo]
Classe de problemas: [classe] — condições de contorno: [condições]
Novidade: em relação a [soluções], o artefato [diferença essencial]
Evidência: [estratégia] — [resultado principal vs. baseline]
Conhecimento de design: [princípios, regras, entendimento do problema]
Posicionamento: [quadrante], porque domínio [maduro/pouco maduro: evidência] e solução [madura/pouco madura: evidência]
Níveis: [1 / 2 / 3] — [o que corresponde a cada nível]
Implicações para pesquisa:
Implicações para prática:
```

---

## 11. DSR Grid (vom Brocke & Maedche, 2019)

| Problema | Conhecimento de entrada | Processo de pesquisa |
|---|---|---|
| Qual problema, para quem, com que evidência? | Que teorias, métodos e artefatos foram usados? | Que atividades e iterações, com quais métodos? |
| **Conceitos-chave** | **Solução** | **Conhecimento de saída** |
| Quais conceitos definem o espaço do problema e da solução? | Que artefato foi construído e como funciona? | Que conhecimento de design e que evidências foram produzidos? |

---

## 12. Canvas de teoria de design (Gregor & Jones, 2007)

| Componente | Conteúdo |
|---|---|
| 1. Propósito e escopo | |
| 2. Construtos | |
| 3. Princípios de forma e função | |
| 4. Mutabilidade do artefato | |
| 5. Proposições testáveis | |
| 6. Conhecimento justificatório | |
| 7. Princípios de implementação (opcional) | |
| 8. Instanciação expositiva (opcional) | |

---

## 13. Parecer de revisão DSR

```markdown
# Parecer — [título do manuscrito]

## 1. Síntese do trabalho
Problema, artefato, abordagem, avaliação e contribuição declarada, em 5–8 linhas e nas palavras do revisor.

## 2. Enquadramento DSR
O trabalho é DSR? O processo declarado corresponde ao seguido?

## 3. Pontos fortes

## 4. Avaliação por dimensão (R1–R10)
Para cada dimensão: avaliação curta e achados com localização.

## 5. Achados críticos
[C1] Descrição — localização — por que é crítico — o que seria necessário

## 6. Achados importantes
[I1] ...

## 7. Achados menores
[M1] ...

## 8. Verificação de citações de DSR
Atribuições incorretas ou metadados inconsistentes.

## 9. Recomendação
Aceitar | Revisão menor | Revisão maior | Rejeitar — com justificativa ligada aos achados.

## 10. Sugestões construtivas
Caminhos concretos e priorizados para fortalecer o trabalho.
```

---

## 14. Exemplo completo (ilustrativo)

Exemplo fictício para mostrar a cadeia completa; números e resultados são ilustrativos. Em um
trabalho real, cada teoria de base citada precisa de referência verificada.

**Contexto.** Centros de operações de segurança (SOC) de porte médio recebem milhares de alertas
por dia; analistas gastam a maior parte do turno em triagem, e incidentes críticos se perdem entre
falsos positivos.

**Problema de design.** Melhorar a triagem de alertas em SOCs de porte médio por meio de um método
de priorização explicável e de uma ferramenta que o implementa, que reduza o tempo de triagem sem
aumentar incidentes críticos perdidos, a fim de ajudar analistas e gestores a concentrar esforço
nos alertas relevantes.

**Classe de problemas.** Triagem de grandes volumes de alertas heterogêneos por equipes pequenas,
sob responsabilidade humana pela decisão final. Fora da classe: resposta totalmente automatizada.

**Questões.**
- QP: Como projetar um método de priorização de alertas que reduza o esforço de triagem sem
  aumentar incidentes críticos perdidos em SOCs de porte médio?
- QC1: Quais fatores levam a incidentes críticos perdidos na triagem atual?
- QC3: Qual o efeito do método sobre o tempo de triagem e o recall de incidentes críticos em
  comparação com a ordenação por severidade do SIEM?

**Requisitos.**
| ID | Requisito | Origem |
|---|---|---|
| R1 | Reduzir o tempo médio de triagem em relação ao processo atual | Entrevistas com gestores; métricas do SOC |
| R2 | Não reduzir o recall de incidentes críticos | Entrevistas; política do SOC |
| R3 | Permitir que analistas entendam e contestem cada prioridade | Entrevistas; literatura sobre confiança em automação |
| R4 | Integrar-se ao SIEM existente sem substituí-lo | Restrição organizacional |

**Princípios de design.**
- **DP1 — Justificativa contestável.** Forneça à ferramenta uma justificativa legível dos fatores
  que determinaram cada prioridade, para que analistas possam contestar prioridades incorretas
  antes de agir, dado que respondem pela decisão final sob alta carga.
- **DP2 — Contexto agregado.** Agrupe alertas correlacionados do mesmo ativo em um único item de
  triagem, para que analistas avaliem incidentes em vez de eventos isolados, dado que ataques
  geram múltiplos alertas relacionados.

**Estratégia de avaliação.** Risco humano e efetividade: o maior risco é analistas não confiarem
na priorização nem a usarem.

| # | Momento | Propósito | Paradigma | Método | Comparador | Limiar |
|---|---|---|---|---|---|---|
| E1 | Ex ante | Formativo | Artificial | Revisão de requisitos e princípios por 5 especialistas externos | — | Críticas incorporadas |
| E2 | Ex post | Formativo e somativo | Artificial | Reprocessamento de 6 meses de alertas rotulados; ablação de DP2 | Ordenação do SIEM | Recall ≥ baseline; tempo estimado menor |
| E3 | Ex post | Formativo | Naturalístico | Piloto de 2 semanas com 4 analistas; logs e entrevistas | — | Problemas de uso identificados e tratados |
| E4 | Ex post | Somativo | Naturalístico | Uso por 8 semanas; antes e depois; entrevistas | Período anterior | Tempo menor; sem aumento de críticos perdidos |

**Rastreabilidade (trecho).**
| Problema | Requisito | Princípio | Componente | Critério | Episódio | Evidência |
|---|---|---|---|---|---|---|
| Críticos perdidos no ruído | R2 | DP2 | Agrupador de alertas | Eficácia (recall) | E2, E4 | Tabelas de resultados |
| Desconfiança em automação | R3 | DP1 | Painel de justificativa | Compreensibilidade; uso | E3, E4 | Logs de contestação; entrevistas |

**Contribuição.** Melhoria (problema conhecido e bem documentado; solução nova na combinação de
priorização explicável e agregação por ativo), com contribuição de nível 1 (ferramenta avaliada) e
nível 2 (DP1 e DP2 com condições de contorno).

**Ameaças principais.** Validade de instanciação (efeitos da interface e não dos princípios —
mitigada pela ablação em E2); viés do pesquisador-projetista (métricas extraídas de logs e limiares
fixados antes); validade externa (um SOC — discutida pelas condições de contorno e pela explicação
dos mecanismos).
