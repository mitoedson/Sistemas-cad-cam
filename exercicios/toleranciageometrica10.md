<h2>Tolerância Geométrica - Exercícios</h2>

<img width="354" height="163" alt="image" src="https://github.com/user-attachments/assets/a9b41dce-063b-4707-a54d-257cbad9b4ca" />


### 1. O Referencial (Datum)

* **Elemento:** O quadrado com a letra **A** conectado à superfície cilíndrica menor.
* **Significado:** Ele estabelece o **Eixo de Referência A** (eixo de rotação ideal do cilindro menor). Toda a medição será feita tendo como base que a peça gira perfeitamente em torno desse eixo.

### 2. O Quadro de Tolerância

O retângulo da direita traz três informações cruciais, lidas da esquerda para a direita:

* **Símbolo ($\nearrow$):** Representa o **Batimento Circular** (*Circular Runout*).
* **Valor (0,1):** É o campo ou zona de tolerância expresso em milímetros (0,1 mm).
* **Referência (A):** Indica que o controle é feito em relação ao Datum A.

---

### 3. Interpretação Prática (O que isso significa?)

Como a seta indicativa do quadro de tolerância está apontando diretamente para uma **face plana perpendicular ao eixo** (a face do ressalto maior), estamos falando especificamente de um **Batimento Axial Circular**.

> **Na prática, durante o controle de qualidade:**
> 1. A peça é fixada e rotacionada $360^\circ$ em torno do **Eixo A**.
> 2. O pontal de um relógio comparador é posicionado perpendicularmente contra a face plana indicada, em uma determinada distância do centro (um raio específico).
> 3. Ao dar uma volta completa na peça, a variação máxima registrada no relógio comparador (a diferença entre o ponto mais alto e o mais baixo) **não pode ultrapassar 0,1 mm**.
> 4. Esse teste deve ser repetido em diferentes raios da mesma face, e em nenhum deles a variação pode ser maior que 0,1 mm.
> 
> 

O desenho à direita da face (com as duas linhas verticais afastadas por `0,1`) ilustra justamente a **zona de tolerância**: a face real da peça deve estar contida entre dois planos paralelos distantes 0,1 mm entre si, limitando tanto o erro de circularidade (durante o giro) quanto o erro de perpendicularidade dessa face em relação ao eixo de referência.

Ao ler a superfície plana do cilindro maior com essa configuração, estamos analisando simultaneamente dois desvios geométricos em relação ao eixo de referência: a **perpendicularidade** e o **empenamento (planeza)** dessa face.

Na metrologia, o termo técnico para o que o relógio está medindo em cada círculo é o **Batimento Axial Circular**.

---

### O que essa leitura avalia na prática?

Quando o relógio comparador monitora essa face plana enquanto a peça gira, ele está verificando se a superfície atende a dois requisitos cruciais:

O relógio fica parado em um raio enquanto a peça gira $360^\circ$. O $TIR$ avalia o "empenamento" dinâmico daquela pista circular. ($$TIR = \text{Valor Máximo} - \text{Valor Mínimo}$$)

* **Falta de Perpendicularidade (Inclinação):** Avalia se a face plana está perfeitamente a $90^\circ$ em relação ao eixo do cilindro menor. Se a face estiver "torta" ou inclinada, a ponta do relógio será empurrada para fora e para dentro a cada volta.
* **Erros de Forma (Ondulação/Empenamento):** Avalia se a superfície da face possui irregularidades locais, como deformações, concavidades ou convexidades ao longo do caminho circular percorrido pelo medidor.

---

### Por que esse controle é vital na mecânica?

Imagine que esse componente seja um eixo de transmissão e que outra peça (como uma engrenagem ou um rolamento) seja montada encostada justamente nessa face plana.

* Se essa face tiver um batimento maior que $0,1\text{ mm}$, a peça montada contra ela ficará desalinhada.
* Quando o conjunto girar em alta rotação, esse desalinhamento causará **vibração excessiva**, **desgaste prematuro dos rolamentos** e, eventualmente, a **fadiga mecânica** do sistema.

Portanto, ao ler essa superfície plana, você está garantindo a **estabilidade dinâmica** do componente quando ele estiver girando em sua aplicação real.


<hr>
