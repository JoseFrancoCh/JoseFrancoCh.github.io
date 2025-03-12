---
title: Python
---

Python es un lenguaje de programación versátil, legible y de alto nivel, ampliamente usado en 
desarrollo web, ciencia de datos, automatización y más, gracias a su simplicidad y extensa 
biblioteca estándar. Esta es una referencia rápida con los conceptos y comandos más esenciales 
de Python, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando         | Descripción                                              |
|--------------------------|----------------------------------------------------------|
| `python --version`       | Muestra la versión de Python instalada (en la terminal). |
| `python archivo.py`      | Ejecuta un archivo Python desde la terminal.             |
| `# Comentario`           | Añade un comentario de una línea.                        |
| `"""Texto multilínea"""` | Comentario o cadena multilínea (docstring).              |

---

## Variables y tipos de datos

| Concepto/Comando           | Descripción                                |
|----------------------------|--------------------------------------------|
| `x = 10`                   | Asigna un entero a una variable.           |
| `y = 3.14`                 | Asigna un flotante a una variable.         |
| `texto = "Hola"`           | Asigna una cadena (string) a una variable. |
| `lista = [1, 2, 3]`        | Crea una lista.                            |
| `tupla = (1, 2, 3)`        | Crea una tupla (inmutable).                |
| `dic = {"clave": "valor"}` | Crea un diccionario.                       |
| `conjunto = {1, 2, 3}`     | Crea un conjunto (sin duplicados).         |
| `type(x)`                  | Devuelve el tipo de dato de una variable.  |

---

## Operadores básicos

| Operador                         | Descripción                                         |
|----------------------------------|-----------------------------------------------------|
| `+`, `-`, `*`, `/`               | Suma, resta, multiplicación, división.              |
| `//`                             | División entera (redondea hacia abajo).             |
| `%`                              | Módulo (resto de la división).                      |
| `**`                             | Exponenciación (potencia).                          |
| `==`, `!=`, `<`, `>`, `<=`, `>=` | Comparaciones: igual, diferente, menor, mayor, etc. |
| `and`, `or`, `not`               | Operadores lógicos: y, o, no.                       |

---

## Control de flujo

| Concepto/Comando     | Descripción                                         |
|----------------------|-----------------------------------------------------|
| `if condicion:`      | Inicia una condición.                               |
| `elif condicion:`    | Condición alternativa (else if).                    |
| `else:`              | Caso por defecto si no se cumple ninguna condición. |
| `for i in range(5):` | Itera 5 veces (0 a 4).                              |
| `for item in lista:` | Itera sobre los elementos de una lista.             |
| `while condicion:`   | Bucle mientras la condición sea verdadera.          |
| `break`              | Sale del bucle actual.                              |
| `continue`           | Salta a la siguiente iteración del bucle.           |

---

## Funciones

| Concepto/Comando         | Descripción                                   |
|--------------------------|-----------------------------------------------|
| `def mi_funcion(param):` | Define una función con un parámetro.          |
| `return valor`           | Devuelve un valor desde una función.          |
| `def func(*args):`       | Función con número variable de argumentos.    |
| `def func(**kwargs):`    | Función con argumentos clave-valor variables. |
| `lambda x: x + 1`        | Crea una función anónima (lambda).            |

---

## Listas y estructuras de datos

| Concepto/Comando  | Descripción                                       |
|-------------------|---------------------------------------------------|
| `lista.append(x)` | Añade un elemento al final de la lista.           |
| `lista.pop()`     | Elimina y devuelve el último elemento.            |
| `lista.remove(x)` | Elimina la primera ocurrencia de `x`.             |
| `lista[0]`        | Accede al primer elemento (índice 0).             |
| `lista[1:3]`      | Obtiene un subconjunto (slicing) de índice 1 a 2. |
| `len(lista)`      | Devuelve la longitud de la lista.                 |
| `sorted(lista)`   | Devuelve una nueva lista ordenada.                |

---

## Entrada y salida

| Concepto/Comando          | Descripción                                             |
|---------------------------|---------------------------------------------------------|
| `print("Hola")`           | Imprime un mensaje en la consola.                       |
| `input("Ingresa algo: ")` | Solicita entrada del usuario y la devuelve como string. |
| `f"Hola {variable}"`      | Formatea una cadena con f-strings (Python 3.6+).        |

---

## Manejo de excepciones

| Concepto/Comando            | Descripción                                  |
|-----------------------------|----------------------------------------------|
| `try:`                      | Inicia un bloque para capturar excepciones.  |
| `except Exception as e:`    | Captura una excepción y la almacena en `e`.  |
| `finally:`                  | Ejecuta código siempre, haya o no excepción. |
| `raise ValueError("Error")` | Lanza una excepción personalizada.           |

---

## Módulos y bibliotecas

| Concepto/Comando        | Descripción                                       |
|-------------------------|---------------------------------------------------|
| `import math`           | Importa el módulo `math`.                         |
| `from math import sqrt` | Importa solo la función `sqrt` del módulo `math`. |
| `import mi_archivo`     | Importa un archivo Python personalizado.          |
| `pip install paquete`   | Instala un paquete externo desde la terminal.     |

---

## Comandos avanzados: Comprensiones

| Concepto/Comando              | Descripción                                          |
|-------------------------------|------------------------------------------------------|
| `[x * 2 for x in range(5)]`   | Crea una lista con comprensión (list comprehension). |
| `{x: x**2 for x in range(5)}` | Crea un diccionario con comprensión.                 |
| `{x for x in range(5)}`       | Crea un conjunto con comprensión.                    |

---

## Comandos avanzados: Archivos

| Concepto/Comando                      | Descripción                                      |
|---------------------------------------|--------------------------------------------------|
| `with open("archivo.txt", "r") as f:` | Abre un archivo en modo lectura.                 |
| `with open("archivo.txt", "w") as f:` | Abre un archivo en modo escritura (sobrescribe). |
| `f.read()`                            | Lee todo el contenido del archivo.               |
| `f.write("Texto")`                    | Escribe en el archivo.                           |
| `f.readlines()`                       | Lee todas las líneas como una lista.             |

---

## Comandos avanzados: Clases y OOP

| Concepto/Comando             | Descripción                                  |
|------------------------------|----------------------------------------------|
| `class MiClase:`             | Define una clase.                            |
| `def __init__(self, param):` | Constructor de la clase con parámetros.      |
| `self.atributo = valor`      | Define un atributo de instancia.             |
| `@classmethod`               | Decorador para métodos de clase.             |
| `@staticmethod`              | Decorador para métodos estáticos.            |
| `class Hija(Padre):`         | Define una clase hija que hereda de `Padre`. |

---

## Comandos avanzados: Funciones útiles

| Concepto/Comando      | Descripción                                              |
|-----------------------|----------------------------------------------------------|
| `map(func, lista)`    | Aplica una función a cada elemento de una lista.         |
| `filter(func, lista)` | Filtra elementos de una lista según una condición.       |
| `zip(lista1, lista2)` | Combina dos listas en pares.                             |
| `enumerate(lista)`    | Devuelve índices y valores al iterar una lista.          |
| `any([cond1, cond2])` | Devuelve `True` si alguna condición es verdadera.        |
| `all([cond1, cond2])` | Devuelve `True` si todas las condiciones son verdaderas. |

