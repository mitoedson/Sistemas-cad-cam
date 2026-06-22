<h2>Tolerância Geométrica - Exercícios</h2>

<img width="274" height="156" alt="image" src="https://github.com/user-attachments/assets/2956ffb6-08dd-46c8-bb36-63acfde0c99c" />

Este símbolo — um círculo posicionado entre duas linhas inclinadas paralelas ($/\bigcirc/$) — representa a tolerância de **Cilindricidade**.

Assim como aconteceu no caso da planicidade, você já deve ter reparado no detalhe crucial do quadro: **não há nenhuma letra de referencial (Datum) à direita.** Isso ocorre porque a cilindricidade também é uma tolerância de **forma**. Ela avalia o cilindro por si só, independentemente de como o resto da peça foi fabricado.

---

### 1. O que é a Cilindricidade na prática?

Se a planicidade cria um "sanduíche" de dois planos virtuais para superfícies planas, a cilindricidade cria uma **gaiola tridimensional de dois cilindros virtuais coaxiais (que compartilham o mesmo eixo central)**.

* O cilindro virtual de fora representa a **maior medida** admissível para a forma.
* O cilindro virtual de dentro representa a **menor medida** admissível para a forma.
* A diferença de raio entre esses dois cilindros perfeitos deve ser de exatamente **$0,04\text{ mm}$**.

Toda a superfície real do diâmetro usinado deve ficar contida dentro desse espaço de $0,04\text{ mm}$.

---

### 2. Por que ela é o terror da usinagem? (O "Super Filtro")

A cilindricidade é uma das tolerâncias mais exigentes e completas da mecânica porque ela controla três desvios de forma ao mesmo tempo:

1. **Circularidade:** Garante que cada seção cortada do cilindro seja um círculo perfeito (evita que a peça saia ovalizada).
2. **Retilineidade:** Garante que o corpo do cilindro seja reto (evita que a peça saia "abaulada" ou "bananada").
3. **Paralelismo das geratrizes:** Garante que as paredes do cilindro sejam paralelas entre si (evita que a peça saia cônica/conicidade, ou seja, mais gorda em uma ponta e fina na outra).

### 3. Como funciona a busca por Máximos e Mínimos aqui?

Para medir a cilindricidade em uma bancada tradicional com relógio comparador, o processo exige paciência:

* Você apoia a peça em um dispositivo rotativo de alta precisão.
* O relógio comparador faz a varredura circular completa ($360^\circ$) em uma seção (pega o máximo e mínimo dali).
* Em seguida, você desloca o relógio longitudinalmente para a próxima seção e repete o giro.

O algoritmo (ou o operador) busca o **maior pico absoluto** e o **vale mais profundo absoluto** registrados em *toda* a extensão do cilindro. A variação total acumulada não pode passar de $0,04\text{ mm}$.

Nas indústrias modernas, para medir isso com precisão milimétrica, usa-se um equipamento chamado **Cilindrímetro** (medidor de forma circular), onde uma mesa rotativa ultraprecisa gira a peça enquanto um sensor computadorizado mapeia a superfície criando o modelo virtual em segundos.


<hr>
