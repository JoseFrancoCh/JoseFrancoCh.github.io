---
title: Cálculo Estocástico
---

{% include mathjax.html %}

El cálculo estocástico es una rama de las matemáticas que modela procesos aleatorios, como el 
movimiento browniano o las ecuaciones diferenciales estocásticas, siendo clave en las finanzas. 
Combina herramientas de probabilidad y cálculo tradicional para analizar sistemas con incertidumbre. Esta
es una referencia rápida con los conceptos y fórmulas más esenciales del cálculo estocástico, 
organizada por categorías.

---

## Conceptos fundamentales

| Concepto/Fórmula                                            | Descripción                                                                                           |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **Proceso estocástico**: $X_t$                              | Función aleatoria que depende del tiempo $t$.                                                         |
| **Movimiento Browniano**: $W_t$                             | Proceso continuo con incrementos normales, $W_0 = 0$, $\mathbb{E}[W_t] = 0$, $\mathbb{V}ar[W_t] = t$. |
| **Propiedad de Markov**:                                    | El futuro depende solo del estado actual, no del pasado.                                              |
| **Martingala**: $\mathbb{E}[X_t \mid \mathcal{F}_s] = X(s)$ | Proceso cuya esperanza condicional es constante. $(s \leq t)$.                                        |
| **Filtración**: $\mathcal{F}_t$                             | Conjunto de información disponible hasta el tiempo $t$.                                               |

---

## Movimiento Browniano (Wiener Process)

| Propiedad/Fórmula                                          | Descripción                                        |
|------------------------------------------------------------|----------------------------------------------------|
| **Incrementos independientes**: $W_t - W_s \sim N(0, t-s)$ | Diferencias son normales e independientes.         |
| **Varianza**: $\mathbb{V}ar[W_t - W_s] = t - s$            | Varianza crece linealmente con el tiempo.          |
| **No derivable**: $dW_t/dt$ no existe                      | Trayectorias son continuas pero no diferenciables. |
| **Escalamiento**: $W_{ct} \sim \sqrt{c * W_t}$             | Propiedad de autosimilitud.                        |

---

## Integral estocástica (Itô)

| Fórmula                                                               | Descripción                                                |
|-----------------------------------------------------------------------|------------------------------------------------------------|
| **Definición**: $\int_a^b f(t) dW_t$                                  | Límite de sumas con incrementos de $W_t$.                  |
| **Propiedad**: $\mathbb{E}[\int_a^b f(t) dW_t] = 0$                   | Esperanza de la integral es cero (si $f$ es determinista). |
| **Varianza**: $\mathbb{E}[(\int_a^b f(t) dW_t)²] = \int_a^b f(t)² dt$ | Teorema de isometría de Itô.                               |
| **No anticipativa**:                                                  | $f(t)$ debe depender solo de $\mathcal{F}_t$ (adaptada).   |

---

## Lema de Itô

| Fórmula                                                                | Descripción                                    |
|------------------------------------------------------------------------|------------------------------------------------|
| **Fórmula de Itô**: $dF = (∂F/∂t)dt + (∂F/∂x)dX + (1/2)(∂²F/∂x²)(dX)²$ | Regla de la cadena para procesos estocásticos. |
| **Regla (dX)²**:                                                       | Sustituciones clave:                           |
| - $dt * dt = 0$                                                        | Términos de orden superior desaparecen.        |
| - $dt * dW = 0$                                                        | Producto cruzado es insignificante.            |
| - $dW * dW = dt$                                                       | Propiedad cuadrática del movimiento Browniano. |
| **Ejemplo**: $X_t = W_t²$                                              | $dX = 2W_tdW + dt$                             |

---

## Ecuaciones diferenciales estocásticas (SDE)

| Fórmula                                                   | Descripción                                             |
|-----------------------------------------------------------|---------------------------------------------------------|
| **Forma general**: $dX_t = a(t,X_t)dt + b(t,X_t)dW_t$     | Incluye término determinista ($a$) y estocástico ($b$). |
| **Solución (lineal)**: $dX = μX dt + σX dW$               | Ejemplo: movimiento Browniano geométrico.               |
| **Esperanza**: $\mathbb{E}[X_t]$                          | Resuelve la ecuación determinista asociada $(σ = 0)$.   |
| **Método de Euler-Maruyama**: $X(t+Δt) = X_t + aΔt + bΔW$ | Aproximación numérica de SDEs.                          |

---

## Procesos de difusión

| Concepto/Fórmula                                                      | Descripción                                     |
|-----------------------------------------------------------------------|-------------------------------------------------|
| **Drift**: $a(t, X_t)$                                                | Componente determinista del proceso.            |
| **Difusión**: $b(t, X_t)$                                             | Componente aleatorio (volatilidad).             |
| **Ecuación de Fokker-Planck**: $∂p/∂t = -∂(ap)/∂x + (1/2)∂²(b²p)/∂x²$ | Describe la evolución de la densidad $p(x,t).$  |

---

## Aplicaciones en finanzas

| Fórmula                                                         | Descripción                                  |
|-----------------------------------------------------------------|----------------------------------------------|
| **Black-Scholes**: $dS_t  = μS_t dt + σS_t dW$                  | Modelo para precios de activos (S = precio). |
| **Valor esperado**: $\mathbb{E}[S_t] = S_0e^{(μt)}$             | Crecimiento determinista del activo.         |
| **Fórmula de Black-Scholes**: $C = S_0 N(d₁) - K e^{-rt} N(d₂)$ | Precio de una opción call europea.           |
| - $d₁ = [ln(S_0/K) + (r + σ²/2)t] / (σ√t)$                      | Término auxiliar para la fórmula.            |
| - $d₂ = d₁ - σ√t$                                               | Segundo término auxiliar.                    |

---

## Transformaciones y propiedades

| Concepto/Fórmula                        | Descripción                                         |
|-----------------------------------------|-----------------------------------------------------|
| **Martingala de Itô**: $\int f(t) dW_t$ | Integral estocástica es una martingala.             |
| **Tiempo de parada**: $τ$               | Momento aleatorio en que se cumple una condición.   |
| **Teorema de Girsanov**:                | Cambia la medida para eliminar el drift (finanzas). |

---

## Probabilidad y esperanza

| Fórmula                                    | Descripción                                        |
|--------------------------------------------|----------------------------------------------------|
| **Esperanza**: $\mathbb{E}[X_t]$           | Promedio del proceso en el tiempo $t$.             |
| **Covarianza**: $Cov[W_s, W_t] = min(s,t)$ | Relación entre tiempos en el movimiento Browniano. |
| **Distribución**: $W_t \sim N(0, t)$       | Distribución normal del movimiento Browniano.      |

