<h2>Tolerância Geométrica - Exercícios</h2>

<img width="354" height="163" alt="image" src="https://github.com/user-attachments/assets/a9b41dce-063b-4707-a54d-257cbad9b4ca" />

O símbolo **∕ 0,1 A** significa:

- **∕** → tipo: **inclinação**
- **0,1** → zona entre **dois planos paralelos** afastados 0,1 mm
- **A** → referência: o **eixo do cilindro** (datum A)
- **0,1** → dimensão adicional indicada no desenho, que define a distância entre o eixo do cilindro e a superfície tolerada

---

## Relação com as questões anteriores

| Questão 5 | Questão 6 | Questão 10 |
|---|---|---|
| Angularidade ∠ | Perpendicularidade ⊥ | Inclinação ∕ |
| Ângulo livre | 90° fixo | Ângulo definido pela geometria |
| Superfície inclinada | Superfície perpendicular | Superfície cônica ou inclinada |

---

## Diferença entre angularidade e inclinação

Essa é uma distinção sutil mas importante:

| | Angularidade ∠ | Inclinação ∕ |
|---|---|---|
| **Controla** | Apenas o ângulo | Ângulo **e** posição |
| **Zona** | Dois planos no ângulo certo | Dois planos no ângulo **e** posição certos |
| **Datum** | Define só a direção | Define direção e localização |

A inclinação é mais restritiva — além de controlar o ângulo, controla também **onde** a superfície está posicionada.

---

## Interpretação geométrica

```
         eixo datum A
              │
    ┌─────────┼──────┐
    │         │      │  superfície tolerada
    │    ──── │ ────     deve estar entre
    │   /     │     /    dois planos inclinados
    │  /      │    /     afastados 0,1 mm
    │ /       │   /
    └─────────┼──┘
         0,1 mm (posição)
```

---

## Como verificar na prática

1. Apoiar a peça pelo **datum A** (cilindro) nos prismas V
2. Usar um **bloco angular calibrado** no ângulo correto
3. Deslizar o comparador sobre a superfície inclinada
4. A variação não pode ultrapassar **0,1 mm**

---

## Conclusão geral das 10 questões

Agora que passamos por todas, perceba a hierarquia das tolerâncias geométricas:

| Categoria | Tolerâncias vistas |
|---|---|
| **Forma** | Cilindricidade (Q4), Planicidade (Q7) — sem datum |
| **Orientação** | Paralelismo (Q1,2,3), Perpendicularidade (Q6,8), Angularidade (Q5) |
| **Posição** | Concentricidade (Q9), Inclinação (Q10) |

Tem alguma questão que gostaria de revisar ou aprofundar?
