<h2>Torno</h2>

O **torno** é uma máquina-ferramenta destinada à fabricação de peças **axisimétricas** (geometrias cilíndricas ou cônicas) através do processo de **torneamento**, que consiste na remoção de material (cavaco) enquanto a peça rotaciona. No contexto moderno, o **torno CNC** (Comando Numérico Computadorizado) permite que esses movimentos sejam controlados com extrema precisão por um computador dedicado.

Abaixo, apresento uma análise detalhada sobre a máquina, seus processos e métodos aplicados:

### **1. Configurações e Sistemas de Coordenadas**
O deslocamento da ferramenta no torno ocorre no **plano XZ**.
*   **Eixo X:** Refere-se ao movimento **transversal**, controlando a medida do raio ou diâmetro da peça.
*   **Eixo Z:** Refere-se ao movimento **longitudinal**, controlando o comprimento da usinagem.
<img width="600" alt="image" src="https://github.com/user-attachments/assets/ec1b58a2-31e1-4cac-925b-aaab4a2e7a0a" />

*   **Sentido dos Movimentos:** Pela regra da mão direita, o sentido positivo ocorre quando a ferramenta se afasta da peça.
<img width="600" alt="image" src="https://github.com/user-attachments/assets/9d7ce9d6-4d9d-40d6-a5fe-11f992194400" />

*   **Torres de Ferramentas:** A máquina pode possuir torre dianteira ou traseira, e alguns modelos utilizam revólveres com até 12 posições para diferentes ferramentas.
<img width="600" alt="image" src="https://github.com/user-attachments/assets/b2c022ef-602e-4d22-a251-6da11d6352cd" />



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
<img width="356" height="296" alt="image" src="https://github.com/user-attachments/assets/3054f98e-4e62-4aa4-b9f1-31d30f02a2b1" />
*   **Impacto na Precisão:** Elementos de fixação inadequados podem causar **acúmulo de erros**, afetando as tolerâncias dimensionais e geométricas.
*   **Pontos de Referência:** Para a execução correta, o programador define o **Ponto Zero da Peça (W)**, facilitando a conversão das medidas do desenho em coordenadas de máquina.

### **4. Controle de Qualidade e Tolerâncias Geométricas**
Como nenhum processo é perfeitamente exato, aplicam-se normas (como a **ISO 1101**) para controlar os desvios aceitáveis.
*   **Erros Microgeométricos (Rugosidade):** O torneamento deixa sulcos superficiais. O planejamento deve prever o número de processos: **desbaste** (1 processo para Ra até 10 µm), **semi-acabamento** (2 processos) e **acabamento** (3 ou mais processos para Ra até 1,6 µm).
*   **Batimento (Runout):** É a tolerância composta mais importante para peças que giram. Ela representa a variação máxima permitida em relação a um eixo de referência quando a peça sofre uma **rotação completa de 360º**.
*   **Forma e Orientação:** O torno deve garantir que a peça mantenha a **circularidade** (ovalização controlada) e a **cilindricidade** (controle ao longo de todo o comprimento).

### **5. Tipos de Torno**
Antes de detalhar o CNC, vale situar as variantes de máquina que compartilham a mesma lógica de fabricação:

- **Torno mecânico convencional:** operado manualmente, é o modelo clássico e é composto essencialmente por barramento, cabeçote fixo, cabeçote móvel, carro principal, carro transversal, carro superior e placa de fixação. É indicado para peças de precisão em pequenas séries, mas depende fortemente da habilidade do operador.
- **Torno CNC:** substitui o controlo manual dos carros por comando numérico computadorizado — ideia originada em 1978, quando o comando manual dos carros foi substituído por microprocessadores, permitindo programar e armazenar sequências de movimentos para trocas rápidas de programa.
- **Torno revólver:** voltado para fabricação em série de peças pequenas (buchas, pinos), com um cabeçote adaptado para fixar várias ferramentas simultaneamente, agilizando a troca entre operações.
- **Torno automático:** realiza toda a sequência — da alimentação da barra bruta até a peça finalizada — sem intervenção humana, sendo aplicado em produção seriada de médios e grandes lotes.

### **6. Dispositivos de Fixação (aprofundamento)**
Complementando o que você já tem na seção 3, os principais dispositivos de fixação incluem:

- **Placa autocentrante de 3 castanhas:** as castanhas movem-se simultaneamente, garantindo centralização automática — ideal para peças cilíndricas ou hexagonais e trocas rápidas de peça.
- **Placa de 4 castanhas independentes:** cada castanha é ajustada individualmente, sendo a opção indicada para peças quadradas, retangulares, excêntricas ou torneamento descentralizado (quando o centro da peça não coincide com o centro da placa).
- **Placa de 6 castanhas:** distribui a força em seis pontos de contacto, reduzindo deformação em peças de paredes finas ou tubos.
- **Pinças (mandril de pinça):** usadas para fixar peças de diâmetro menor e mais uniforme, com elevada precisão de centragem.
- **Contraponto (ponto rotativo):** suporta a extremidade oposta da peça, especialmente importante em peças longas, evitando flexão sob a força de corte.
- **Luneta fixa e luneta móvel:** apoios adicionais ao longo do comprimento da peça, usados quando a relação comprimento/diâmetro é elevada e há risco de vibração ou flexão.

A escolha do dispositivo certo impacta diretamente a precisão dimensional, o tempo de setup e a segurança operacional, especialmente em peças de paredes finas, grandes comprimentos ou formas assimétricas.

### **7. Tolerâncias Geométricas (aprofundamento conforme ISO 1101)**
Complementando o que você já introduziu com o batimento, a norma ISO 1101 (Geometrical Product Specifications — Geometric Tolerancing) padroniza a simbologia e os critérios de forma, orientação, posição e batimento aplicáveis a peças torneadas:

- **Circularidade:** controla o desvio da seção transversal em relação a um círculo perfeito, num único plano perpendicular ao eixo. Valores típicos alcançáveis no torneamento situam-se até cerca de 0,01 mm, contra 0,01–0,015 mm no mandrilamento e 0,005–0,015 mm na retificação.
- **Cilindricidade:** é mais restritiva que a circularidade, pois controla a variação ao longo de toda a superfície cilíndrica — combinando circularidade, retilinidade e conicidade — considerando a peça como um todo tridimensional, não apenas uma seção.
- **Batimento circular (runout):** mede a variação de uma superfície em relação a um eixo de referência (datum) durante uma rotação completa de 360°, sendo a tolerância composta mais relevante para peças rotativas.
- **Batimento total:** mais restritivo que o batimento circular, controla a variação ao longo de toda a superfície (não apenas numa seção) durante a rotação, sendo usado quando a aplicação exige controlo simultâneo de forma e orientação.

Essas tolerâncias são especialmente críticas em componentes rotativos de precisão (eixos, mancais), onde erros de forma se traduzem diretamente em vibração, desgaste prematuro de rolamentos e perda de desempenho em serviço.

### Referências

<pre>
GROOVER M.P.; ZIMMERS, E. W.; CAD/CAM:Computer-Aided Design And Manufacturing, Upper Saddle River, USA: Prentice Hall PTR, 1984. Xix, 489p., il ISBN 9780131101302.

HALEVI, G.; Process and operation planning.Dordrecht, NLD: Kluwer academic/PlenumPublishers, 2003. Xvi, 335., il ISBN 9789048164370.
  
COMO a eletroerosão lida com tolerâncias geométricas extremas. **Galpão das Máquinas**, 6 fev. 2026. Disponível em: https://galpaodasmaquinas.com.br/blog/metal_e_mecanica/eletroerosao/eletroerosao-e-tolerancias-geometricas/. Acesso em: 9 jul. 2026.

COMPONENTES para placas de torno. **World Tools**, [s.d.]. Disponível em: https://www.worldtools.com.br/acessorios-para-maquinas/placa-de-torno/componentes-para-placas-de-torno. Acesso em: 9 jul. 2026.

DIFERENTES tipos de tornos CNC. **Indusmart**, 17 jan. 2025. Disponível em: https://indusmart.com.br/usinagem-tornos-cnc/. Acesso em: 9 jul. 2026.

ESCOLA ESTADUAL DE EDUCAÇÃO PROFISSIONAL (EEEP). **Mecânica: usinagem com máquinas convencionais**. Ensino Médio Integrado à Educação Profissional. Ceará: SEDUC, [s.d.]. Disponível em: https://www.seduc.ce.gov.br/wp-content/uploads/sites/37/2012/06/mecanica_usinagem_com_maquinas_convencionais.pdf. Acesso em: 9 jul. 2026.

GD&T — tolerâncias geométricas. **Metrology RS**, [s.d.]. Disponível em: https://www.metrologyrs.com.br/treinamentos2/tolerancias-geometricas/. Acesso em: 9 jul. 2026.

INSTITUTO FEDERAL DE BRASÍLIA. **Tolerância geométrica**: elementos de máquinas. Técnico em Eletromecânica, [s.d.]. Disponível em: https://s14057791a82db508.jimcontent.com/download/version/1402614008/module/8801738369/name/Tolerancia_Geom%C3%A9trica.pdf. Acesso em: 9 jul. 2026.

INTERPRETAÇÃO de GD&T conforme ISO 1101. **Udemy**, 19 jan. 2024. Disponível em: https://www.udemy.com/course/interpretacao-de-gdt-conforme-iso-1101/. Acesso em: 9 jul. 2026.

NBR ISO 2768: tolerâncias gerais, parte 2. **[documento técnico]**, [s.d.]. Disponível em: https://hudsonbonazza.wordpress.com/wp-content/uploads/2012/09/nbr-iso-2768-tolerancias-gerais-parte-2.pdf. Acesso em: 9 jul. 2026.

O PROCESSO mecânico de usinagem: torneamento. **[apostila]**, [s.d.]. Disponível em: https://www.jorgestreet.com.br/offline/4BN/4BN_MATERIAL_PFB%20IV_MENEZES_Apostila%20Torneamento.pdf. Acesso em: 9 jul. 2026.

PLACA para torno: autocentrante 3, 4 e 6 castanhas. **Fermec**, [s.d.]. Disponível em: https://fermec.com.br/cat/Placas-para-Torno-69.html. Acesso em: 9 jul. 2026.

PLACA para torno mecânico: conheça os tipos e usos comuns. **Wolf Brasil**, 5 nov. 2023. Disponível em: https://wolfbrasil.com.br/placa-torno-mecanico/. Acesso em: 9 jul. 2026.

QUAL a definição de tolerância geométrica (GD&T)? **GBR Engenharia**, 15 abr. 2026. Disponível em: https://gbrengenharia.com/qual-a-definicao-de-tolerancia-geometrica/. Acesso em: 9 jul. 2026.

TOLERÂNCIAS geométricas e GD&T: o guia para peças. **Bruson**, 18 maio 2026. Disponível em: https://bruson.com.br/blog/tolerancias-geometricas-e-gdt/. Acesso em: 9 jul. 2026.

TORNO mecânico: guia completo 2026. **Galpão das Máquinas**, 13 mar. 2026. Disponível em: https://galpaodasmaquinas.com.br/blog/metal_e_mecanica/tornos/torno-mecanico/. Acesso em: 9 jul. 2026.

TORNOS convencionais horizontais. **Automatools**, [s.d.]. Disponível em: https://www.automatools.com.br/folder/Folder-InterCNC-Torno-Convencional.pdf. Acesso em: 9 jul. 2026.

USINAGEM convencional. **[apostila]**. Instituto Federal de Santa Catarina (IFSC), [s.d.]. Disponível em: https://docente.ifsc.edu.br/cleverson.guandalin/fic/Apostila_Usinagem_Convencional_Operacoes.pdf. Acesso em: 9 jul. 2026.

WHAT are the standards for the cylindricity of metal turned parts? **CJ Metal Parts Blog**, 6 nov. 2025. Disponível em: https://www.cjmetalparts.com/blog/what-are-the-standards-for-the-cylindricity-of-metal-turned-parts-1695441.html. Acesso em: 9 jul. 2026.
</pre>

