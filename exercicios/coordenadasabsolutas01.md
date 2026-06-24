<h2>Coordenadas Absolutas e Relativas - Torneamento CNC</h2>

<img width="501" height="474" alt="image" src="https://github.com/user-attachments/assets/6360e008-45eb-493c-8682-f082491a4485" />

**Sistema de referência (zero-peça):**
- Origem (X0, Z0) = intersecção do eixo da peça com a face direita da peça acabada
- X em **diâmetro** (convenção usual de torno)
- Z+ para a direita, Z- para a esquerda (conforme indicado na figura)
- P1 é o ponto inicial da ferramenta, fora da peça: X=Ø150, Z=50

**Como decompus o perfil (direita → esquerda):**
- Chanfro 3x45° na Ø20 (lado direito): reduz o diâmetro em 6 mm (3 mm de raio) ao longo de 3 mm em Z → de Ø14 (na face) até Ø20
- Trecho cilíndrico Ø20: de Z=-3 até Z=-20
- Degrau (90°, sem chanfro/raio indicado) entre Ø20 e Ø40, em Z=-20
- Trecho cilíndrico Ø40: de Z=-20 até Z=-40
- Concordância R3 entre Ø40 e Ø60, em Z=-40 (aplicada como comando de raio no canto, não como ponto extra)
- Trecho cilíndrico Ø60: de Z=-40 até Z=-60
- Chanfro 3x45° na Ø60 (lado esquerdo, face final): de Ø60 até Ø54

**Tabela de coordenadas:**

| Ponto | Absoluta (X, Z) | Relativa/Incremental (ΔX, ΔZ) |
|---|---|---|
| P1 | (150, 50) | — (partida) |
| P2 | (20, 3) | (-130, -47) |
| P3 | (14, 0) | (-6, -3) |
| P4 | (20, -3) | (+6, -3) |
| P5 | (20, -20) | (0, -17) |
| P6 | (40, -20) | (+20, 0) |
| P7 | (40, -40) | (0, -20) |
| P8 | (60, -40) | (+20, 0) |
| P9 | (60, -60) | (0, -20) |
| P10 | (54, -60) | (-6, 0) |

As coordenadas relativas são sempre a diferença entre o ponto atual e o anterior (X_atual - X_anterior, Z_atual - Z_anterior).
