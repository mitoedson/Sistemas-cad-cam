<h2>Tolerância de forma</h2>

São um grupo de controles geométricos que limitam o quanto um elemento (como uma linha ou superfície) pode variar em relação à sua **forma geométrica teórica/ideal** representada no desenho. Diferente de outras tolerâncias, estas se aplicam exclusivamente a **elementos isolados**, o que significa que não dependem de um elemento de referência (*datum*) para serem verificadas.
<p>
<img width="381" height="156" alt="image" src="https://github.com/user-attachments/assets/e7bd61f5-0971-415a-a235-4721a8cd56a1" />
<p>
Abaixo, detalho os tipos de tolerâncias de forma conforme o material técnico:

### 1. Retilineidade (Retitude) — Símbolo: —
Refere-se ao desvio permitido de uma linha real em relação a uma linha reta teórica. O **campo de tolerância** pode assumir três formas principais:
*   **No plano:** Duas retas paralelas afastadas pela distância "t".
*   **Cilíndrica:** Quando aplicada a eixos de revolução, o campo é um cilindro imaginário de diâmetro "t" dentro do qual o eixo real deve estar contido (indicado pelo símbolo $\varnothing$ antes do valor).
*   **Prismática:** Se a tolerância for especificada em duas direções perpendiculares, o campo torna-se um paralelepípedo.

### 2. Planeza (Planicidade) — Símbolo: ⏥
Controla o desvio de uma superfície em relação a um plano perfeitamente liso. 
*   **Campo de Tolerância:** É definido pelo espaço entre **dois planos paralelos** afastados pela distância "t".
*   **Desvios Comuns:** Os erros mais frequentes são a concavidade e a convexidade. Restrições como "não convexo" podem ser adicionadas para garantir a funcionalidade da peça.

### 3. Circularidade — Símbolo: ○
Define o desvio aceitável de uma forma circular em seções transversais, sendo aplicada principalmente em peças cônicas e cilíndricas.
*   **Campo de Tolerância:** Consiste na área entre **dois círculos concêntricos e coplanares** (no mesmo plano) afastados radialmente por uma distância "t".

### 4. Cilindricidade — Símbolo: ⌭
É um controle mais abrangente que a circularidade, pois analisa toda a superfície cilíndrica de uma vez, incluindo erros de forma ao longo do comprimento (como conicidade ou concavidade).
*   **Campo de Tolerância:** É o espaço entre **dois cilindros coaxiais** cujos raios diferem pelo valor "t". Note que a especificação de cilindricidade já inclui implicitamente a de circularidade e retilineidade das geratrizes.

### 5. Perfil de uma Linha Qualquer — Símbolo: ⌒
Utilizada para controlar formas irregulares compostas por raios e curvas.
*   **Campo de Tolerância:** É a região limitada por duas linhas envolventes que tangenciam círculos de diâmetro "t", cujos centros estão localizados sobre a **linha geométrica ideal**.

### 6. Perfil de uma Superfície Qualquer — Símbolo: ⌓
Semelhante ao perfil de linha, mas aplicado de forma tridimensional a superfícies complexas.
*   **Campo de Tolerância:** É o espaço entre duas superfícies envolventes geradas por esferas de diâmetro "t", cujos centros situam-se exatamente sobre a **superfície teórica** projetada.

**Regra importante:** Salvo indicação contrária, a tolerância de forma aplica-se a toda a extensão (comprimento ou largura) do elemento considerado.
