<h1>Sistemas CAD CAM</h1>

## Apresentação

Esta disciplina é baseada nas aulas teóricas e práticas, ministrada pelo Prof. Dr. Rovilson Mafalda, da UFABC.

### Objetivos

 O aluno seja capaz de reconhecer a importância da computação gráfica e modelagem 3D nos processos modernos de projeto e manufatura. Interpretar a linguagem técnica do desenho e traduzir para processos de fabricação mecânica.  Entender a linguagem de programação de máquinas e sua operação. Descrever as diversas ferramentas computacionais disponíveis nos dias de hoje para auxiliar o processo de manufatura industrial. 

## Introdução 

CAD (Computer-Aided Design) e CAM (Computer-Aided Manufacturing) são dois sistemas computacionais complementares muito usados na indústria mecânica, que juntos formam o que chamamos de sistema CAD/CAM.

CAD – Projeto Assistido por Computador
É o software usado para criar e editar modelos geométricos de peças e conjuntos, seja em 2D (desenhos técnicos) ou 3D (modelos sólidos e superfícies). Exemplos conhecidos: AutoCAD, SolidWorks, CATIA, Fusion 360.
O CAD substitui a prancheta de desenho e permite ao engenheiro/designer criar a geometria da peça com alta precisão, simular montagens, verificar interferências e gerar documentação técnica.

CAM – Fabricação Assistida por Computador
É o software que recebe o modelo geométrico vindo do CAD e gera automaticamente as trajetórias de ferramenta e o código de comando numérico (CNC/G-code) para as máquinas de usinagem (tornos CNC, centros de usinagem, fresadoras CNC etc.).
O CAM traduz o modelo 3D em movimentos reais de máquina, otimizando velocidades de corte, avanços e sequência de operações. Exemplos: Mastercam, EdgeCAM, HSMWorks, PowerMill.

Ideia → CAD (modelagem da peça) → CAM (geração do código) → Máquina CNC (fabricação)

Essa integração reduz erros, aumenta a produtividade e permite fabricar peças de altíssima complexidade geométrica com repetibilidade e precisão, coisas que seriam inviáveis manualmente. Por isso o CAD/CAM é fundamental em indústrias como a aeroespacial, automotiva, médica e de moldes.


## Conteúdo programático
<ul>
<h4><a href="/teoria/toleranciadimensional.md">Tolerância Dimensional</a></h4>
Tolerância Dimensional trata especificamente de variações permitidas nas medidas lineares (comprimentos, diâmetros, espessuras) de uma peça — ou seja, o quanto uma dimensão pode variar em relação ao valor nominal e ainda ser considerada aceitável.<br>

<h4><a href="/teoria/rugosidade.md">Acabamento Superficial / Rugosidade</a></h4>
A rugosidade refere-se às imperfeições superficiais de uma peça resultantes do seu processo de fabricação (usinagem, tratamento térmico, forjamento ou fundição).<br>
 
<h4><a href="/teoria/gdt.md">Dimensionamento e Tolerância Geométrica</a></h4>
O Dimensionamento e Tolerância Geométrica, conhecido mundialmente pela sigla GD&T (Geometric Dimensioning and Tolerancing), é uma linguagem internacional utilizada em desenhos de engenharia para descrever de forma exata e matemática o tamanho, a forma, a orientação e a localização dos elementos de uma peça.<br>

<h4><a href="/teoria/usinagem.md">Processos de usinagem</a></h4>
Usinagem é o processo de fabricação como um todo: qualquer método que produza uma peça através da remoção de material (cavaco) de um bloco bruto, até obter a forma, dimensão e acabamento desejados.<br>

<h4><a href="/teoria/torneamento.md">Processos de torneamento</a></h4>
O torneamento é um dos processos de usinagem — especificamente aquele em que a peça gira (presa numa placa do torno) enquanto uma ferramenta de corte, geralmente estacionária ou com movimento controlado, remove material para gerar formas cilíndricas ou cônicas.<br>

<h4><a href="/teoria/torno.md">Torno</a></h4>
O torno é uma máquina-ferramenta destinada à fabricação de peças axisimétricas (geometrias cilíndricas ou cônicas) através do processo de torneamento, que consiste na remoção de material (cavaco) enquanto a peça rotaciona. 

<h4><a href="/teoria/fresamento.md">Fresamento</a></h4>
É um processo de usinagem destinado à obtenção de superfícies planas, contornos, perfis e cavidades em peças de geometria prismática. Diferente do torneamento, onde a peça gira, no fresamento a ferramenta de corte é que possui o movimento de rotação.

<h4><a href="/teoria/elementos_fixacao.md">Elementos de Fixação</a></h4>
Elementos de fixação (jigs & fixtures) são dispositivos usados em processos de usinagem para posicionar e imobilizar a peça durante a fabricação, garantindo que ela permaneça na posição correta em relação à ferramenta de corte durante todo o processo
 
<h4><a href="/teoria/cae.md">CAE - Computer-Aided Engineering</a></h4>
O CAE (Computer-Aided Engineering, ou Engenharia Auxiliada por Computador) é a tecnologia que utiliza softwares de computador para simular, validar e otimizar projetos e processos de engenharia. <br>
 
<h4><a href="/teoria/programacaocnc.md">Programação CNC - Torno</a></h4>
A programação CNC (Comando Numérico Computadorizado) para tornos é um processo matemático e técnico que permite o controle preciso dos movimentos da máquina-ferramenta por meio de um computador dedicado.

<h4><a href="/teoria/pertcpm.md">PERT/CPM</a></h4>
O sistema PERT/CPM busca garantir que o projeto seja entregue no menor tempo e com o menor custo possível, mantendo a qualidade adequada e a otimização dos recursos disponíveis.

<h4><a href="/teoria/dfma.md">Design for Manufacturing and Assembly</a></h4>
O Design for Manufacturing and Assembly (DFMA) é uma técnica de apoio ao projeto de produtos que integra as considerações de manufatura e montagem logo nas etapas iniciais de criação

<br>
</ul>

## Biobliografia principal

GROOVER M.P.; ZIMMERS, E. W.; CAD/CAM: Computer-Aided Design And Manufacturing, Upper Saddle River, USA: Prentice Hall PTR, 1984. Xix, 489 p., il ISBN 9780131101302.

HALEVI, G.; Process and operation planning. Dordrecht, NLD: Kluwer Academic/PlenumPublishers, 2003. Xvi, 335., il ISBN 9789048164370. 

SOUZA, Adriano Fagali de; ULBRICH, Cristiane Brasil Lima. Engenharia integrada por computador e sistemas CAD/CAM/CNC: princípios e aplicações. 2 ed. São Paulo, SP: Artliber, 2013. 358 p., il ISBN 9788588098909.

Bibliografia Complementar: 

LEE, Kunwoo. Principles of CAD/CAM/CAE Systems. Reading, USA: Prentice Hall, 1999. Xvii, 582 p., il ISBN 9780201380361.

ALVES FILHO, Avelino. Elementos Finitos: a Base da Tecnologia CAE, 6ª. ed. São Paulo, SP: Érica, 2007. 300 p., il ISBN 9788571947412.

MCMAHON, Chris; BROWNE, Jimmie. CADCAM: Principles, Practice and Manufacturing Management. 2 ed. Harlow, GBR: Addison-Wesley Publishing, 1998. xxii, 665 p., il ISBN 9780201178197.

AHRENS, Carlos Henrique et al. Prototipagem rápida: tecnologias e aplicações. Edição de Neri Volpato. São Paulo, SP: Blucher, 2006. Xxi, 244 p., il ISBN 9788521203889. 

