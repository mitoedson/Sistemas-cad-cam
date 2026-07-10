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
A precisão da usinagem depende diretamente de como a peça é presa à máquina. Os dispositivos de fixação, como placas e castanhas, devem manter a peça firmemente posicionada sob a ação das forças de corte.
Elementos de fixação mal projetados podem causar acúmulo de erros e afetar a precisão dimensional e geométrica da peça.
O sistema de referência no torno utiliza o plano XZ, onde X controla o diâmetro e Z o comprimento.

### 4. Qualidade e Acabamento Superficial (Rugosidade)
A usinagem deixa marcas ou sulcos na superfície (erros microgeométricos), conhecidos como <a href="rugosidade.md">rugosidade</a>. Qualquer processo de usinagem envolve uma ferramenta física com uma geometria de corte (aresta, raio de ponta, ângulos) a remover material em movimento relativo com a peça. Esse contacto mecânico, por mais fino que seja o corte, deixa inevitavelmente:
<ul>
<li>Marcas ou sulcos correspondentes ao trajeto da ferramenta (por exemplo, a "espiral" deixada pelo avanço no torneamento).
<li>Deformações microscópicas do material na superfície, causadas pela pressão e pelo calor do corte.
</ul>
Isso é o que se chama de erro microgeométrico, ou rugosidade — não é um defeito de fabricação no sentido de "algo deu errado", é uma consequência física inerente ao próprio ato de cortar material. Não há processo de usinagem capaz de gerar uma superfície perfeitamente lisa a nível atômico. O que existe são diferentes níveis de rugosidade alcançáveis. O planejamento do processo deve considerar a rugosidade média (Ra) desejada:
<ul>
<li>Desbaste: Apenas 1 processo, para rugosidades de até 10 µm
<li>Semi-acabamento: 2 processos, para rugosidades de até 6,3 µm
<li>Acabamento: 3 ou mais processos (incluindo retificação), para rugosidades finas de até 1,6 µm ou menos
</ul>
<p>
Mesmo os processos de acabamento mais refinados (polimento, lapidação) reduzem a rugosidade a valores extremamente baixos, mas não a eliminam por completo — apenas a tornam imperceptível para a aplicação em questão.
<p>
As fontes indicam que quanto melhor o acabamento exigido, maior será o custo de fabricação. Existe também uma relação direta entre o acabamento e a precisão: a tolerância dimensional em milímetros que se pode obter pode ser estimada dividindo-se o valor da rugosidade (em mícron) por 40. 

### 5. Programação e Execução (CNC)
No torneamento moderno, utiliza-se a programação via funções preparatórias (G) e auxiliares (M) para automatizar o caminho da ferramenta. O uso de ciclos automáticos (como o G71 para desbaste e G76 para roscas) simplifica a fabricação de geometrias complexas, enquanto a compensação do raio da ferramenta (G41/G42) garante a exatidão em superfícies inclinadas e raios.

Aqui está um complemento à sua análise, organizado como continuação da numeração que você já tem:

## 6. Materiais das Ferramentas de Corte

A seleção do material da ferramenta é determinante para a produtividade e o acabamento obtido, pois cada material oferece um equilíbrio diferente entre dureza, tenacidade e resistência térmica.

- **Aço rápido (HSS):** liga historicamente importante, hoje usada sobretudo em operações de menor velocidade ou em ferramentas de geometria complexa.
- **Metal duro (carboneto de tungstênio + cobalto):** é composto por carbonetos e cobalto, responsáveis respetivamente pela dureza e pela tenacidade, com partículas entre 1 e 10 mícrons que ocupam geralmente 60% a 95% do volume da pastilha. A primeira composição de metal duro utilizava 81% de tungstênio, 6% de carbono e 13% de cobalto. É o material mais utilizado atualmente na indústria, muitas vezes revestido para aumentar a vida útil.
- **Cermet:** composto de cerâmica e metal (à base de titânio), apresenta baixa tendência à formação de aresta postiça, boa resistência à corrosão e alta estabilidade química, sendo indicado para acabamentos finos.
- **Cerâmica:** oferece alta dureza e resistência à abrasão, além de manter a resistência à flexão mesmo em temperaturas elevadas, com boa estabilidade química e baixa afinidade com metais. Em contrapartida, é mais frágil e menos tenaz que o metal duro.
- **CBN (Nitreto de Boro Cúbico):** mantém suas propriedades mesmo em temperaturas entre 1200°C e 1300°C e não reage com metais do grupo do ferro, sendo indicado para usinagem de materiais endurecidos e de difícil corte.
- **PCD (Diamante Policristalino):** possui altíssima dureza, mas a temperatura na área de corte não deve ultrapassar 600°C e o material não pode ser usado para usinar metais ferrosos, sendo reservado a ligas não ferrosas e materiais não metálicos.

Um estudo comparativo indica que ferramentas de CBN e cerâmica apresentam boa usinabilidade a 100 m/min com rugosidade inferior a 1 µm, enquanto ferramentas de metal duro (carbide) apresentaram melhores resultados em outras condições de teste, reforçando que a escolha do material depende das condições específicas do processo.

## 7. Formação e Tipos de Cavaco

O cavaco pode representar até metade do peso do material bruto original, e sua forma fornece informações valiosas sobre o estado da usinagem — desgaste da ferramenta, geração de calor e eficácia do fluido de corte.

Classificam-se geralmente quatro tipos básicos de cavaco:

- **Cavaco contínuo:** típico de materiais dúcteis usinados sob condições ideais (alta velocidade de corte, grandes ângulos de saída). O fluxo contínuo do material resulta em força de corte estável e, consequentemente, em boa qualidade superficial.
- **Cavaco cisalhado (ou lamelar):** ocorre em materiais de baixa ductilidade ou em condições de corte severas; apresenta superfície fortemente indentada, já que os segmentos do cavaco se deformam e voltam a soldar-se no plano de cisalhamento.
- **Cavaco em forma de lamela/segmentado:** comum em materiais semidúcteis ou em corte severo, incluindo titânio e ligas endurecidas; pode indicar superaquecimento ou parâmetros de corte inadequados.
- **Cavaco arrancado/quebradiço:** típico de materiais frágeis como ferro fundido, onde a presença de grafita gera descontinuidades na microestrutura; resulta em acabamento inferior devido à ruptura em segmentos.

O uso de fluido de corte altera a forma do cavaco por reduzir o atrito, diminuir o tempo de contato entre cavaco e ferramenta (reduzindo a transferência de calor) e provocar deflexão mecânica do cavaco pela injeção do fluido.

## 8. Fluidos de Corte

Os fluidos de corte (emulsões ou óleos de corte) cumprem duas funções principais: lubrificação (redução do atrito na interface ferramenta-cavaco) e refrigeração (dissipação do calor gerado no processo). A ausência de fluido de corte tende a aumentar o desgaste da ferramenta e o calor gerado no processo, o que é especialmente crítico em operações a seco de materiais de baixa usinabilidade.

## 9. Parâmetros de Corte — Fórmulas e Relações

Complementando os conceitos que você já apresentou, os três parâmetros fundamentais no torneamento relacionam-se da seguinte forma:

- **Velocidade de corte (Vc):** velocidade tangencial da peça em relação à ferramenta, expressa em m/min, calculada a partir do diâmetro da peça e da rotação (rpm).
- **Avanço (f):** distância percorrida pela ferramenta por rotação da peça, em mm/rot. É o fator com maior influência direta sobre a rugosidade média (Ra) e sobre o raio de ponta da ferramenta.
- **Profundidade de corte (ap):** camada de material removida em cada passe, em mm.

Estudos indicam que o avanço influencia diretamente a rugosidade média e o raio de ponta inserido, enquanto a profundidade de corte tem impacto limitado na rugosidade — exceto acima de 1 mm, onde pode causar um leve aumento. Já em relação à velocidade de corte, em valores baixos ela está fortemente ligada à força de corte e à formação de aresta postiça, mas acima de 100 m/min a rugosidade tende a se estabilizar.

Para o cálculo da **potência de corte** (Pc, em kW), utiliza-se a fórmula que relaciona profundidade de corte (ap), avanço (f), velocidade de corte (vc) e o coeficiente de força específica de corte (Kc, em MPa), dividido pelo rendimento da máquina — um exemplo prático apresentado pela Mitsubishi Materials mostra que, para um aço de baixo carbono usinado a 120 m/min, com profundidade de 3 mm e avanço de 0,2 mm/rot (Kc = 3.100 MPa, rendimento de 80%), a potência necessária é de aproximadamente 4,65 kW.

## 10. Desgaste da Ferramenta

O desgaste da ferramenta de corte ocorre por diversos mecanismos que atuam simultaneamente ou de forma predominante dependendo da combinação material-ferramenta e das condições de corte: abrasão mecânica, difusão química entre cavaco e ferramenta, adesão (formação de aresta postiça de corte) e oxidação em altas temperaturas. Um exemplo histórico é o das primeiras ferramentas de metal duro compostas apenas por carboneto de tungstênio e cobalto: ao usinar aço (diferente do ferro fundido, para o qual eram adequadas), formava-se cratera na face da ferramenta devido a fenômenos de difusão e dissolução entre o cavaco e a face de saída — problema que impulsionou o desenvolvimento de revestimentos e composições mais avançadas.

### Referências:

<pre>
GROOVER M.P.; ZIMMERS, E. W.; CAD/CAM: Computer-Aided Design And Manufacturing, Upper Saddle River, USA: Prentice Hall PTR, 1984. Xix, 489p., il ISBN 9780131101302.
    
HALEVI, G.; Process and operation planning. Dordrecht, NLD: Kluwer Academic/PlenumPublishers, 2003. Xvi, 335., il ISBN 9789048164370.
    
AULA Nº 3 — mecanismo de formação do cavaco. **LABUSIG/UFPR**, [s.d.]. Disponível em: https://labusig.ufpr.br/wp-content/uploads/2024/02/aula3_2017s1.pdf. Acesso em: 9 jul. 2026.

CAVACO de usinagem: o que é, tipos e como otimizá-lo. **FBM**, 13 jan. 2026. Disponível em: https://www.fbm.ind.br/blog/cavaco/cavaco-de-usinagem-o-que-e-tipos-e-como-otimiza-lo/. Acesso em: 9 jul. 2026.

CAVACO e formação do cavaco. **FZ Tool Store**, 3 fev. 2025. Disponível em: https://www.fztoolstore.com.br/blog/tecnologia/cavaco. Acesso em: 9 jul. 2026.

DEFINIÇÃO dos parâmetros de corte para usinagem de aço inoxidável duplex. **Contribuciones a las Ciencias Sociales**, São José dos Pinhais, v. 17, n. 5, [s.d.]. Disponível em: https://ojs.revistacontribuciones.com/ojs/index.php/clcs/article/download/6739/4455/20551. Acesso em: 9 jul. 2026.

ENTENDA as variáveis e parâmetros de corte. **CIMM**, 3 ago. 2022. Disponível em: https://www.cimm.com.br/portal/noticia/exibir_noticia/7401-entenda-as-variaveis-e-parametros-de-corte. Acesso em: 9 jul. 2026.

EQUAÇÕES para cálculo do tempo de corte em torneamento. **Revista Máquinas e Metais**, [s.d.]. Disponível em: https://www.arandanet.com.br/revista/mm/artigo_tecnico/60-Equacoes-para-calculo-do-tempo-de-corte-em-torneamento.html. Acesso em: 9 jul. 2026.

FATORES que influenciam os diferentes tipos e formas de cavaco. **CIMM**, 15 mar. 2019. Disponível em: https://www.cimm.com.br/portal/material_didatico/3650-fatores-que-influenciam-os-diferentes-tipos-e-formas-de-cavaco. Acesso em: 9 jul. 2026.

FERRAMENTAS de corte para usinagem: tipos de materiais. **RML Máquinas e Equipamentos**, [s.d.]. Disponível em: https://www.rmlmaquinas.com.br/usinagem-e-maquinas-operatrizes/ferramentas-de-corte-para-usinagem-tipos-de-materiais. Acesso em: 9 jul. 2026.

FUNDAMENTOS do processo de usinagem. **Molde Injeção Plásticos**, 20 fev. 2023. Disponível em: http://moldesinjecaoplasticos.com.br/fundamentos-do-processo-de-usinagem/. Acesso em: 9 jul. 2026.

INFLUÊNCIA da velocidade de corte na integridade superficial em torneamento de aço inoxidável duplex. **CEFET-RJ**, [s.d.]. Disponível em: https://www.cefet-rj.br/attachments/article/2943/Projeto%20Final%202017_1%20Influ%C3%AAncia%20da%20Velocidade%20de%20Corte%20na%20Integridade%20Superficial%20em%20Toneamento%20A%C3%A7o%20Inoxid%C3%A1vel%20Duples.pdf. Acesso em: 9 jul. 2026.

O QUE é cavaco e quais as suas características. **Simco**, 16 set. 2025. Disponível em: http://simcomaq.com.br/o-que-e-cavaco-e-quais-as-suas-caracteristicas/. Acesso em: 9 jul. 2026.

OS MATERIAIS das ferramentas de corte. **CIMM**, 27 fev. 2014. Disponível em: https://www.cimm.com.br/portal/noticia/exibir_noticia/7058-os-materiais-das-ferramentas-de-corte. Acesso em: 9 jul. 2026.

PARÂMETROS de corte no torneamento. **Enginerium**, 19 fev. 2025. Disponível em: https://enginerium.com.br/parametros-de-corte-no-torneamento. Acesso em: 9 jul. 2026.

POTÊNCIA de corte — torneamento: informações técnicas e fórmulas. **Mitsubishi Materials do Brasil**, [s.d.]. Disponível em: https://www.mmc-carbide.com/br/technical_information/formula/tec_turning_cutting_power_formula. Acesso em: 9 jul. 2026.

QUAIS são os principais materiais utilizados como ferramenta de corte? **JNA Ferramentas**, 28 maio 2024. Disponível em: https://jnaferramentas.com.br/materiais-utilizados-como-ferramenta-de-corte/. Acesso em: 9 jul. 2026.

TIPOS de cavaco. **CIMM**, 15 mar. 2019. Disponível em: https://www.cimm.com.br/portal/material_didatico/3648-tipos-de-cavaco. Acesso em: 9 jul. 2026.

USINAGEM CNC de cerâmica: materiais, métodos, desafios e insights práticos. **FastPreci**, 28 abr. 2026. Disponível em: https://www.fastpreci.com/pt/blog/ceramic-cnc-machining/. Acesso em: 9 jul. 2026.

USINAGEM: cavacos. **[blog]**, [s.d.]. Disponível em: https://superusinagem.blogspot.com/2011/03/cavacos.html. Acesso em: 9 jul. 2026.

USINAGEM de metal: os 5 principais materiais para ferramentas de corte. **COMPRACO Soluções e Tecnologias**, 5 set. 2024. Disponível em: https://compraco.com.br/blogs/industria/usinagem-de-metal-os-5-principais-materiais-para-ferramentas-de-corte. Acesso em: 9 jul. 2026.

VELHOS efeitos das condições de corte para torneamento. **Mitsubishi Carbide**, [s.d.]. Disponível em: https://www.mitsubishicarbide.net/contents/mht/pt/html/product/technical_information/information/turning_effects.html. Acesso em: 9 jul. 2026.

ABBRUZZINI, Lucas Rodrigues. **Estudos de mecanismos de desgaste em ferramentas de corte**. Repositório UFU, [s.d.]. Disponível em: https://repositorio.ufu.br/bitstream/123456789/27829/1/EstudosDeMecanismos.pdf. Acesso em: 9 jul. 2026.
</pre>
