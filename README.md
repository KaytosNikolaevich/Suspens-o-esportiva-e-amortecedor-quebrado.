# 🏎️ Simulação de Suspensão Automotiva (Quarter Car Model)

![Octave](https://img.shields.io/badge/Octave-DarkBlue?style=for-the-badge&logo=octave&logoColor=white)
![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen?style=for-the-badge)

Este repositório contém a implementação e análise de um modelo de suspensão veicular de dois graus de liberdade (2-DOF), conhecido como **Quarter Car Model**. O objetivo é analisar o comportamento dinâmico do chassi e da roda diante de um obstáculo tipo degrau (10cm).

## 📊 Casos Analisados

O projeto compara três cenários distintos de dirigibilidade:
1. **Suspensão Original:** Equilíbrio entre conforto e estabilidade.
2. **Suspensão Esportiva:** Alta rigidez ($k$) e amortecimento ($c$) para máxima performance.
3. **Amortecedor Quebrado:** Simulação de falha crítica no amortecimento, resultando em oscilações persistentes.

## ⚙️ Modelagem Matemática

O sistema é modelado utilizando **Espaço de Estados (State-Space)**, definido pelas equações:

$$\dot{x} = Ax + Bu$$
$$y = Cx + Du$$

Onde o vetor de estado é $x = [x_1, \dot{x}_1, x_2, \dot{x}_2]^T$, representando posições e velocidades da massa suspensa ($m_2$) e não suspensa ($m_1$).

### Parâmetros Base:
- **Massa Suspensa ($m_2$):** 300 kg
- **Massa Não Suspensa ($m_1$):** 40 kg
- **Rigidez do Pneu ($k_t$):** 150.000 N/m

## 📈 Resultados

As simulações foram realizadas no **GNU Octave**.

| Configuração | Rigidez ($k_1$) | Amortecimento ($c_1$) | Comportamento Observado |
| :--- | :--- | :--- | :--- |
| **Original** | 15.000 N/m | 1.000 N.s/m | Resposta padrão de fábrica. |
| **Esportiva** | 35.000 N/m | 2.500 N.s/m | Estabilização rápida, maior rigidez. |
| **Quebrada** | 15.000 N/m | 100 N.s/m | Oscilações excessivas (efeito pula-pula). |

---

## 🚀 Como Executar

1. Utilize o [Octave Online](https://octave-online.net/).
