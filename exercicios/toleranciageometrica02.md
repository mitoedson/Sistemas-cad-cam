<h2>Tolerância Geométrica - Exercícios</h2>

<img width="320" height="163" alt="image" src="https://github.com/user-attachments/assets/e6721ba5-6b9e-4abc-ab02-d11042bc5df0" />

### Paralelismo de uma Face com um Eixo ($//$)

* **O Referencial (Datum B):** O triângulo está acoplado à linha de extensão do diâmetro do eixo. Portanto, o nosso referencial é o **Eixo Geométrico B** (o centro do cilindro).
* **O Quadro de Tolerância ($//\ | \ 0,1\ |\ B$):** Exige que a face plana fresada seja **paralela** ao Eixo B dentro de uma zona de tolerância de $0,1\text{ mm}$.

> **Como funciona essa zona de tolerância virtual?**
> Imaginamos dois planos paralelos entre si, distantes exatamente $0,1\text{ mm}$, e que são perfeitamente paralelos ao Eixo B. A face usinada deve caber inteira dentro desse espaço. Se ela for fresada "rampada" (mais funda em uma extremidade do que na outra), o erro de paralelismo será pego.

Para fazer a aferição, o processo em bancada exige que materializemos o **Eixo B** como a nossa referência física e, a partir dele, meçamos a variação da superfície plana fresada.

Aqui está o passo a passo padrão de como faria essa medição utilizando a metrologia tradicional:

---

### 1. O Desafio e a Solução de Fixação

Como o referencial **Datum B** é o eixo geométrico do cilindro, não podemos simplesmente apoiar a peça diretamente de qualquer maneira na bancada, pois a superfície cilíndrica rolaria ou ficaria desalinhada.

* **O Instrumento:** Utilizamos **blocos em V** retificados (prismas em V).
* **A Montagem:** Apoia-se a parte cilíndrica perfeita da peça sobre dois blocos em V posicionados em cima da placa de desempeno de granito.
* **O Resultado:** Ao fazer isso, o **Eixo B torna-se perfeitamente paralelo à superfície da bancada de granito**, independentemente de o rebaixo estar torto ou não. A bancada passa a ser o espelho do nosso Datum B.

---

### 2. O Processo de Varredura com o Relógio Comparador

Com a peça rigidamente apoiada e com o rebaixo voltado para cima, seguimos o roteiro:

1. **Posicionamento:** Fixe um relógio comparador (ou um relógio apalpador, que é ideal para superfícies planas usinadas) numa coluna de medição (suporte magnético ou traçador de altura).
2. **Ponto Inicial:** Encoste a ponta de contacto do relógio numa das extremidades da face plana fresada e **zere o mostrador** (ou anote o valor inicial).
3. **O Movimento (Varredura Longitudinal):** Desloque a coluna do relógio ao longo da placa de desempeno, fazendo com que o apalpador percorra uma linha reta sobre o rebaixo, indo de uma extremidade à outra do comprimento da peça.

---

### 3. A Procura pelos Valores Máximos e Mínimos ($TIR$)

Durante o percurso da haste ao longo do rebaixo:

* Se o fresamento foi perfeito e paralelo ao eixo do cilindro, o ponteiro do relógio manter-se-á no zero do início ao fim.
* Se a ferramenta de corte entrou mais fundo numa ponta do que na outra (gerando uma rampa), o ponteiro vai girar continuamente numa direção.
* Anote a **maior leitura (valor máximo)** e a **menor leitura (valor mínimo)** registadas durante toda a extensão do rebaixo.

Para garantir que a face não está inclinada também "para os lados" (torção), é boa prática fazer essa varredura em pelo menos duas ou três linhas paralelas ao longo da largura do rebaixo.

---

### 4. O Veredicto da Tolerância

A diferença total calculada:

$$\text{Variação Total (TIR)} = \text{Valor Máximo} - \text{Valor Mínimo}$$

* Se essa variação total for **menor ou igual a $0,1\text{ mm}$**, a peça está **aprovada**. O paralelismo está dentro do especificado.
* Se ultrapassar $0,1\text{ mm}$, significa que o rebaixo ficou excessivamente inclinado em relação ao eixo original da barra, e a peça é rejeitada.

Compreendeu como os blocos em V fazem a "ponte" mecânica para transformar o eixo invisível da peça numa linha perfeitamente paralela à mesa de medição?

<hr>



