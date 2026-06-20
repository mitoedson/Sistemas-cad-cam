<h2>Tolerância de Orientação</h2>

As **tolerâncias de orientação** estabelecem os limites para os desvios angulares aceitáveis de um elemento da peça (como uma linha ou superfície) em relação a uma inclinação ideal prescrita no desenho técnico. Diferente das tolerâncias de forma, que se aplicam a elementos isolados, as de orientação aplicam-se obrigatoriamente a **elementos associados**, o que significa que exigem sempre um **elemento de referência** (conhecido como *datum*) para que a verificação seja realizada.

Abaixo, apresento uma análise detalhada baseada nas fontes:

### **1. Categorias e Simbologia**
O sistema GD&T (NBR 6409 / ISO 1101) classifica as condições de orientação em três tipos principais:
*   **Paralelismo (//):** Os elementos devem manter uma distância equidistante constante e não formar ângulo entre si.
*   **Perpendicularidade (⊥):** Condição onde o elemento tolerado deve formar um ângulo reto exato de 90º em relação à referência.
*   **Inclinação ou Angularidade (∠):** Aplicada quando o projeto exige um ângulo específico diferente de 90º entre as partes.

### **2. Campo de Tolerância (Zona de Tolerância)**
O campo de tolerância é a região espacial dentro da qual o elemento real deve estar contido para ser aprovado. Na orientação, esse campo é definido por planos ou linhas que guardam a relação angular exata com a referência:
*   **Dois planos paralelos:** Afastados por uma distância "**t**", rigorosamente posicionados (paralelos, perpendiculares ou inclinados) em relação ao plano de referência.
*   **Duas retas paralelas:** Quando a tolerância é verificada em um plano específico para o eixo de um furo ou uma aresta.
*   **Zona Cilíndrica:** Se o valor da tolerância for precedido pelo símbolo de diâmetro (**$\varnothing$**), o eixo da peça deve situar-se dentro de um cilindro imaginário paralelo ou perpendicular à referência.
*   **Paralelepípedo:** Quando a tolerância é especificada em duas direções perpendiculares entre si (seção transversal $t_1 \times t_2$).

### **3. Princípios de Verificação e Interpretação**
*   **Referência Ideal:** Durante a medição, assume-se que o elemento de referência é **geometricamente perfeito** (isento de erros), mesmo que na prática ele possua variações reais. Isso é necessário para isolar e medir apenas o desvio de orientação do elemento tolerado.
*   **Cotas Básicas:** Para tolerâncias de inclinação, o ângulo ideal deve ser indicado como uma **cota básica** (dentro de uma moldura retangular), o que indica que aquela medida é teoricamente exata e não possui tolerância dimensional própria, sendo controlada pelo quadro de tolerância geométrica.
*   **Tolerância Projetada (P):** Em casos de orientação de eixos (como pinos ou furos), a tolerância pode ser aplicada não apenas ao elemento em si, mas ao seu prolongamento, garantindo que o desalinhamento não prejudique a montagem de peças adjacentes.

### **4. Relação com outras Tolerâncias**
É importante notar que algumas tolerâncias englobam outras. Por exemplo, a especificação de **paralelismo** contém implicitamente a condição de **retitude** (retilineidade), embora o inverso não seja verdadeiro: uma peça pode ser perfeitamente reta, mas não estar paralela à sua base. Além disso, desvios de orientação são frequentemente captados durante a medição de **batimento total**, que analisa simultaneamente forma, orientação e posição.
