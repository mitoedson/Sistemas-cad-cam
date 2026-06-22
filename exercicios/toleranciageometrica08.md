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
> 

A sua intuição estava certa: os erros de fabricação que provocam a falta de perpendicularidade aqui são exatamente os mesmos que geram o batimento axial (como o desalinhamento da ferramenta no torno ou o empenamento da peça). A diferença está apenas em como a norma isola o desvio de orientação (perpendicularidade) sem necessariamente focar na dinâmica de rotação contínua (batimento).
