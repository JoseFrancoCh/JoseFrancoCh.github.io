---
title: Estadística
---

{% include mathjax.html %}

La estadística es la ciencia de recolectar, analizar e interpretar datos para entender patrones y tomar 
decisiones bajo incertidumbre. Cubre desde medidas de tendencia central (como la media) hasta pruebas de 
hipótesis y regresiones, siendo clave en investigación y análisis de datos. Esta es una referencia rápida 
con los conceptos y fórmulas más esenciales de estadística, organizada por categorías.

---

## Conceptos básicos

| Concepto/Fórmula | Descripción                                              |
|------------------|----------------------------------------------------------|
| **Población**    | Conjunto completo de datos de interés.                   |
| **Muestra**      | Subconjunto representativo de la población.              |
| **Variable**     | Característica que se mide (cuantitativa o cualitativa). |
| **Dato**         | Valor específico de una variable.                        |

---

## Medidas de tendencia central

| Fórmula                                                                           | Descripción                                                                        |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Media (promedio)**: $μ = (Σx_i) / N$ (población) o $x̄ = (Σx_i) / n$ (muestra)  | Suma de valores dividida por el número de datos.                                   |
| **Mediana**                                                                       | Valor central al ordenar los datos (si $n$ es par, promedio de los dos centrales). |
| **Moda**                                                                          | Valor que aparece con mayor frecuencia.                                            |
| **Media ponderada**: $x̄ = (Σw_i * x_i) / Σw_i$                                   | Promedio con pesos asignados a cada valor.                                         |

---

## Medidas de dispersión

| Fórmula                                                              | Descripción                                              |
|----------------------------------------------------------------------|----------------------------------------------------------|
| **Rango**: $R = max - min$                                           | Diferencia entre el valor máximo y mínimo.               |
| **Varianza (población)**: $σ² = Σ(x_i - μ)² / N$                     | Promedio de las desviaciones al cuadrado.                |
| **Varianza (muestra)**: $s² = Σ(x_i - x̄)² / (n-1)$                  | Similar, pero divide entre $n-1$ (corrección de Bessel). |
| **Desviación estándar**: $σ = √σ²$ (población) o $s = √s²$ (muestra) | Raíz cuadrada de la varianza.                            |
| **Rango intercuartílico**: $IQR = Q3 - Q1$                           | Diferencia entre el tercer y primer cuartil.             |

---

## Distribuciones y percentiles

| Concepto/Fórmula                                   | Descripción                                                     |
|----------------------------------------------------|-----------------------------------------------------------------|
| **Cuartiles**: $Q1, Q2, Q3$                        | Divide los datos ordenados en 4 partes iguales (25%, 50%, 75%). |
| **Percentiles**: $P_k$                             | Valor por debajo del cual está el $k%$ de los datos.            |
| **Distribución simétrica**: Media = Mediana = Moda | Curva en forma de campana (ej. normal).                         |
| **Sesgo**:                                         | Forma de la distribución:                                       |
| - Positivo (derecha)                               | Cola larga a la derecha (media > mediana).                      |
| - Negativo (izquierda)                             | Cola larga a la izquierda (media < mediana).                    |

---

## Probabilidad básica

| Fórmula                                          | Descripción                                      |
|--------------------------------------------------|--------------------------------------------------|
| **Probabilidad**: $P(A) = n(A) / n(S)$           | Número de casos favorables sobre casos posibles. |
| **Suma**: $P(A ∪ B) = P(A) + P(B) - P(A ∩ B)$    | Probabilidad de A o B (regla de adición).        |
| **Producto**: $P(A ∩ B) = P(A) * P(B)$           | Si A y B son independientes.                     |
| **Complemento**: $P(A') = 1 - P(A)$              | Probabilidad de que A no ocurra.                 |
| **Condicional**: $P(A \mid B) = P(A ∩ B) / P(B)$ | Probabilidad de A dado B.                        |

---

## Distribuciones de probabilidad

| Distribución/Fórmula              | Descripción                                      |
|-----------------------------------|-------------------------------------------------|
| **Uniforme**: $P(x) = 1/(b-a)$    | Todos los valores tienen igual probabilidad.    |
| **Binomial**: $P(x) = (nCx) * p^x * (1-p)^(n-x)$ | Éxitos en $n$ ensayos, probabilidad $p$.     |
| **Normal**: $f(x) = (1/σ√(2π)) * e^(-(x-μ)²/(2σ²))$ | Curva en campana, definida por $μ$ y $σ$.   |
| **Z-score**: $z = (x - μ) / σ$    | Estandariza un valor en una distribución normal. |

---

## Inferencia estadística

| Concepto/Fórmula                              | Descripción                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| **Intervalo de confianza**: $x̄ ± z * (s/√n)$ | Rango estimado para el parámetro (ej. 95% con $z = 1.96$).                      |
| **Error estándar**: $SE = s / √n$             | Desviación estándar de la media muestral.                                       |
| **Prueba de hipótesis**:                      | Pasos: 1) H₀ (nula), 2) H₁ (alternativa), 3) Valor p, 4) Decisión.              |
| **Valor p**:                                  | Probabilidad de observar los datos si H₀ es cierta (menor que α → rechazar H₀). |
| **Nivel de significancia**: $α$               | Umbral para rechazar H₀ (ej. 0.05 = 5%).                                        |

---

## Correlación y regresión

| Fórmula                                                                                   | Descripción                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| **Correlación (Pearson)**: $r = Σ[(x_i - x̄)(y_i - ȳ)] / √[Σ(x_i - x̄)² * Σ(y_i - ȳ)²]$ | Mide relación lineal (-1 a 1).                          |
| **Regresión lineal**: $y = a + bx$                                                        | Línea que predice $y$ a partir de $x$.                  |
| - Pendiente: $b = Σ[(x_i - x̄)(y_i - ȳ)] / Σ(x_i - x̄)²$                                 | Cambio en $y$ por unidad de $x$.                        |
| - Intersección: $a = ȳ - b * x̄$                                                         | Punto donde la línea cruza el eje $y$.                  |
| **R²**:                                                                                   | Proporción de varianza explicada por el modelo (0 a 1). |

---

## Análisis de datos

| Concepto/Fórmula                | Descripción                                         |
|---------------------------------|-----------------------------------------------------|
| **Diagrama de caja (boxplot)**: | Muestra mediana, cuartiles, IQR y valores atípicos. |
| **Histograma**:                 | Representa la frecuencia de datos en intervalos.    |
| **Dispersión (scatter)**:       | Muestra relación entre dos variables.               |
| **Valores atípicos**:           | Datos fuera de $Q1 - 1.5*IQR$ o $Q3 + 1.5*IQR$.     |

---

## Fórmulas útiles

| Fórmula                                                            | Descripción                               |
|--------------------------------------------------------------------|-------------------------------------------|
| **Combinaciones**: $nCx = n! / [x!(n-x)!]$                         | Número de formas de elegir $x$ de $n$.    |
| **Factorial**: $n! = n * (n-1) * ... * 1$                          | Producto de enteros hasta $n$.            |
| **Esperanza (media)**: $\mathbb{E}(X) = Σx_i * P(x_i)$             | Valor esperado de una variable aleatoria. |
| **Varianza**: $\mathbb{V}ar(X) = \mathbb{E}[(X - \mathbb{E}(X))²]$ | Dispersión alrededor de la esperanza.     |

