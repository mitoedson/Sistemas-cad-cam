<h2>Tolerância Geométrica - Exercícios</h2>

<img width="320" height="163" alt="image" src="https://github.com/user-attachments/assets/e6721ba5-6b9e-4abc-ab02-d11042bc5df0" />

O símbolo **∥ 0,1 B** significa:

- **∥** → tipo: **paralelismo**
- **0,1** → zona de tolerância entre **dois planos paralelos** afastados 0,1 mm
- **B** → referência: o **eixo do furo** (datum B)
- **Sem Ø** → a zona é planar, não cilíndrica — controla apenas **uma direção**

---

## Diferença fundamental em relação à questão 1

| | Questão 1 | Questão 2 |
|---|---|---|
| **Símbolo** | ∥ **Ø**0,03 A | ∥ 0,1 B |
| **Zona de tolerância** | Cilindro Ø0,03 | Dois planos 0,1 mm |
| **Direções controladas** | Todas (360°) | Apenas uma direção |
| **Elemento tolerado** | Eixo do pino | Superfície plana lateral |

---

## Interpretação geométrica

A **superfície plana lateral** da peça deve estar contida entre dois planos imaginários paralelos ao datum B, separados por **0,1 mm**.

```
        ←—— 0,1 mm ——→
        ________________   plano superior
        
        superfície real
        deve ficar aqui
        ________________   plano inferior
        
        paralelo ao datum B (eixo do furo)
```

---

## Como verificar na prática

Com o comparador deslizando sobre a **superfície plana**, a leitura máxima não pode ultrapassar **0,1 mm**.


**1. Apoiar a peça** — o datum B (cilindro/furo) é apoiado em prismas V sobre a mesa de desempeno, garantindo que ele seja a referência.

**2. Zerar o comparador** — encosta a haste do relógio na superfície a medir e zera a leitura.

**3. Deslizar e registrar** — move o comparador ao longo de toda a superfície, registrando a variação máxima entre o maior e menor valor lido.

**4. Avaliar** — se a variação total for **≤ 0,1 mm**, a peça está aprovada. Se ultrapassar, está reprovada.

O ponto chave é que o comparador **não mede um valor absoluto** — ele mede a **diferença entre os pontos mais alto e mais baixo** da superfície. Essa diferença é o desvio de paralelismo.

<hr>



