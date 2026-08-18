# PERT/CPM — Planejamento e Controle de Projetos

## Sumário
- [1. Introdução](#1-introdução)
- [2. Histórico](#2-histórico)
- [3. PERT vs. CPM](#3-pert-vs-cpm)
- [4. Representação da rede](#4-representação-da-rede)
- [5. Eventos e atividades](#5-eventos-e-atividades)
- [6. Tipos de atividades](#6-tipos-de-atividades)
- [7. Tipos de dependência](#7-tipos-de-dependência)
- [8. Princípios básicos para construção de redes](#8-princípios-básicos-para-construção-de-redes)
- [9. Datas cedo e tarde](#9-datas-cedo-e-tarde)
- [10. Folgas](#10-folgas)
- [11. Caminho crítico](#11-caminho-crítico)
- [12. Fases de execução (planejamento, programação, controle)](#12-fases-de-execução-planejamento-programação-controle)
- [13. Softwares que usam PERT/CPM](#13-softwares-que-usam-pertcpm)
- [14. Bibliografia](#14-bibliografia)


## 1. Introdução

PERT (*Program Evaluation and Review Technique*) e CPM (*Critical Path Method*) são metodologias de **gerenciamento de projetos**, usadas no planejamento, programação e controle, desde a definição das atividades até o acompanhamento da execução.

A apresentação do projeto em forma de **rede** permite identificar interdependências e a sequência lógica das atividades. Atrasos em atividades da rede repercutem diretamente no prazo final do projeto.

Antes das redes PERT/CPM, o planejamento era feito majoritariamente com o **gráfico de Gantt**, que representa tarefas como barras horizontais ao longo de uma linha do tempo (início/término), mas não evidencia bem as interdependências entre atividades.


## 2. Histórico

- **~1900** — primeiras técnicas de organização do trabalho (especialização de atividades de Taylor; <a href="graficogantt.md">gráfico de Gantt</a>).
- **2ª Guerra Mundial** — grande desenvolvimento de técnicas matemáticas para tomada de decisão; após a guerra, esses especialistas migram para empresas privadas.

### PERT
- **Ano:** 1957
- **Desenvolvido por:** US Navy, em colaboração com a consultoria Booz Allen Hamilton
- **Motivação:** gerenciar o desenvolvimento do míssil balístico Polaris — projeto complexo e com muitas incertezas

### CPM
- **Ano:** final dos anos 1950 (1957–1959)
- **Desenvolvido por:** DuPont Corporation, em colaboração com a Remington Rand Corporation
- **Motivação:** otimizar o gerenciamento de projetos de manutenção de plantas químicas da DuPont, frequentes e complexos


## 3. PERT vs. CPM

| | **PERT** | **CPM** |
|---|---|---|
| Foco | Tempo | Tempo e custo |
| Natureza | Probabilística (incerteza na duração) | Determinística (durações conhecidas) |
| Estimativas | 3 tempos por atividade (otimista, mais provável, pessimista) | Tempo único por atividade |
| Aplicação típica | P&D, projetos inéditos, alta incerteza | Construção civil, manutenção industrial, atividades repetitivas |

**Tempo esperado (PERT):**

```math
TE = \frac{O + 4M + P}{6}
```

onde:
- **O** = tempo otimista (mínimo necessário)
- **M** = tempo mais provável
- **P** = tempo pessimista (máximo, em condições desfavoráveis)

Na prática, PERT e CPM costumam ser combinados — a maioria dos softwares de gestão de projetos integra os dois conceitos (rede + caminho crítico + estimativa probabilística quando aplicável).


## 4. Representação da rede

#### Caminho (rede)

A apresentação em forma de rede, permite identificar interdependências e a seqüência lógica das atividades. Atividades realizadas, em caso de atraso, repercutem diretamente no prazo final do projeto.

#### Representação

Existem dois métodos clássicos de representação gráfica:

### Método americano (atividade na seta)
- Os **eventos** (nós) são representados por círculos.
- A **atividade** é representada pela seta que liga dois eventos, com identificação e duração escritas sobre/sob a seta.

<img src="image-35.png" width=600><br>

### Método francês (atividade no nó)
- A **atividade** é representada por um retângulo (nó).
- As setas indicam apenas a sequência/dependência entre atividades.

<img src="image-36.png" width=600><br>


### Exemplo comparativo
Atividades A, B, C precedem D, E, F (sem precedência entre A, B, C):

| Atividade | Duração |
|---|---|
| A | 2 |
| B | 3 |
| C | 4 |
| D | 5 |
| E | 6 |
| F | 7 |

- **Método americano:** três caminhos paralelos saindo do evento inicial (1) e convergindo no evento final (5), passando pelos eventos intermediários 2, 3, 4.

<img src="image-37.png" width=600><br>

- **Método francês:** três ramos paralelos entre os nós "Início" e "Fim", cada um com uma atividade precedente e uma sucessora (A→D, B→E, C→F).

<img src="image-38.png" width=600><br>


## 5. Eventos e atividades

- **Evento:** marca o início ou o fim de uma atividade. Não consome tempo nem recursos.
- **Atividade:** delimitada por dois eventos. Consome tempo e/ou recursos financeiros.
- Uma atividade só pode começar quando o evento inicial for atingido, ou seja, quando **todas** as atividades que chegam a esse evento estiverem concluídas.
- Entre dois eventos sucessivos existe **somente uma** atividade.
- Não existem atividades em sentido retrógrado — a rede flui sempre para o futuro (sem *loops*).
- Tudo que consome tempo e pode ser previsto é uma atividade (ex.: cura do concreto, prazo de entrega de material, disponibilidade de equipamento).


## 6. Tipos de atividades

### 6.1 Atividade fantasma (fictícia)
Criada quando existem atividades paralelas entre os mesmos dois eventos, o que geraria ambiguidade na identificação (ex.: duas atividades "2-3"). Resolve-se inserindo um evento e uma atividade fictícios, representados por uma **seta tracejada**, que não consome tempo nem recursos.
<img src="image-39.png" width=600><br>

A regra de priorização é clara: quem tem outro compromisso vira dummy. Quando há duas atividades paralelas, e nenhuma tem outro compromisso, a escolha de qual das duas vira dummy é arbitrária — qualquer uma das duas serve, contanto que:

* Só uma delas continue como seta "real" (com nome e duração) entre os dois eventos originais;
* A outra seja redesenhada passando por um evento novo, intermediário, criado só para separar as duas — ligada por uma dummy de duração zero até (ou a partir) desse novo evento.


<img src="image-40.png" width=600><br>

### 6.2 Atividade dependente
Depende do cumprimento integral de outras atividades. Qualquer atividade que parte de um nó depende de todas as atividades que chegam a esse nó.
<img src="image-41.png" width=600><br>

### 6.3 Atividade independente
Quando uma atividade depende apenas de parte das atividades que convergem para um nó, é necessário usar uma atividade fantasma para representar corretamente a dependência parcial (evitando impor uma dependência que não existe).
<img src="image-42.png" width=600><br>


### 6.4 Atividade condicionante
Impõe uma restrição ou uma data para a realização de outra atividade. Como não consomem tempo nem recursos, **atividades condicionantes são sempre atividades fantasmas**.

Exemplo:

Planejamento da concretagem de um bloco de fundação de um equipamento mecânico.
* Escavação fundação;
* Fôrmas;
* Armação;
* Ausência de Chuvas;
* Concretagem;
* Chegada do Equipamento na obra.

<img src="image-43.png" width=600><br>

A atividade “3-4” poderia ser uma restrição de data, exemplo: “Não iniciar antes de 30/10/2009”.

## 7. Tipos de dependência

### Tipos lógicos de dependência (relação entre início/fim)

Essa é a classificação mais usada na prática:

| Tipo | Sigla | O que significa | Exemplo |
|---|---|---|---|
| **Término-Início** | FS (Finish-to-Start) | A sucessora só pode **começar** depois que a predecessora **terminar** | O que usamos o tempo todo: D só começa depois que B termina |
| **Início-Início** | SS (Start-to-Start) | A sucessora só pode **começar** depois que a predecessora **começar** (não precisa esperar terminar) | Pintar uma parede pode começar assim que começar a preparar a superfície, sem esperar toda a preparação acabar |
| **Término-Término** | FF (Finish-to-Finish) | A sucessora só pode **terminar** depois que a predecessora **terminar** | Testar um sistema só pode terminar depois que a documentação também terminar |
| **Início-Término** | SF (Start-to-Finish) | A sucessora só pode **terminar** depois que a predecessora **começar** | Rara na prática — ex: o turno da noite só "termina" quando o turno do dia "começa" |

A rede que construímos (AON e AOA) assume implicitamente que toda dependência é **FS** — é por isso que a lógica ficou sempre "ES = maior EF das predecessoras", sem nenhuma defasagem ou sobreposição. Redes AOA tradicionais, inclusive, **só conseguem representar FS nativamente** — é uma das limitações do método que não veio à tona na nossa conversa porque seu projeto não precisou de outro tipo.


### Tipos de dependência quanto à natureza (por que ela existe)
- **Mandatória (Obrigatória, ou hard logic):** inerente à natureza física do trabalho. Ex.: não se pinta sem que a parede fique seca.
- **Discricionária (Arbitrária, ou soft logic):** baseada no julgamento de quem planeja, ou em boas práticas/metodologias da área, não de imposições físicas (ex.: inspecionar ferramentas antes de usar).
- **Externa:** relaciona atividades do projeto com atividades externas a ele (ex.: testes de integração dependendo da disponibilidade de um ambiente de outro projeto). Ou seja, depende de algo fora do controle do projeto (ex: aprovação de um orgão regulador, entrega de um fornecedor etc). Costuma se basear em dados históricos de projetos semelhantes.
- **Interna:** Depende de outra atividade do próprio projeto (é o caso mais comum, e o único presente no projeto).


Boa pergunta para fechar o quadro — isso reúne duas coisas: **como as relações de dependência são definidas** e **quais regras de construção** garantem que a rede faça sentido matematicamente. Vamos por partes.

### Como as atividades se relacionam

A relação nasce sempre da **tabela de precedências** — a mesma lógica desde o início da nossa conversa: cada atividade lista **quem precisa terminar antes dela começar** (no seu caso, sempre dependências Término-Início).

Essa relação se propaga em cadeia por toda a rede, criando três papéis possíveis para cada atividade:

| Papel | O que significa | Exemplo do seu projeto |
|---|---|---|
| **Predecessora** | Vem antes, "libera" outra atividade | B é predecessora de D |
| **Sucessora** | Vem depois, "depende" de outra | D é sucessora de B |
| **Paralela (concorrente)** | Não depende uma da outra, podem rodar ao mesmo tempo | D, E, F, G — todas dependem só de B, mas nenhuma depende das outras |

### As regras de construção da rede

Aqui estão as regras que **precisam** ser respeitadas para a rede ser matematicamente válida — algumas você já esbarrou nelas sem perceber, ao longo da nossa conversa:

#### Regra 1 — Não pode haver ciclos (loops)

Uma atividade nunca pode, direta ou indiretamente, depender de si mesma. Se A depende de B, B não pode depender de A (nem através de uma cadeia mais longa, tipo B→C→A). Sem essa regra, seria impossível calcular ES/EF — o cálculo ficaria "girando em círculo", sem nunca encontrar um ponto de partida.

#### Regra 2 — Início e fim únicos

A rede precisa ter **um único ponto de partida** (nenhuma atividade "solta" sem chegar de algum início) e, idealmente, **converge para um único ponto de chegada**. Foi exatamente por isso que, no AOA, precisamos daquelas dummies finais (12→16, 13→16, 14→16, 15→16) — para unificar L, M, N, O em um único evento de término, em vez de deixar quatro finais soltos.

#### Regra 3 — Toda atividade (exceto as iniciais) precisa de ao menos uma predecessora

E toda atividade (exceto as finais) precisa alimentar ao menos uma sucessora. Não pode existir uma atividade "isolada", sem ligação com o resto da rede — senão ela não teria como ser posicionada no tempo em relação às outras.

#### Regra 4 (específica do AOA) — Numeração crescente na direção das setas

Todo evento de chegada precisa ter um número **maior** que o evento de origem da mesma seta. Foi por isso que, quando você pediu para renumerar a rede, eu me certifiquei de que a nova numeração ainda respeitava essa ordem — senão o diagrama ficaria contraditório (uma seta "andando para trás" no tempo).

#### Regra 5 (específica do AOA) — Duas atividades não podem compartilhar o mesmo par de eventos

Se duas atividades diferentes tivessem exatamente o mesmo evento de início e o mesmo evento de fim, ficaria impossível diferenciá-las no diagrama (ambas seriam "a seta de 3 para 4", por exemplo). Quando isso aconteceria naturalmente, insere-se uma dummy para separar os caminhos — essa é, inclusive, mais uma das razões (além da lógica de precedência) pela qual dummies existem no método.

#### Regra 6 — Evitar dependências redundantes

Se A→B→C já implica que A precede C indiretamente, **não se desenha uma seta direta extra de A para C** — isso seria uma informação redundante que só polui o diagrama sem mudar nenhum cálculo. A rede deve representar cada relação de precedência **uma única vez**, da forma mais direta possível.

#### Resumindo a lógica geral

> A rede é construída conectando cada atividade às suas predecessoras diretas (nunca indiretas/redundantes), sem formar ciclos, convergindo para um único início e um único fim — e, no caso do AOA, respeitando ainda a numeração crescente dos eventos e evitando pares de eventos duplicados entre atividades diferentes.


> **Atenção a um erro comum de representação:** se A e B podem ocorrer em paralelo, C depende de A e B, e D depende só de B — **não** se deve fazer A e B convergirem no mesmo nó do qual saem C e D, pois isso impõe implicitamente que D também dependa de A. A representação correta usa uma atividade fantasma para isolar a dependência de D em relação apenas a B.
<img src="image-44.png" width=600><br>
<img src="image-45.png" width=600><br>
<img src="image-46.png" width=600><br>

## 8. Princípios básicos para construção de redes

1. Listar as atividades do projeto.
2. Definir a duração de cada atividade.
3. Definir as interdependências (sequência lógica), identificando quais atividades podem ocorrer simultaneamente (economia de tempo total).

Quais as atividades podem ser executadas simultaneamente (economia do tempo total).

Atividade consome tempo e/ou recursos financeiros, já evento não.

Atividade só pode ser executada se o evento inicial foi atingido, ou seja, concluídas todas as atividades que a ele chegam.

Entre dois eventos sucessivos existe somente uma atividade.
Tudo que consome tempo e pode ser previsto é uma atividade. 

Exemplos:
* Cura do concreto;
* Demora na entrega de material;
* Disponibilidade de equipamento.

Não existem atividades em sentido retrógrado. A rede não permite “looping” – flui sempre para o futuro.


## 9. Data cedo e tarde


- **Data cedo ou Early Time (DC ou TE):** primeira data em que se abre a possibilidade de iniciar as atividades que se originam de um determinado evento.
- **Data tarde ou Latest Time (DT ou TL):** última data em que devem estar concluídas todas as atividades que chegam a um determinado evento, sem atrasar o projeto.

**TE** e **TL** são as siglas usadas nos **eventos** (círculos) da rede AOA — o equivalente ao ES/EF/LS/LF que usamos nas **atividades** da rede AON.

### O que cada sigla significa

| Sigla | Nome completo (inglês) | Nome em português | O que representa |
|---|---|---|---|
| **TE** | Earliest Time (ou Earliest Event Time) | **Tempo mais cedo** (ou Data cedo) | O instante mais cedo em que aquele evento pode acontecer |
| **TL** | Latest Time (ou Latest Event Time) | **Tempo mais tarde** (ou Data tarde) | O instante mais tarde em que aquele evento pode acontecer, sem atrasar o projeto |

O T vem de **Time** (tempo) — porque, diferente das atividades (que têm início *e* fim, exigindo quatro letras: ES, EF, LS, LF), um **evento não dura nada** — ele é um instante único, um marco no tempo. Por isso só precisa de duas siglas (TE e TL), não quatro.

### Resumindo a relação

- **TE** faz o mesmo papel do ES/EF combinados (é o "lado cedo" da rede, calculado na passagem de avanço);
- **TL** faz o mesmo papel do LS/LF combinados (é o "lado tarde" da rede, calculado na passagem de retorno).

É exatamente essa correspondência que permitiu a gente "traduzir" TE/TL de cada evento para ES/EF/LS/LF de cada atividade, na tabela completa que montamos.


Em notação CPM equivalente:
- **ES** (*Early Start*) / **EF** (*Early Finish*) — início/término mais cedo.
- **LS** (*Late Start*) / **LF** (*Late Finish*) — início/término mais tarde.


Pensa na simetria: assim como o TE do evento de origem já *é* diretamente o ES da atividade (sem nenhuma conta extra), o TL do evento de destino já *é* diretamente o **LF** da atividade — porque o LF representa justamente "o mais tarde que essa atividade pode terminar", e isso é exatamente o que o TL do evento de chegada representa.


### Resumindo as quatro associações completas

| Valor da atividade | Vem de | Precisa de conta extra? |
|---|---|---|
| **ES** | TE do evento de origem | Não — é direto |
| **EF** | TE do evento de origem + duração | Sim, soma a duração |
| **LF** | TL do evento de destino | Não — é direto |
| **LS** | TL do evento de destino − duração | Sim, subtrai a duração |

### A regra de ouro para não confundir

**TE sempre "gruda" no início da atividade (ES); TL sempre "gruda" no fim da atividade (LF).** As versões com soma/subtração de duração (EF e LS) são sempre as que precisam de um passo a mais de conta.


## 10. Folgas

**Folga** é a diferença entre o tempo disponível para realizar uma atividade e sua duração.

### Folga total (flexibilidade do cronograma)
Quantidade de tempo que uma atividade pode ser atrasada ou estendida a partir de sua data de início mais cedo, **sem atrasar a data de término do projeto** nem violar uma restrição do cronograma.

```
Ft = (Dtf - Dci) - d
```
onde `Dtf` = data tarde final, `Dci` = data cedo inicial, `d` = duração da atividade.

### Folga livre (*free float*)
Tempo permitido para atraso de uma atividade **sem atrasar a data de início mais cedo de qualquer atividade sucessora imediata**.

```
Fl = (Dcf - Dci) - d
```
onde `Dcf` = data cedo final, `Dci` = data cedo inicial, `d` = duração da atividade.



### Confirmando as duas redes

| | Rede AOA | Rede AON |
|---|---|---|
| **Folga Total** | TL(sucessor) − TE(antecessor) − duração | LF(atividade) − EF(atividade) *(equivale a LS − ES)* |
| **Folga Livre** | TE(sucessor) − TE(antecessor) − duração | ES(sucessora) − EF(atividade) |


## 11. Caminho crítico

Conjunto de atividades ou etapas de um projeto que **não podem sofrer atrasos** em sua execução sem prejudicar o prazo final do projeto. É o caminho mais longo da rede, com a menor (ou nula) folga.

Objetivos da análise do caminho crítico:
- Determinar quais etapas devem seguir uma programação rígida para que o projeto não atrase.
- Determinar como executar as etapas sem exceder os recursos disponíveis.
- Determinar o custo de execução do projeto e como ele se comporta ao se tentar acelerar a execução.


## 12. Fases de execução (planejamento, programação, controle)

1. **Planejamento:** estabelece as atividades necessárias à conclusão do projeto, suas relações de dependência, e a ordem de execução (diagrama de flechas/rede).
2. **Programação:** estabelece o tempo de execução de cada atividade e identifica quais delas determinam a duração total do projeto (caminho crítico).
3. **Controle:** acompanha a execução do projeto, confrontando-a com o planejado/programado, gerando informações para intervenções e tomada de decisão.

Planejamento e programação devem estar completos antes do início do projeto; o controle ocorre durante a execução, é o meio de reconhecer as dificuldades durante a execução.

#### Classificação de projetos quanto à duração
* Projetos de longa duração – Construção de uma fábrica
* Projetos de média duração – Fazer o jantar
* Projetos de curta duração – Manutenção de uma máquina – Limpeza de uma sal

<a href="planejamento_projeto.md">Ir para Planejamento de Projeto PERT/CPM</a>



## 13. Softwares que usam PERT/CPM

- **Microsoft Project** — diagramas de Gantt, cálculo de caminho crítico, análise PERT, relatórios.
- **Primavera P6 (Oracle)** —d gestão de projetos/portfólios complexos, análise de riscos, usado em engenharia/construção/manufatura.
- **Trello** — gestão baseada em Kanban (to do / doing / done); não é uma ferramenta de rede PERT/CPM propriamente, mas é citada como parte do ecossistema de gerenciamento de projetos.


## 14. Bibliografia

- HIRSCHFELD, H. *Planejamento com PERT-CPM e análise de desempenho: método manual e por computadores aplicados a todos os fins*. 9. ed. rev. e ampl. São Paulo: Atlas, 1987. 335 p.
- KERZNER, H. *Project Management: A Systems Approach to Planning, Scheduling, and Controlling*. ISBN 978-1119587293.
- MEREDITH, J. R.; MANTEL Jr., S. J.; SHAFER, S. M. *Project Management: A Managerial Approach*. ISBN 978-1118945834.
- PROJECT MANAGEMENT INSTITUTE (PMI). *A Guide to the Project Management Body of Knowledge (PMBOK Guide)*. ISBN 978-1628256642.
- EAST, W. *Critical Path Method (CPM) Tutor for Construction Planning and Scheduling*. ISBN 978-1260440362.
- SRINATH, L. S. *PERT and CPM: Techniques for Project Management*. ISBN 978-8178000000.

---

> **Nota:** os exercícios dirigidos (planejamento da construção de uma casa popular; construção de rede PERT/CPM com cálculo de datas cedo/tarde e folgas) foram propositalmente deixados fora deste documento e podem ser adicionados depois, resolvidos, como material complementar.