<h2>Tolerância dimensional</h2>

A **tolerância dimensional** é a variação permitida em uma dimensão específica de uma peça, essencial porque é impossível fabricar componentes com medidas rigorosamente exatas devido a imprecisões inerentes aos processos de manufatura (máquinas, materiais e falhas humanas). Seu principal objetivo é garantir a **intercambiabilidade**, permitindo que peças sejam substituídas sem a necessidade de reparos ou ajustes manuais.

Abaixo estão os detalhes fundamentais extraídos do material:

### **1. Elementos da Cota com Tolerância**
Para entender como uma dimensão varia, utilizam-se os seguintes conceitos:
*   **Dimensão Nominal:** É a medida de referência indicada no desenho técnico.
*   **Afastamentos:** São desvios aceitáveis para mais ou para menos em relação à dimensão nominal.
    *   **Afastamento Superior:** Define o limite máximo da cota.
    *   **Afastamento Inferior:** Define o limite mínimo da cota.
*   **Limites Dimensionais:** A **Dimensão Máxima** e a **Dimensão Mínima** são os valores extremos aceitáveis. A medida real da peça após a fabricação (**Dimensão Efetiva** = **Dimensão Real**) deve estar entre esses dois limites.
*   **Cálculo da Tolerância:** Corresponde ao valor absoluto da diferença entre a dimensão máxima e a mínima.

### **2. Sistema ISO de Tolerâncias (ABNT NBR 6158)**
A norma padroniza a indicação de tolerâncias para facilitar a produção global:
*   **Unidade de Medida:** O padrão é o **micrometro (mícron)**, onde $1\mu\text{m} = 0,001\text{ mm}$.
*   **Qualidades de Trabalho (Graus IT):** Existem 18 qualidades, de **IT 01 a IT 16**. Quanto menor o número, maior a precisão. Graus baixos são usados para instrumentos de medição (mecânica extraprecisa), enquanto graus elevados são para mecânica grosseira.
*   **Campos de Tolerância (Letras):** O sistema utiliza letras para indicar a posição da tolerância. Letras **maiúsculas** (A a ZC) referem-se a **furos** (medidas internas) e letras **minúsculas** (a a zc) referem-se a **eixos** (medidas externas).

### **3. Tipos de Ajustes e Sistemas de Referência**
O ajuste é o encaixe entre duas peças (eixo e furo). Existem três classes:
<img width="800" alt="image" src="https://github.com/user-attachments/assets/d1aed5c6-2846-495f-8520-2eee2d8d75d5" />

*   **Ajuste com Folga:** A dimensão máxima do eixo é menor ou, em casos extremos, igual à dimensão mínima do furo, permitindo rotação ou deslizamento.
*   **Ajuste com Interferência:** A dimensão mínima do eixo é maior ou, em casos extremos, igual à dimensão máxima do furo, exigindo esforço ou pressão para a montagem, resultando em um encaixe fixo.
*   **Ajuste Incerto:** Os campos de tolerância se sobrepõem, podendo resultar em folga ou interferência conforme as medidas reais fabricadas. A dimensão máxima do eixo é maior que a dimensão mínima do furo, e a dimensão máxima do furo é maior que a dimensão mínima do eixo. O resultado depende das dimensões efetivas após a fabricação.

Para racionalizar a produção, a indústria adota sistemas de base fixa:
*   **Sistema Furo-Base (H):** Ou Furo Padrão, é o sistema de maior aceitação na indústria. Nele, a tolerância do furo permanece fixa (identificada pela letra H) e variam-se as tolerâncias dos eixos para obter o ajuste desejado. No furo H, o afastamento inferior é sempre zero.
*   **Sistema Eixo-Base (h):** Ou Eixo Padrão, a tolerância do eixo permanece constante (identificada pela letra h) e fabricam-se furos com tolerâncias variáveis. No eixo h, o afastamento superior é sempre zero.

### **4. Relação com a Rugosidade**
As fontes indicam que o controle dimensional e o acabamento superficial estão interligados. Uma regra prática para estimar a tolerância dimensional possível de se obter em um processo é dividir o valor da rugosidade (**Ra** em mícrons) por 40.
