---
title: ¿Se puede hacer un bootstrapping con fórmulas cerradas?
layout: splash
date:   2025-02-28
---

{% include mathjax.html %}

# ¿Se puede hacer un bootstrapping con fórmulas cerradas?

En este artículo exploramos la posibilidad de generar una curva cero cupón a partir de 
insumos de mercado, mediante un bootstrapping, utilizando fórmulas cerradas de valorización. 
Este acercamiento evita el uso de optimizadores, lo que reduce el tiempo y complejidad de 
ejecución, pero introduce potenciales fuentes de error en el cálculo.

Este acercamiento al bootstrapping puede ser util en simulaciones donde se requiera una gran 
cantidad de cambios en los precios de los insumos de mercado con recálculo en las curvas afectadas, 
y a la vez no se requiera un alto nivel de precisión.

Comenzaremos analizando distintos instrumentos, del más simple al más complejo, e
iremos generando fórmulas y aproximaciones para cada uno.

## Tasas Overnight

Una tasa overnight $r^{ON}$ puede ser fácilmente convertida a un factor de descuento dependiendo de
su convención, ej. si consideramos una convención líneal tendremos:

$$P(t_{ON})=(1+r^{ON}\cdot\phi(t_{ON}))^{-1}$$

## Tasas Tomorrow Night

En este caso contamos con un mecanismo parecido al de las tasas overnight, con la diferencia que estas
tienen que ser compuestas sobre la tasa overnight:

$$P(t_{TN})=P(t_{ON})\cdot(1+r^{TN}\cdot\phi(t_{ON}, t_{TN}))^{-1}$$

## Tasas Bullet

Los instrumentos bullet cuentan con un solo flujo donde se pagan los intereses y el nocional, pero con 
la particularidad de que cuentan con un pequeño lag de inicio o start lag $(t_{sl})$, obteniendo la 
fórmula:

$$P(t_{t_end})=P(t_{st})\cdot(1+r\cdot\phi(t_{sl}, t_{end}))^{-1}$$

## Interest Rate Swaps (Misma Colateralización)

Pasando a un instrumento un poco más complejo tenemos un Swap de tasa de interés (IRS) que se encuentra
colateralizado en la misma moneda de su nocional. Si consideramos una figura simplificada con:

- Sin intercambio inicial o final de Nocionales $(N)$
- Sin amortizaciones
- Start Lag
- Sin Pay Lag en ningún flujo
- Con $n$ flujos
- Sin amortizaciones

La pata fija sería expresada como:

$$V_0^{fix} = \sum_{i=1}^{n}N\cdot r\cdot\phi(t_{i-1}, t_{i}) \cdot P(t_i) $$

Mientras que si la pata flotante se encuentra expresada como:

$$V_0^{float} = \sum_{i=1}^{n}N\cdot r_i\cdot\phi(t_{i-1}, t_{i})\cdot P(t_i) $$

Donde:

$$r_i = \left(\frac{P(t_{i-1})}{P(t_i)}-1\right)\cdot \phi(t_{i-1}, t_{i})^{-1}$$

Con estas ecuaciones debemos encontrar el valor de $P(t_n)$, tal que $V_0^{fix}-V_0^{float}=0$. 
Comenzamos por desarrollar igualar ambos valores:

$$V_0^{fix}=V_0^{float}$$

Reemplazamos por las fórmulas originales

$$\sum_{i=1}^{n}N\cdot r\cdot\phi(t_{i-1}, t_{i})\cdot P(t_i) = \sum_{i=1}^{n}N\cdot r_i\cdot\phi(t_{i-1}, t_{i}) \cdot P(t_i) $$

Extraemos los elementos fijos de las sumatorias y simplificamos:

$$N\cdot r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = N\cdot\sum_{i=1}^{n}r_i\cdot\phi(t_{i-1}, t_{i})\cdot P(t_i)$$

$$r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = \sum_{i=1}^{n}r_i\cdot\phi(t_{i-1}, t_{i})\cdot P(t_i)$$

Trabajamos sobre la definición de $r_i$:

$$r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = \sum_{i=1}^{n}\left(\frac{P(t_{i-1})}{P(t_i)}-1\right)\cdot \phi(t_{i-1}, t_{i})^{-1}\cdot\phi(t_{i-1}, t_{i})\cdot P(t_i)$$

$$r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = \sum_{i=1}^{n}\left(\frac{P(t_{i-1})}{P(t_i)}-1\right)\cdot P(t_i)$$

$$r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = \sum_{i=1}^{n}\left(P(t_{i-1}) - P(t_i)\right)$$

$$r \cdot \sum_{i=1}^{n}\phi(t_{i-1}, t_{i})\cdot P(t_i) = P(t_{0}) - P(t_n)$$

Aislamos el último flujo de la pata fija:

$$r \cdot \left[\sum_{i=1}^{n-1}\phi(t_{i-1}, t_{i})\cdot P(t_i)\right] + \phi(t_{n-1}, t_{n})\cdot P(t_n)= P(t_{0}) - P(t_n)$$

Finalmente despejamos la incognita:

$$ r \cdot \left[\sum_{i=1}^{n-1}\phi(t_{i-1}, t_{i})\cdot P(t_i)\right] + \phi(t_{n-1}, t_{n})\cdot P(t_n)= P(t_{0}) - P(t_n)$$
