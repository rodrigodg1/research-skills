# Artefatos, contribuição e teoria em DSR

## Sumário
1. Tipos de artefato
2. Conhecimento descritivo (Ω) e prescritivo (Λ)
3. Matriz de contribuição e níveis (Gregor & Hevner, 2013)
4. Equilíbrio entre artefato e teoria (Baskerville et al., 2018)
5. Teoria de design: Walls et al. (1992), Gregor & Jones (2007), Gregor (2006)
6. Teorias de base, requisitos e meta-requisitos
7. Princípios de design
8. Regras tecnológicas e lógica CIMO
9. Generalização, abstração e validade de instanciação
10. Declaração de contribuição

---

## 1. Tipos de artefato

### March & Smith (1995)
| Tipo | Definição (paráfrase) | Exemplos em computação, segurança e gestão | Representação típica |
|---|---|---|---|
| **Construto** | Vocabulário e símbolos para definir e comunicar problemas e soluções | Taxonomia de ataques; ontologia de consentimento; notação de modelagem; conceitos de uma linguagem de políticas | Definições, metamodelo, glossário formal |
| **Modelo** | Proposições que relacionam construtos; representam problema e espaço de solução | Modelo de maturidade; arquitetura de referência; modelo de processo; modelo formal de ameaça | Diagramas, especificações, modelos formais |
| **Método** | Conjunto de passos (algoritmo ou orientação) para executar uma tarefa | Algoritmo; método de avaliação de risco; procedimento de auditoria; processo de desenvolvimento | Pseudocódigo, fluxos, guias passo a passo |
| **Instanciação** | Realização do artefato no ambiente; operacionaliza construtos, modelos e métodos e demonstra viabilidade | Protótipo; sistema implantado; implementação de protocolo; ferramenta | Código, sistema em execução, implantação |

Atividades cruzadas com esses tipos: **construir** (mostrar que o artefato pode ser feito para um
propósito), **avaliar** (definir critérios e medir desempenho), **teorizar** (explicar por que e
como o artefato funciona no ambiente) e **justificar** (reunir evidências que testem essa
explicação).

### Tipos observados na literatura de SI (Offermann et al., 2010)
Projeto de sistema, método, linguagem ou notação, algoritmo, diretriz, requisitos, padrão
(*pattern*) e métrica. Úteis quando a classificação de March & Smith é grossa demais — por
exemplo, "métrica" e "padrão" são artefatos legítimos que ficariam mal encaixados.

### Artefatos mais abstratos
Gregor & Hevner (2013) e Gregor & Jones (2007) tratam **princípios de design** e **teorias de
design** como saídas de DSR em nível mais alto de abstração (ver §3 e §5).

### Observações práticas
- Uma pesquisa costuma produzir vários tipos ao mesmo tempo (p. ex., um método e uma
  instanciação que o implementa). Declare qual é o artefato **principal** — é ele que a
  avaliação precisa sustentar.
- Artefatos em DSR podem ser sociotécnicos (processos, políticas, estruturas organizacionais),
  não apenas software.
- Uma instanciação sozinha raramente basta como contribuição científica; o que a torna pesquisa é
  o conhecimento que ela permite testar ou extrair.

---

## 2. Conhecimento descritivo (Ω) e prescritivo (Λ)

Gregor & Hevner (2013) distinguem dois tipos de conhecimento que interagem em DSR:

| | Ω — descritivo (o quê, como, por quê) | Λ — prescritivo (como fazer) |
|---|---|---|
| Conteúdo | Fenômenos (observações, classificações, medições) e compreensão (leis, regularidades, princípios, padrões, teorias) | Construtos, modelos, métodos, instanciações e teorias de design |
| Papel em DSR | Fundamenta decisões de design (teorias de base); explica por que o artefato funciona | Estado da arte das soluções; aquilo a que DSR principalmente contribui |

**Aplicação na revisão de literatura:** organize em (a) o que se sabe sobre o problema e seus
mecanismos (Ω) e (b) que soluções existem e quão bem funcionam (Λ). A lacuna de DSR normalmente
está em (b), justificada por (a). DSR também pode contribuir para Ω — por exemplo, ao explicar
por que o artefato produziu o efeito observado.

---

## 3. Matriz de contribuição e níveis (Gregor & Hevner, 2013)

### Matriz de contribuição de conhecimento (DSR Knowledge Contribution Framework)
Eixos: **maturidade do domínio de aplicação** (o problema é conhecido e bem entendido?) e
**maturidade da solução** (existem soluções conhecidas e adequadas?).

| | Maturidade da solução **baixa** | Maturidade da solução **alta** |
|---|---|---|
| **Domínio maduro** (problema conhecido) | **Melhoria** — nova solução para problema conhecido | **Design rotineiro** — solução conhecida para problema conhecido |
| **Domínio pouco maduro** (problema novo) | **Invenção** — nova solução para problema novo | **Exaptação** — solução conhecida estendida a problema novo |

| Quadrante | O que precisa ser demonstrado | Armadilha comum |
|---|---|---|
| Melhoria | Estado da arte das soluções bem mapeado; avaliação comparativa mostrando que o novo artefato é melhor em critérios relevantes | Comparar com baseline fraco ou desatualizado |
| Invenção | Que o problema é realmente novo e importante; viabilidade e utilidade inicial do artefato | Chamar de invenção o que é melhoria; ignorar trabalhos correlatos em outras áreas |
| Exaptação | Que a transferência não é trivial: adaptações necessárias, por que não era óbvia, o que se aprende sobre o novo domínio | Aplicação direta de técnica conhecida apresentada como contribuição |
| Design rotineiro | Normalmente não constitui contribuição de pesquisa; só vira pesquisa se revelar resultados inesperados que levem a outro quadrante | Tese inteira neste quadrante com jargão de DSR |

**Uso na orientação:** peça ao usuário evidências para cada eixo. Maturidade do domínio se mostra
com literatura e dados sobre o problema; maturidade da solução, com o mapeamento de soluções
existentes e suas limitações.

### Níveis de contribuição
| Nível | Tipo | Exemplos | Evidência esperada |
|---|---|---|---|
| **3** | Teoria de design bem desenvolvida sobre fenômenos embutidos | Teorias de médio alcance ou abrangentes | Múltiplos estudos, contextos e instanciações; explicação consolidada |
| **2** | Teoria de design nascente — conhecimento como princípios operacionais ou arquitetura | Construtos, métodos, modelos, princípios de design, regras tecnológicas | Artefato avaliado e abstração justificada; condições de contorno declaradas |
| **1** | Implementação situada do artefato | Instanciações: software, processos implementados | Artefato funcionando e avaliado em contexto |

- Um projeto pode contribuir em mais de um nível; teses e artigos típicos combinam os níveis 1 e 2.
- O nível declarado precisa ser proporcional à evidência. Afirmar nível 3 com um único estudo é
  crítica certa.
- Gregor & Hevner (2013) também propõem um esquema de publicação para DSR
  (ver `writing-and-reviewing.md` §1).

---

## 4. Equilíbrio entre artefato e teoria (Baskerville et al., 2018)

Existe tensão, especialmente em periódicos de SI, entre exigir teoria e valorizar artefatos.
Baskerville et al. (2018) argumentam por equilíbrio: artefatos novos e úteis são, eles mesmos,
conhecimento valioso, e a abstração teórica deve ser proporcional ao objetivo do estudo e à
evidência disponível.

**Orientação prática:**
- Declare explicitamente onde está o peso da contribuição: no artefato, no conhecimento de
  design abstraído ou em ambos.
- Periódicos de SI de alto impacto tendem a esperar abstração (princípios ou teoria). Venues de
  computação tendem a valorizar o artefato e sua avaliação. Ajuste ao público-alvo.
- Não fabrique teoria: princípios de design bem fundamentados e avaliados já são contribuição de
  nível 2.

---

## 5. Teoria de design

### Tipos de teoria em SI (Gregor, 2006)
Cinco tipos: I análise; II explicação; III predição; IV explicação e predição; **V design e
ação** — diz como fazer algo, com prescrições explícitas. Teorias de design em DSR são do tipo V
e costumam se apoiar em teorias dos tipos I a IV como teorias de base.

### Teoria de design de SI — ISDT (Walls et al., 1992)
| Aspecto | Componente | Descrição (paráfrase) |
|---|---|---|
| Produto | Meta-requisitos | Classe de objetivos à qual a teoria se aplica |
| | Meta-design | Classe de artefatos que se supõe atender aos meta-requisitos |
| | Teorias de base | Teorias das ciências naturais ou sociais que governam os requisitos de design |
| | Hipóteses testáveis do produto | Testam se o meta-design satisfaz os meta-requisitos |
| Processo | Método de design | Procedimentos para construir o artefato |
| | Teorias de base | Teorias que governam o processo de design |
| | Hipóteses testáveis do processo | Verificam se o método resulta em artefato consistente com o meta-design |

### Anatomia de uma teoria de design (Gregor & Jones, 2007)
| # | Componente | Pergunta-guia |
|---|---|---|
| 1 | Propósito e escopo | Para que serve o artefato? Que meta-requisitos atende? Em que limites? |
| 2 | Construtos | Quais entidades de interesse a teoria usa e como são definidas? |
| 3 | Princípios de forma e função | Qual o "projeto abstrato": estrutura, arquitetura, funções? |
| 4 | Mutabilidade do artefato | Que mudanças de estado ou adaptações do artefato a teoria prevê? |
| 5 | Proposições testáveis | Se o artefato seguir os princípios, que resultados observáveis se esperam? |
| 6 | Conhecimento justificatório | Que teorias ou conhecimentos explicam por que o design deve funcionar? |
| 7 | Princípios de implementação* | Como implantar o artefato em contextos específicos? |
| 8 | Instanciação expositiva* | Que implementação concreta ilustra e permite testar a teoria? |

\* Componentes adicionais; os seis primeiros são o núcleo. Canvas em `templates.md` §12.

**Uso:** o quadro serve tanto para *construir* a teoria (preencher cada componente) quanto para
*revisar* afirmações teóricas (componentes vazios mostram o que falta). Se vários componentes
ficam vazios, a contribuição provavelmente é de nível 1 ou 2, e o texto deve dizer isso.

---

## 6. Teorias de base, requisitos e meta-requisitos

### O que conta como conhecimento justificatório
- Teorias das ciências sociais e comportamentais (carga cognitiva, confiança em automação,
  teoria da agência, aprendizagem).
- Teorias formais e matemáticas (teoria das filas, complexidade computacional, teoria dos jogos,
  pressupostos criptográficos).
- Conhecimento de design: padrões, arquiteturas de referência, artefatos anteriores.
- Achados empíricos consolidados e normas técnicas ou regulatórias.
- Experiência e expertise do domínio — a base de conhecimento de Hevner (2007) inclui isso.

Quando o design se apoia em conhecimento de engenharia e não em teoria comportamental, diga isso
com clareza. É mais honesto e mais defensável do que forçar uma teoria.

### Cadeia de derivação
```
Proposição da teoria de base
  → meta-requisito (para a classe de problemas)
    → princípio de design
      → característica do artefato (instância)
        → proposição testável
          → critério e episódio de avaliação
```
Exemplo: *teoria de base* — usuários calibram confiança em sistemas automatizados quando entendem
o raciocínio do sistema → *meta-requisito* — o sistema deve permitir que usuários avaliem a base
de cada recomendação → *princípio* — fornecer justificativa legível para cada recomendação →
*característica* — painel com os três fatores que mais pesaram → *proposição* — usuários com
justificativa aceitam menos recomendações erradas do que usuários sem ela → *avaliação* —
experimento comparando as duas condições.

### Requisitos de boa qualidade
- **Específicos e verificáveis:** "reduzir o tempo de triagem em relação ao processo atual" em vez
  de "ser eficiente".
- **Rastreáveis:** cada requisito indica a origem (entrevista, dado, literatura, norma, teoria).
- **Classificados:** funcionais e de qualidade (desempenho, segurança, usabilidade); prioridade.
- **Independentes da solução:** descrevem o que se precisa, não como o artefato o faz.
- **Em nível de classe, quando a contribuição é abstrata:** meta-requisitos.

**Fontes de elicitação:** revisão sistemática, entrevistas e grupos focais com stakeholders,
análise de documentos e incidentes, normas e regulações (p. ex., LGPD, ISO), modelagem de
ameaças para requisitos de segurança, observação do trabalho real.

### Teorias de design e teorias explicativas
Kuechler & Vaishnavi (2012) distinguem teorias de design (prescritivas) de teorias explicativas
ou preditivas relevantes para o design, que explicam por que um artefato funciona e podem fazer a
ponte entre teoria de base e teoria de design.

### Falhas comuns
- Teorias listadas no referencial e nunca usadas no design.
- Teoria encaixada depois de o artefato estar pronto, sem influência real nas decisões. Se isso
  aconteceu, é melhor apresentar a teoria como *explicação* dos resultados do que como
  *fundamento* do design.

---

## 7. Princípios de design

**O que são.** Enunciados prescritivos que capturam conhecimento de design transferível para uma
classe de problemas. São a forma mais comum de contribuição de nível 2.

### Modelo de Chandra, Seidel & Gregor (2015)
Princípios devem articular **materialidade** (propriedades do artefato), **ação** (o que usuários
podem fazer) e **condições de contorno**. Modelo adaptado:
> Forneça ao sistema **[propriedade material, em termos de forma e função]** para que
> **[usuários ou grupo]** possam **[ação ou atividade]**, dado que **[condições de contorno:
> características dos usuários ou do contexto de implantação]**.

### Anatomia de Gregor, Chandra Kruse & Seidel (2020)
Componentes: **objetivo** (*aim*), **atores** — implementador, usuário e executor (*enactor*) —,
**contexto**, **mecanismo** (ações, atividades, processos ou propriedades materiais) e
**justificativa** (*rationale*, baseada em teoria ou evidência). Modelo adaptado:
> Para que o **implementador I** alcance ou permita o **objetivo A** para o **usuário U** no
> **contexto C**, empregue os **mecanismos M1, M2…**, executados por **E1, E2…**, porque
> **[justificativa R]**.

### Qualidades de um bom princípio
- Prescritivo e orientado à ação.
- Endereçado a uma classe de situações, não a uma instância.
- Independente de uma tecnologia específica — "use blockchain" é uma característica; "garanta
  registros à prova de adulteração verificáveis por partes que não confiam entre si" é um
  princípio.
- Justificado (teoria ou evidência) e com condições de contorno.
- Testável: implica efeitos observáveis.
- Compreensível e reutilizável por praticantes.

### Fraco vs. forte
- **Fraco:** "O sistema deve ser fácil de usar."
- **Forte:** "Forneça ao sistema de triagem uma justificativa legível dos fatores que determinaram
  cada prioridade, para que analistas possam contestar prioridades incorretas antes de agir, dado
  que operam sob alta carga de alertas e responsabilidade pela decisão final."

### De onde vêm os princípios
- **A priori:** derivados de meta-requisitos e teorias de base antes da construção; testados na
  avaliação.
- **A posteriori:** extraídos por reflexão sobre o artefato e os resultados da avaliação; precisam
  de nova avaliação para ganhar força.
Declare qual foi o caso. Princípios a posteriori apresentados como se tivessem guiado o design
desde o início são um problema de integridade.

### Como avaliar princípios
Instanciar e medir os efeitos previstos; verificar a validade de instanciação (§9); comparar
instanciações com e sem o mecanismo (ablação); consultar especialistas sobre compreensão e
reutilização; testar em mais de um contexto.

---

## 8. Regras tecnológicas e lógica CIMO

### Regra tecnológica (van Aken, 2004)
> Se você quer alcançar **Y** na situação **Z**, então algo como a ação **X** ajudará.

- "Algo como" indica prescrição **heurística**, que precisa ser adaptada ao contexto, em oposição
  a prescrições **algorítmicas**, seguidas à risca.
- Regras fortes são **testadas em campo** (na prática) e **fundamentadas** (explicadas por
  mecanismos ou teoria).
- Em engenharia de software, a regra tecnológica é a forma usual de contribuição
  (`frameworks.md` §10).

### Lógica CIMO (Denyer et al., 2008)
Proposições de design com quatro elementos:
- **C**ontexto: a classe de situações problemáticas;
- **I**ntervenção: o tipo de intervenção;
- **M**ecanismo: o mecanismo gerador que a intervenção aciona — o *porquê* funciona;
- **O**utcome (resultado): os resultados produzidos.
> Em contextos do tipo **C**, use intervenções do tipo **I** para acionar os mecanismos **M** e
> produzir os resultados **O**.

O mecanismo é o elo com a teoria de base; CIMO sem mecanismo é só uma recomendação.

### Qual formato usar
| Público | Formato preferido |
|---|---|
| Sistemas de Informação | Princípios de design (Gregor et al., 2020) |
| Gestão e engenharia de produção | Regras tecnológicas ou CIMO |
| Engenharia de software | Regras tecnológicas |
| Computação e segurança | Objetivos e princípios de projeto em linguagem técnica; lições generalizáveis |

---

## 9. Generalização, abstração e validade de instanciação

**O problema.** A avaliação ocorre em instâncias; as afirmações de contribuição são sobre classes.
Esse salto precisa ser argumentado.

**Tipos de generalização (Lee & Baskerville, 2003).** Distinguem generalizar de dados empíricos
para dados empíricos, de dados empíricos para teoria, de teoria para dados empíricos e de teoria
para teoria. Uma avaliação DSR num contexto normalmente sustenta generalização para *teoria*
(princípios e mecanismos), não generalização estatística para uma população. Aplicar os princípios
num novo contexto exige verificar se as condições se mantêm.

**Estratégias para fortalecer a generalização:**
1. Definir explicitamente a classe de problemas e as condições de contorno.
2. Explicar *por que* o artefato funciona (mecanismos): onde o mecanismo opera, o efeito deve se
   repetir — é o raciocínio de Wieringa (2014) por semelhança de arquitetura.
3. Instanciar e avaliar em mais de um contexto ou em contextos deliberadamente variados.
4. Ampliar condições gradualmente (laboratório → piloto → campo).
5. Consultar especialistas sobre transferibilidade.
6. Abstrair o conhecimento em princípios ou regras e declarar o que ficou fora.

**Validade de instanciação (Lukyanenko et al., 2014).** Quanto a instância construída representa de
fato o artefato abstrato ou os princípios de design. Detalhes de implementação (interface,
desempenho, escolhas incidentais) podem causar os efeitos observados em vez dos princípios.
Mitigações: documentar o mapeamento princípio → característica; múltiplas instanciações;
verificações de manipulação; estudos de ablação; manter constantes os aspectos incidentais entre
condições.

**Calibração da linguagem:**
- Evite: "o artefato resolve o problema de X".
- Prefira: "no contexto avaliado, o artefato reduziu Y em relação a Z; os mecanismos M sugerem
  que o efeito deve se repetir em contextos com as características C1 e C2".

---

## 10. Declaração de contribuição

Uma boa declaração responde:
1. **Que artefato?** Tipo e forma.
2. **O que é novo?** Em relação a quais soluções anteriores, e em que aspecto.
3. **Para que classe de problemas?** Com condições de contorno.
4. **Com que evidência?** Estratégia e resultados principais da avaliação.
5. **Que conhecimento de design?** Princípios, regras, entendimento do problema.
6. **Para quem?** Implicações para pesquisa e para prática.
7. **Onde na matriz?** Quadrante e nível.

**Exemplo de estrutura (adaptar):**
> Este trabalho contribui com [artefato], um [tipo] para [classe de problemas]. Diferentemente de
> [soluções anteriores], que [limitação], o artefato [diferença essencial]. A avaliação
> [estratégia: artificial/naturalística; formativa/somativa] mostrou [resultado principal em
> relação ao baseline]. Dessa experiência derivamos [n] princípios de design que [propósito] em
> contextos com [condições]. Na matriz de Gregor & Hevner (2013), trata-se de uma contribuição de
> [quadrante], nos níveis [1 e 2].

Modelo completo em `templates.md` §10.
