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
*   **PERT (1957):** Desenvolvido pela Marinha dos Estados Unidos, em colaboração com a Booz Allen Hamilton, para gerenciar o desenvolvimento do míssil Polaris, um projeto com alto nível de incerteza e complexidade.
*   **CPM (1957-1959):** Criado pela DuPont Corporation, em colaboração com a Remington Rand Corporation, para otimizar o gerenciamento de projetos de manutenção de plantas químicas da DuPont, que eram frequentes e complexos.


### 2. Diferenças Fundamentais: Probabilístico vs. Determinístico
Embora sejam frequentemente usadas juntas em softwares modernos, as duas técnicas possuem focos distintos:
*   **PERT:** Possui abordagem **probabilística**, sendo ideal para projetos onde não se sabe o tempo exato das tarefas (como pesquisa e desenvolvimento). Utiliza três estimativas de tempo: **Otimista (O)**, **Mais Provável (M)** e **Pessimista (P)**. O tempo esperado (**TE**) é calculado pela fórmula: $(TE = \frac{O + 4M + P}{6}$).
O objetivo é melhorar a coordenação e controle de
projetos, identificar o caminho crítico (sequência de
atividades que determina o tempo total do projeto) e
calcular o tempo esperado para a conclusão do projeto.

*   **CPM:** Adota uma abordagem **determinística**, adequada para projetos com atividades repetitivas e bem definidas (como construção civil) onde a duração é conhecida (usa tempos únicos para a estimativa de duração das atividades), através de experiência acumulada. O foco reside no equilíbrio entre **tempo e custo**. O objetivo é identificar o caminho crítico, reduzir os custos e o tempo do projeto, e otimizar a alocação de recursos.

### 3. Comparação e integração das duas metodologias
* PERT é mais adequado para projetos onde há muita incerteza e variação nas estimativas de tempo.
* CPM é mais adequado para projetos com atividades bem definidas e repetitivas.
<ul>
<ol>
<li> Ambos as metodologias são usados para planejamento e controle de projetos, mas suas abordagens e aplicabilidade variam dependendo da
natureza do projeto.
<li>Estão presentes em vários softwares - neles combinam-se as técnicas de PERT e CPM para oferecer soluções completas de gerenciamento de projetos.
</ol>
</ul>


### 4. O Caminho Crítico e as Fases do Projeto
O **Caminho Crítico** é definido como o conjunto de atividades que não podem sofrer atrasos, pois qualquer demora nelas repercute diretamente no prazo final do projeto. A execução de um projeto através dessas técnicas prevê três fases:
1.  **Planejamento:** Listagem de atividades e definição de dependências.
2.  **Programação:** Estabelecimento de durações e identificação das atividades críticas.
3.  **Controle:** Acompanhamento da execução e tomada de decisões para correções.

### 5. Estrutura da Rede: Atividades e Eventos
Na representação gráfica de uma rede (notação americana ou francesa), distinguem-se dois elementos:
*   **Evento (ou Marco):** Ponto que marca o início ou fim de uma atividade; não consome tempo nem recursos.
*   **Atividade:** Tarefa que consome tempo e recursos; deve ser concluída para que o evento final seja atingido.
Existem tipos específicos de atividades, como as **Fantasmas** (fictícias), usadas para indicar precedência sem consumir recursos, e as **Condicionantes**, que impõem restrições de datas.

### 6. Gestão de Folgas e Datas
O sistema permite calcular as margens de manobra do cronograma através das folgas:
*   **Folga Total:** Quantidade de tempo que uma atividade pode ser atrasada sem comprometer a data final do projeto. Ft= [Dtf-Dci]-d
*   **Folga Livre:** Tempo que uma tarefa pode atrasar sem impactar o início da atividade imediatamente seguinte. Fl= [Dcf-Dci]-d

Também definem-se a **Data Cedo** (primeira possibilidade de início) e a **Data Tarde** (limite máximo para conclusão sem atrasar o projeto) para cada evento.

### 7. Ferramentas e Aplicações Práticas
As técnicas de caminho crítico são aplicadas em diversas escalas, desde a manutenção de máquinas e festas de música até a construção de edifícios e fábricas. Atualmente, o mercado utiliza softwares que integram PERT e CPM, tais como:

*   **Microsoft Project:** 
<ul>

* Descrição: Um dos softwares de gerenciamento de projetos mais populares, oferece recursos para planejamento, agendamento, atribuição de recursos, rastreamento do progresso, e análise de caminhos críticos.

* Recursos: Diagramas de Gantt, cálculo de caminho crítico, análise PERT, relatórios personalizados.

Para planejamento, agendamento e análise de caminhos críticos.
</ul>

*   **Primavera P6:** 
<ul>

* Descrição: Um software de gerenciamento de projetos e portfólios da Oracle, amplamente utilizado em indústrias de engenharia, construção e manufatura.

* Recursos: Planejamento e agendamento de projetos complexos, gerenciamento de recursos, análise de caminho crítico, análise de riscos, integração com outras ferramentas.
</ul>

*   **Trello:** 

<ul>

* Descrição: Uma ferramenta de gerenciamento de projetos baseada em Kanban (to do, doing, done), que usa quadros, listas e cartões para organizar tarefas.

* Recursos: Visualização de tarefas, checklists, etiquetas e prazos, integrações com outras ferramentas, automação com Butler.
</ul>


### 8. Livros
"Project Management: A Systems Approach to Planning, Scheduling, and Controlling" - Harold Kerzner.
Descrição: Um dos livros mais completos sobre gerenciamento de projetos, abordando técnicas de PERT e CPM em detalhes. ISBN: 978-1119587293

"Project Management: A Managerial Approach" - Jack R. Meredith, Samuel J. Mantel Jr., Scott M. Shafer
○ Descrição: Fornece uma abordagem prática e teórica para o gerenciamento de projetos, com explicações
sobre PERT e CPM. ISBN: 978-1118945834

"A Guide to the Project Management Body of Knowledge (PMBOK Guide)" - Project Management Institute
(PMI). Descrição: Um guia padrão para o gerenciamento de projetos, que inclui métodos de planejamento e controle, como PERT e CPM. ISBN: 978-1628256642

"Critical Path Method (CPM) Tutor for Construction Planning and Scheduling" - William East. Descrição: Um livro focado na aplicação do CPM na construção, com exemplos práticos e exercícios. ISBN: 978-1260440362

"PERT and CPM: Techniques for Project Management" - L.S. Srinath. Descrição: Um livro que explora as técnicas de PERT e CPM de maneira detalhada, ideal para estudantes e profissionais. ISBN: 978-8178000000


Em suma, o sistema PERT/CPM busca garantir que o projeto seja entregue no **menor tempo e com o menor custo possível**, mantendo a qualidade adequada e a otimização dos recursos disponíveis.