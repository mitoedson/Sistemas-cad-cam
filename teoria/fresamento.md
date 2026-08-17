<h1>Fresamento</h1>

É um processo de usinagem destinado à obtenção de superfícies planas, contornos, perfis e cavidades em peças de geometria **prismática**. Diferente do torneamento, onde a peça gira, no fresamento a ferramenta de corte é que possui o movimento de rotação.

Abaixo, detalho a análise do processo e o método de usinagem com base nas fontes:

### **1. Princípio Mecânico do Fresamento**
O processo baseia-se na remoção de material através de uma ferramenta rotativa multidentada chamada **fresa**. 
*   **Dinâmica de Corte:** A fresa gira em alta velocidade enquanto a peça é fixada em uma mesa que se desloca (avanço) gradualmente em direção à ferramenta.
*   **Geração de Cavacos:** A remoção ocorre quando as arestas cortantes da fresa entram em contato com a peça, cortando ou raspando o material e gerando o cavaco.
*   **Versatilidade:** O método permite usinar uma grande variedade de materiais com alta eficiência de remoção.

### **2. A Máquina e seus Eixos (Fresadora CNC)**
Nas fresadoras e centros de usinagem, o sistema de coordenadas define a trajetória da ferramenta no espaço:
*   **Eixo Z:** Corresponde ao **eixo-árvore** (onde a ferramenta é fixada). Pode ser posicionado na vertical ou na horizontal.
*   **Eixo X:** Refere-se ao movimento **longitudinal** da mesa.
*   **Eixo Y:** Refere-se ao movimento **transversal** da mesa.

#### A convenção padrão
* Eixo X → movimento longitudinal (o de maior curso na mesa, geralmente da esquerda para a direita, olhando de frente para a máquina)
* Eixo Y → movimento transversal (perpendicular a X, geralmente de trás para frente/frente para trás)
* Eixo Z → movimento vertical, paralelo ao eixo-árvore (como já confirmamos)

#### Uma forma prática de fixar isso

Numa fresa vertical convencional, imagine-se de frente para a máquina, olhando para a mesa:

* Mover a mesa da esquerda para a direita = eixo X
* Mover a mesa para dentro/fora, na sua direção = eixo Y
* Subir/descer o cabeçote (ou a mesa, dependendo da máquina) = eixo Z

#### Conectando com os localizadores

| Eixo da máquina | Movimento | Grau de liberdade que os localizadores travam |
|---|---|---|
| Z | Vertical (avanço/recuo da ferramenta) | Translação em Z → travada pelos 3 pontos (plano XY) |
| X | Longitudinal | Translação em X → travada pelo 1 ponto final |
| Y | Transversal | Translação em Y → travada pelos 2 pontos |




### **3. Principais Operações de Usinagem**
O processo é dividido em operações específicas conforme o formato desejado:
*   **Faceamento:** Usado para produzir superfícies planas perpendiculares ao eixo da fresa, geralmente para nivelar a peça. Utiliza-se um **cabeçote fresador**.
*   **Fresamento de Topo:** Remove material para criar perfis ou cavidades, utilizando uma **fresa de topo**.
*   **Rasgo ou Canal:** Cria aberturas em linha reta (como rasgos de chaveta) com fresas de corte reto.
*   **Arredondamento e Faceamento de Cantos:** Operações para suavizar cantos vivos (gerar raios) ou criar rebaixos a 90º.
*   **Usinagem 3D:** Estratégias complexas de remoção de volume para criar formas tridimensionais.

### **4. Programação e Estratégias (CNC)**
Na usinagem por fresamento controlada por computador, seguem-se códigos padronizados para guiar o **caminho de corte**:
*   **Compensação de Diâmetro (G41/G42):** Essencial para que o CNC calcule o deslocamento necessário da ferramenta em relação ao contorno da peça, considerando o raio da fresa.
*   **Interpolações:** O comando **G01** realiza cortes em linha reta, enquanto **G02 (horário)** e **G03 (anti-horário)** realizam arcos e perfis circulares.
*   **Ciclos Fixos:** Utilizados para automatizar tarefas repetitivas como a furação (G81-G89) frontal ou lateral.

### **5. Qualidade e Acabamento (Rugosidade)**
A rugosidade (erros microgeométricos) no fresamento é influenciada pelas marcas deixadas pelos dentes da fresa durante o avanço.
*   **Simbologia:** No desenho técnico, a indicação de fresamento é feita sobre o símbolo básico de rugosidade ($\sqrt{ }$) com a inscrição "**fresado**".
*   **Planejamento:** Para atingir acabamentos finos (Ra até 1,6 µm), o planejamento deve prever ao menos três etapas: **desbaste**, **semi-acabamento** e **acabamento**.

A precisão do fresamento depende criticamente do **posicionamento e fixação da peça** na mesa (usando morsas ou grampos), garantindo que ela suporte as forças dinâmicas da usinagem sem vibrações excessivas.
