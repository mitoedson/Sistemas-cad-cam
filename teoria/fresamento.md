# Fresamento

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

### **3. Classificação quanto ao Sentido de Corte: Concordante e Discordante**
Antes de detalhar as operações, é fundamental entender como a fresa se relaciona com o sentido de avanço da peça — essa é a classificação mais importante do processo, com impacto direto em acabamento, vibração e vida útil da ferramenta.

*   **Fresamento Discordante (convencional):** O sentido de rotação da fresa é **contrário** ao sentido de avanço da peça. O cavaco começa fino e termina espesso — a ferramenta "raspa" a peça antes de efetivamente cortar, gerando mais atrito e calor no início do contato. É mais indicado para peças brutas ou com casca de fundição/laminação, pois a fresa "entra por baixo" da superfície irregular, sem impactar diretamente contra ela.
*   **Fresamento Concordante:** O sentido de rotação da fresa é **igual** ao sentido de avanço da peça. O cavaco começa espesso e termina fino, reduzindo o atrito no início do corte e gerando melhor acabamento superficial. Exige, porém, uma máquina rígida e sem folgas no fuso da mesa — caso contrário, a força de corte pode "puxar" a peça e a ferramenta, causando vibração ou quebra de dentes.

| Aspecto | Discordante | Concordante |
|---|---|---|
| Espessura do cavaco | Cresce (fino → espesso) | Decresce (espesso → fino) |
| Desgaste da ferramenta | Maior (atrito inicial) | Menor |
| Acabamento superficial | Inferior | Superior |
| Exigência da máquina | Menor (tolera folgas) | Maior (requer rigidez, sem folga no fuso) |
| Indicação típica | Peças brutas, cascas duras | Peças pré-usinadas, acabamento fino |

### **4. Classificação quanto à Orientação: Tangencial e Frontal**
Complementando a classificação anterior, o fresamento também se divide conforme a posição do eixo da fresa em relação à superfície gerada:

*   **Fresamento Tangencial (periférico):** O eixo da fresa é **paralelo** à superfície usinada — o corte ocorre pela periferia (dentes ao redor da fresa), como em uma fresa cilíndrica ou fresa de disco. É o princípio por trás de operações como rasgos e canais.
*   **Fresamento Frontal (de topo/facial):** O eixo da fresa é **perpendicular** à superfície usinada — o corte ocorre principalmente pelos dentes na face frontal da ferramenta, como no faceamento com cabeçote fresador. Costuma gerar superfícies mais planas e é mais produtivo para grandes áreas.

Muitas fresas modernas (como as fresas de topo) combinam os dois princípios ao mesmo tempo: cortam tanto pela periferia (lateral) quanto pela face (frontal), permitindo tanto faceamento quanto abertura de cavidades com a mesma ferramenta.

### **5. Tipos de Fresadoras**
A escolha da máquina influencia diretamente a rigidez do processo e o tipo de operação viável:

*   **Fresadora Horizontal:** O eixo-árvore é paralelo à mesa. Tradicionalmente usada para fresamento tangencial, rasgos e canais, com boa rigidez para desbaste pesado.
*   **Fresadora Vertical:** O eixo-árvore é perpendicular à mesa. É a configuração mais comum atualmente, adequada para faceamento, cavidades e contornos.
*   **Fresadora Universal:** Permite girar o cabeçote, combinando as capacidades horizontal e vertical na mesma máquina.
*   **Centro de Usinagem CNC:** Fresadora com controle numérico computadorizado, geralmente com troca automática de ferramentas (ATC) e capacidade de operar em 3, 4 ou 5 eixos simultâneos, permitindo usinagem 3D complexa sem reposicionamento manual da peça.

### **6. Principais Operações de Usinagem**
O processo é dividido em operações específicas conforme o formato desejado:
*   **Faceamento:** Usado para produzir superfícies planas perpendiculares ao eixo da fresa, geralmente para nivelar a peça. Utiliza-se um **cabeçote fresador**.
*   **Fresamento de Topo:** Remove material para criar perfis ou cavidades, utilizando uma **fresa de topo**.
*   **Rasgo ou Canal:** Cria aberturas em linha reta (como rasgos de chaveta) com fresas de corte reto.
*   **Arredondamento e Faceamento de Cantos:** Operações para suavizar cantos vivos (gerar raios) ou criar rebaixos a 90º.
*   **Usinagem 3D:** Estratégias complexas de remoção de volume para criar formas tridimensionais.

### **7. Tipos de Fresas (Ferramentas)**
Cada geometria de fresa é projetada para um propósito específico:

*   **Fresa de Topo (end mill):** Corta pela periferia e pela ponta; a mais versátil, usada em cavidades, contornos e rasgos.
*   **Fresa de Disco (fresa de fenda):** Corta apenas pela periferia, ideal para rasgos estreitos e profundos ou seccionamento.
*   **Fresa Angular:** Possui arestas de corte inclinadas, usada para chanfros e rasgos em ângulo (como guias em cauda de andorinha).
*   **Fresa de Perfil (módulo):** Possui geometria específica para gerar um perfil determinado em uma única passada, como dentes de engrenagem.
*   **Fresa de Rosqueamento (thread mill):** Gera roscas internas ou externas por interpolação helicoidal, alternativa ao macho de roscar tradicional.
*   **Cabeçote Fresador (fresa de facear):** Grande diâmetro, múltiplos insertos intercambiáveis, usado especificamente para faceamento de grandes áreas com alta produtividade.

### **8. Parâmetros de Corte**
A produtividade e a qualidade do fresamento dependem do ajuste correto de três parâmetros principais:

*   **Velocidade de Corte (Vc):** Velocidade tangencial na periferia da fresa, geralmente em m/min. Depende do material da peça e da ferramenta (definindo a rotação da árvore, em rpm).
*   **Avanço por Dente (fz):** Espessura de material removida por cada dente da fresa a cada volta, geralmente em mm/dente. Combinado ao número de dentes e à rotação, define o avanço da mesa (mm/min).
*   **Profundidade de Corte (ap) e Penetração de Trabalho (ae):** ap é a profundidade axial (o quanto a fresa penetra ao longo do seu eixo); ae é a penetração radial (o quanto a fresa avança lateralmente na peça). Juntos, determinam o volume de material removido por passada.

O equilíbrio entre esses parâmetros define se a operação está otimizada para desbaste (alta remoção, tolerâncias abertas) ou para acabamento (baixa remoção, alta precisão) — reforçando a lógica de etapas já mencionada na seção de qualidade.

### **9. Programação e Estratégias (CNC)**
Na usinagem por fresamento controlada por computador, seguem-se códigos padronizados para guiar o **caminho de corte**:
*   **Compensação de Diâmetro (G41/G42):** Essencial para que o CNC calcule o deslocamento necessário da ferramenta em relação ao contorno da peça, considerando o raio da fresa.
*   **Interpolações:** O comando **G01** realiza cortes em linha reta, enquanto **G02 (horário)** e **G03 (anti-horário)** realizam arcos e perfis circulares.
*   **Ciclos Fixos:** Utilizados para automatizar tarefas repetitivas como a furação (G81-G89) frontal ou lateral.
*   **Fresamento de Roscas e Interpolação Helicoidal:** Combina os movimentos G02/G03 (arco) com um deslocamento simultâneo no eixo Z, fazendo a fresa de rosqueamento percorrer uma trajetória helicoidal. Permite gerar roscas internas ou externas com uma única ferramenta, substituindo o macho de roscar convencional e reduzindo o risco de quebra da ferramenta em furos cegos.

### **10. Qualidade e Acabamento (Rugosidade)**
A rugosidade (erros microgeométricos) no fresamento é influenciada pelas marcas deixadas pelos dentes da fresa durante o avanço.
*   **Simbologia:** No desenho técnico, a indicação de fresamento é feita sobre o símbolo básico de rugosidade ($\sqrt{ }$) com a inscrição "**fresado**".
*   **Planejamento:** Para atingir acabamentos finos (Ra até 1,6 µm), o planejamento deve prever ao menos três etapas: **desbaste**, **semi-acabamento** e **acabamento**.
*   **Influência do sentido de corte:** Como visto na Seção 3, o fresamento concordante tende a gerar melhor acabamento que o discordante, sendo preferido nas etapas finais quando a máquina permite.

A precisão do fresamento depende criticamente do **posicionamento e fixação da peça** na mesa (usando morsas ou grampos), garantindo que ela suporte as forças dinâmicas da usinagem sem vibrações excessivas.