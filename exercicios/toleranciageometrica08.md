<h2>Tolerância Geométrica - Exercícios</h2>

<img width="274" height="151" alt="image" src="https://github.com/user-attachments/assets/745a5338-c3db-4ff0-b530-09950cc90811" />

### 1. O Símbolo ($\perp$)

O símbolo com uma linha horizontal e outra perfeitamente vertical representa a tolerância de **Perpendicularidade**.

### 2. O Quadro de Tolerância

Lendo a especificação:

* **Símbolo ($\perp$):** Perpendicularidade.
* **Campo de Tolerância (0,08):** A zona de tolerância é um espaço delimitado por dois planos paralelos afastados em $0,08\text{ mm}$. (Note que não há o símbolo $\varnothing$ aqui, pois estamos a controlar uma superfície plana, não um cilindro).
* **Referência (D):** O referencial mudou de nome, agora chama-se **Datum D**, que é o eixo geométrico do cilindro menor.

---

### 3. A Sacada Intermediária: Perpendicularidade vs. Batimento Axial

Esta imagem é muito parecida com a do batimento axial circular $\nearrow$, mas com uma diferença crucial na **forma como o controle de qualidade valida a peça**.

> **O que estamos a analisar aqui?**
> * **Teoricamente:** A face plana do cilindro maior deve estar a exatamente $90^\circ$ em relação ao Eixo D. Toda a superfície real daquela face deve caber dentro de uma "gaiola" invisível formada por dois planos paralelos distantes $0,08\text{ mm}$ entre si, e que são perfeitamente perpendiculares ao Eixo D.
> * **A diferença prática na medição:** No primeiro caso (batimento $\nearrow$), o relógio comparador ficava parado e líamos apenas círculos isolados enquanto a peça girava. Aqui, no controle de **perpendicularidade pura**, a peça normalmente fica estática e o relógio comparador (ou uma máquina de medir por coordenadas - MMC/CMM) varre a superfície plana movimentando-se radialmente para mapear a inclinação da face como um todo.
> 

Como as superfícies físicas nunca são perfeitamente planas (elas possuem micro-picos e vales devido às marcas da ferramenta de corte), esses planos da zona de tolerância são estabelecidos de forma matemática (ou virtual) a partir dos pontos extremos coletados na peça.

Existem duas formas principais de materializar ou "criar virtualmente" esses planos na prática:

---

### 4.1. Medição Por Medição Computacional (MMC / Braço Articulado)

Quando você usa uma Máquina de Medir por Coordenadas (MMC) ou um software associado a um scanner/palpador, o processo é puramente matemático:

* O sensor coleta uma nuvem de pontos sobre a face real do cilindro maior.
* O software calcula um **Plano Médio Matemático** (geralmente por mínimos quadrados) e o projeta a exatamente $90^\circ$ em relação ao Eixo D.
* A partir desse plano ideal, o sistema identifica o **ponto mais alto (maior medida)** e o **ponto mais baixo (menor medida)** na direção do eixo.
* A distância entre o plano virtual que passa pelo pico mais alto e o plano virtual que passa pelo vale mais profundo deve ser, no máximo, **$0,08\text{ mm}$**.

### 4.2. Por Metrologia Tradicional (Placa de Desempeno e Relógio)

Se você estivesse medindo isso em uma bancada sem computador, o processo "físico" simularia esses planos virtuais:

* O eixo (Datum D) é alinhado perfeitamente paralelo a uma placa de desempeno de granito (que serve como nossa referência plana ultraprecisa).
* Um relógio comparador montado em uma coluna corre ao longo da face plana da peça.
* Você zera o relógio no ponto mais recuado (**menor medida**) e varre a superfície até achar o ponto mais saliente (**maior medida**).
* A diferença geométrica entre o "zero" (plano inferior virtual) e o pico máximo (plano superior virtual) é a distância que não pode passar de $0,08\text{ mm}$.


<hr>
