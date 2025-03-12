# Teorema de Girsanov: Cambio de Medida y Aplicaciones en Ingeniería Financiera

## Introducción

El **Teorema de Girsanov** es una herramienta fundamental en la teoría de procesos estocásticos, con una relevancia particular en la ingeniería financiera. Este teorema permite **cambiar la medida de probabilidad** bajo la cual se define un proceso estocástico, como un movimiento browniano, transformándolo de un proceso con deriva a uno sin deriva. Este cambio es crucial en finanzas, ya que facilita la transición de la **medida física** (que refleja el comportamiento real de los activos) a la **medida de riesgo neutral**, bajo la cual los precios descontados de los activos son martingalas. Esto simplifica enormemente la valoración de derivados, como opciones, al permitir calcular sus precios como expectativas descontadas bajo una dinámica más manejable.

En este artículo, dirigido a profesionales con experiencia en ingeniería financiera, explicaremos el Teorema de Girsanov de manera clara y detallada. Abordaremos su formulación matemática, su aplicación en la valoración de activos y proporcionaremos ejemplos prácticos para ilustrar su uso en el modelo de Black-Scholes y en un modelo binomial simple. Además, mencionaremos brevemente algunas implicaciones avanzadas del teorema en la valoración de instrumentos financieros más complejos.

---

## Cuerpo

### 1. Formulación del Teorema de Girsanov

El Teorema de Girsanov describe cómo ajustar un proceso browniano bajo una medida de probabilidad para que, bajo una nueva medida, se comporte como un proceso sin deriva. Formalmente, consideremos un espacio de probabilidad \((\Omega, \mathcal{F}, P)\) y un movimiento browniano \(W_t\) bajo la medida \(P\). Si definimos un proceso adaptado \(\theta_t\), podemos construir un nuevo proceso:

\[
\widetilde{W}_t = W_t + \int_0^t \theta_s \, ds
\]

El teorema asegura que \(\widetilde{W}_t\) será un movimiento browniano bajo una nueva medida \(Q\), siempre que \(Q\) se defina mediante la **densidad de Radon-Nikodym**:

\[
\frac{dQ}{dP} = \exp\left( -\int_0^T \theta_s \, dW_s - \frac{1}{2} \int_0^T \theta_s^2 \, ds \right)
\]

Para que esta densidad sea una martingala y, por tanto, una medida de probabilidad válida, se debe cumplir una condición técnica, como la **condición de Novikov**:

\[
E_P\left[ \exp\left( \frac{1}{2} \int_0^T \theta_s^2 \, ds \right) \right] < \infty
\]

En términos simples, el teorema "elimina" la deriva del proceso original ajustando las probabilidades asociadas al movimiento browniano, lo que permite trabajar con un proceso más sencillo bajo la nueva medida.

### 2. Aplicación en Finanzas: La Medida de Riesgo Neutral

En ingeniería financiera, el Teorema de Girsanov se utiliza para cambiar de la medida física \(P\) a la medida de riesgo neutral \(Q\). Bajo \(Q\), los precios descontados de los activos son martingalas, lo que permite valorar derivados de manera más sencilla. Veamos cómo se aplica esto en el modelo de Black-Scholes.

Supongamos que el precio de una acción \(S_t\) sigue la siguiente ecuación bajo la medida \(P\):

\[
dS_t = \mu S_t \, dt + \sigma S_t \, dW_t
\]

donde \(\mu\) es la tasa de retorno esperada y \(\sigma\) es la volatilidad. Para valorar una opción sobre esta acción, necesitamos que la deriva sea igual a la tasa libre de riesgo \(r\), no a \(\mu\). Usando el Teorema de Girsanov, definimos:

\[
\theta_t = \frac{\mu - r}{\sigma}
\]

Entonces, bajo la medida \(Q\), el nuevo proceso browniano es:

\[
\widetilde{W}_t = W_t + \int_0^t \frac{\mu - r}{\sigma} \, ds
\]

y la dinámica de \(S_t\) se transforma en:

\[
dS_t = r S_t \, dt + \sigma S_t \, d\widetilde{W}_t
\]

Ahora, el precio descontado \(\tilde{S}_t = e^{-rt} S_t\) es una martingala bajo \(Q\), lo que permite calcular el precio de una opción europea como:

\[
C_0 = E_Q\left[ e^{-rT} \max(S_T - K, 0) \right]
\]

Este cambio de medida elimina la dependencia de \(\mu\) (que es difícil de estimar) y permite trabajar solo con la tasa libre de riesgo \(r\), simplificando el cálculo del precio de la opción.

### 3. Ejemplo Práctico: Modelo Binomial Simple

Para ilustrar el Teorema de Girsanov de manera más concreta, consideremos un modelo binomial de un solo período. Supongamos que una acción tiene un precio inicial \(S_0 = 100\). En el siguiente período, puede subir a \(S_1 = 110\) con probabilidad \(p = 0.6\) o bajar a \(S_1 = 90\) con probabilidad \(0.4\), bajo la medida física \(P\). La tasa libre de riesgo es \(r = 0.05\).

Queremos valorar una opción de compra europea con precio de ejercicio \(K = 100\). Bajo la medida de riesgo neutral \(Q\), el precio descontado debe ser una martingala:

\[
E_Q\left[ \frac{S_1}{1 + r} \right] = S_0
\]

Sustituyendo los valores:

\[
q \cdot \frac{110}{1.05} + (1 - q) \cdot \frac{90}{1.05} = 100
\]

Resolviendo para \(q\), la probabilidad de subida bajo \(Q\), obtenemos:

\[
q \approx 0.4762
\]

Así, bajo \(Q\), la probabilidad de subida es \(0.4762\) y la de bajada es \(0.5238\). El precio de la opción es:

\[
C_0 = \frac{1}{1.05} \left[ 0.4762 \cdot (110 - 100) + 0.5238 \cdot (90 - 100) \right] = \frac{1}{1.05} \left[ 4.762 \right] \approx 4.535
\]

Este ajuste de probabilidades refleja el cambio de medida que facilita el Teorema de Girsanov, permitiendo calcular el precio de la opción de manera consistente con la hipótesis de no arbitraje.

### 4. Implicaciones en la Valoración de Derivados

El Teorema de Girsanov no solo es fundamental en el modelo de Black-Scholes, sino que también se aplica en modelos más complejos, como:

- **Volatilidad estocástica**: Para ajustar procesos donde la volatilidad varía aleatoriamente (por ejemplo, en el modelo de Heston).
- **Mercados con saltos**: Para manejar discontinuidades en los precios de los activos, como en el modelo de Merton.
- **Optimización de carteras**: Para analizar estrategias de inversión bajo diferentes medidas de probabilidad.

En todos estos casos, el teorema permite trabajar bajo una medida donde las dinámicas de los procesos son más tratables, facilitando la valoración y el análisis de riesgos.

---

## Referencias

- Shreve, S. E. (2004). *Stochastic Calculus for Finance II: Continuous-Time Models*. Springer.
- Hull, J. C. (2017). *Options, Futures, and Other Derivatives* (10th ed.). Pearson.
- [Wikipedia: Teorema de Girsanov](https://es.wikipedia.org/wiki/Teorema_de_Girsanov)
