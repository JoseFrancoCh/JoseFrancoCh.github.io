# Teorema de Arbitraje: Fundamentos y Aplicaciones en Ingeniería Financiera

## Introducción

El **Teorema de Arbitraje** es una piedra angular en la teoría de la valoración de activos y la ingeniería financiera. Este teorema define las condiciones bajo las cuales no existen oportunidades de arbitraje en un mercado financiero, es decir, situaciones en las que un inversor podría obtener ganancias sin riesgo ni inversión inicial. Este principio es esencial para modelos de valoración de derivados como el de Black-Scholes y para la gestión de riesgos financieros.

En este artículo, exploraremos el Teorema de Arbitraje de manera directa y práctica, con un enfoque académico pero conversacional. Incluiremos su formulación matemática, ejemplos concretos y sus implicaciones en el mundo real, asumiendo que los lectores tienen experiencia en conceptos financieros como martingalas y procesos estocásticos.

---

## Cuerpo

### 1. ¿Qué entendemos por arbitraje?

El arbitraje ocurre cuando un inversor puede aprovechar diferencias de precios entre mercados para obtener una ganancia segura sin riesgo. En un mercado eficiente, estas oportunidades deberían ser efímeras, ya que los participantes las explotan rápidamente hasta que desaparecen.

**Ejemplo**: Imagina una acción que cuesta 100 USD en Nueva York y 102 USD en Londres al mismo tiempo. Comprarla en Nueva York y venderla en Londres genera una ganancia de 2 USD por acción sin riesgo. Esto es un arbitraje puro. El Teorema de Arbitraje nos dice que, en un mercado bien estructurado, tales oportunidades no deberían existir de forma persistente.

### 2. El Teorema de Arbitraje en detalle

El Teorema de Arbitraje establece una conexión entre la ausencia de oportunidades de arbitraje y la existencia de una **medida de probabilidad equivalente** (o medida de riesgo neutral) bajo la cual los precios descontados de los activos son martingalas. En términos simples, asegura que los precios de los activos se ajustan para evitar ganancias sin riesgo.

Matemáticamente, en un mercado con activos de precios \(S_t\) y un activo libre de riesgo \(B_t\) (como un bono), el teorema dice que no hay arbitraje si existe una medida \(Q\) tal que:

\[
\frac{S_t}{B_t} \text{ es una martingala bajo } Q
\]

Esto significa que:

\[
E_Q\left[ \frac{S_{t+1}}{B_{t+1}} \middle| \mathcal{F}_t \right] = \frac{S_t}{B_t}
\]

donde \(\mathcal{F}_t\) representa la información disponible hasta el tiempo \(t\). Esta ecuación asegura que el valor esperado del precio descontado no cambia con el tiempo bajo la medida \(Q\).

### 3. ¿Por qué importa?

La ausencia de arbitraje tiene implicaciones profundas. Por ejemplo, lleva a la **ley del precio único**: dos activos con los mismos flujos de efectivo futuros deben tener el mismo precio hoy. Además, es la base para valorar derivados financieros, ya que permite determinar precios consistentes con el mercado.

### 4. Ejemplo: Una opción en un modelo binomial

Consideremos un modelo binomial simple para entender cómo funciona el teorema. Una acción vale \(S_0 = 100\) hoy. En un período, puede subir a \(S_1 = 110\) o bajar a \(S_1 = 90\). La tasa libre de riesgo es \(r = 0.05\). Queremos valorar una opción de compra con precio de ejercicio \(K = 100\).

Para que no haya arbitraje, el precio descontado de la acción debe ser una martingala bajo \(Q\):

\[
E_Q\left[ \frac{S_1}{1 + r} \right] = S_0
\]

Si \(q\) es la probabilidad de que suba bajo \(Q\):

\[
q \cdot \frac{110}{1.05} + (1 - q) \cdot \frac{90}{1.05} = 100
\]

Resolviendo:

\[
q \approx 0.4762
\]

Entonces, bajo \(Q\), la probabilidad de subida es 0.4762 y la de bajada es 0.5238. El precio de la opción (\(C_0\)) se calcula como:

\[
C_0 = \frac{1}{1 + r} E_Q\left[ \max(S_1 - K, 0) \right]
\]

Sustituyendo:

\[
C_0 = \frac{1}{1.05} \left[ 0.4762 \cdot (110 - 100) + 0.5238 \cdot (90 - 100) \right]
\]

\[
C_0 = \frac{1}{1.05} \left[ 0.4762 \cdot 10 + 0.5238 \cdot 0 \right] \approx 4.535
\]

Este precio de 4.535 USD refleja el valor justo de la opción, garantizado por la ausencia de arbitraje.

### 5. El Teorema Fundamental del Arbitraje

En términos más amplios, el **Teorema Fundamental del Arbitraje** dice que un mercado está libre de arbitraje si y solo si existe al menos una medida \(Q\) que haga martingalas a los precios descontados. En mercados completos, esta medida es única, lo que simplifica la valoración. En mercados incompletos, puede haber varias medidas, resultando en rangos de precios para los derivados.

### 6. Aplicaciones en la gestión de riesgos

El teorema también es clave en la gestión de riesgos. Por ejemplo, al cubrir una opción con una estrategia delta, se construye un portafolio que elimina el riesgo, y la ausencia de arbitraje asegura que el costo de esta cobertura iguale el precio de la opción. En la **Arbitrage Pricing Theory (APT)**, se usa para vincular rendimientos esperados con factores de riesgo.

---

## Referencias

- Harrison, J. M., & Pliska, S. R. (1981). Martingales and stochastic integrals in the theory of continuous trading. *Stochastic Processes and their Applications*, 11(3), 215-260.
- Hull, J. C. (2017). *Options, Futures, and Other Derivatives* (10th ed.). Pearson.
- Shreve, S. E. (2004). *Stochastic Calculus for Finance II: Continuous-Time Models*. Springer.

---
