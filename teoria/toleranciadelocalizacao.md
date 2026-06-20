<h2>Tolerância de Localização (Posição)</h2>

As **tolerâncias de localização (ou posição)** estabelecem o desvio admissível na localização de um elemento geométrico (ponto, reta ou plano) em relação à sua **posição teoricamente exata** prescrita no projeto. Elas são aplicadas obrigatoriamente a **elementos associados**, o que significa que exigem elementos de referência (*datums*) para sua verificação.

Abaixo, apresento uma análise detalhada sobre o funcionamento e as categorias deste grupo de tolerâncias:

### **1. Importância e Objetivo**
A principal função das tolerâncias de localização é **racionalizar os processos de montagem**. Elas garantem que peças fabricadas separadamente se encaixem perfeitamente, evitando a necessidade de ajustes manuais custosos. Um benefício técnico crucial é a **prevenção do acúmulo de erros** que ocorre em sistemas de cotagem em cadeia tradicionais, onde cada tolerância dimensional se soma à anterior.

### **2. O Conceito de Cota Básica**
Para definir a localização ideal, utilizam-se as **cotas básicas** (dimensões emolduradas por um retângulo, ex: $$). Estas cotas representam medidas teoricamente exatas e **não possuem tolerância dimensional direta**; a variação permitida para o elemento é dada exclusivamente pelo quadro de tolerância geométrica associado.

### **3. Categorias de Tolerâncias de Localização**
O sistema GD&T (NBR 6409 / ISO 1101) divide este grupo em:

*   **Posição de um Ponto:** O campo de tolerância é geralmente uma área circular ou uma esfera cujo centro coincide com a posição teórica exata. Para ser aprovado, o ponto efetivo deve estar contido dentro desse diâmetro "t".
*   **Posição de uma Linha (Eixo):** O campo de tolerância pode ser um **paralelepípedo** (seção transversal $t_1 \times t_2$) ou um **cilindro** (se o valor for precedido pelo símbolo $\varnothing$). O eixo real da peça deve situar-se dentro deste volume imaginário posicionado exatamente sobre a linha teórica.
*   **Posição de uma Superfície ou Plano Médio:** Define o desvio permitido para um plano em relação à sua localização ideal. O campo é limitado por **dois planos paralelos** afastados pela distância "t" e dispostos simetricamente em relação à posição teórica.
*   **Concentricidade:** Trata do desvio permitido na posição do centro de um círculo em relação ao centro de outro círculo tomado como referência. O campo é um círculo de diâmetro "t" concêntrico ao elemento de referência.
*   **Coaxialidade:** É um caso de concentricidade aplicado ao longo de eixos de simetria. O eixo da parte tolerada deve estar contido dentro de um **cilindro de tolerância** cujo eixo central é o elemento de referência.
*   **Simetria:** Define os limites para erros de simetria de planos médios ou eixos. O campo é formado por dois planos ou retas paralelas dispostas simetricamente em torno do plano (ou linha) de referência.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/d8cf130d-e55f-4e5e-9e28-d234b17cecac" />


### **4. Campo de Tolerância (Zonas de Controle)**
Diferente das tolerâncias cartesianas, que geram zonas quadradas, o GD&T utiliza frequentemente **campos de tolerância cilíndricos**, o que permite um ganho de **57% na margem de erro aceitável** para a fabricação sem comprometer a funcionalidade da montagem.

### **5. Modificadores (Bônus de Tolerância)**
A aplicação da **Condição de Máximo Material ($\textcircled{M}$)** é comum em tolerâncias de posição de furos e eixos. Ela permite que, se o elemento for fabricado fora de sua dimensão de máximo material (ex: um furo maior que o mínimo permitido), a diferença se transforme em um **bônus**, aumentando a tolerância de localização daquela peça e reduzindo o descarte de componentes funcionais.
