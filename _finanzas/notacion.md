---
title: Notación Matemático-Financiera
layout: single
sidebar:
    nav: "finanzas"
toc: True
toc_label: Notaciones
---

{% include mathjax.html %}

La definición de una notación financiera y matemática es necesaria para poder establecer un lenguaje común que nos 
permita entender distintas fuentes de información y distintos autores. Esta sección desglosa la notación en las 
siguientes notaciones clave: 

## Matemáticas Básicas

- $x, y, z:$ Valores numéricos genéricos. 
- $f(x), g(x):$ Denota una función de $x$. 
- $\frac{\partial f}{\partial x}:$ Derivadas parciales.
- $\sum_{i=1}^n a_i:$ Representa la sumatoria de términos $a_i$ desde $i = 1$ hasta $n$.
- $\prod_{i=1}^n a_i:$ Producto de una secuencia $a_i$ desde $i = 1$ hasta $n$.  
- $\lim_{x \to y} f(x):$ Límite de $f(x)$ cuando $x$ tiende a $y$.
- $\pi$: Constante matemática ($\approx 3.1416$), usada en cálculos geométricos.
- $\infty$: Infinito, representa un valor no acotado.
- $\nabla f$: Gradiente de $f$, vector de derivadas parciales.
- $a!$ : Factorial de $a$, producto de enteros desde 1 hasta $a$.  
- $\binom{n}{k}$: Coeficiente binomial, número de combinaciones de $n$ en $k$.
- $\mathbb{R}$: Conjunto de números reales.  
- $\mathbb{C}$: Conjunto de números complejos.  
- $\mathbb{Z}$: Conjunto de números enteros.  
- $\mathbb{Q}$: Conjunto de números racionales.  
- $\mathbb{N}$: Conjunto de números naturales.
- $\cup$: Unión de conjuntos, elementos en al menos uno de los conjuntos.  
- $\cap$: Intersección de conjuntos, elementos en ambos conjuntos.  
- $\subseteq$: Subconjunto, indica que un conjunto está contenido en otro.  
- $\in$: Pertenece, indica que un elemento está en un conjunto.  
- $\notin$: No pertenece, indica que un elemento no está en un conjunto.  
- $\forall$: Para todo, cuantificador universal.  
- $\exists$: Existe, cuantificador existencial.  
- $\implies$: Implica, indica una implicación lógica.  
- $\iff$: Si y solo si, indica equivalencia lógica.  
- $\neg$: Negación lógica, invierte la verdad de una proposición.  
- $\land$: Y lógico, conjunción de proposiciones.  
- $\lor$: O lógico, disyunción de proposiciones.

## Álgebra Matricial

- $A$: Matriz genérica, arreglo rectangular de números.  
- $a_{ij}$: Elemento en la fila $i$, columna $j$ de la matriz $A$.  
- $I_n$: Matriz identidad de tamaño $n \times n$, con 1s en la diagonal.  
- $0$: Matriz cero, todos sus elementos son 0.  
- $A^T$: Transpuesta de $A$, intercambia filas por columnas.  
- $A^{-1}$: Inversa de $A$, tal que $A A^{-1} = I$.  
- $\det(A)$: Determinante de $A$, escalar que indica propiedades de $A$.  
- $\text{tr}(A)$: Traza de $A$, suma de los elementos diagonales.  
- $\text{rank}(A)$: Rango de $A$, número de filas o columnas linealmente independientes.  
- $\text{span}(v_1, \dots, v_k)$: Espacio generado por los vectores $v_1, \dots, v_k$.  
- $\lambda$: Valor propio (eigenvalue) de una matriz.  
- $v$: Vector propio (eigenvector) asociado a $\lambda$.  
- $A v = \lambda v$: Ecuación de valores propios.  
- $\langle u, v \rangle$: Producto interno de vectores $u$ y $v$.  
- $\| v \|$: Norma del vector $v$, medida de su longitud.  
- $U$: Matriz unitaria, $U^* U = I$.  
- $Q$: Matriz ortogonal, $Q^T Q = I$.  
- $\Sigma$: Matriz diagonal de valores singulares en SVD.  
- $A^+$: Pseudoinversa de $A$, generalización de la inversa.  
- $\text{ker}(A)$: Núcleo de $A$, conjunto de vectores $v$ tales que $A v = 0$.  
- $\text{im}(A)$: Imagen de $A$, conjunto de vectores $A v$ para todo $v$.  
- $A \otimes B$: Producto tensorial de matrices $A$ y $B$.  
- $A \oplus B$: Suma directa de matrices $A$ y $B$.  

## Estadística

- $\mu: $ Media esperada de una variable aleatoria.
- $\sigma^2:$ Varianza de una variable aleatoria.
- $\sigma: $ Desviación estándar o volatilidad.
- $Cov(X, Y): $ Covarianza entre $X$ y $Y$.
- $\rho_{X,Y}: $ Correlación entre $X$ y $Y$.
- $n:$ Tamaño de la muestra o número de observaciones.  
- $\mathcal{z}:$ Variable normal estándar, con media 0 y varianza 1.

## Probabilidad

- $P(A):$ Probabilidad de un evento.
- $\mathbb{E}[X]:$ Esperanza, el valor promedio ponderado de una variable $X$.
- $P(A \cap B)$: Probabilidad de la intersección de eventos $A$ y $B$.  
- $P(A \cup B)$: Probabilidad de la unión de eventos $A$ y $B$.  
- $P(A\mid B)$: Probabilidad condicional de $A$ dado $B$.
- $\Omega$: Espacio muestral, conjunto de todos los resultados posibles.  
- $\emptyset$: Evento imposible, conjunto vacío con probabilidad 0.  
- $A^c$: Complemento del evento $A$, $A^c = \Omega \setminus A$.
- $Q$: Medida de probabilidad neutral al riesgo, usada en valoración financiera.
- $X \sim D$: $X$ sigue la distribución $D$ (e.g., $X \sim N(0,1)$).
- $\mathcal{N}(\mu, \sigma): $ Distribución normal con media $\mu$ y desviación $\sigma$.
- $\mathcal{B}(n,p)$: Distribución binomial con parámetros $n$ y $p$.  
- $\mathcal{P}(\lambda)$: Distribución de Poisson con parámetro $\lambda$.  
- $\mathcal{U}(a,b)$: Distribución uniforme en el intervalo $[a,b]$.  
- $\mathcal{E}(\lambda)$: Distribución exponencial con parámetro $\lambda$.  
- $\mathcal{G}(\alpha,\beta)$: Distribución gamma con parámetros $\alpha$ y $\beta$.
- $\mathcal{L}ognormal(\mu,\sigma)$: Distribución lognormal con parámetros $\mu$ y $\sigma$.
- $\mathcal{C}hi^2(k)$: Distribución chi-cuadrado con $k$ grados de libertad.
- $\mathcal{T}(n)$: Distribución t de Student con $n$ grados de libertad.

## Cálculo Estocástico

- $W_t: $ Movimiento de Wiener o Browniano bajo medida real.
- $dW_t$: Incremento infinitesimal del movimiento browniano, $dW_t \sim N(0, dt)$.
- $(dW_t)^2$: Cuadrado del incremento browniano, igual a $dt$ por la regla de Itô.
- $W_t^Q$: Movimiento browniano bajo la medida $Q$.
- $dS_t$: Diferencial estocástico de $S_t$.
- $W_t^Q$: Movimiento browniano bajo la medida $Q$.
- $\int_0^t S_u dW_u$: Integral estocástica de $S_u$ respecto a $W_u$ hasta $t$.  
- $\mathcal{F}_t$: Filtración en el tiempo $t$, información disponible hasta $t$.  
- $M_t$: Martingala, proceso con $E[M_t \mid \mathcal{F}_s] = M_s$ para $s < t$.  
- $\langle X \rangle_t$: Variación cuadrática del proceso $X$ hasta $t$.  
- $d[X]_t$: Incremento de la variación cuadrática, e.g., $d[W]_t = dt$.
- $\rho_{W_1, W_2}$: Correlación entre dos movimientos brownianos $W_1$ y $W_2$.
- $\kappa$: Parámetro de reversión a la media en procesos como Ornstein-Uhlenbeck.  
- $\theta$: Nivel de reversión o media a largo plazo.


## Ingeniería Financiera

- $S_t: $ Proceso estocástico para tipos de cambio.
- $K:$ Precio de ejercicio o Strike.
- $r, q:$ Tasa de interés.
- $\Delta:$ Sensibilidad a la variación del subyacente.
- $\Gamma:$ Convexidad.
- $\Theta:$ Sensibilidad al tiempo.
- $\mathcal{V}:$ Sensibilidad a la volatilidad (Vega).
- $V_t(\cdot):$ Valor de un instrumento a plazo $t$.
- $P_t^X(T):$ Factor de descuento en $t$ para plazo $T$ para $X$.
- $C_t^X(T):$ Factor de capitalización en $t$ para plazo $T$ para $X$.

## Notación Temporal

- $t$: Momento específico de tiempo.
- $t_i$: i-esimo momento.
- $T:$ Fecha de vencimiento.
- $\tau:$ Tiempo restante.
- $\Delta t$: Variación entre dos momentos en el tiempo.
- $\phi^x$:Función de fracción de año bajo convención $x$.

