<h2>Elementos finitos</h2>

Elementos finitos são a ideia central por trás do método de análise mais usado em CAE (FEA — Finite Element Analysis). A ideia é simples de entender, mesmo sendo poderosa matematicamente.

## A ideia básica

Imagina que quer calcular como uma peça complexa — por exemplo, o chassis de um carro — se deforma sob uma força. Resolver as equações físicas (elasticidade, calor, fluidos, etc.) para a forma inteira e complexa de uma só vez é praticamente impossível analiticamente.

A solução: **dividir a peça em muitos pedaços pequenos e simples** — triângulos, quadrados, tetraedros, cubos — chamados **elementos finitos**. Cada elemento é pequeno e regular o suficiente para que as equações físicas sejam fáceis de resolver dentro dele.

## Os dois ingredientes principais

**Elementos** — as pequenas peças em que a peça é dividida (triângulos ou quadriláteros em 2D, tetraedros ou hexaedros em 3D). Cada elemento tem uma forma simples, o que torna as equações de física resolvíveis com precisão matemática dentro dele.

**Nós** — os pontos (normalmente nos vértices, por vezes também nas arestas) onde os elementos se ligam uns aos outros. É nestes pontos que o programa calcula os valores reais — deslocamento, tensão, temperatura, etc. — e a partir daí interpola o que acontece dentro de cada elemento.

## Porque é que isto funciona

Em vez de tentar resolver uma equação diferencial complicada para toda a peça de uma vez, o software:

1. Escreve equações simples para cada elemento individual (baseadas em como esse elemento se comporta sob carga).
2. Junta todas essas equações num sistema enorme (podem ser milhões de equações), tendo em conta como os elementos partilham nós entre si.
3. Resolve esse sistema todo em simultâneo com métodos numéricos.

O resultado é uma aproximação do comportamento real da peça — e quanto mais fina for a malha (mais elementos pequenos), mais precisa é a aproximação, mas também mais caro computacionalmente fica.

## Uma analogia útil

É um pouco como aproximar uma curva com muitos segmentos de reta pequenos: cada segmento individual é uma reta simples, mas juntos conseguem seguir uma curva complicada com bastante fidelidade — desde que os segmentos sejam suficientemente pequenos.


## Exemplo

O **redesenho de um suporte metálico (bracket)** que segura um componente num braço de suspensão automóvel, onde o objetivo é reduzir peso sem comprometer a resistência.

## O cenário

A equipe de engenharia quer tornar o suporte mais leve (para poupar combustível/autonomia), mas ele precisa de aguentar as forças da estrada sem fraturar nem deformar-se permanentemente.

<img width="600" alt="image" src="https://github.com/user-attachments/assets/f5d61892-069e-4794-85e8-5a382abb348d" />

## Passo a passo do exemplo

**1. Modelo CAD** — o engenheiro desenha a geometria 3D do suporte em SolidWorks, Catia ou similar — a versão original, mais pesada.

**2. Pré-processamento** — o modelo é importado para o software CAE (por exemplo, Ansys ou Abaqus), onde se define:
- O **material** (ex.: aço, com o seu módulo de elasticidade e limite de cedência).
- A **malha** de elementos finitos — mais fina nas zonas críticas (furos, cantos), mais grosseira noutras.

**3. Condições de fronteira** — aqui entra o conhecimento do problema real:
- Onde o suporte está fixo ao chassis (restrições de deslocamento).
- Que forças atuam sobre ele — por exemplo, uma carga de 5.000 N simulando um impacto de lombada a alta velocidade, ou cargas cíclicas para fadiga.

**4. Resolução** — o solver resolve o sistema de equações e calcula, em cada nó, tensões, deformações e deslocamentos.

**5. Pós-processamento** — o engenheiro vê um mapa de cores sobre a peça: vermelho onde a tensão está mais próxima (ou acima) do limite do material, azul onde há folga estrutural. Calcula-se o **fator de segurança** (razão entre a tensão que o material aguenta e a tensão real prevista).

**6. Decisão e iteração** — se há zonas com folga excessiva (muito material a mais, tensão baixa), o engenheiro remove material aí — muitas vezes usando **otimização de topologia**, uma técnica que sugere automaticamente onde retirar material sem comprometer a resistência. O modelo volta ao passo 1 com a geometria revista, e o ciclo repete-se.

## O resultado prático

Depois de várias iterações, obtém-se um suporte talvez 20-30% mais leve, mas que ainda cumpre o fator de segurança exigido — tudo isto **sem fabricar um único protótipo físico**. Só depois de o modelo virtual estar validado é que se avança para testes físicos de confirmação, normalmente muito mais baratos porque já se espera que a peça passe.

Este mesmo fluxo aplica-se a problemas muito diferentes — análise térmica de uma placa eletrónica, aerodinâmica de uma carroçaria (CFD), ou vibração de uma estrutura de edifício — muda a física envolvida, mas o processo de pré-processar → resolver → pós-processar → iterar mantém-se.




