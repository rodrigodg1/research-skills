# Processos e frameworks de DSR

Conteúdo parafraseado das fontes originais. Ao escrever texto acadêmico, cite a fonte primária
(ver `bibliography.md`) e deixe claro quando houver adaptação.

## Sumário
1. Fundamentos: ciências do artificial e paradigma de design
2. Hevner et al. (2004): sete diretrizes
3. Hevner (2007): três ciclos; Drechsler & Hevner (2016): quarto ciclo
4. Peffers et al. (2007): Design Science Research Methodology (DSRM)
5. Vaishnavi & Kuechler: ciclo geral de design
6. Wieringa (2014): ciclo de design e ciclo de engenharia
7. Action Design Research (Sein et al., 2011) e eADR (Mullarkey & Hevner, 2019)
8. Dresch, Lacerda & Antunes Jr. (2015)
9. Duas estratégias de DSR (Iivari, 2015)
10. DSR em engenharia de software e computação
11. Como escolher e combinar
12. Tabela de equivalências

---

## 1. Fundamentos

**Ciências do artificial (Simon, 1996).** As ciências naturais descrevem como as coisas são; as
ciências do artificial tratam de como as coisas deveriam ser para atingir objetivos. Projetar é
conceber cursos de ação que transformam situações existentes em situações preferidas. Um
artefato é a interface entre um *ambiente interno* (sua organização e substância) e um *ambiente
externo* (o contexto em que opera). Em problemas complexos, busca-se uma solução satisfatória
(*satisficing*), não necessariamente ótima.

**Paradigmas complementares (Hevner et al., 2004).** A pesquisa comportamental busca verdade:
desenvolver e justificar teorias que explicam ou predizem fenômenos. DSR busca utilidade:
construir e avaliar artefatos. Os dois se alimentam: teorias informam o design, e artefatos em
uso geram fenômenos a explicar.

**Saídas e atividades (March & Smith, 1995).** Quatro tipos de saída (construtos, modelos,
métodos, instanciações) cruzados com quatro atividades (construir, avaliar, teorizar,
justificar). As duas primeiras são típicas de design science; as duas últimas, de ciência
natural. Detalhes em `contributions-and-theory.md` §1.

**Precursor em SI.** Nunamaker et al. (1990) defenderam o desenvolvimento de sistemas como
metodologia de pesquisa, antecipando vários elementos da DSR.

**Princípios do memorando alemão (Österle et al., 2011).** Pesquisa orientada a design deve
atender a quatro princípios: *abstração* (aplicável a uma classe de problemas), *originalidade*
(contribui para o corpo de conhecimento), *justificação* (validável de forma compreensível) e
*benefício* (gera valor para stakeholders, hoje ou no futuro).

**Postura epistemológica.** DSR costuma ser associada ao pragmatismo: conhecimento válido é o que
funciona para resolver problemas, e aprende-se construindo e avaliando. Declare a postura na
metodologia apenas se o público espera (comum em teses e em SI).

**Terminologia.** Evite usar indistintamente *design science* (o paradigma e o corpo de
conhecimento), *design science research* (a atividade de pesquisa) e *design research* (que em
algumas áreas significa pesquisa sobre o processo de design). Dresch et al. (2015) distinguem
explicitamente design science (base epistemológica) de design science research (método que a
operacionaliza).

---

## 2. Hevner et al. (2004): sete diretrizes

Os autores apresentam as diretrizes como apoio ao julgamento de pesquisadores, revisores e
editores, não como checklist obrigatório. Use-as para *examinar* um projeto, não para
*declarar* conformidade.

| # | Diretriz | O que pede (paráfrase) | O que evidenciar | Falha típica |
|---|---|---|---|---|
| 1 | Design como artefato | Produzir um artefato viável: construto, modelo, método ou instanciação | Descrição reproduzível; artefato efetivamente construído | Ideia ou esboço apresentado como artefato |
| 2 | Relevância do problema | Soluções para problemas importantes e relevantes | Stakeholders; dados; custo do problema; lacuna das soluções atuais | Problema inventado para caber na solução |
| 3 | Avaliação do design | Utilidade, qualidade e eficácia demonstradas com métodos bem executados | Estratégia, critérios, métricas, baseline, resultados | Evidência anedótica ou só demonstração |
| 4 | Contribuições de pesquisa | Contribuições claras e verificáveis no artefato, nos fundamentos de design ou nas metodologias de design | Declaração de contribuição comparada ao estado da arte | "Contribuição" = ter construído algo |
| 5 | Rigor da pesquisa | Métodos rigorosos na construção e na avaliação | Fundamentação na base de conhecimento; métodos de avaliação adequados | Rigor só na avaliação, design arbitrário |
| 6 | Design como busca | Usar meios disponíveis para atingir fins desejados, respeitando as leis do ambiente | Alternativas, iterações, heurísticas, trade-offs | Solução apresentada como óbvia e única |
| 7 | Comunicação | Apresentar a públicos orientados a tecnologia e a gestão | Detalhe técnico suficiente e implicações práticas | Texto só técnico ou só gerencial |

Os métodos de avaliação propostos no mesmo artigo estão em `evaluation.md` §1.

---

## 3. Três ciclos (Hevner, 2007) e quarto ciclo (Drechsler & Hevner, 2016)

**Ciclo de relevância.** Liga o ambiente de aplicação (pessoas, sistemas organizacionais,
sistemas técnicos, problemas e oportunidades) à pesquisa. Traz requisitos e critérios de
aceitação; leva o artefato de volta ao ambiente para teste de campo. Se o teste de campo revela
deficiências, inicia-se nova iteração.

**Ciclo de rigor.** Liga a pesquisa à base de conhecimento. Traz teorias e métodos científicos,
experiência e expertise do domínio e artefatos ou processos de design existentes. Devolve à base
extensões de teorias e métodos, novos meta-artefatos (produtos e processos de design) e
experiência. Hevner enfatiza que o pesquisador precisa demonstrar que o artefato é de fato novo,
e não aplicação rotineira de conhecimento conhecido.

**Ciclo de design.** O núcleo: iteração rápida entre construir e avaliar alternativas até obter
um design satisfatório. O esforço deve se equilibrar entre construção e avaliação; ambos
precisam estar fundamentados nos outros dois ciclos.

**Como usar na escrita.** Uma tabela que mostre, para cada ciclo, o que entrou e o que saiu do
projeto é uma forma compacta de demonstrar relevância e rigor:

| Ciclo | Entradas no projeto | Saídas do projeto |
|---|---|---|
| Relevância | Problema, stakeholders, requisitos, critérios de aceitação | Artefato testado em campo; evidências de utilidade |
| Rigor | Teorias de base, métodos, artefatos anteriores | Princípios de design, extensões de teoria, novos métodos |
| Design | Alternativas, protótipos, avaliações formativas | Artefato final; histórico de iterações |

**Quarto ciclo — mudança e impacto (Drechsler & Hevner, 2016).** Acrescenta um ciclo que liga o
contexto imediato de aplicação a um ambiente mais amplo e dinâmico. Captura a necessidade de o
artefato evoluir quando o ambiente muda e os efeitos que o próprio artefato provoca na
organização, gerando novos esforços de design. Útil para plataformas, sistemas de longa duração,
ecossistemas e ambientes voláteis.

---

## 4. DSRM (Peffers et al., 2007)

Processo nominal em seis atividades, com retornos iterativos da avaliação e da comunicação para
a definição de objetivos e para o projeto.

### Atividade 1 — Identificação do problema e motivação
Definir o problema de pesquisa específico e justificar o valor de uma solução. Decompor o
problema conceitualmente ajuda a solução a capturar sua complexidade. Recursos: conhecimento do
estado do problema e da importância de resolvê-lo.
**Na tese:** capítulo de introdução e, se houver, estudo exploratório do problema.

### Atividade 2 — Definição dos objetivos da solução
Inferir objetivos a partir da definição do problema e do conhecimento sobre o que é possível e
viável. Objetivos podem ser **quantitativos** (em que termos a nova solução seria melhor que as
atuais) ou **qualitativos** (como o artefato apoiará soluções para problemas ainda não
tratados). Recursos: conhecimento sobre soluções atuais e sua eficácia.
**Na tese:** requisitos e objetivos de design, com origem rastreável.

### Atividade 3 — Projeto e desenvolvimento
Criar o artefato: determinar funcionalidade e arquitetura desejadas e então construí-lo.
Recursos: teoria aplicável à solução.
**Na tese:** capítulo do artefato, com decisões de design e fundamentação.

### Atividade 4 — Demonstração
Mostrar o uso do artefato para resolver uma ou mais instâncias do problema — por experimento,
simulação, estudo de caso, prova ou outra atividade apropriada. Recursos: conhecimento de como
usar o artefato.

### Atividade 5 — Avaliação
Observar e medir quão bem o artefato apoia a solução, comparando objetivos com resultados
observados. Pode incluir comparação de funcionalidades com objetivos, medidas quantitativas de
desempenho, pesquisas de satisfação, feedback de clientes ou simulações. Ao final, decide-se
voltar à atividade 2 ou 3 ou seguir para a comunicação.

### Atividade 6 — Comunicação
Comunicar o problema e sua importância, o artefato, sua utilidade e novidade, o rigor do design
e sua eficácia a pesquisadores e a outros públicos relevantes, como profissionais. Os autores
sugerem que a estrutura do processo pode organizar artigos acadêmicos, assim como o processo
empírico nominal organiza artigos empíricos.

### Pontos de entrada
| Entrada | Começa em | Situação típica |
|---|---|---|
| Iniciação centrada no problema | Atividade 1 | Problema observado ou sugerido por pesquisa anterior |
| Solução centrada em objetivos | Atividade 2 | Necessidade da indústria ou da pesquisa que pode ser atendida por um artefato |
| Iniciação centrada em projeto e desenvolvimento | Atividade 3 | Artefato existente ainda não pensado formalmente como solução para um domínio de problemas |
| Iniciação pelo cliente ou contexto | Atividade 4 | Solução prática que funcionou; pesquisadores trabalham de trás para frente aplicando rigor |

Ao usar uma entrada que não seja a atividade 1, diga isso explicitamente na metodologia. É mais
defensável do que narrar um processo linear que não aconteceu.

---

## 5. Ciclo geral de design (Vaishnavi & Kuechler)

Derivado de modelos de processo de design em engenharia e adotado por Kuechler & Vaishnavi (2008)
e Vaishnavi & Kuechler (2015).

| Fase | Saída |
|---|---|
| Consciência do problema (*awareness of problem*) | Proposta |
| Sugestão (*suggestion*) | Design tentativo |
| Desenvolvimento (*development*) | Artefato |
| Avaliação (*evaluation*) | Medidas de desempenho |
| Conclusão (*conclusion*) | Resultados |

**Fluxos de conhecimento.** Quando o desenvolvimento ou a avaliação revelam que o artefato não
se comporta como previsto, gera-se conhecimento de *circunscrição* (*circumscription*): entende-se
melhor as restrições e os limites da teoria, e o ciclo volta à consciência do problema. Há
também conhecimento de *operação e objetivo* (*operation and goal knowledge*) produzido ao longo
do ciclo.

**Ênfase.** Este modelo destaca DSR como geradora e refinadora de teoria: Kuechler & Vaishnavi
(2008) mostram como um projeto de design pode estender uma teoria de base, e Kuechler &
Vaishnavi (2012) discutem teorias de design e teorias explicativas relevantes para design.
A fase de conclusão registra também "pontas soltas" — comportamentos não explicados que viram
agenda de pesquisa.

---

## 6. Wieringa (2014)

**Objeto.** Design science é o projeto e a investigação de artefatos *em contexto*. Um artefato
sozinho não resolve nada; o que produz efeitos é a interação artefato × contexto (o
*tratamento*).

**Dois tipos de problema — mantenha separados.**
- **Problemas de design** pedem mudança no mundo; têm muitas soluções possíveis, avaliadas pela
  utilidade para os objetivos dos stakeholders.
- **Questões de conhecimento** pedem conhecimento sobre o mundo; têm uma resposta (possivelmente
  incerta), avaliada pela verdade.
Um projeto DSR é uma hierarquia de problemas de design e questões de conhecimento aninhados.
Misturá-los numa única "questão de pesquisa" gera confusão sobre o que conta como resposta.

**Modelo para problema de design (paráfrase):**
> Melhorar <contexto do problema>
> por meio de <(re)projeto de um artefato>
> que satisfaça <requisitos>
> a fim de <ajudar stakeholders a alcançar objetivos>.

**Ciclo de design.**
1. *Investigação do problema*: stakeholders, objetivos, fenômenos, causas, mecanismos, efeitos;
   avaliação da situação atual.
2. *Projeto do tratamento*: especificar requisitos, examinar tratamentos disponíveis, projetar
   novos.
3. *Validação do tratamento*: prever os efeitos do artefato no contexto, antes da implantação
   real. Questões típicas:
   - efeito: artefato × contexto → que efeitos? Satisfazem os requisitos?
   - trade-off: artefatos alternativos × contexto → efeitos?
   - sensibilidade: artefato × contextos alternativos → efeitos?

**Ciclo de engenharia.** Ciclo de design mais *implementação do tratamento* (transferência para
o mundo real) e *avaliação da implementação* (que funciona como nova investigação de problema).
DSR acadêmico geralmente vai até a validação; a implementação real costuma ficar fora do escopo.

**Métodos de validação.**
| Método | Descrição | Quando usar |
|---|---|---|
| Opinião de especialistas | Especialistas preveem efeitos do artefato no contexto | Cedo; barato; não substitui testes |
| Experimento de mecanismo em caso único | Protótipo testado em contexto simulado; comportamento explicado por mecanismos | Artefatos técnicos; engenharia de software |
| Pesquisa-ação técnica (TAR) | Pesquisador usa o artefato para ajudar um cliente real e aprende com isso | Transição do laboratório para a prática |
| Experimento estatístico de diferença | Grupos com e sem tratamento comparados estatisticamente | Quando há amostra suficiente e controle |

Na TAR (Wieringa & Moralı, 2012), o pesquisador acumula papéis — projetista do artefato,
pesquisador empírico que responde a questões de conhecimento e ajudante do cliente — e precisa
separá-los conscientemente.

**Generalização.** Por analogia, com base em semelhança de arquitetura entre casos (mesmos
componentes e mecanismos), e por ampliação gradual das condições: do laboratório a condições
cada vez mais realistas (*scaling up*).

**Atenção terminológica.** Em Wieringa, *validação* ocorre antes da implantação e *avaliação* é
da implementação real. Em Peffers et al. (2007), *avaliação* cobre ambos. Defina os termos no
texto.

---

## 7. Action Design Research

### ADR (Sein et al., 2011)
**Motivação.** Artefatos de TI são moldados pelo contexto organizacional durante o
desenvolvimento e o uso. Separar "construir" e "avaliar" em etapas estanques ignora isso; ADR
entrelaça construção, intervenção e avaliação.

| Estágio | Princípios |
|---|---|
| 1. Formulação do problema | P1 Pesquisa inspirada na prática — problemas de campo como oportunidades de criar conhecimento; P2 Artefato impregnado de teoria — teorias informam o artefato |
| 2. Construção, intervenção e avaliação (BIE) | P3 Moldagem recíproca — artefato e contexto organizacional se influenciam; P4 Papéis mutuamente influentes — pesquisadores e praticantes aprendem uns com os outros; P5 Avaliação autêntica e concorrente — avaliação contínua, não etapa final |
| 3. Reflexão e aprendizagem | P6 Emergência guiada — o artefato reflete o design inicial e a moldagem contínua pelo uso e pela avaliação |
| 4. Formalização da aprendizagem | P7 Resultados generalizados — generalizar instância do problema para classe de problemas, instância da solução para classe de soluções e derivar princípios de design |

**Estágio 1 envolve:** conceber a oportunidade de pesquisa, formular questões iniciais, tratar o
problema como instância de uma classe, identificar bases teóricas e avanços tecnológicos
anteriores, garantir compromisso organizacional de longo prazo e definir papéis.

**Esquemas de BIE.**
- *Dominado por TI*: inovação tecnológica; versão alfa com avaliação em contexto limitado,
  versão beta em uso organizacional mais amplo.
- *Dominado pela organização*: inovação principalmente na intervenção organizacional.

**Quando usar.** O pesquisador tem acesso e papel ativo em uma organização, o artefato só faz
sentido em uso, e praticantes participam do design. **Quando evitar.** Artefatos puramente
técnicos avaliados em laboratório; nesse caso, ADR vira rótulo.

**Cuidados.** Documente intervenções (quem decidiu o quê, quando, com base em quê), gerencie o
viés de quem é simultaneamente designer e avaliador e registre as mudanças no contexto.

### eADR (Mullarkey & Hevner, 2019)
Elabora o ADR em quatro estágios — **diagnóstico, design, implementação e evolução** — cada um
executando seu próprio ciclo ADR (formulação do problema e planejamento, criação do artefato,
avaliação, reflexão e aprendizagem). Permite entrar no processo em qualquer estágio e reconhece
que cada estágio pode gerar seus próprios artefatos e contribuições, por exemplo artefatos de
diagnóstico do problema.

---

## 8. Dresch, Lacerda & Antunes Jr. (2015)

Referência muito usada no Brasil, especialmente em engenharia de produção e gestão (há edição em
português pela Bookman, 2015; ver também Lacerda et al., 2013).

**Etapas do método:**
1. Identificação do problema
2. Conscientização do problema
3. Revisão sistemática da literatura
4. Identificação dos artefatos e configuração das classes de problemas
5. Proposição de artefatos para resolver o problema específico
6. Projeto do artefato selecionado
7. Desenvolvimento do artefato
8. Avaliação do artefato
9. Explicitação das aprendizagens
10. Conclusões
11. Generalização para uma classe de problemas
12. Comunicação dos resultados

**Conceitos centrais.**
- **Classe de problemas:** organização de um conjunto de problemas, práticos ou teóricos, que
  contém artefatos úteis para a ação. Configurá-la cedo (etapa 4) orienta a revisão de literatura
  e a generalização (etapa 11).
- A revisão sistemática aparece como etapa explícita, o que reforça o ciclo de rigor.
- Aprendizagens e generalização são etapas próprias, não apêndices da avaliação.

**Quando usar.** Bancas brasileiras de engenharia de produção, administração e áreas afins que
conhecem o método; projetos que precisam de revisão sistemática formal. Pode ser combinado com
FEDS para detalhar a avaliação.

---

## 9. Duas estratégias de DSR (Iivari, 2015)

| | Estratégia 1 | Estratégia 2 |
|---|---|---|
| Ponto de partida | Conceito de solução geral (meta-artefato) para uma classe de problemas | Problema específico de um cliente |
| Movimento | Do geral para instâncias: construir o meta-artefato, instanciar e avaliar | Do específico para o geral: construir artefato concreto em contexto e depois destilar conhecimento prescritivo |
| Proximidade | DSR "clássico" de laboratório e campo | ADR e pesquisa-ação |
| Desafio de generalização | Mostrar que funciona em contextos reais variados | Mostrar que o aprendizado vale além do cliente |

Declarar a estratégia ajuda a justificar o desenho de avaliação e as afirmações de
generalidade.

---

## 10. DSR em engenharia de software e computação

**Par problema–solução e regra tecnológica.** Runeson et al. (2020) e Engström et al. (2020)
enquadram pesquisa em engenharia de software como DSR: uma instância de problema e uma instância
de solução, ligadas por três atividades — conceituação do problema, projeto da solução e
validação empírica — e uma **regra tecnológica** como contribuição generalizável:
> Para alcançar <efeito> em <situação>, aplique <intervenção>.

**Visual abstract (Storey et al., 2017).** Um quadro de uma página com a regra tecnológica, as
três atividades e a avaliação do estudo em três lentes: **relevância** (a regra importa para
praticantes?), **rigor** (a validação sustenta a regra?) e **novidade** (a regra é nova?).
Engström et al. (2020) usaram essas lentes para analisar artigos de engenharia de software.

**Computação e segurança.** Artigos de sistemas, redes e segurança costumam seguir a lógica DSR
sem o nome: motivação e modelo de ameaça (problema), objetivos de projeto (requisitos),
arquitetura e protocolo (artefato), análise de segurança ou provas (avaliação analítica),
implementação (instanciação), benchmarks contra baselines (avaliação experimental). Ver
`writing-and-reviewing.md` §5 para o mapeamento de seções.

---

## 11. Como escolher e combinar

| Situação | Processo recomendado | Por quê |
|---|---|---|
| Artefato de TI ou SI, público de Sistemas de Informação | DSRM + três ciclos | Mais reconhecido; atividades claras; ciclos explicitam rigor e relevância |
| Artefato construído dentro de uma organização, com intervenção do pesquisador | ADR ou eADR | Entrelaça construção, intervenção e avaliação em contexto real |
| Engenharia de software ou sistemas; foco em validar antes de implantar | Wieringa | Separa problemas de design e questões de conhecimento; métodos de validação detalhados |
| Ênfase em construir ou refinar teoria de design | Vaishnavi & Kuechler | Circunscrição e conclusão explicitam aprendizado teórico |
| Engenharia de produção ou gestão no Brasil | Dresch et al. | Familiar a bancas; classe de problemas e revisão sistemática explícitas |
| Computação ou segurança em venues que não usam "DSR" | Wieringa ou par problema–solução com regra tecnológica, no vocabulário da área | Rigor de DSR sem jargão estranho à comunidade |
| Artefato longevo em ambiente volátil | Três ciclos + ciclo de mudança e impacto | Captura evolução e efeitos do artefato |

**Pilha coerente frequente:** DSRM para o processo, três ciclos para relevância e rigor, FEDS
para a avaliação e matriz de Gregor & Hevner para a contribuição. Cada framework cumpre um papel
distinto.

**Evite a "salada de frameworks":** citar cinco modelos sem dizer que papel cada um cumpre no
projeto. Para cada framework citado, a metodologia deve dizer *o que ele organiza* e *onde isso
aparece* no trabalho.

**Adaptações** são legítimas quando declaradas e justificadas (p. ex., "a atividade de
demonstração foi incorporada ao primeiro episódio de avaliação porque…").

---

## 12. Tabela de equivalências

Correspondência aproximada; os modelos não são isomórficos.

| DSRM (Peffers) | Ciclos (Hevner) | Vaishnavi & Kuechler | Wieringa | ADR (Sein et al.) | Dresch et al. |
|---|---|---|---|---|---|
| 1 Problema e motivação | Relevância | Consciência do problema | Investigação do problema | Estágio 1 (P1) | 1–3 |
| 2 Objetivos da solução | Relevância (requisitos) e rigor | Sugestão | Projeto do tratamento (requisitos) | Estágio 1 (P2) | 4–5 |
| 3 Projeto e desenvolvimento | Design e rigor | Desenvolvimento | Projeto do tratamento | Estágio 2 (P3, P4) | 6–7 |
| 4 Demonstração | Design | Desenvolvimento / avaliação | Validação do tratamento | Estágio 2 | 7–8 |
| 5 Avaliação | Design (interna) e relevância (campo) | Avaliação | Validação; avaliação da implementação | Estágio 2 (P5) | 8 |
| Retornos iterativos | Rigor (adições à base) | Circunscrição; conclusão | Novo ciclo | Estágio 3 (P6) | 9–11 |
| 6 Comunicação | Rigor | Conclusão | — | Estágio 4 (P7) | 12 |
