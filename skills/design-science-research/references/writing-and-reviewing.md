# Escrita, publicação e revisão de DSR

## Sumário
1. Esquema de publicação (Gregor & Hevner, 2013)
2. Estrutura de tese, dissertação e qualificação
3. Questões de pesquisa, objetivos e checklist de Hevner & Chatterjee
4. Título, resumo e introdução
5. Venues e vocabulário por comunidade
6. Sínteses de uma página: DSR Grid e visual abstract
7. Rubrica de revisão de manuscritos DSR
8. Atribuições trocadas e erros de citação frequentes
9. Críticas frequentes de revisores e como responder

---

## 1. Esquema de publicação (Gregor & Hevner, 2013)

| Seção | Conteúdo esperado | Dicas |
|---|---|---|
| **1. Introdução** | Problema e relevância; questão ou objetivo de pesquisa; abordagem DSR; resumo das contribuições; estrutura do texto | Declare cedo o artefato e o tipo de contribuição; o leitor não deve chegar à seção 4 sem saber o que foi construído |
| **2. Revisão de literatura** | Conhecimento sobre o problema (Ω); soluções existentes e suas limitações (Λ); teorias de base; lacuna | Termine com critérios de comparação que reaparecem na avaliação |
| **3. Método** | Por que DSR; processo e adaptações; iterações; estratégia de avaliação; dados e participantes; ética | Justifique as escolhas; inclua figura ou tabela com o processo efetivamente seguido |
| **4. Descrição do artefato** | Requisitos; arquitetura ou estrutura; decisões de design e fundamentação; alternativas; princípios; processo de busca | Detalhe suficiente para reconstrução; material extenso em apêndice ou repositório |
| **5. Avaliação** | Episódios, métodos, critérios, resultados, ameaças à validade | Organize por requisito ou por episódio, mas mantenha a ligação requisito → resultado |
| **6. Discussão** | Interpretação; contribuição ao conhecimento (quadrante, nível, princípios); implicações para pesquisa e prática; generalização; limitações | É aqui que o artefato vira conhecimento |
| **7. Conclusões** | Resposta às questões; contribuições; trabalhos futuros | Sem resultados novos |

A ordem é flexível: em projetos com várias iterações, descrição do artefato e avaliação podem se
alternar por ciclo.

---

## 2. Estrutura de tese, dissertação e qualificação

### Opção A — Monografia tradicional
1. **Introdução** — contexto, problema, motivação, questões, objetivos, contribuições, estrutura.
2. **Fundamentação teórica** — conceitos e teorias de base (Ω).
3. **Trabalhos relacionados** — estado da arte das soluções (Λ), com tabela comparativa por
   critérios que voltarão na avaliação.
4. **Metodologia** — DSR e justificativa; processo e adaptações; mapa *etapas do processo ×
   capítulos*; estratégia de avaliação; protocolo; ética; visão geral das iterações.
5. **Investigação do problema e requisitos** — quando há estudo próprio do problema.
6. **Artefato** — design, decisões, alternativas, princípios.
7. **Avaliação** — episódios e resultados.
8. **Discussão** — contribuições (quadrante, níveis), princípios de design, generalização,
   implicações, limitações.
9. **Conclusão** — respostas às questões e trabalhos futuros.

### Opção B — Por iterações
Após a metodologia, um capítulo por ciclo de design (refinamento do problema → design → avaliação →
aprendizagens → mudanças), seguido de discussão consolidada. Mostra a busca e a evolução do
artefato de forma natural; exige disciplina para não repetir conteúdo.

### Opção C — Coletânea de artigos
- Capítulo introdutório integrador que apresenta o arco DSR completo.
- Tabela que posiciona cada artigo: atividade do processo, ciclo, episódio de avaliação,
  contribuição.
- Textos de ligação entre artigos explicando o que cada um mudou no artefato.
- Discussão integrada com a contribuição global, que não é a soma dos artigos.
- Artigos publicados em venues de computação podem não usar o vocabulário DSR; o capítulo
  integrador faz a tradução.

### Qualificação ou proposta
A banca espera ver: evidência do problema; requisitos preliminares com origem; design inicial ou
protótipo; plano de avaliação com estratégia e episódios; cronograma por iterações; riscos e
alternativas; aspectos éticos. Um protocolo DSR (`templates.md` §1) cobre esses itens.

---

## 3. Questões de pesquisa, objetivos e checklist

### Questão principal (problema de design)
- "Como projetar [artefato ou classe de artefatos] para [objetivo] em [contexto ou classe de
  contextos]?"
- "Quais princípios de design orientam [classe de artefatos] para alcançar [objetivo] em
  [classe de contextos]?"

### Subquestões (questões de conhecimento, à maneira de Wieringa, 2014)
| Finalidade | Modelo |
|---|---|
| Investigação do problema | "Quais são as causas e os efeitos de [problema] em [contexto]?" |
| Requisitos | "Que requisitos um [artefato] deve satisfazer para [objetivo] segundo [stakeholders ou literatura]?" |
| Efeito | "Qual o efeito de [artefato] sobre [critério] em comparação com [baseline] em [contexto]?" |
| Trade-off | "Como [alternativas de design] se comparam quanto a [critérios]?" |
| Sensibilidade | "Como o efeito de [artefato] varia com [característica do contexto]?" |

Separe explicitamente a questão de design (resposta: um artefato) das questões de conhecimento
(resposta: fatos ou explicações).

### Objetivos
- **Geral:** "Projetar e avaliar [artefato] para [objetivo] em [contexto]."
- **Específicos**, formulados como resultados e alinhados às atividades do processo:
  "caracterizar [problema] em [contexto]"; "definir requisitos para [artefato]"; "projetar e
  instanciar [artefato]"; "avaliar [artefato] quanto a [critérios]"; "derivar princípios de design
  para [classe]".
- Evite objetivos que são tarefas ("realizar revisão de literatura", "estudar o tema").

### Checklist de DSR (Hevner & Chatterjee, 2010)
Use como autoverificação de proposta ou manuscrito:
1. Qual é a questão de pesquisa (requisitos de design)?
2. Qual é o artefato e como é representado?
3. Que processos de design (heurísticas de busca) serão usados para construí-lo?
4. Como o artefato e os processos de design se apoiam na base de conhecimento? Que teorias os
   sustentam?
5. Que avaliações são feitas nos ciclos internos de design e que melhorias elas geram?
6. Como o artefato é introduzido no ambiente de aplicação e testado em campo? Que métricas mostram
   sua utilidade e sua melhoria em relação a artefatos anteriores?
7. Que conhecimento novo é adicionado à base de conhecimento, e em que forma?
8. A questão de pesquisa foi respondida satisfatoriamente?

---

## 4. Título, resumo e introdução

### Títulos
- "[Nome do artefato]: [tipo de artefato] para [objetivo] em [contexto]"
- "Projetando [classe de artefato] para [objetivo]: princípios de design e avaliação em [contexto]"
Evite títulos que nomeiam só a tecnologia ("Uma solução baseada em X").

### Resumo estruturado
1. Contexto e problema (1–2 frases, com dado de relevância se possível)
2. Lacuna nas soluções atuais
3. Objetivo
4. Método: DSR, processo, número de iterações
5. Artefato: o que é, em uma frase
6. Avaliação: estratégia, métodos, participantes ou dados
7. Resultados principais, com números
8. Contribuição: conhecimento de design e implicações

### Movimentos da introdução
1. Por que o problema importa (evidência).
2. O que já se tentou e por que não basta.
3. O que este trabalho faz (artefato e abordagem).
4. Como foi avaliado e o que se encontrou.
5. Lista de contribuições, verificáveis e específicas.
6. Estrutura do texto.

---

## 5. Venues e vocabulário por comunidade

As expectativas mudam muito entre comunidades. Verifique sempre as chamadas e as normas atuais da
venue-alvo.

| Comunidade | Exemplos de venues | Expectativas |
|---|---|---|
| Sistemas de Informação | MIS Quarterly, ISR, JMIS, JAIS, EJIS, BISE; conferências DESRIST, ICIS, ECIS, PACIS, AMCIS, HICSS | Vocabulário DSR explícito; abstração (princípios ou teoria); discussão de contribuição; frameworks canônicos citados |
| Engenharia de software | ICSE, FSE, ESEM; EMSE, IST, JSS, TSE | Regras tecnológicas; validação empírica rigorosa; ameaças à validade; artefatos disponíveis. Os ACM SIGSOFT Empirical Standards têm um padrão para pesquisa de engenharia (design science) — consulte a versão atual |
| Computação, sistemas, redes, segurança | Conferências e periódicos da área | Raramente usam "DSR"; esperam modelo de ameaça ou de sistema, objetivos de projeto, análise, implementação e avaliação experimental forte contra o estado da arte |
| Gestão e engenharia de produção | Periódicos de operações e gestão; no Brasil, p. ex., Gestão & Produção | Regras tecnológicas, CIMO, Dresch et al.; relevância gerencial |
| Brasil — SI | SBSI; iSys — Revista Brasileira de Sistemas de Informação | Vocabulário DSR bem aceito; contribuições aplicadas |

### DSR em artigos de computação e segurança
Mantenha a lógica e troque o vocabulário:

| Elemento DSR | Seção típica | Como escrever |
|---|---|---|
| Problema e relevância | Introdução, motivação | Cenário concreto, custo ou impacto, limitações do estado da arte |
| Base de conhecimento (Ω) | Background | Conceitos e pressupostos necessários |
| Requisitos | Modelo de ameaça ou de sistema; objetivos de projeto; não objetivos | Objetivos numerados, referenciados depois na avaliação |
| Artefato e decisões | Design ou arquitetura; protocolo | Cada decisão ligada a um objetivo; alternativas em "design alternatives" ou na discussão |
| Avaliação analítica | Análise de segurança; provas | Propriedades sob o modelo de ameaça |
| Instanciação | Implementação | Detalhes suficientes para reprodução; código disponível |
| Avaliação empírica | Evaluation | Perguntas de avaliação explícitas; baselines; ablação |
| Conhecimento de design | Discussion, lessons learned | Lições generalizáveis e condições em que valem |
| Estado da arte das soluções (Λ) | Related work | Comparação por dimensões, não lista de trabalhos |
| Limitações | Limitations, discussion | Pressupostos, ameaças, fora de escopo |

Na tese, o capítulo de metodologia pode explicitar DSR e mapear os artigos para o processo, mesmo
que os artigos não usem o termo.

---

## 6. Sínteses de uma página

### DSR Grid (vom Brocke & Maedche, 2019)
Seis dimensões para planejar e comunicar um projeto numa página: **problema**, **conhecimento de
entrada**, **processo de pesquisa**, **conceitos-chave**, **solução** e **conhecimento de saída**.
Útil em propostas, qualificações, pôsteres e para alinhar com orientador. Modelo em
`templates.md` §11.

### Visual abstract (Storey et al., 2017)
Para engenharia de software: regra tecnológica no centro; instância do problema, conceituação do
problema, projeto da solução e validação empírica em volta; e avaliação em três lentes —
relevância, rigor e novidade.

---

## 7. Rubrica de revisão de manuscritos DSR

Se outra rubrica geral de revisão estiver em uso, esta a complementa com as dimensões específicas de
DSR. Para cada dimensão, registre achados com localização (seção, figura, tabela) e severidade.

**Severidade:**
- **Crítico** — compromete a existência da contribuição ou a validade das conclusões principais
  (p. ex., sem avaliação, novidade inexistente, afirmações sem evidência).
- **Importante** — enfraquece significativamente o trabalho, mas é corrigível (baseline fraco,
  requisitos sem origem, ameaças à validade ausentes).
- **Menor** — clareza, terminologia, apresentação.

| # | Dimensão | Perguntas-guia |
|---|---|---|
| R1 | **Enquadramento** | A pergunta é prescritiva? DSR é a abordagem adequada e está justificado? O processo declarado é o seguido? |
| R2 | **Problema e relevância** | Há evidência do problema? Stakeholders identificados? Classe de problemas definida? |
| R3 | **Base de conhecimento** | O estado da arte das soluções está mapeado com critérios? As teorias de base são usadas nas decisões de design? |
| R4 | **Requisitos** | Explícitos, verificáveis e com origem? Definidos antes da avaliação? |
| R5 | **Artefato e busca** | Descrição suficiente para reconstrução? Decisões justificadas? Alternativas e iterações relatadas? |
| R6 | **Avaliação** | Estratégia justificada pelos riscos? Critérios ligados aos requisitos? Métodos adequados ao tipo de artefato? Baseline adequado? Formativa e somativa? Participantes e dados adequados? Ética? |
| R7 | **Resultados vs. afirmações** | As conclusões se limitam ao que a evidência mostra? Resultados negativos relatados? |
| R8 | **Contribuição e novidade** | Quadrante e nível plausíveis? Conhecimento de design explícito, além do artefato? |
| R9 | **Generalização e limites** | Condições de contorno declaradas? Validade de instanciação discutida? Ameaças específicas? |
| R10 | **Comunicação e reprodutibilidade** | Estrutura clara para públicos técnicos e gerenciais? Artefato, instrumentos e dados disponíveis? Citações de DSR corretas (§8)? |

**Síntese da recomendação:**
- Nenhum achado crítico e poucos importantes → aceitar ou revisão menor.
- Achados importantes corrigíveis dentro do escopo do estudo → revisão maior.
- Achado crítico que exige novo estudo (p. ex., avaliação inexistente) → rejeitar ou reenviar como
  novo trabalho.

Estrutura do parecer em `templates.md` §13.

---

## 8. Atribuições trocadas e erros de citação frequentes

| Conceito | Fonte correta | Erro comum |
|---|---|---|
| Sete diretrizes de DSR | Hevner, March, Park & Ram (2004), *MIS Quarterly* 28(1) | Atribuir a Peffers et al. ou a Hevner (2007) |
| Três ciclos (relevância, design, rigor) | Hevner (2007), *Scandinavian Journal of Information Systems* 19(2) | Atribuir a Hevner et al. (2004) |
| DSRM (seis atividades, pontos de entrada) | Peffers, Tuunanen, Rothenberger & Chatterjee (2007), *JMIS* 24(3) | "DSRM de Hevner" |
| Construtos, modelos, métodos, instanciações | March & Smith (1995) | Citar só Hevner et al. (2004), que adotam a tipologia citando March & Smith |
| Melhoria, invenção, exaptação, design rotineiro; níveis 1–3 | Gregor & Hevner (2013) | Atribuir a Hevner et al. (2004) |
| FEDS e as quatro estratégias | Venable, Pries-Heje & Baskerville (2016), *EJIS* 25(1) | Citar o framework de 2012 ou as estratégias de 2008 como FEDS |
| Ex ante / ex post; artificial / naturalística | Pries-Heje, Baskerville & Venable (2008); Venable et al. (2012) | Atribuir a Hevner |
| ADR (estágios e sete princípios) | Sein, Henfridsson, Purao, Rossi & Lindgren (2011) | Atribuir a Hevner; confundir com pesquisa-ação clássica |
| eADR | Mullarkey & Hevner (2019) | — |
| Oito componentes da teoria de design | Gregor & Jones (2007) | Confundir com ISDT de Walls et al. (1992) |
| Anatomia de princípio de design | Gregor, Chandra Kruse & Seidel (2020) | — |
| Regra tecnológica | van Aken (2004) | Atribuir à engenharia de software em geral |
| CIMO | Denyer, Tranfield & van Aken (2008) | — |
| Ciclo de design e ciclo de engenharia; problemas de design vs. questões de conhecimento | Wieringa (2014) | — |
| DSR Grid | vom Brocke & Maedche (2019) | — |
| *The Sciences of the Artificial* | Simon — 1ª ed. 1969; 3ª ed. 1996 | Citar ano de uma edição com a paginação de outra |

Outros cuidados: confirme páginas, volume e número em `bibliography.md`; não use DOI de capítulo
para citar o livro inteiro (e vice-versa); indique a edição usada.

---

## 9. Críticas frequentes de revisores e como responder

| Crítica | O que geralmente está por trás | Como responder (e o que mudar) |
|---|---|---|
| "É só engenharia ou desenvolvimento" | Conhecimento de design implícito; novidade não posicionada | Explicitar princípios ou regras; posicionar na matriz de Gregor & Hevner; comparar com soluções anteriores |
| "A avaliação é fraca" | Só demonstração ou só percepção; sem baseline | Adicionar episódio somativo; justificar a estratégia FEDS; incluir baseline e ameaças; se não for possível, reduzir as afirmações |
| "Não há contribuição teórica" | Venue espera abstração | Abstrair princípios com justificativa; argumentar com Baskerville et al. (2018) quando o artefato é a contribuição; ou mudar de venue |
| "Os resultados não generalizam" | Contexto único; classe de problemas vaga | Condições de contorno; explicação por mecanismos; contexto adicional se viável; linguagem calibrada |
| "Por que DSR e não outro método?" | Pergunta não formulada como prescritiva | Reformular a questão; justificar pela natureza do problema |
| "Os requisitos parecem arbitrários" | Origem não documentada | Tabela de requisitos com fontes; matriz de rastreabilidade |
| "O pesquisador avaliou o próprio artefato" | Risco de viés | Relatar mitigação; avaliadores independentes; dados brutos; limiares definidos antes |
| "O artefato não está descrito o suficiente" | Descrição narrativa sem especificação | Especificação, modelos, pseudocódigo, repositório |
| "Frameworks citados sem uso" | Salada de frameworks | Dizer o que cada framework organiza e onde aparece; remover o que não é usado |

### Carta de resposta
1. Agradecimento breve e resumo das principais mudanças.
2. Para cada comentário: transcrição ou resumo do comentário → resposta → mudança feita, com
   localização (seção, página, tabela).
3. Quando discordar: reconheça a preocupação, apresente evidência ou literatura, e mostre o que foi
   ajustado para evitar o mal-entendido.
4. Não prometa mudanças que não estão no texto revisado.
