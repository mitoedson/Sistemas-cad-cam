<h2>Tolerância Geométrica - Exercícios</h2>

<img width="274" height="178" alt="image" src="https://github.com/user-attachments/assets/528a1273-1718-46e7-82d5-22d4b640611e" />


### 1. O Símbolo ($\angle$)

O símbolo geométrico formado por duas linhas inclinadas representa a tolerância de **Inclinação**.

### 2. O Quadro de Tolerância e a Cota Básica

Lendo o conjunto de informações do desenho:

* **Símbolo ($\angle$):** Inclinação.
* **Valor (0,08):** A zona de tolerância é um espaço delimitado por dois planos paralelos afastados em $0,08\text{ mm}$.
* **Referência (E):** O referencial **Datum E** é a face plana inferior da peça (a base de apoio).
* **Ângulo emoldurado ($40^\circ$):** O quadrado ao redor do valor indica que esta é uma **Cota Teoricamente Exata** (ou cota básica). Ela define o ângulo nominal perfeito e imutável que serve de base para o cálculo geométrico.

---

### 3. Como funciona a zona de tolerância e a leitura de máximos e mínimos?

Aqui, os planos virtuais que você deduziu nos exemplos anteriores ganham uma inclinação fixa e rígida no espaço.

> **Interpretação Prática da "Gaiola Virtual":**
> * O software ou o dispositivo de medição projeta um plano ideal inclinado a **exatamente $40^\circ$** em relação à base (Datum E).
> * A zona de tolerância de $0,08\text{ mm}$ cria um "sanduíche" virtual formado por dois planos paralelos entre si, inclinados rigidamente a $40^\circ$, distantes $0,08\text{ mm}$ um do outro.
> * A face inclinada real da peça (com suas cristas e vales de usinagem) deve conseguir caber inteiramente dentro dessa folga de $0,08\text{ mm}$.
> 
> 

### Como o Relógio Comparador mapeia essa superfície?

Para encontrar as maiores e menores medidas nesta configuração, o ensaio de bancada exige um acessório de apoio angular (como uma mesa de senos ou um bloco padrão angular):

1. **Montagem:** A peça é fixada sobre uma mesa de senos ajustada a exatamente $40^\circ$. Ao fazer isso, a face inclinada da peça teoricamente passa a ficar **paralela** à superfície da bancada de granito se o ângulo estivesse perfeito.
2. **Varredura:** Um relógio comparador fixo em uma coluna desliza ao longo da face inclinada da peça.
3. **Análise:** Você move o relógio de ponta a ponta da rampa procurando a **maior medida (pico)** e a **menor medida (vale)**.

Se a variação total ($TIR$) entre o ponto mais alto e o mais baixo for menor ou igual a $0,08\text{ mm}$, a peça está aprovada. Isso garante que a inclinação real não está "deitada" ou "em pé" demais em relação aos $40^\circ$ exigidos pelo projeto.

<hr>
