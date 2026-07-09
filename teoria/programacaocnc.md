<h2>Programação CNC - Torno</h2>

A **programação CNC** (Comando Numérico Computadorizado) para tornos é um processo matemático e técnico que permite o controle preciso dos movimentos da máquina-ferramenta por meio de um computador dedicado.

### 1. Fundamentos e Normas de Programação
A programação segue normas internacionais como a **ISO 6983**, que padroniza o formato das instruções para garantir a intercambiabilidade de programas entre diferentes máquinas, e a **ISO 841**, que define a nomenclatura de eixos e movimentos. 
*   **Regra da Mão Direita:** Utilizada para identificar o sentido positivo dos eixos.
*   **Eixos do Torno:** O deslocamento ocorre no plano **XZ**, onde **X** refere-se ao eixo transversal (diâmetro ou raio) e **Z** ao eixo longitudinal (comprimento).

### 2. Pontos de Referência e Sistemas de Coordenadas
O programador deve gerenciar diferentes pontos "zero" para que a ferramenta percorra a trajetória correta:
*   **Ponto Zero da Máquina (M):** Definido pelo fabricante, é a origem de todos os sistemas.
*   **Ponto de Referência (R):** Serve para aferição e controle do sistema de medição.
*   **Ponto Zero da Peça (W):** Definido pelo programador para facilitar a conversão das medidas do desenho técnico em valores de coordenadas.

Existem dois métodos principais para definir posições:
*   **Coordenadas Absolutas (G90):** O ponto é dado em relação ao **zero-peça**.
*   **Coordenadas Incrementais (G91):** O ponto é dado em relação à **posição anterior** da ferramenta ("quanto falta para chegar").

### 3. Funções de Programação (G e M)
As fontes detalham comandos específicos que compõem os blocos de programa:
*   **Funções Preparatórias (G):**
    *   **G00:** Interpolação linear com **avanço rápido** (posicionamento).
    *   **G01:** Interpolação linear com **avanço de trabalho** (usinagem reta).
    *   **G02 / G03:** Interpolação circular nos sentidos **horário** e **anti-horário**, respectivamente.
*   **Funções Auxiliares (M):** Comandos miscelâneos como **M30** (fim de programa), **M07/M09** (liga/desliga refrigerante) e controle de rotação.

### 4. Recursos Avançados e Ciclos Automáticos
Para simplificar a programação de geometrias complexas, utilizam-se:
*   **Compensação de Raio da Ferramenta (G40, G41, G42):** Essencial para corrigir o erro gerado pelo raio da ponta da pastilha em superfícies inclinadas ou arcos.
*   **Ciclos Fixos:**
    *   **G71:** Ciclo automático de **desbaste longitudinal**.
    *   **G70:** Ciclo de **acabamento** final.
    *   **G76:** Ciclo automático para **abertura de roscas**.
    *   **G81 / G83:** Ciclos de **furação** (simples e profunda com quebra de cavaco).

### 5. Estrutura do Programa
Um programa otimizado deve conter o número do programa (**O**), números de sentença (**N**), definição de ferramentas (**T**), velocidade de corte (**S**) e avanço (**F**). Cada bloco de informação termina com o caractere **EOB** (End of Block), representado por **;**.

A análise das fontes demonstra que a precisão final da peça usinada depende não apenas do código, mas também da correta **fixação da peça** (castanhas e placas) e da seleção de processos compatíveis com a rugosidade e tolerância exigidas no projeto.

<hr>


