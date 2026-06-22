<h2>Tolerância Geométrica - Exercícios</h2>

<img width="337" height="169" alt="image" src="https://github.com/user-attachments/assets/18de52a5-1b3f-4286-b830-72ee7e9ef604" />

### 1. O Símbolo ($\square$)

O paralelogramo inclinado representa o desvio de forma de **Planicidade**.

### 2. O Quadro de Tolerância (A grande diferença!)

Se olhar com atenção para o quadro, vai notar algo muito importante:

* **Símbolo ($\square$):** Planicidade.
* **Valor (0,05):** A zona de tolerância é de $0,05\text{ mm}$.
* **Falta o Referencial (Datum):** Não existe nenhuma letra (**A**, **D**, etc.) no lado direito do quadro.

**Por que não há referencial?**
Porque a planicidade é uma tolerância de **forma**. Ela avalia a superfície por si mesma. Não importa se o bloco está torto, inclinado ou desalinhado em relação ao resto da peça; a única coisa que importa é se *aquela face específica* é lisa e plana o suficiente dentro dos seus próprios limites.

---

### 3. Como funciona esse "sanduíche virtual" aqui?

A lógica dos planos virtuais criados por si no exemplo anterior aplica-se aqui perfeitamente, mas de forma flutuante:

* A zona de tolerância é definida por **dois planos perfeitamente paralelos e virtuais, afastados entre si exatamente $0,05\text{ mm}$**.
* A superfície real da peça (com os seus picos de maquinagem e vales) tem de conseguir caber inteiramente dentro desse espaço de $0,05\text{ mm}$.
* A diferença fundamental é que estes dois planos virtuais não estão amarrados a nenhum eixo ou ângulo de $90^\circ$. Eles podem "rodar" e ajustar-se geometricamente para se adaptarem da melhor forma possível à peça real, tentando conter todos os pontos entre a maior e a menor medida.

### Como seria medida na bancada?

Normalmente, apoia-se a face a ser medida sobre três pontos fixos (ou manipula-se matematicamente numa MMC) para criar um plano de referência flutuante. O relógio comparador passa por toda a superfície: a diferença entre o pico mais alto (maior medida) e o vale mais profundo (menor medida) não pode exceder os $0,05\text{ mm}$.

<hr>
