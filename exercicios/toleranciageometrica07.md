<h2>Tolerância Geométrica - Exercícios</h2>

<img width="337" height="169" alt="image" src="https://github.com/user-attachments/assets/18de52a5-1b3f-4286-b830-72ee7e9ef604" />

### 1. O Símbolo ($\square$)

O paralelogramo inclinado representa o desvio de forma de **Planicidade**.

### 2. O Quadro de Tolerância 

Se olhar com atenção para o quadro, vai notar algo muito importante:

* **Símbolo ($\square$):** Planicidade.
* **Valor (0,05):** A zona de tolerância é de $0,05\text{ mm}$.
* **Falta o Referencial (Datum):** Não existe nenhuma letra (**A**, **D**, etc.) no lado direito do quadro.

**Por que não há referencial?**
Porque a planicidade é uma tolerância de **forma**. Ela avalia a superfície por si mesma. Não importa se o bloco está torto, inclinado ou desalinhado em relação ao resto da peça; a única coisa que importa é se *aquela face específica* é lisa e plana o suficiente dentro dos seus próprios limites.

---

### 3. Como funciona esse "sanduíche virtual"?

A lógica dos planos virtuais criados por si no exemplo anterior aplica-se aqui perfeitamente, mas de forma flutuante:

* A zona de tolerância é definida por **dois planos perfeitamente paralelos e virtuais, afastados entre si exatamente $0,05\text{ mm}$**.
* A superfície real da peça (com os seus picos de maquinagem e vales) tem de conseguir caber inteiramente dentro desse espaço de $0,05\text{ mm}$.
* A diferença fundamental é que estes dois planos virtuais não estão amarrados a nenhum eixo ou ângulo de $90^\circ$. Eles podem "rodar" e ajustar-se geometricamente para se adaptarem da melhor forma possível à peça real, tentando conter todos os pontos entre a maior e a menor medida.

### Como seria medida na bancada?

Normalmente, apoia-se a face a ser medida sobre três pontos fixos (ou manipula-se matematicamente numa MMC) para criar um plano de referência flutuante. O relógio comparador passa por toda a superfície: a diferença entre o pico mais alto (maior medida) e o vale mais profundo (menor medida) não pode exceder os $0,05\text{ mm}$.

A varredura (ou leitura) dessa superfície obedece a padrões bem definidos na metrologia para garantir que nenhum "pico" ou "vale" fique de fora. Como não há um eixo de rotação para guiar o movimento (como nos casos anteriores), o padrão de leitura serve para cobrir a maior área útil possível.

O método varia dependendo do instrumento que você está utilizando:

---

### 4.1. Com Relógio Comparador (Método Manual na Bancada)

Se você estiver em uma mesa de desempeno usando um relógio comparador fixo em uma coluna, move-se a peça (ou a base do relógio) seguindo dois padrões clássicos:

* **Padrão em Grelha (ou Linhas Cruzadas):** Realizam-se leituras em linhas paralelas verticais e, depois, em linhas paralelas horizontais. Isso mapeia ondulações da ferramenta.
* **Padrão em Estrela (ou "X" com Diagonais):** Passa-se o relógio pelas duas diagonais principais da face, além de linhas cruzadas pelo centro. É excelente para pegar empenamentos em que as bordas da peça estão "levantadas" ou "caídas" (peças côncavas ou convexas).

O relógio varre a face e busca a maior e menor medida de forma totalmente livre, sem nenhuma amarra ou obrigação com o resto da peça.

---

### 4.2. Com Máquina de Medir por Coordenadas (MMC / CMM)

Se a medição for automatizada por contato ou laser, o padrão é programado no software e obedece a estratégias geométricas rígidas:

* **Padrão de Mecanismo de Linhas (Zig-Zag):** O palpador percorre a peça de um lado para o outro de forma contínua, mantendo um passo constante (ex: a cada 2 mm ou 5 mm), cobrindo toda a extensão.
* **Padrão de Pontos Mínimos por Norma (ISO 12181 / ISO 1101):** Em vez de varredura contínua, a norma ou o software exige um número mínimo de pontos amostrados uniformemente (por exemplo, no mínimo 9 ou 25 pontos distribuídos em uma malha quadrada) para que o algoritmo consiga calcular matematicamente a distância entre o plano superior e inferior.

### O objetivo de qualquer padrão

Independentemente do desenho do caminho (seja em zigue-zague, grelha ou estrela), a regra de ouro é: **o padrão deve passar obrigatoriamente pelas extremidades (bordas e cantos) e pelo centro da superfície**. É quase sempre nas bordas e nos cantos que o processo de fabricação (como o fresamento ou a retífica) deixa os maiores desvios de planicidade.

<hr>
