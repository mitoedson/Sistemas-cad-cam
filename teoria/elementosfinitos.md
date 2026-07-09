<h2>Elementos finitos</h2>

Elementos finitos são a ideia central por trás do método de análise mais usado em CAE (FEA — Finite Element Analysis). A ideia é simples de entender, mesmo sendo poderosa matematicamente.

## A ideia básica

Imagina que queres calcular como uma peça complexa — por exemplo, o chassis de um carro — se deforma sob uma força. Resolver as equações físicas (elasticidade, calor, fluidos, etc.) para a forma inteira e complexa de uma só vez é praticamente impossível analiticamente.

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

Queres que veja também como se escolhe o tamanho e tipo de malha, ou como isto se aplica a um caso concreto (por exemplo, análise estrutural de uma peça mecânica)?
