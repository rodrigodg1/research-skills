# Avaliação em DSR

A avaliação é onde projetos DSR mais perdem credibilidade. Uma boa avaliação responde a três
perguntas: **o artefato produz o efeito pretendido?** (eficácia), **produz esse efeito em
situações reais?** (efetividade) e **por que produz?** (mecanismo). E responde com critérios
derivados dos requisitos, fixados antes de olhar os resultados.

## Sumário
1. Métodos de avaliação de Hevner et al. (2004)
2. Tipos de método observados (Peffers et al., 2012)
3. Ex ante e ex post; artificial e naturalística
4. FEDS (Venable et al., 2016)
5. EVAL1–EVAL4 (Sonnenberg & vom Brocke, 2012)
6. Hierarquia de critérios (Prat et al., 2015)
7. Do requisito ao critério e à métrica
8. Avaliação por tipo de artefato
9. Fichas de métodos
10. Ameaças à validade
11. Ética
12. Checklist do plano de avaliação

---

## 1. Métodos de avaliação de Hevner et al. (2004)

| Categoria | Método | Descrição (paráfrase) |
|---|---|---|
| Observacional | Estudo de caso | Estudar o artefato em profundidade no ambiente de negócio |
| | Estudo de campo | Monitorar o uso do artefato em múltiplos projetos |
| Analítico | Análise estática | Examinar a estrutura do artefato quanto a qualidades estáticas (p. ex., complexidade) |
| | Análise de arquitetura | Estudar o encaixe do artefato na arquitetura técnica |
| | Otimização | Demonstrar propriedades ótimas ou limites de otimalidade do comportamento |
| | Análise dinâmica | Estudar o artefato em uso quanto a qualidades dinâmicas (p. ex., desempenho) |
| Experimental | Experimento controlado | Estudar o artefato em ambiente controlado (p. ex., usabilidade) |
| | Simulação | Executar o artefato com dados artificiais |
| Teste | Funcional (caixa-preta) | Executar interfaces do artefato para descobrir falhas |
| | Estrutural (caixa-branca) | Testes de cobertura de alguma métrica da implementação |
| Descritivo | Argumento informado | Usar a base de conhecimento para construir argumento convincente de utilidade |
| | Cenários | Construir cenários detalhados em torno do artefato para demonstrar utilidade |

Os autores reservam os métodos descritivos para artefatos especialmente inovadores, quando outras
formas de avaliação não são viáveis. Em teses, métodos descritivos isolados costumam ser
considerados fracos.

---

## 2. Tipos de método observados (Peffers et al., 2012)

Ao analisar artigos de DSR, Peffers et al. (2012) identificaram tipos recorrentes de avaliação:
argumento lógico, avaliação por especialistas, experimento técnico, experimento com sujeitos,
pesquisa-ação, protótipo, cenário ilustrativo e estudo de caso. Os tipos se associam a tipos de
artefato — por exemplo, algoritmos tendem a experimentos técnicos, e modelos e métodos a
cenários, casos ou especialistas. Use essa lista para verificar se o método escolhido é usual
para o tipo de artefato e, se não for, justificar.

---

## 3. Ex ante e ex post; artificial e naturalística

Pries-Heje et al. (2008) e Venable et al. (2012) organizam a avaliação em duas distinções:

**Quando:**
- **Ex ante** — antes de construir ou instanciar: avalia o design, a especificação, os requisitos.
  Barato; reduz risco cedo; não mostra desempenho real.
- **Ex post** — depois de instanciar: avalia o artefato construído.

**Onde:**
- **Artificial** — algum elemento não é real (usuários, sistema ou problema): experimentos de
  laboratório, simulações, análise por critérios, argumentos teóricos, provas.
  Controle e reprodutibilidade altos; realismo baixo.
- **Naturalística** — pessoas reais, sistemas reais, problemas reais: estudos de caso, estudos de
  campo, pesquisa-ação, surveys. Realismo alto; custo, risco e confundidores também.

| | Artificial | Naturalística |
|---|---|---|
| **Ex ante** | Avaliação de especificação por critérios; prova sobre o modelo; revisão por especialistas em laboratório | Grupo focal com praticantes sobre o design; avaliação do design pela organização-alvo |
| **Ex post** | Benchmark; simulação; experimento controlado com protótipo | Implantação piloto; estudo de caso; pesquisa-ação |

Exemplos ilustrativos, não uma classificação oficial.

---

## 4. FEDS — Framework for Evaluation in Design Science (Venable et al., 2016)

### Duas dimensões
- **Propósito funcional:** *formativa* (produzir melhorias; avaliação ao longo do design) →
  *somativa* (julgar o resultado; atribuir significado aos efeitos).
- **Paradigma:** *artificial* → *naturalística*.

Cada **episódio** de avaliação é um ponto nesse plano. A sequência de episódios forma a
**trajetória** da avaliação.

### Objetivos que o desenho de avaliação equilibra
1. **Rigor** — mostrar que a melhoria se deve ao artefato (*eficácia*) e que ele funciona em
   situações reais (*efetividade*).
2. **Redução de incerteza e risco** — riscos humanos e sociais (o artefato será usado? aceito?) e
   riscos técnicos (vai funcionar? escalar?).
3. **Ética** — riscos para pessoas, organizações e sociedade, inclusive durante a avaliação.
4. **Eficiência** — equilibrar os objetivos acima com os recursos disponíveis.

### Quatro estratégias
| Estratégia | Trajetória | Quando escolher |
|---|---|---|
| **Rápida e simples** | Poucos episódios; vai cedo para somativa naturalística | Design pequeno e simples; baixo risco social e técnico |
| **Risco humano e efetividade** | Formativas artificiais cedo; logo formativas naturalísticas; termina em somativas naturalísticas | Principal risco é social ou do usuário; objetivo é mostrar que a utilidade se mantém em situações reais e no longo prazo |
| **Risco técnico e eficácia** | Formativas artificiais; somativas artificiais; naturalística só no final | Principal risco é técnico; avaliar com usuários reais é caro demais; objetivo é mostrar com rigor que o benefício vem do artefato |
| **Puramente técnica** | Somativas artificiais | Artefato sem usuários humanos, ou uso real previsto só para muito depois |

### Quatro passos
1. **Explicitar os objetivos da avaliação** (rigor, risco, ética, eficiência) e suas prioridades.
2. **Escolher a estratégia** (ou combinação) de acordo com os riscos e os objetivos.
3. **Determinar as propriedades a avaliar** — derivadas de requisitos, objetivos e proposições.
4. **Projetar os episódios individuais** — considerando restrições de tempo, dinheiro, acesso a
   pessoas e organizações; definindo quantos episódios, quando, com que método e com que dados.

### Aplicação em computação e segurança
Artefatos técnicos (protocolos, algoritmos, arquiteturas) geralmente seguem **risco técnico e
eficácia** ou **puramente técnica**: análise formal e benchmarks primeiro, e estudo com operadores
ou implantação piloto no final, se o artefato tiver usuários. Se o sucesso depende de pessoas
adotarem ou confiarem no artefato (ferramentas para analistas, interfaces de privacidade), o
risco humano domina e a estratégia muda.

Modelo de plano em `templates.md` §8.

---

## 5. EVAL1–EVAL4 (Sonnenberg & vom Brocke, 2012)

Propõem avaliar ao longo de todo o processo, não só no fim, com quatro tipos de episódio ligados às
atividades de design. Critérios e métodos abaixo são exemplos típicos.

| Episódio | Momento | O que valida | Critérios típicos | Métodos típicos |
|---|---|---|---|---|
| **EVAL1** | Ex ante, após identificar o problema | Enunciado do problema e lacuna de pesquisa justificados | Importância, novidade, viabilidade | Revisão de literatura, entrevistas com especialistas, grupos focais |
| **EVAL2** | Ex ante, após o projeto | Especificação de design validada | Clareza, completude, consistência, viabilidade | Especialistas, grupos focais, argumento lógico |
| **EVAL3** | Ex post, após a construção | Instanciação validada em ambiente artificial | Viabilidade, eficácia, eficiência, facilidade de uso | Demonstração com protótipo, experimento, simulação, benchmark |
| **EVAL4** | Ex post, após o uso | Artefato validado em uso naturalístico | Aplicabilidade, efetividade, impacto, adequação ao contexto | Estudo de caso, experimento de campo, survey, entrevistas |

Útil para mostrar à banca que a avaliação começou antes do protótipo.

---

## 6. Hierarquia de critérios (Prat et al., 2015)

Critérios organizados pelas dimensões de um sistema. Use como catálogo para não esquecer
critérios relevantes, não para avaliar tudo.

| Dimensão | Critérios |
|---|---|
| **Objetivo** | Eficácia; validade (o artefato funciona corretamente e faz o que deve); generalidade |
| **Ambiente — pessoas** | Utilidade; compreensibilidade; facilidade de uso; eticidade; efeitos colaterais |
| **Ambiente — organização** | Utilidade; adequação à organização; efeitos colaterais |
| **Ambiente — tecnologia** | Harmonização com outras tecnologias; viabilidade; efeitos colaterais |
| **Estrutura** | Completude; simplicidade; clareza; estilo; homomorfismo (correspondência com outro modelo; fidelidade ao fenômeno modelado); nível de detalhe; consistência |
| **Atividade** | Completude; consistência; acurácia; desempenho; eficiência |
| **Evolução** | Robustez; capacidade de aprendizado |

---

## 7. Do requisito ao critério e à métrica

Para cada requisito, defina **antes** da avaliação:

| Elemento | Pergunta | Exemplo |
|---|---|---|
| Requisito | O que o artefato precisa garantir? | R2 — não aumentar incidentes críticos perdidos |
| Critério | Que propriedade observa isso? | Eficácia (Prat: objetivo) |
| Pergunta | O que queremos saber? | A priorização perde mais incidentes críticos que o processo atual? |
| Métrica | Como medir? | Recall de incidentes críticos no top-k |
| Fonte de dados | De onde vêm os dados? | Base histórica rotulada de 6 meses |
| Comparador | Contra o quê? | Ordenação por severidade do SIEM (baseline) |
| Limiar de sucesso | O que conta como atender? | Recall ≥ baseline, com intervalo de confiança reportado |
| Episódio | Onde se mede? | E2 — artificial, somativo |

Fixar limiares e comparadores antes evita o ajuste posterior de critérios aos resultados — uma
das críticas mais graves em avaliações DSR. Se algo mudou durante o projeto, relate a mudança e o
motivo.

---

## 8. Avaliação por tipo de artefato

Síntese orientadora; adapte ao caso.

| Artefato | Critérios centrais | Métodos usuais | Observações |
|---|---|---|---|
| **Construto** (taxonomia, ontologia, conceitos) | Completude, clareza, consistência, utilidade para classificar ou comunicar | Especialistas; aplicação a casos reais; comparação com esquemas existentes; testes de concordância entre avaliadores | Mostre que alguém consegue usar os construtos, não só que estão bem definidos |
| **Modelo** (referência, maturidade, processo) | Fidelidade, completude, nível de detalhe, compreensibilidade, utilidade | Especialistas, grupos focais, estudos de caso, cenários | Modelos de maturidade pedem validação da progressão entre níveis |
| **Método** (processo, procedimento, técnica) | Eficácia, eficiência, operacionalidade, facilidade de uso, generalidade | Estudo de caso, experimento com usuários, pesquisa-ação técnica, comparação com método atual | Avalie o resultado do método e a execução do método |
| **Algoritmo** | Corretude, complexidade, desempenho, acurácia, robustez | Análise formal, benchmarks com baselines, testes em dados reais e sintéticos, ablação | Baselines atuais e fortes; variação e significância estatística |
| **Protocolo ou mecanismo de segurança** | Propriedades de segurança sob o modelo de ameaça, custo, desempenho, implantabilidade | Provas ou verificação formal, análise de segurança, implementação e benchmarks, estudo de implantação | Declare pressupostos e o que está fora do modelo de ameaça |
| **Arquitetura ou sistema** | Atendimento a atributos de qualidade, viabilidade, escalabilidade, integração | Cenários de qualidade, protótipo, testes de desempenho e carga, estudo de caso | Mostre os trade-offs das decisões de arquitetura |
| **Ferramenta ou interface** | Eficácia na tarefa, eficiência, usabilidade, aceitação | Experimento com usuários, testes de usabilidade, estudo de campo com logs | Combine desempenho em tarefas com percepção |
| **Princípios de design** | Efeitos previstos, reutilização, compreensibilidade, generalidade | Instanciação e avaliação; ablação; especialistas; múltiplos contextos | Verifique a validade de instanciação |
| **Teoria de design** | Proposições testáveis confirmadas, poder explicativo, abrangência | Múltiplos estudos; instanciações variadas | Evidência cumulativa |

---

## 9. Fichas de métodos

### A. Argumento informado e análise lógica
- **Quando:** ex ante; artefatos muito novos; complemento de outros métodos.
- **Cuidados:** premissas explícitas; argumento ligado à base de conhecimento; considerar
  contra-argumentos.
- **Armadilha:** usar como única avaliação em tese ou artigo empírico.

### B. Provas formais e verificação
- **Quando:** protocolos, algoritmos, mecanismos de segurança, sistemas críticos.
- **Cuidados:** definir o modelo (ameaça, falhas, pressupostos) antes; indicar o que a prova cobre e
  o que não cobre; para verificação automatizada, disponibilizar modelos e scripts.
- **Relate:** teorema ou propriedade, pressupostos, esboço da prova ou ferramenta, limites.

### C. Cenários ilustrativos
- **Quando:** mostrar aplicabilidade a situações variadas; complementar avaliação quantitativa.
- **Cuidados:** cenários realistas, preferencialmente baseados em casos reais; incluir cenários
  difíceis ou em que o artefato falha.
- **Armadilha:** cenários escolhidos para favorecer o artefato.

### D. Avaliação por especialistas
- **Quando:** ex ante (requisitos, design) e ex post (modelos, métodos, princípios).
- **Seleção:** critérios explícitos de expertise (anos, função, domínio); diversidade de
  perspectivas; independência em relação ao pesquisador sempre que possível.
- **Instrumento:** perguntas ligadas aos critérios; escalas acompanhadas de justificativas
  qualitativas; roteiro publicado em apêndice.
- **Tamanho:** não há número mágico. Justifique pela saturação das respostas ou pelo desenho
  (p. ex., rodadas Delphi até o consenso).
- **Relate:** perfil dos especialistas, instrumento, análise, divergências e o que mudou no artefato.

### E. Grupos focais (Tremblay et al., 2010)
- **Grupos focais exploratórios:** formativos; melhorias incrementais do design.
- **Grupos focais confirmatórios:** somativos; demonstram a utilidade do artefato em uso real.
- **Cuidados:** moderador que não defenda o artefato; roteiro; gravação e análise sistemática;
  relatar o que mudou entre rodadas.

### F. Experimentos técnicos e benchmarks
- **Quando:** algoritmos, sistemas, protocolos, pipelines.
- **Cuidados:**
  - baselines fortes e atuais, com configuração justa (mesmo hardware, ajuste equivalente);
  - cargas de trabalho e dados representativos da classe de problemas, reais quando possível;
  - repetições, variância, intervalos de confiança e testes estatísticos adequados;
  - **ablação** para ligar cada decisão de design ou princípio ao efeito — evidência muito forte
    em DSR, porque mostra *por que* o artefato funciona;
  - artefato, dados e scripts disponíveis para reprodução.
- **Armadilha:** comparar só com a versão anterior do próprio artefato.

### G. Simulação
- **Quando:** ambientes caros, perigosos ou ainda inexistentes; escala.
- **Cuidados:** validar o simulador ou o modelo; análise de sensibilidade dos parâmetros; discutir a
  distância entre simulação e realidade.

### H. Experimentos com usuários
- **Quando:** efeito do artefato sobre o desempenho ou o comportamento de pessoas.
- **Cuidados:** hipóteses e medidas definidas antes; condição de controle (sem artefato ou com
  alternativa); desenho entre sujeitos ou intra-sujeitos, com contrabalanceamento; tarefas
  realistas; cálculo ou justificativa do tamanho da amostra; checagens de manipulação.
- **Armadilhas:** colegas de laboratório como participantes; participantes que sabem qual
  condição é "a do pesquisador".

### I. Estudo de caso e estudo de campo
- **Quando:** avaliação naturalística; efetividade e adequação ao contexto.
- **Cuidados:** protocolo de caso; múltiplas fontes de evidência (logs, entrevistas, documentos,
  métricas); critérios definidos antes; relato de problemas e usos inesperados.
- **Relate:** contexto detalhado (para permitir julgamento de transferibilidade), período,
  participantes, dados, análise.

### J. Pesquisa-ação técnica e ADR
- **Quando:** artefato usado para resolver problema de um cliente real, com o pesquisador
  envolvido.
- **Cuidados:** separar os papéis de projetista, pesquisador e ajudante (Wieringa & Moralı, 2012);
  diário de intervenções; acordo com a organização; reflexão explícita sobre viés.

### K. Questionários de percepção
- **Quando:** aceitação, usabilidade e utilidade percebida, como complemento.
- **Cuidados:** instrumentos validados na versão e no idioma usados; relatar o instrumento
  completo; não tratar percepção como prova de eficácia.
- **Armadilha:** "avaliação" composta só de um questionário aplicado a poucas pessoas próximas do
  pesquisador.

### L. Custo, viabilidade e adoção
- **Quando:** artefatos organizacionais; argumento de valor prático.
- **Cuidados:** premissas de custo explícitas; análise de sensibilidade; incluir custos de
  implantação e manutenção.

---

## 10. Ameaças à validade

| Tipo | Ameaça típica em DSR | Mitigações |
|---|---|---|
| **Instanciação** | A instância não materializa fielmente os princípios; efeitos vêm de detalhes incidentais | Mapear princípio → característica; múltiplas instanciações; ablação; manter constantes os aspectos incidentais |
| **Construto** | A métrica não mede o requisito (p. ex., satisfação no lugar de eficácia) | Derivar métricas dos requisitos; métricas múltiplas; instrumentos validados |
| **Interna** | Pesquisador projeta e avalia; efeito novidade; participantes querem agradar; aprendizado entre tarefas | Avaliadores independentes; limiares prévios; cegamento; contrabalanceamento; condição de controle |
| **Externa** | Contexto, participantes ou dados não representam a classe de problemas | Declarar condições de contorno; contextos variados; descrição rica do contexto |
| **Conclusão** | Amostra pequena; testes inadequados; muitas comparações; variância ignorada em benchmarks | Poder estatístico; correções para múltiplas comparações; repetições; tamanhos de efeito |
| **Ecológica** | Ambiente artificial distante do uso real | Trajetória FEDS até o naturalístico; discutir a distância |
| **Reprodutibilidade** | Artefato, dados ou configuração indisponíveis | Repositório versionado; dados ou dados sintéticos equivalentes; descrição do ambiente |

Relate as ameaças que de fato se aplicam, com a mitigação adotada e o risco residual. Uma lista
genérica sem ligação com o estudo é lida como formalidade.

---

## 11. Ética

### Princípios éticos para DSR (Myers & Venable, 2014)
1. **Interesse público** — considerar se o artefato e seu uso beneficiam ou prejudicam
   stakeholders e a sociedade.
2. **Consentimento informado** — de quem participa do design e da avaliação.
3. **Privacidade** — proteção de dados pessoais usados ou coletados.
4. **Honestidade e precisão** — relatar resultados, limitações e autoria corretamente.
5. **Propriedade** — direitos sobre o artefato e a propriedade intelectual, acordados com as
   partes.
6. **Qualidade do artefato** — cuidado para que o artefato não cause danos por defeitos.

### Contexto brasileiro
- Pesquisas com seres humanos: apreciação por Comitê de Ética em Pesquisa (CEP) via Plataforma
  Brasil, conforme as Resoluções CNS nº 466/2012 e nº 510/2016 (esta para ciências humanas e
  sociais). Verifique com o CEP da instituição quais etapas da avaliação exigem apreciação.
- Dados pessoais: LGPD (Lei nº 13.709/2018) — base legal, minimização, anonimização.
- Em outros países, use o equivalente (IRB, GDPR etc.).

### Segurança e uso dual
- Testes apenas em sistemas com autorização explícita.
- Divulgação responsável de vulnerabilidades encontradas.
- Discussão dos riscos de mau uso do artefato e de mitigações.

---

## 12. Checklist do plano de avaliação

- [ ] Objetivos da avaliação explícitos e priorizados (rigor, risco, ética, eficiência)
- [ ] Estratégia escolhida e justificada pelos riscos do projeto
- [ ] Cada requisito ligado a critério, métrica, comparador e limiar definidos antes
- [ ] Episódios distribuídos ao longo do projeto (formativos e somativos)
- [ ] Pelo menos um episódio somativo adequado ao tipo de artefato e às afirmações do trabalho
- [ ] Baseline ou comparador relevante e atual
- [ ] Participantes, dados e contextos descritos e justificados
- [ ] Viés de quem projeta e avalia mitigado
- [ ] Ameaças à validade específicas e mitigações
- [ ] Aprovação ética e proteção de dados, quando aplicável
- [ ] Artefato, instrumentos e dados disponíveis para reprodução, quando possível
- [ ] Resultados negativos e mudanças no artefato registrados no histórico de iterações
