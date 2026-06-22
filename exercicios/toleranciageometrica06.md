<h2>Tolerância Geométrica - Exercícios</h2>

<img width="234" height="111" alt="image" src="https://github.com/user-attachments/assets/22d33cd9-de68-4c34-8b5b-846bdfb0677c" />

### 1. O Referencial mudou de natureza

* **Datum A:** Repare que o triângulo do referencial **A** está apoiado diretamente sobre uma linha de extensão que representa a **face plana inferior** da peça (a base do flange).
* **Significado:** O nosso referencial ideal agora é um **plano**, e não mais um eixo mecânico.

### 2. O Quadro de Tolerância

* **Símbolo ($\perp$):** Continua sendo Perpendicularidade.
* **Valor (0,1):** A zona de tolerância é de $0,1\text{ mm}$.
* **Referência (A):** Indica que o controle é feito em relação à face plana inferior.

---

### 3. O que estamos analisando aqui?

A seta do quadro de tolerância está apontando para a **superfície cilíndrica externa**. Quando a perpendicularidade é aplicada a um cilindro tendo um plano como referência, nós não estamos medindo a superfície externa de forma direta, mas sim o **eixo do cilindro**.

> **Interpretação Prática da Zona de Tolerância:**
> * O eixo teórico do cilindro superior deve ser perfeitamente perpendicular ($90^\circ$) em relação à face plana inferior (Datum A).
> * A zona de tolerância de $0,1\text{ mm}$ cria uma **gaiola cilíndrica virtual** de diâmetro $0,1\text{ mm}$ que se projeta para cima, exatamente a $90^\circ$ da base.
> * O eixo real do cilindro fabricado precisa estar completamente contido dentro desse tubo imaginário de $0,1\text{ mm}$.
> 
> 

### Como funcionam os Valores Máximos e Mínimos na Bancada?

Como estamos avaliando o quanto o "corpo" do cilindro está inclinado (torta para o lado) em relação à base, a medição física inverte o processo:

1. **Fixação:** A peça é assentada pela sua base plana diretamente sobre uma placa de desempeno ultraprecisa (materializando o Datum A). O cilindro fica apontando para cima.
2. **Varredura:** O relógio comparador é montado em uma coluna vertical de medição. O operador encosta o palpador na lateral do cilindro.
3. **A Busca pelos Extremos:** Você move o relógio verticalmente (de baixo para cima) ao longo de uma geratriz do cilindro para encontrar a maior e a menor medida de inclinação. Depois, gira-se a peça para mapear o cilindro em outras direções ($0^\circ, 90^\circ, 180^\circ, 270^\circ$).

Se a diferença entre o ponto mais "afastado" (máximo) e o ponto mais "próximo" (mínimo) na inclinação do eixo ultrapassar $0,1\text{ mm}$, significa que o cilindro foi usinado "torto" em relação à base e a peça será rejeitada.


<hr>
