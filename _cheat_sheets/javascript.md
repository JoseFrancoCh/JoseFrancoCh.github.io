---
title: JavaScript
---

JavaScript es un lenguaje de programación dinámico y esencial para el desarrollo web, usado para añadir 
interactividad a páginas con manipulación del DOM, eventos y lógica del lado del cliente. 
Esta es una referencia rápida con los conceptos y estructuras más esenciales de JavaScript, 
organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando                     | Descripción                               |
|--------------------------------------|-------------------------------------------|
| `<script src="archivo.js"></script>` | Incluye un archivo JS en HTML.            |
| `console.log("Hola")`                | Imprime en la consola del navegador.      |
| `// Comentario`                      | Comentario de una línea.                  |
| `/* Comentario */`                   | Comentario multilínea.                    |
| `alert("Mensaje")`                   | Muestra un mensaje emergente.             |
| `typeof variable`                    | Devuelve el tipo de dato de una variable. |

---

## Variables y tipos de datos

| Concepto/Comando | Descripción                                   |
|------------------|-----------------------------------------------|
| `var x = 10;`    | Declara una variable (ámbito función, hoist). |
| `let y = 20;`    | Declara una variable (ámbito bloque, ES6).    |
| `const z = 30;`  | Declara una constante (no reasignable, ES6).  |
| `number`         | Tipo de dato numérico (ej. `5`, `3.14`).      |
| `string`         | Tipo de dato texto (ej. `"hola"`, `'mundo'`). |
| `boolean`        | Tipo de dato lógico (`true`, `false`).        |
| `null`           | Valor nulo intencional.                       |
| `undefined`      | Variable declarada pero sin valor asignado.   |

---

## Operadores básicos

| Operador           | Descripción                                              |
|--------------------|----------------------------------------------------------|
| `+`, `-`, `*`, `/` | Suma, resta, multiplicación, división.                   |
| `%`                | Módulo (resto de la división).                           |
| `++`, `--`         | Incremento y decremento.                                 |
| `==`, `!=`         | Comparación de igualdad/diferencia (conversión de tipo). |
| `===`, `!==`       | Comparación estricta (sin conversión de tipo).           |
| `&&`, `!`          | Operadores lógicos: y, no.                               |

---

## Control de flujo

| Concepto/Comando                 | Descripción                                |
|----------------------------------|--------------------------------------------|
| `if (condicion) {}`              | Condicional básico.                        |
| `else if (condicion) {}`         | Condicional alternativo.                   |
| `else {}`                        | Caso por defecto.                          |
| `for (let i = 0; i < 5; i++) {}` | Bucle for con contador.                    |
| `while (condicion) {}`           | Bucle mientras la condición sea verdadera. |
| `switch (valor) { case 1: }`     | Selección múltiple basada en valores.      |
| `break;`                         | Sale del bucle o caso actual.              |

---

## Funciones

| Concepto/Comando                           | Descripción                           |
|--------------------------------------------|---------------------------------------|
| `function nombre(param) { return param; }` | Define una función tradicional.       |
| `const nombre = (param) => param;`         | Función flecha (arrow function, ES6). |
| `nombre(arg);`                             | Llama a una función con un argumento. |
| `function suma(a, b = 10) {}`              | Parámetro con valor por defecto.      |
| `const obj = { metodo() {} };`             | Método dentro de un objeto (ES6).     |

---

## Arreglos (Arrays)

| Concepto/Comando                    | Descripción                                         |
|-------------------------------------|-----------------------------------------------------|
| `let arr = [1, 2, 3];`              | Declara un arreglo.                                 |
| `arr.push(4);`                      | Añade un elemento al final.                         |
| `arr.pop();`                        | Elimina y devuelve el último elemento.              |
| `arr.length`                        | Devuelve la longitud del arreglo.                   |
| `arr.map(x => x * 2);`              | Aplica una función a cada elemento (nuevo arreglo). |
| `arr.filter(x => x > 1);`           | Filtra elementos según una condición.               |
| `arr.forEach(x => console.log(x));` | Ejecuta una función por cada elemento.              |

---

## Objetos

| Concepto/Comando                | Descripción                          |
|---------------------------------|--------------------------------------|
| `let obj = { clave: "valor" };` | Declara un objeto.                   |
| `obj.clave` o `obj["clave"]`    | Accede a una propiedad.              |
| `obj.nueva = "dato";`           | Añade una nueva propiedad.           |
| `delete obj.clave;`             | Elimina una propiedad.               |
| `Object.keys(obj);`             | Devuelve un arreglo con las claves.  |
| `Object.values(obj);`           | Devuelve un arreglo con los valores. |

---

## Manipulación del DOM

| Concepto/Comando                      | Descripción                                      |
|---------------------------------------|--------------------------------------------------|
| `document.getElementById("id")`       | Selecciona un elemento por su ID.                |
| `document.querySelector(".clase")`    | Selecciona el primer elemento por selector CSS.  |
| `document.querySelectorAll(".clase")` | Selecciona todos los elementos por selector CSS. |
| `elem.innerHTML = "texto";`           | Cambia el contenido HTML de un elemento.         |
| `elem.style.color = "red";`           | Cambia una propiedad CSS del elemento.           |
| `elem.addEventListener("click", fn);` | Añade un evento (ej. clic) al elemento.          |

---

## Manejo de errores

| Concepto/Comando                    | Descripción                                     |
|-------------------------------------|-------------------------------------------------|
| `try { /* código */ } catch (e) {}` | Captura errores en un bloque.                   |
| `throw new Error("Mensaje");`       | Lanza un error personalizado.                   |
| `finally {}`                        | Ejecuta código después de `try/catch`, siempre. |

---

## Comandos avanzados: Promesas y async/await

| Concepto/Comando                              | Descripción                                       |
|-----------------------------------------------|---------------------------------------------------|
| `new Promise((resolve, reject) => {})`        | Crea una promesa (ES6).                           |
| `promise.then(result => {}).catch(err => {})` | Maneja el resultado o error de una promesa.       |
| `async function fn() {}`                      | Define una función asíncrona (ES8).               |
| `await promesa;`                              | Pausa ejecución hasta que la promesa se resuelva. |
| `fetch("url").then(res => res.json())`        | Realiza una solicitud HTTP (API).                 |

---

## Comandos avanzados: Arrays y objetos (ES6+)

| Concepto/Comando                          | Descripción                                 |
|-------------------------------------------|---------------------------------------------|
| `const [a, b] = [1, 2];`                  | Desestructuración de arreglo.               |
| `const { clave } = obj;`                  | Desestructuración de objeto.                |
| `arr.reduce((acc, val) => acc + val, 0);` | Reduce un arreglo a un solo valor.          |
| `...arr`                                  | Operador spread (expande arreglo u objeto). |
| `{ ...obj, nueva: "valor" }`              | Copia y extiende un objeto.                 |

---

## Comandos avanzados: Clases (ES6)

| Concepto/Comando                     | Descripción                             |
|--------------------------------------|-----------------------------------------|
| `class MiClase { constructor() {} }` | Define una clase.                       |
| `method() {}`                        | Define un método en la clase.           |
| `extends SuperClase`                 | Hereda de otra clase.                   |
| `super()`                            | Llama al constructor de la clase padre. |
| `static metodo() {}`                 | Define un método estático.              |

---

## Comandos avanzados: Módulos (ES6)

| Concepto/Comando                         | Descripción                      |
|------------------------------------------|----------------------------------|
| `export const nombre = valor;`           | Exporta una variable o función.  |
| `import { nombre } from './archivo.js';` | Importa desde otro archivo.      |
| `export default funcion;`                | Exporta un valor predeterminado. |
| `import funcion from './archivo.js';`    | Importa el valor predeterminado. |

