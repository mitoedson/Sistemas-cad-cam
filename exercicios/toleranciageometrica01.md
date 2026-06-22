<h2>Tolerância Geométrica - Exercícios</h2>

<img width="218" height="209" alt="image" src="https://github.com/user-attachments/assets/389e0c13-640d-43b7-b7df-2d32ab40455b" />

#### 1. O Quadro de Tolerância ($//\ | \ \varnothing 0,03\ |\ A$)

* **Símbolo ($//$):** Paralelismo.
* **Zona de Tolerância ($\varnothing 0,03$):** Atenção ao detalhe! Há o símbolo de diâmetro ($\varnothing$). Isso significa que a zona de tolerância não é um "sanduíche" de duas placas paralelas, mas sim um **tubo cilíndrico virtual de diâmetro $0,03\text{ mm}$**.
* **Referencial (Datum A):** O triângulo invertido está acoplado à linha de cota do **furo inferior**. Portanto, o Datum A é o **eixo geométrico ideal do furo maior**.

#### 2. O que estamos controlando?

A seta do quadro aponta para o **furo superior** (menor). Estamos controlando o paralelismo entre os eixos dos dois furos. O eixo real do furo menor precisa caber inteiramente dentro daquele tubo virtual de $\varnothing 0,03\text{ mm}$ que corre perfeitamente paralelo ao Eixo A.

---

### O Grande Teste Prático: Quantos pinos precisamos aqui?

Para medir essa peça usando a metrologia tradicional, você precisará de **dois pinos de referência (mandris)** ao mesmo tempo. Veja a física do setup:

1. **Materializando o Datum A (Furo Inferior):** Insere-se um pino retificado justo dentro do furo maior. Esse pino é apoiado sobre dois blocos em V em cima da bancada de granito. **Resultado:** O Eixo A agora está materializado e perfeitamente paralelo à bancada.
2. **Materializando o Eixo a ser Medido (Furo Superior):** Como o relógio comparador não entra no furo menor, insere-se um **segundo pino retificado** dentro dele. Este pino joga o eixo real do furo superior para fora da peça.
3. **A Varredura:** O relógio comparador desliza na bancada e percorre o topo do segundo pino (da esquerda para a direita) buscando a maior e a menor medida ($TIR$).


--

### O detalhe crucial do desenho (A pegadinha do Datum)

Olhe bem para onde a ponta do triângulo do **Datum A** está apontando na imagem. Ela não está tocando a linha externa do corpo da biela; ela está alinhada exatamente com a **linha de cota do diâmetro interno do furo**.

Isso significa que o projetista definiu que o referencial é o **eixo do furo (vazio)**, e não o eixo da superfície externa (metal).

### O que acontece se usarmos o bloco em V direto na peça?

Se você apoiar a parte externa da biela direto no bloco em V, você estará usando a **superfície externa** como referência. Se o processo de fabricação não tiver uma concentricidade perfeita entre o diâmetro externo e o furo interno (o que é muito comum), o furo vai ficar desalinhado.

* **Com o bloco em V direto na peça:** Você mede o paralelismo do furo superior em relação ao *contorno externo* da biela.
* **Com o pino dentro do furo inferior:** O pino se ajusta perfeitamente ao furo interno. Quando você apóia os extremos desse pino nos blocos em V, você garante que é o **eixo real do furo** que está perfeitamente paralelo à bancada de granito.


<hr>
