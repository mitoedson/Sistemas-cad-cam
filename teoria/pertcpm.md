# Planejamento e Gerenciamento de Projetos: Uma Análise do Sistema PERT/CPM

O gerenciamento moderno de projetos fundamenta-se em duas metodologias principais que visam o planejamento, a programação e o controle rigoroso de projetos: o **PERT** (*Program Evaluation and Review Technique*) e o **CPM** (*Critical Path Method*). Ambas utilizam a representação de **redes** para identificar a sequência lógica de atividades e suas interdependências.

### 1. Contexto Histórico e Origens
Po volta de 1900 surgem as primeiras técnicas de
organização de trabalho.

* Taylor (especialização de atividades)

* <a href="graficogantt.md">Gráfico de Gantt</a> (planejamento, programação)
 Durante a Segunda Guerra Mundial, houve um grande
desenvolvimento de técnicas matemáticas para a tomada de decisão. O gráfico representa tarefas por barras em uma linha do tempo, mas carecia da visão de interdependência profunda que o sistema de redes proporciona.

* Após o término da Guerra estes especialistas em tomada de decisão foram absorvidos por empresas privadas. 

As técnicas surgiram de forma independente no final da década de 1950 para resolver desafios complexos de gestão:
*   **PERT (1957):** Desenvolvido pela Marinha dos Estados Unidos para gerenciar o desenvolvimento do míssil Polaris, um projeto com alto nível de incerteza e complexidade.
*   **CPM (1957-1959):** Criado pela DuPont Corporation para otimizar a manutenção de plantas químicas, focando em atividades repetitivas e bem definidas.


### 2. Diferenças Fundamentais: Probabilístico vs. Determinístico
Embora sejam frequentemente usadas juntas em softwares modernos, as duas técnicas possuem focos distintos:
*   **PERT:** Possui abordagem **probabilística**, sendo ideal para projetos onde não se sabe o tempo exato das tarefas (como pesquisa e desenvolvimento). Utiliza três estimativas de tempo: **Otimista (O)**, **Mais Provável (M)** e **Pessimista (P)**. O tempo esperado (**TE**) é calculado pela fórmula: \\(TE = \frac{O + 4M + P}{6}\\).
*   **CPM:** Adota uma abordagem **determinística**, adequada para projetos com atividades bem definidas (como construção civil) onde a duração é conhecida através de experiência acumulada. O foco reside no equilíbrio entre **tempo e custo**.

### 3. O Caminho Crítico e as Fases do Projeto
O **Caminho Crítico** é definido como o conjunto de atividades que não podem sofrer atrasos, pois qualquer demora nelas repercute diretamente no prazo final do projeto. A execução de um projeto através dessas técnicas prevê três fases:
1.  **Planejamento:** Listagem de atividades e definição de dependências.
2.  **Programação:** Estabelecimento de durações e identificação das atividades críticas.
3.  **Controle:** Acompanhamento da execução e tomada de decisões para correções.

### 4. Estrutura da Rede: Atividades e Eventos
Na representação gráfica de uma rede (notação americana ou francesa), distinguem-se dois elementos:
*   **Evento (ou Marco):** Ponto que marca o início ou fim de uma atividade; não consome tempo nem recursos.
*   **Atividade:** Tarefa que consome tempo e recursos; deve ser concluída para que o evento final seja atingido.
Existem tipos específicos de atividades, como as **Fantasmas** (fictícias), usadas para indicar precedência sem consumir recursos, e as **Condicionantes**, que impõem restrições de datas.

### 5. Gestão de Folgas e Datas
O sistema permite calcular as margens de manobra do cronograma através das folgas:
*   **Folga Total:** Quantidade de tempo que uma atividade pode ser atrasada sem comprometer a data final do projeto.
*   **Folga Livre:** Tempo que uma tarefa pode atrasar sem impactar o início da atividade imediatamente seguinte.
Também definem-se a **Data Cedo** (primeira possibilidade de início) e a **Data Tarde** (limite máximo para conclusão sem atrasar o projeto) para cada evento.

### 6. Ferramentas e Aplicações Práticas
As técnicas de caminho crítico são aplicadas em diversas escalas, desde a manutenção de máquinas e festas de música até a construção de edifícios e fábricas. Atualmente, o mercado utiliza softwares que integram PERT e CPM, tais como:
*   **Microsoft Project:** Para planejamento, agendamento e análise de caminhos críticos.
*   **Primavera P6:** Focado em indústrias de engenharia e construção pesada.
*   **Trello:** Embora baseado em Kanban, é utilizado para organização visual de tarefas.

Em suma, o sistema PERT/CPM busca garantir que o projeto seja entregue no **menor tempo e com o menor custo possível**, mantendo a qualidade adequada e a otimização dos recursos disponíveis.