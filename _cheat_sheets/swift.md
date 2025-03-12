---
title: Swift
---

Swift es un lenguaje de programación creado por Apple, rápido y seguro, diseñado para aplicaciones iOS,
macOS, watchOS y tvOS. Combina potencia con una sintaxis clara, siendo ideal para desarrolladores 
de apps modernas. Esta es una referencia rápida con los conceptos y estructuras más esenciales de 
Swift, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando      | Descripción                                       |
|-----------------------|---------------------------------------------------|
| `swift --version`     | Muestra la versión de Swift instalada (terminal). |
| `swift archivo.swift` | Ejecuta un archivo Swift desde la terminal.       |
| `// Comentario`       | Comentario de una línea.                          |
| `/* Comentario */`    | Comentario multilínea.                            |
| `import UIKit`        | Importa un framework (ej. UIKit para iOS).        |
| `print("Hola")`       | Imprime en consola.                               |

---

## Variables y tipos de datos

| Concepto/Comando                | Descripción                                       |
|---------------------------------|---------------------------------------------------|
| `var x = 10`                    | Declara una variable mutable (entero inferido).   |
| `let y = 3.14`                  | Declara una constante inmutable (doble inferido). |
| `var z: Int = 5`                | Declara una variable con tipo explícito.          |
| `var texto = "Hola"`            | Declara una cadena (String).                      |
| `var lista = [1, 2, 3]`         | Declara un arreglo (Array).                       |
| `var dic = ["clave": "valor"]`  | Declara un diccionario (Dictionary).              |
| `var conjunto = Set([1, 2, 3])` | Declara un conjunto (Set, sin duplicados).        |

---

## Operadores básicos

| Operador                         | Descripción                                         |
|----------------------------------|-----------------------------------------------------|
| `+`, `-`, `*`, `/`               | Suma, resta, multiplicación, división.              |
| `%`                              | Módulo (resto de la división).                      |
| `==`, `!=`, `<`, `>`, `<=`, `>=` | Comparaciones: igual, diferente, menor, mayor, etc. |
| `&&`, `!`                        | Operadores lógicos: y, no.                          |
| `+=`, `-=`, `*=`                 | Operadores de asignación compuesta.                 |

---

## Control de flujo

| Concepto/Comando           | Descripción                                         |
|----------------------------|-----------------------------------------------------|
| `if condicion {}`          | Condicional básico.                                 |
| `else if condicion {}`     | Condicional alternativo.                            |
| `else {}`                  | Caso por defecto.                                   |
| `for i in 0..<5 {}`        | Bucle for con rango (0 a 4).                        |
| `for item in lista {}`     | Bucle for sobre una colección.                      |
| `while condicion {}`       | Bucle mientras la condición sea verdadera.          |
| `switch valor { case 1: }` | Selección múltiple con casos (no requiere `break`). |
| `break`                    | Sale del bucle o caso actual.                       |
| `continue`                 | Salta a la siguiente iteración del bucle.           |

---

## Opcionales (Optionals)

| Concepto/Comando                      | Descripción                                                |
|---------------------------------------|------------------------------------------------------------|
| `var x: Int? = nil`                   | Declara un opcional que puede ser `nil`.                   |
| `if let valor = x {}`                 | Desenvuelve un opcional de forma segura (unwrapping).      |
| `x ?? 0`                              | Proporciona un valor por defecto si es `nil`.              |
| `x!`                                  | Fuerza el desempaquetado de un opcional (riesgo de crash). |
| `guard let valor = x else { return }` | Salida temprana si el opcional es `nil`.                   |

---

## Funciones

| Concepto/Comando                                    | Descripción                                 |
|-----------------------------------------------------|---------------------------------------------|
| `func suma(a: Int, b: Int) -> Int { return a + b }` | Define una función con retorno.             |
| `func saludar() { print("Hola") }`                  | Función sin retorno.                        |
| `func nombre(_ param: String)`                      | Omite la etiqueta del parámetro al llamar.  |
| `func valor(def: Int = 10)`                         | Parámetro con valor por defecto.            |
| `@discardableResult func x() -> Int`                | Permite ignorar el resultado de la función. |

---

## Arreglos y colecciones

| Concepto/Comando          | Descripción                                    |
|---------------------------|------------------------------------------------|
| `lista.append(4)`         | Añade un elemento al final del arreglo.        |
| `lista.remove(at: 0)`     | Elimina un elemento en el índice especificado. |
| `lista.count`             | Devuelve el número de elementos.               |
| `dic["clave"] = "nuevo"`  | Añade o actualiza un valor en el diccionario.  |
| `conjunto.insert(4)`      | Añade un elemento al conjunto.                 |
| `lista.filter { $0 > 2 }` | Filtra elementos según una condición.          |

---

## Clases y estructuras

| Concepto/Comando                                          | Descripción                    |
|-----------------------------------------------------------|--------------------------------|
| `class MiClase { var x = 0 }`                             | Define una clase (referencia). |
| `struct MiStruct { var x = 0 }`                           | Define una estructura (valor). |
| `init(x: Int) { self.x = x }`                             | Constructor (inicializador).   |
| `deinit {}`                                               | Destructor (solo para clases). |
| `var prop: Int { get { return x } set { x = newValue } }` | Propiedad computada.           |

---

## Protocolos y herencia

| Concepto/Comando                             | Descripción                                |
|----------------------------------------------|--------------------------------------------|
| `protocol MiProtocolo { func metodo() }`     | Define un protocolo.                       |
| `class Subclase: Superclase, MiProtocolo {}` | Herencia y adopción de protocolo.          |
| `override func metodo() {}`                  | Sobrescribe un método de la superclase.    |
| `extension MiClase { func nuevo() {} }`      | Añade funcionalidad a una clase existente. |

---

## Manejo de errores

| Concepto/Comando                             | Descripción                            |
|----------------------------------------------|----------------------------------------|
| `enum MiError: Error { case caso }`          | Define un tipo de error personalizado. |
| `func lanza() throws { throw MiError.caso }` | Función que puede lanzar un error.     |
| `do { try lanza() } catch {}`                | Captura errores con `do-catch`.        |
| `try? lanza()`                               | Convierte el resultado en un opcional. |

---

## Comandos avanzados: Cierres (Closures)

| Concepto/Comando                              | Descripción                                    |
|-----------------------------------------------|------------------------------------------------|
| `{ (param: Int) -> Int in return param + 1 }` | Define un cierre (closure).                    |
| `lista.map { $0 * 2 }`                        | Aplica un cierre a cada elemento de una lista. |
| `@escaping`                                   | Indica que un cierre puede escapar del ámbito. |
| `[weak self]`                                 | Evita ciclos de retención en cierres.          |

---

## Comandos avanzados: Concurrencia (Swift 5.5+)

| Concepto/Comando              | Descripción                               |
|-------------------------------|-------------------------------------------|
| `async func tarea() {}`       | Define una función asíncrona.             |
| `await tarea()`               | Llama a una función asíncrona.            |
| `Task { await tarea() }`      | Inicia una tarea asíncrona.               |
| `actor MiActor { var x = 0 }` | Define un actor para concurrencia segura. |

---

## Comandos avanzados: Generics

| Concepto/Comando                  | Descripción                                                  |
|-----------------------------------|--------------------------------------------------------------|
| `func suma<T>(a: T, b: T) -> T`   | Función genérica (requiere conformidad a protocolo si suma). |
| `struct Caja<T> { var valor: T }` | Estructura genérica.                                         |
| `where T: Equatable`              | Restringe el tipo genérico a un protocolo.                   |

---

## Comandos avanzados: Tuplas y patrones

| Concepto/Comando                    | Descripción                              |
|-------------------------------------|------------------------------------------|
| `let tupla = (1, "Hola")`           | Declara una tupla.                       |
| `let (x, y) = tupla`                | Descompone una tupla en variables.       |
| `switch tupla { case (1, let s): }` | Usa coincidencia de patrones con tuplas. |

