---
title: Cálculo Básico
---

{% include mathjax.html %}

El cálculo es una rama de las matemáticas que estudia el cambio y las relaciones entre cantidades que varían. 
Se divide principalmente en dos áreas: el cálculo diferencial, que analiza cómo cambian las funciones 
(como tasas de variación o pendientes, a través de derivadas), y el cálculo integral, que se ocupa de 
acumular cantidades (como áreas bajo curvas o volúmenes, mediante integrales). 

La siguiente es una referencia rápida con los conceptos y fórmulas más esenciales del cálculo.

---

## Conceptos fundamentales

| Concepto/Fórmula                                                        | Descripción                                            |
|-------------------------------------------------------------------------|--------------------------------------------------------|
| **Límite**: $lim_{x → a} f(x )$                                         | Valor al que se acerca $f(x)$ cuando $x$ tiende a $a$. |
| **Continuidad**: $f(a)$ existe, $lim_{x → a} f(x)$ existe y son iguales | Condición para que una función sea continua en $a$.    |
| **Derivada**: $f'(x) = lim_{h → 0} \frac{f(x + h) - f(x)}{h}$           | Tasa de cambio instantánea de $f(x)$.                  |
| **Integral**: $\int f(x) dx$                                            | Área bajo la curva o antiderivada de $f(x)$.           |

---

## Reglas básicas de derivadas

| Fórmula                                                           | Descripción                     |
|-------------------------------------------------------------------|---------------------------------|
| $\frac{d}{dx} (c) = 0$                                            | Derivada de una constante es 0. |
| $\frac{d}{dx} (x^n) = n * x^(n-1)$                                | Regla de la potencia.           |
| $\frac{d}{dx} [f(x) + g(x)] = f'(x) + g'(x)$                      | Regla de la suma.               |
| $\frac{d}{dx} [f(x) * g(x)] = f'(x)g(x) + f(x)g'(x)$              | Regla del producto.             |
| $\frac{d}{dx} [f(x) / g(x)] = [f'(x)g(x) - f(x)g'(x)] / [g(x)]^2$ | Regla del cociente.             |
| $\frac{d}{dx} [f(g(x))] = f'(g(x)) * g'(x)$                       | Regla de la cadena.             |

---

## Derivadas comunes

| Función                           | Derivada                             |
|-----------------------------------|--------------------------------------|
| $\frac{d}{dx} (sin x) = cos x$    | Derivada del seno.                   |
| $\frac{d}{dx} (cos x) = -sin x$   | Derivada del coseno.                 |
| $\frac{d}{dx} (tan x) = sec^2 x$  | Derivada de la tangente.             |
| $\frac{d}{dx} (e^x) = e^x$        | Derivada de la función exponencial.  |
| $\frac{d}{dx} (ln x) = 1/x$       | Derivada del logaritmo natural.      |
| $\frac{d}{dx} (a^x) = a^x * ln a$ | Derivada de una exponencial general. |

---

## Reglas básicas de integrales

| Fórmula                                               | Descripción                                               |
|-------------------------------------------------------|-----------------------------------------------------------|
| $\int c dx = c * x + C$                               | Integral de una constante.                                |
| $\int x^n dx = (x^{(n+1)})/(n+1) + C $                | Regla de la potencia para integración. ($\forall n ≠ -1$) |
| $\int [f(x) + g(x)] dx = \int f(x) dx + \int g(x) dx$ | Regla de la suma.                                         |
| $\int c * f(x) dx = c * \int f(x) dx$                 | Constante fuera de la integral.                           |

---

## Integrales comunes

| Función                             | Integral indefinida                         |
|-------------------------------------|---------------------------------------------|
| $\int sin x dx = -cos x + C$        | Integral del seno.                          |
| $\int cos x dx = sin x + C$         | Integral del coseno.                        |
| $\int sec^2 x dx = tan x + C$       | Integral de la secante al cuadrado.         |
| $\int e^x dx = e^x + C$             | Integral de la exponencial.                 |
| $\int 1/x dx = ln(x) + C$           | Integral del recíproco (logaritmo natural). |
| $\int a^x dx = (a^x)/(ln(a)) + C$   | Integral de una exponencial general.        |

---

## Propiedades de límites

| Propiedad                                                                                                                         | Descripción               |
|-----------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| $lim_{x → a} [f(x) + g(x)] = lim_{x → a} f(x) + lim_{x → a} g(x)$                                                                 | Suma de límites.          |
| $lim_{x → a} [f(x) * g(x)] = lim_{x → a} f(x) * lim_{x → a} g(x)$                                                                 | Producto de límites.      |
| $lim_{x → a} [f(x) / g(x)] = lim_{x → a} f(x) / lim_{x → a} g(x)$ (si g(x) ≠ 0)                                                   | Cociente de límites.      |
| **Teorema del valor intermedio**: Si $f$ es continua en $[a, b]$, toma todos los valores entre $f(a)$ y $f(b)$.                   | Propiedad de continuidad. |
| **Teorema del valor medio**: Si $f$ es continua y derivable, existe un $c$ en $(a, b)$ tal que $f'(c) = [f(b) - f(a)] / (b - a)$. | Tasa de cambio promedio.  |

---

## Integrales definidas

| Fórmula                                                           | Descripción                                               |
|-------------------------------------------------------------------|-----------------------------------------------------------|
| $\int_a^b f(x) dx = F(b) - F(a)$                                  | Teorema fundamental del cálculo ($F$ es la antiderivada). |
| $\int_a^b [f(x) + g(x)] dx = \int_a^b f(x) dx + \int_a^b g(x) dx$ | Suma de integrales.                                       |
| $\int_a^a f(x) dx = 0$                                            | Integral en un punto es cero.                             |
| $\int_b^a f(x) dx = -\int_a^b f(x) dx$                            | Cambio de límites invierte el signo.                      |

---

## Aplicaciones de derivadas

| Concepto/Fórmula                 | Descripción                                         |
|----------------------------------|-----------------------------------------------------|
| **Pendiente**: $f'(x)$           | Pendiente de la recta tangente en $x$.              |
| **Máximos/Mínimos**: $f'(x) = 0$ | Puntos críticos (evaluar $f''(x)$ para concavidad). |
| **Concavidad**: $f''(x) > 0$     | Cóncava hacia arriba (mínimo).                      |
| $f''(x) < 0$                     | Cóncava hacia abajo (máximo).                       |
| **Velocidad**: $dx/dt$           | Derivada del desplazamiento respecto al tiempo.     |
| **Aceleración**: $d^2x/dt^2$     | Segunda derivada del desplazamiento.                |

---

## Aplicaciones de integrales

| Concepto/Fórmula                                           | Descripción                                 |
|------------------------------------------------------------|---------------------------------------------|
| **Área bajo la curva**: $\int_a^b f(x) dx$                 | Área entre $f(x)$ y el eje x de $a$ a $b$.  |
| **Volumen (discos)**: $\pi * \int_a^b [f(x)]^2 dx$         | Volumen de un sólido de revolución (eje x). |
| **Longitud de arco**: $\int_a^b \sqrt{1 + [f'(x)]^2} dx$   | Longitud de una curva entre $a$ y $b$.      |
| **Trabajo**: $\int_a^b F(x) dx$                            | Trabajo realizado por una fuerza variable.  |

---

## Técnicas de integración

| Técnica/Fórmula                                           | Descripción                                |
|-----------------------------------------------------------|--------------------------------------------|
| **Sustitución**: $\int f(g(x)) * g'(x) dx = \int f(u) du$ | Cambia variable con $u = g(x)$.            |
| **Por partes**: $\int u dv = uv - \int v du$              | Usa cuando el producto es integrable.      |
| **Fracciones parciales**: $\int [A/(x-a) + B/(x-b)] dx$   | Descompone racionales en términos simples. |
