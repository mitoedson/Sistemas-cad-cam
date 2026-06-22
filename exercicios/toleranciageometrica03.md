<h2>Tolerância Geométrica - Exercícios</h2>

<img width="320" height="160" alt="image" src="https://github.com/user-attachments/assets/6d015063-222e-45ec-ae15-30dc650b85f5" />

### 1. O Símbolo ($//$)

As duas linhas inclinadas paralelas representam a tolerância de orientação de **Paralelismo**.

### 2. O Quadro de Tolerância

* **Símbolo ($//$):** Paralelismo.
* **Valor (0,2):** A zona de tolerância é um espaço delimitado por dois planos paralelos afastados em $0,2\text{ mm}$ (ou um cilindro, caso houvesse o símbolo $\varnothing$). Como a seta aponta para as linhas de centro/extensão do furo, estamos controlando o **eixo do furo**.
* **Referência (C):** O referencial **Datum C** está associado à face plana inferior do bloco (indicado pelo triângulo sobre a linha de base).

---

### 3. O que estamos analisando aqui?

Diferente do batimento axial (que mede o empenamento de uma face externa enquanto a peça gira), o paralelismo aqui está preocupado em garantir que o **furo interno não saia "subindo" ou "descendo"** em relação à base de apoio do bloco.

> **Interpretação da Zona de Tolerância:**
> * O Datum C materializa um plano perfeito na base.
> * A tolerância de $0,2\text{ mm}$ cria uma "gaiola" virtual de dois planos paralelos entre si e **rigorosamente paralelos ao Datum C**, distantes $0,2\text{ mm}$ um do outro.
> * O eixo real do furo passante (gerado a partir dos pontos internos coletados) deve estar totalmente contido dentro dessa folga de $0,2\text{ mm}$.
> 
> 

---

### Como funcionam os Valores Máximos e Mínimos na Bancada?

Como estamos medindo um furo interno, o controle de qualidade costuma usar um acessório chamado **pino padrão** (*mandrel*) que se ajusta perfeitamente ao diâmetro interno para "jogar para fora" o eixo real do furo.

Se tentássemos colocar o relógio comparador diretamente dentro daquele furo sem o pino, esbarraríamos em limitações físicas intransponíveis:

### 4.1. O obstáculo físico do próprio instrumento

A haste e o corpo do relógio comparador convencional são grandes. Se o furo for longo e estreito, o corpo do relógio bateria na entrada do furo antes mesmo de o palpador chegar ao meio da peça.

### 4.2. O erro do ângulo de medição (Efeito Cosseno)

Para medir o paralelismo de uma linha, a ponta do relógio precisa deslizar perfeitamente perpendicular à superfície. Dentro de um furo côncavo, a inclinação da ponta mudaria conforme avançamos, distorcendo completamente a leitura e gerando erros matemáticos na caça pelos máximos e mínimos.

1. **Fixação:** O bloco é assentado pela sua base (Datum C) diretamente sobre a placa de desempeno.
2. **Materialização do Eixo:** Insere-se o pino retificado dentro do furo. O corpo do pino que fica para fora agora representa fielmente a inclinação do eixo do furo.
3. **Varredura:** Um relógio comparador montado em uma coluna desliza ao longo do topo do pino projetado, deslocando-se da entrada até a saída do furo.
4. **Análise de Extremos:** Você procura a **maior medida (ponto mais alto)** e a **menor medida (ponto mais baixo)** ao longo do comprimento do furo.

Se a diferença total ($TIR$) entre a leitura na entrada e na saída do furo for maior que $0,2\text{ mm}$, significa que o furo foi brotado/usinado inclinado em relação à base, o que impediria, por exemplo, que um eixo passasse reto por ali em uma montagem mecânica.

### Como a indústria resolve isso no mundo moderno, sem o pino?

Quando não se quer usar o pino físico, a única alternativa viável é abandonar a metrologia convencional de bancada e migrar para a alta tecnologia:

* **Palpadores Estiletes Longos (MMC):** Máquinas de Medir por Coordenadas utilizam agulhas de rubi extra longas montadas em cabeçotes articulados que entram no furo sem tocar nas bordas, coletando os pontos eletronicamente.
* **Sensores Ópticos / Laser de Furo:** Sensores rotativos a laser que entram no furo e mapeiam o diâmetro interno por reflexão de luz, calculando o eixo virtual por software.

> **O veredicto:** Para a metrologia tradicional com relógio comparador, a sua análise está **100% correta**. Sem o pino para "projetar" o eixo do furo para o lado de fora, a medição manual seria fisicamente impossível de realizar de um extremo a outro.

Essa percepção do espaço e das limitações das ferramentas mostra que você já está visualizando o processo com os olhos de quem planeja e executa a engenharia na prática!



