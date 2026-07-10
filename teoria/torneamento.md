<h2>Processos de usinagem e torneamento</h2>

A usinagem e o torneamento são processos fundamentais de fabricação voltados para a transformação de um corpo bruto em uma peça acabada através da remoção de material (cavaco)

### 1. Visão Geral da Usinagem
A usinagem é o método de produção que permite obter formas, dimensões e acabamentos superficiais específicos, garantindo que a peça esteja de acordo com o desenho técnico
<p>
<b>Finalidade Técnica:</b> É essencial para garantir a funcionalidade e intercambiabilidade das peças, permitindo que componentes sejam substituídos sem ajustes manuais.
<p>
<b>Classificação por Formato:</b><br> 
Os processos são selecionados de acordo com a geometria da superfície:
<ul>
<li>Axisimétricos: Torneamento, retificação, brunimento e polimento
<li>Prismáticos: Fresamento, retificação e lapidação
<li>Recursos Adicionais: Furação, alargamento, mandrilamento e roscamento
</ul>

### 2. O Processo de Torneamento
O torneamento é a operação de usinagem destinada à fabricação de peças axisimétricas (cilíndricas ou cônicas). Ele pode ser realizado em tornos convencionais ou em tornos CNC (Comando Numérico Computadorizado), onde o controle dos movimentos é feito por um computador dedicado
<p>
<b>Principais Operações de Torneamento:</b>
<ul>
    <li>Torneamento Longitudinal (Straight Turning): Gera perfis ao longo do eixo da peça
    <li>Faceamento (Facing): Usinagem da face transversal da peça para garantir planeza e comprimento
    <li>Mandrilamento (Boring): Torneamento de superfícies internas (furos existentes)
    <li>Sangramento (Grooving / Cut-off): Abertura de canais ou corte final da peça
    <li>Roscamento (Threading): Abertura de roscas internas ou externas, paralelas ou cônicas
</ul>

### 3. Posicionamento e Fixação
A precisão da usinagem depende diretamente de como a peça é presa à máquina. Os dispositivos de fixação, como placas e castanhas, devem manter a peça firmemente posicionada sob a ação das forças de corte
.
Elementos de fixação mal projetados podem causar acúmulo de erros e afetar a precisão dimensional e geométrica da peça
.
O sistema de referência no torno utiliza o plano XZ, onde X controla o diâmetro e Z o comprimento
.
### 4. Qualidade e Acabamento Superficial (Rugosidade)
A usinagem deixa marcas ou sulcos na superfície (erros microgeométricos), conhecidos como rugosidade
. O planejamento do processo deve considerar a rugosidade média (Ra) desejada:
Desbaste: Apenas 1 processo, para rugosidades de até 10 µm
.
Semi-acabamento: 2 processos, para rugosidades de até 6,3 µm
.
Acabamento: 3 ou mais processos (incluindo retificação), para rugosidades finas de até 1,6 µm ou menos
.
As fontes indicam que quanto melhor o acabamento exigido, maior será o custo de fabricação
. Existe também uma relação direta entre o acabamento e a precisão: a tolerância dimensional em milímetros que se pode obter pode ser estimada dividindo-se o valor da rugosidade (em mícron) por 40
.
### 5. Programação e Execução (CNC)
No torneamento moderno, utiliza-se a programação via funções preparatórias (G) e auxiliares (M) para automatizar o caminho da ferramenta
. O uso de ciclos automáticos (como o G71 para desbaste e G76 para roscas) simplifica a fabricação de geometrias complexas, enquanto a compensação do raio da ferramenta (G41/G42) garante a exatidão em superfícies inclinadas e raios
.
