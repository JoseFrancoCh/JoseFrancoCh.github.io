---
layout: single
---

# Convenciones de Conteo de Días

En esta sección nos enfocamos en describir las principales **convenciones de conteo de días**, 
un tema que puede parecer un poco técnico, pero que te prometo hacer súper claro y 
hasta divertido. Imagina que estamos charlando sobre cómo los bancos, las empresas y los 
inversionistas calculan intereses o plazos en contratos financieros como préstamos, bonos o 
derivados. No siempre usan el calendario que conocemos, sino que siguen unas reglas especiales para contar los días. Estas reglas son esenciales para que todo sea justo y consistente, y hoy las vamos a explorar juntas con un estilo que mezcla lo académico y lo conversacional. Además, incluiré las fórmulas de cálculo para cada una y referencias en formato APA por si quieres investigar más. ¿Listo? ¡Aquí vamos!

---

## **¿Qué son las Convenciones de Conteo de Días?**

En el mundo financiero, cuando calculamos intereses o determinamos cuánto tiempo pasa entre dos fechas, necesitamos saber dos cosas básicas: cuántos días hay entre esas fechas y cuántos días tiene el año según las reglas que usemos. Parece simple, pero no siempre se trata de contar días en el calendario como lo harías para planear tus vacaciones. Las **convenciones de conteo de días** son acuerdos estandarizados que definen cómo se hace ese cálculo en contratos financieros. Por ejemplo, a veces se asume que un año tiene 360 días o que cada mes tiene 30 días, aunque en la vida real no sea así. ¿Por qué? Porque esto ayuda a que los cálculos sean uniformes y no haya malentendidos entre las partes.

Piénsalo como un truco práctico que los financieros usan para hablar el mismo idioma. Sin estas convenciones, podrías calcular intereses de una forma y tu banco de otra, ¡y eso sería un desastre! Ahora, vamos a conocer las principales convenciones, con sus fórmulas y ejemplos para que veas cómo funcionan en acción.

---

## **Las Principales Convenciones de Conteo de Días**

Aquí te presento las cinco convenciones más comunes en los derivados financieros. Para cada una, te daré una explicación sencilla, la fórmula matemática que se usa para calcular la fracción de año y un ejemplo práctico. ¡Prepárate para verlo todo clarito!

### **1. Actual/Actual (ACT/ACT)**

- **¿Qué es?**: Esta convención es la más realista porque usa el número exacto de días entre dos fechas y el número real de días en el año (365 si no es bisiesto, 366 si lo es). Se usa mucho en bonos del Tesoro de Estados Unidos y algunos swaps de tasas de interés por su precisión.
- **Fórmula**:
  \[
  \text{Fracción de año} = \frac{\text{Número de días entre fechas}}{\text{Número de días en el año}}
  \]
- **Ejemplo práctico**: Imagina que prestas dinero del 1 de enero de 2024 al 1 de julio de 2024. El 2024 no es bisiesto, así que el año tiene 365 días. Entre esas fechas hay 182 días (contando del 1 de enero al 30 de junio, más 1 día de julio). Entonces:
  \[
  \text{Fracción de año} = \frac{182}{365} \approx 0.4986
  \]
  Esto significa que pasó casi medio año. Fácil, ¿verdad?

**Dato extra**: Hay variantes como *ACT/ACT ISDA*, pero la idea principal es siempre usar los días reales.

### **2. Actual/360 (ACT/360)**

- **¿Qué es?**: Aquí también contamos los días reales entre dos fechas, pero asumimos que el año tiene 360 días. Esto hace que cada día "valga" un poquito más en los cálculos. Es muy común en mercados de dinero, como préstamos a corto plazo o eurodólares.
- **Fórmula**:
  \[
  \text{Fracción de año} = \frac{\text{Número de días entre fechas}}{360}
  \]
- **Ejemplo práctico**: Supongamos que tienes un préstamo por 90 días. La fracción de año sería:
  \[
  \text{Fracción de año} = \frac{90}{360} = 0.25
  \]
  Es decir, un cuarto de año según esta convención, aunque en un año real de 365 días, 90 días sería menos que eso. ¡Simple y directo!

**Curiosidad**: Esta convención es un favorito en Europa porque facilita los cálculos rápidos.

### **3. Actual/365 Fixed (ACT/365)**

- **¿Qué es?**: Parecida a ACT/360, pero aquí el año siempre tiene 365 días, sin importar si es bisiesto o no. Es popular en el Reino Unido y en algunos bonos porque es consistente y fácil de usar.
- **Fórmula**:
  \[
  \text{Fracción de año} = \frac{\text{Número de días entre fechas}}{365}
  \]
- **Ejemplo práctico**: Si tienes un período de 182 días (como del 1 de enero al 1 de julio en un año no bisiesto), calculamos:
  \[
  \text{Fracción de año} = \frac{182}{365} \approx 0.4986
  \]
  Incluso en un año bisiesto, seguimos usando 365 días, lo que hace todo más predecible.

**Nota**: Es genial para contratos largos porque no tienes que ajustar por años bisiestos.

### **4. 30/360 (o 360/360)**

- **¿Qué es?**: Esta convención simplifica las cosas asumiendo que cada mes tiene 30 días y el año tiene 360 días. No es tan precisa como las otras, pero es súper práctica para bonos corporativos y algunos swaps donde se quieren pagos regulares y predecibles.
- **Fórmula**:
  \[
  \text{Fracción de año} = \frac{[360 \times (\text{Año}_2 - \text{Año}_1) + 30 \times (\text{Mes}_2 - \text{Mes}_1) + (\text{Día}_2 - \text{Día}_1)]}{360}
  \]
  **Ajuste**: Si el día inicial o final es 31, se cambia a 30 (con excepciones menores).
- **Ejemplo práctico**: Calcula el tiempo del 31 de enero de 2025 al 31 de marzo de 2025:
  - Ajustamos 31 de enero a 30 y 31 de marzo a 30.
  - Diferencia: 2 meses (febrero y marzo), días de 30 a 30 (0 días adicionales).
  - Entonces:
  \[
  \text{Fracción de año} = \frac{360 \times 0 + 30 \times 2 + (30 - 30)}{360} = \frac{60}{360} = 0.1667
  \]
  ¡Dos meses exactos según esta regla!

**Ventaja**: Hace que los cálculos sean uniformes y fáciles de planificar.

### **5. 30E/360 (European 30/360)**

- **¿Qué es?**: Muy parecida a 30/360, pero más estricta: si una fecha es 31, siempre se ajusta a 30, sin excepciones. Es típica en Europa, especialmente en mercados de bonos.
- **Fórmula**: Igual que 30/360:
  \[
  \text{Fracción de año} = \frac{[360 \times (\text{Año}_2 - \text{Año}_1) + 30 \times (\text{Mes}_2 - \text{Mes}_1) + (\text{Día}_2 - \text{Día}_1)]}{360}
  \]
- **Ejemplo práctico**: Del 31 de mayo de 2025 al 31 de julio de 2025:
  - Ambas fechas se ajustan a 30.
  - Diferencia: 2 meses, días 30 a 30.
  - Cálculo:
  \[
  \text{Fracción de año} = \frac{60}{360} = 0.1667
  \]

**Dato curioso**: Su nombre viene de su uso extendido en Europa, ¡y es tan estricta como suena!

---

## **¿Cómo se Usan Estas Convenciones en la Vida Real?**

En los contratos financieros, estas convenciones se escriben con una notación clara, como **ACT/360** o **30/360**. El numerador (ACT o 30) dice cómo contamos los días entre fechas, y el denominador (360, 365 o ACT) indica cuántos días tiene el año según la regla. Esta fracción de año luego se usa en fórmulas como la del interés simple:

\[
I = P \times r \times t
\]

Donde:
- \(I\): Interés.
- \(P\): Monto principal.
- \(r\): Tasa de interés anual.
- \(t\): Fracción de año según la convención.

**Ejemplo real**: Supón que prestas $10,000 al 5% anual del 1 de enero de 2025 al 1 de julio de 2025 (181 días):
- **Con ACT/365**:
  \[
  t = \frac{181}{365} \approx 0.4959 \quad \rightarrow \quad I = 10,000 \times 0.05 \times 0.4959 \approx 247.95
  \]
- **Con ACT/360**:
  \[
  t = \frac{181}{360} \approx 0.5028 \quad \rightarrow \quad I = 10,000 \times 0.05 \times 0.5028 \approx 251.40
  \]

¡Mira cómo cambia el interés según la convención! Por eso es tan importante elegir la correcta y dejarlo claro en el contrato.

---

## **Para Cerrar**

Las convenciones de conteo de días son como las reglas de un juego financiero: aseguran que todos jueguen limpio y con las mismas cartas. Cada una tiene su lugar dependiendo del instrumento financiero o el mercado, y entenderlas te da una ventaja enorme si trabajas con dinero o inversiones. Espero que este paseo por el tema te haya aclarado las cosas y hasta te haya sacado una sonrisa. Si quieres saber más, echa un vistazo a las referencias abajo. ¡Gracias por leerme!

---

## **Referencias**

Hull, J. C. (2018). *Options, Futures, and Other Derivatives* (10th ed.). Pearson.  

International Swaps and Derivatives Association. (2006). *2006 ISDA Definitions*. https://www.isda.org  

Fabozzi, F. J. (2012). *Bond Markets, Analysis, and Strategies* (8th ed.). Prentice Hall.  

Association Française des Banques. (s.f.). *AFB Master Agreement for Financial Transactions*. https://www.afb.fr  

---