<h2>Torno</h2>

O **torno** é uma máquina-ferramenta destinada à fabricação de peças **axisimétricas** (geometrias cilíndricas ou cônicas) através do processo de **torneamento**, que consiste na remoção de material (cavaco) enquanto a peça rotaciona. No contexto moderno, o **torno CNC** (Comando Numérico Computadorizado) permite que esses movimentos sejam controlados com extrema precisão por um computador dedicado.

Abaixo, apresento uma análise detalhada sobre a máquina, seus processos e métodos aplicados:

### **1. Configurações e Sistemas de Coordenadas**
O deslocamento da ferramenta no torno ocorre no **plano XZ**.
*   **Eixo X:** Refere-se ao movimento **transversal**, controlando a medida do raio ou diâmetro da peça.
*   **Eixo Z:** Refere-se ao movimento **longitudinal**, controlando o comprimento da usinagem.
*   **Sentido dos Movimentos:** Pela regra da mão direita, o sentido positivo ocorre quando a ferramenta se afasta da peça.
*   **Torres de Ferramentas:** A máquina pode possuir torre dianteira ou traseira, e alguns modelos utilizam revólveres com até 12 posições para diferentes ferramentas.

### **2. Processos de Torneamento**
As operações de torneamento são classificadas de acordo com o formato final desejado e a trajetória da ferramenta:
*   **Torneamento Longitudinal (Straight Turning):** Gera perfis cilíndricos ao longo do eixo da peça.
*   **Faceamento (Facing):** Usinagem da face transversal para garantir planeza e o comprimento exato.
*   **Mandrilamento (Boring):** Torneamento de superfícies internas.
*   **Sangramento (Grooving / Cut-off):** Abertura de canais ou o corte final para separar a peça do material bruto.
*   **Roscamento (Threading):** Abertura de roscas internas ou externas, que podem ser paralelas ou cônicas.
*   **Furação (Drilling):** Realizada geralmente no centro de rotação da peça.

### **3. Métodos de Posicionamento e Fixação**
A qualidade da usinagem depende diretamente da estabilidade da peça na máquina.
*   **Dispositivos de Fixação:** Utilizam-se **placas e castanhas** para manter a peça firmemente posicionada sob as forças de corte.
*   **Impacto na Precisão:** Elementos de fixação inadequados podem causar **acúmulo de erros**, afetando as tolerâncias dimensionais e geométricas.
*   **Pontos de Referência:** Para a execução correta, o programador define o **Ponto Zero da Peça (W)**, facilitando a conversão das medidas do desenho em coordenadas de máquina.

### **4. Controle de Qualidade e Tolerâncias Geométricas**
Como nenhum processo é perfeitamente exato, aplicam-se normas (como a **ISO 1101**) para controlar os desvios aceitáveis.
*   **Erros Microgeométricos (Rugosidade):** O torneamento deixa sulcos superficiais. O planejamento deve prever o número de processos: **desbaste** (1 processo para Ra até 10 µm), **semi-acabamento** (2 processos) e **acabamento** (3 ou mais processos para Ra até 1,6 µm).
*   **Batimento (Runout):** É a tolerância composta mais importante para peças que giram. Ela representa a variação máxima permitida em relação a um eixo de referência quando a peça sofre uma **rotação completa de 360º**.
*   **Forma e Orientação:** O torno deve garantir que a peça mantenha a **circularidade** (ovalização controlada) e a **cilindricidade** (controle ao longo de todo o comprimento).

Existe uma relação direta entre o acabamento e a precisão: a **tolerância dimensional** em milímetros que se pode obter pode ser estimada dividindo-se o valor da rugosidade (em mícron) por 40. Por exemplo, uma rugosidade Ra de 0,1 µm equivale a uma tolerância de aproximadamente **±0,0025 mm**.

Aqui está um complemento à sua análise sobre o torno, seguindo a numeração como continuação:

### 5. Tipos de Torno

Antes de detalhar o CNC, vale situar as variantes de máquina que compartilham a mesma lógica de fabricação:

- **Torno mecânico convencional:** operado manualmente, é o modelo clássico e é composto essencialmente por barramento, cabeçote fixo, cabeçote móvel, carro principal, carro transversal, carro superior e placa de fixação. É indicado para peças de precisão em pequenas séries, mas depende fortemente da habilidade do operador.
- **Torno CNC:** substitui o controlo manual dos carros por comando numérico computadorizado — ideia originada em 1978, quando o comando manual dos carros foi substituído por microprocessadores, permitindo programar e armazenar sequências de movimentos para trocas rápidas de programa.
- **Torno revólver:** voltado para fabricação em série de peças pequenas (buchas, pinos), com um cabeçote adaptado para fixar várias ferramentas simultaneamente, agilizando a troca entre operações.
- **Torno automático:** realiza toda a sequência — da alimentação da barra bruta até a peça finalizada — sem intervenção humana, sendo aplicado em produção seriada de médios e grandes lotes.

### 6. Dispositivos de Fixação (aprofundamento)

Complementando o que você já tem na seção 3, os principais dispositivos de fixação incluem:

- **Placa autocentrante de 3 castanhas:** as castanhas movem-se simultaneamente, garantindo centralização automática — ideal para peças cilíndricas ou hexagonais e trocas rápidas de peça.
- **Placa de 4 castanhas independentes:** cada castanha é ajustada individualmente, sendo a opção indicada para peças quadradas, retangulares, excêntricas ou torneamento descentralizado (quando o centro da peça não coincide com o centro da placa).
- **Placa de 6 castanhas:** distribui a força em seis pontos de contacto, reduzindo deformação em peças de paredes finas ou tubos.
- **Pinças (mandril de pinça):** usadas para fixar peças de diâmetro menor e mais uniforme, com elevada precisão de centragem.
- **Contraponto (ponto rotativo):** suporta a extremidade oposta da peça, especialmente importante em peças longas, evitando flexão sob a força de corte.
- **Luneta fixa e luneta móvel:** apoios adicionais ao longo do comprimento da peça, usados quando a relação comprimento/diâmetro é elevada e há risco de vibração ou flexão.

A escolha do dispositivo certo impacta diretamente a precisão dimensional, o tempo de setup e a segurança operacional, especialmente em peças de paredes finas, grandes comprimentos ou formas assimétricas.

### 7. Tolerâncias Geométricas (aprofundamento conforme ISO 1101)

Complementando o que você já introduziu com o batimento, a norma ISO 1101 (Geometrical Product Specifications — Geometric Tolerancing) padroniza a simbologia e os critérios de forma, orientação, posição e batimento aplicáveis a peças torneadas:

- **Circularidade:** controla o desvio da seção transversal em relação a um círculo perfeito, num único plano perpendicular ao eixo. Valores típicos alcançáveis no torneamento situam-se até cerca de 0,01 mm, contra 0,01–0,015 mm no mandrilamento e 0,005–0,015 mm na retificação.
- **Cilindricidade:** é mais restritiva que a circularidade, pois controla a variação ao longo de toda a superfície cilíndrica — combinando circularidade, retilinidade e conicidade — considerando a peça como um todo tridimensional, não apenas uma seção.
- **Batimento circular (runout):** mede a variação de uma superfície em relação a um eixo de referência (datum) durante uma rotação completa de 360°, sendo a tolerância composta mais relevante para peças rotativas.
- **Batimento total:** mais restritivo que o batimento circular, controla a variação ao longo de toda a superfície (não apenas numa seção) durante a rotação, sendo usado quando a aplicação exige controlo simultâneo de forma e orientação.

Essas tolerâncias são especialmente críticas em componentes rotativos de precisão (eixos, mancais), onde erros de forma se traduzem diretamente em vibração, desgaste prematuro de rolamentos e perda de desempenho em serviço.



