---
title: Cálculo Multivariado
---

{% include mathjax.html %}

El cálculo multivariado extiende el cálculo a funciones de varias variables, abordando temas como 
derivadas parciales, integrales múltiples y optimización en espacios de mayor dimensión. 
Es fundamental en finanzas y análisis de datos para modelar sistemas complejos. Esta es una referencia rápida 
con los conceptos y fórmulas más esenciales del cálculo multivariado, organizada por categorías.

---

## Conceptos fundamentales

| Concepto/Fórmula                                                                    | Descripción                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------|
| **Función multivariada**: $f(x, y)$                                                 | Función con dos o más variables independientes.             |
| **Límite**: $lim_{(x,y) → (a,b)} f(x,y)$                                            | Valor al que se acerca $f$ cuando $(x,y)$ tiende a $(a,b)$. |
| **Continuidad**: $f(a,b)$ existe, $lim_{(x,y) → (a,b)} f(x,y)$ existe y son iguales | Condición para continuidad en un punto.                     |

---

## Derivadas parciales

| Fórmula                                                           | Descripción                                                                 |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------|
| $∂f/∂x = lim_{h → 0} [f(x+h,y) - f(x,y)]/h$                       | Derivada parcial respecto a $x$ (trata $y$ como constante).                 |
| $∂f/∂y = lim_{h → 0} [f(x,y+h) - f(x,y)]/h$                       | Derivada parcial respecto a $y$ (trata $x$ como constante).                 |
| **Segunda parcial**: $∂²f/∂x²$                                    | Derivada parcial de $∂f/∂x$ respecto a $x$.                                 |
| **Parcial cruzada**: $∂²f/∂x∂y$                                   | Derivada de $∂f/∂y$ respecto a $x$ (igual a $∂²f/∂y∂x$ si $f$ es continua). |
| **Regla de la cadena**: $dz/dt = (∂z/∂x)(dx/dt) + (∂z/∂y)(dy/dt)$ | Para $z = f(x(t), y(t))$.                                                   |

---

## Gradiente y derivada direccional

| Fórmula                                                                   | Descripción                                                           |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Gradiente**: $∇f = (∂f/∂x, ∂f/∂y)$                                      | Vector de derivadas parciales; indica dirección de mayor crecimiento. |
| **Derivada direccional**: $D_u f = ∇f · u$                                | Tasa de cambio en la dirección del vector unitario $u$.               |
| **Norma del gradiente**: $ \Vert ∇f \Vert = \sqrt{[(∂f/∂x)² + (∂f/∂y)²]}$ | Magnitud del gradiente.                                               |

---

## Optimización

| Concepto/Fórmula                                                      | Descripción                               |
|-----------------------------------------------------------------------|-------------------------------------------|
| **Puntos críticos**: $∇f = (0, 0)$                                    | Donde las derivadas parciales son cero.   |
| **Matriz Hessiana**: $H = [[∂²f/∂x², ∂²f/∂x∂y], [∂²f/∂y∂x, ∂²f/∂y²]]$ | Matriz de segundas parciales.             |
| **Criterio de la segunda derivada**:                                  | Evalúa el tipo de punto crítico:          |
| - $det(H) > 0, ∂²f/∂x² > 0$                                           | Mínimo local.                             |
| - $det(H) > 0, ∂²f/∂x² < 0$                                           | Máximo local.                             |
| - $det(H) < 0$                                                        | Punto de silla (saddle point).            |
| **Multiplicadores de Lagrange**: $∇f = λ∇g$, $g(x,y) = c$             | Optimiza $f$ sujeta a la restricción $g$. |

---

## Integrales múltiples

| Fórmula                                              | Descripción                                       |
|------------------------------------------------------|---------------------------------------------------|
| **Integral doble**: $∫∫_R f(x,y) dA$                 | Área bajo $f(x,y)$ sobre la región $R$.           |
| **Orden de integración**: $∫_a^b ∫_c^d f(x,y) dy dx$ | Integra primero respecto a $y$, luego $x$.        |
| **Cambio de orden**: $∫_c^d ∫_a^b f(x,y) dx dy$      | Invierte el orden según límites de $R$.           |
| **Coordenadas polares**: $∫∫_R f(r,θ) r dr dθ$       | Usa $x = r cos θ$, $y = r sin θ$, $dA = r dr dθ$. |
| **Integral triple**: $∫∫∫_V f(x,y,z) dV$             | Volumen bajo $f$ en la región $V$.                |

---

## Teoremas fundamentales

| Teorema/Fórmula                                                   | Descripción                                        |
|-------------------------------------------------------------------|----------------------------------------------------|
| **Teorema de Green**: $∫_C P dx + Q dy = ∫∫_R (∂Q/∂x - ∂P/∂y) dA$ | Relaciona integral de línea con integral doble.    |
| **Teorema de Stokes**: $∫_C F · dr = ∫∫_S (∇ × F) · dS$           | Relaciona flujo con circulación en superficies.    |
| **Teorema de la divergencia**: $∫∫_S F · dS = ∫∫∫_V ∇ · F dV$     | Flujo a través de una superficie igual al volumen. |

---

## Campos vectoriales

| Concepto/Fórmula                                    | Descripción                                                         |
|-----------------------------------------------------|---------------------------------------------------------------------|
| **Campo vectorial**: $F = (P, Q)$ o $F = (P, Q, R)$ | Función que asigna vectores a puntos en el plano o espacio.         |
| **Divergencia**: $∇ · F = ∂P/∂x + ∂Q/∂y$ (2D)       | Mide expansión o contracción del campo.                             |
| **Rotacional**: $∇ × F = (∂Q/∂x - ∂P/∂y)k$ (2D)     | Mide rotación del campo (en 3D da un vector).                       |
| **Conservativo**: $∇ × F = 0$                       | Si el rotacional es cero, existe un potencial $f$ tal que $F = ∇f$. |

---

## Coordenadas y transformaciones

| Sistema/Fórmula                                                                                              | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Polares (2D)**: $x = r \cdot cos θ$, $y = r \cdot sin θ$                                                   | Convierte cartesiano a polar.                            |
| **Cilíndricas (3D)**: $x = r \cdot cos θ$, $y = r\cdot sin θ$, $z = z$                                       | Extiende polares con altura $z$.                         |
| **Esféricas (3D)**: $x = ρ \cdot \sin{φ} \cdot\cos{θ}$, $y = ρ \cdot sin φ \cdot sin θ$, $z = ρ \cdot cos φ$ | Usa radio $ρ$, ángulo polar $φ$, azimutal $θ$.           |
| **Jacobiano**: $ J = ∂(x,y)/∂(u,v)$                                                                          | Factor de escala para cambio de variables en integrales. |


