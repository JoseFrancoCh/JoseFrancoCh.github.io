---
title: C++
---

C++ es un lenguaje de programación potente y versátil, conocido por su eficiencia y control a bajo nivel, 
ampliamente usado en desarrollo de software, videojuegos y sistemas embebidos. Combina programación 
orientada a objetos, genérica y procedural. Esta es una referencia rápida con los conceptos y estructuras 
más esenciales de C++, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando              | Descripción                                       |
|-------------------------------|---------------------------------------------------|
| `#include <iostream>`         | Incluye la librería estándar para entrada/salida. |
| `int main() { return 0; }`    | Estructura mínima de un programa C++.             |
| `g++ archivo.cpp -o programa` | Compila un archivo C++ en un ejecutable.          |
| `./programa`                  | Ejecuta el programa compilado (Linux/Mac).        |
| `// Comentario`               | Comentario de una línea.                          |
| `/* Comentario */`            | Comentario multilínea.                            |

---

## Variables y tipos de datos

| Concepto/Comando      | Descripción                                        |
|-----------------------|----------------------------------------------------|
| `int x = 10;`         | Declara un entero.                                 |
| `float y = 3.14;`     | Declara un flotante.                               |
| `double z = 3.14159;` | Declara un doble precisión.                        |
| `char c = 'A';`       | Declara un carácter.                               |
| `bool flag = true;`   | Declara un booleano (`true` o `false`).            |
| `string s = "Hola";`  | Declara una cadena (requiere `#include <string>`). |
| `auto x = 10;`        | Deduce el tipo automáticamente (C++11).            |

---

## Operadores básicos

| Operador                         | Descripción                                         |
|----------------------------------|-----------------------------------------------------|
| `+`, `-`, `*`, `/`               | Suma, resta, multiplicación, división.              |
| `%`                              | Módulo (resto de la división).                      |
| `++`, `--`                       | Incremento y decremento.                            |
| `==`, `!=`, `<`, `>`, `<=`, `>=` | Comparaciones: igual, diferente, menor, mayor, etc. |
| `&&`,  `!`                       | Operadores lógicos: y, no.                          |
| `&`, `^`, `~`                    | Operadores a nivel de bits: AND, XOR, NOT.          |

---

## Entrada y salida

| Concepto/Comando        | Descripción                                                |
|-------------------------|------------------------------------------------------------|
| `std::cout << "Hola";`  | Imprime en consola (requiere `<iostream>`).                |
| `std::cin >> variable;` | Lee entrada del usuario.                                   |
| `std::endl`             | Añade un salto de línea en `cout`.                         |
| `using namespace std;`  | Evita escribir `std::` (opcional, cuidado con conflictos). |

---

## Control de flujo

| Concepto/Comando                 | Descripción                                |
|----------------------------------|--------------------------------------------|
| `if (condicion) {}`              | Condicional básico.                        |
| `else if (condicion) {}`         | Condicional alternativo.                   |
| `else {}`                        | Caso por defecto.                          |
| `for (int i = 0; i < 5; i++) {}` | Bucle for con contador.                    |
| `while (condicion) {}`           | Bucle mientras la condición sea verdadera. |
| `do {} while (condicion);`       | Bucle que se ejecuta al menos una vez.     |
| `switch (variable) { case 1: }`  | Selección múltiple basada en valores.      |
| `break;`                         | Sale del bucle o caso actual.              |

---

## Funciones

| Concepto/Comando                           | Descripción                                            |
|--------------------------------------------|--------------------------------------------------------|
| `int suma(int a, int b) { return a + b; }` | Define una función con parámetros y retorno.           |
| `void funcion() {}`                        | Función sin retorno.                                   |
| `int main(int argc, char* argv[])`         | Función principal con argumentos de línea de comandos. |
| `inline int func() {}`                     | Sugiere al compilador que inlinee la función.          |
| `int& ref(int& x) { return x; }`           | Función que retorna una referencia.                    |

---

## Arreglos y contenedores

| Concepto/Comando                           | Descripción                            |
|--------------------------------------------|----------------------------------------|
| `int arr[5] = {1, 2, 3, 4, 5};`            | Declara un arreglo estático.           |
| `#include <vector>` `std::vector<int> v;`  | Declara un vector dinámico (C++ STL).  |
| `v.push_back(10);`                         | Añade un elemento al final del vector. |
| `v.pop_back();`                            | Elimina el último elemento del vector. |
| `v.size();`                                | Devuelve el tamaño del vector.         |
| `#include <array>` `std::array<int, 5> a;` | Arreglo de tamaño fijo (C++11).        |

---

## Punteros y referencias

| Concepto/Comando        | Descripción                                             |
|-------------------------|---------------------------------------------------------|
| `int* ptr = &variable;` | Declara un puntero y asigna la dirección de `variable`. |
| `*ptr`                  | Accede al valor apuntado por el puntero.                |
| `int& ref = variable;`  | Declara una referencia (alias de `variable`).           |
| `new int(5)`            | Asigna memoria dinámica para un entero.                 |
| `delete ptr;`           | Libera memoria asignada dinámicamente.                  |

---

## Clases y OOP

| Concepto/Comando                    | Descripción                                  |
|-------------------------------------|----------------------------------------------|
| `class MiClase { public: int x; };` | Define una clase simple.                     |
| `MiClase() { x = 0; }`              | Constructor por defecto.                     |
| `~MiClase() {}`                     | Destructor.                                  |
| `private:`                          | Miembros accesibles solo dentro de la clase. |
| `public:`                           | Miembros accesibles desde fuera.             |
| `class Hija : public Padre {}`      | Herencia pública de una clase base.          |
| `virtual void func() = 0;`          | Método virtual puro (clase abstracta).       |

---

## Manejo de excepciones

| Concepto/Comando                     | Descripción                        |
|--------------------------------------|------------------------------------|
| `try { /* código */ }`               | Bloque para capturar excepciones.  |
| `catch (std::exception& e) {}`       | Captura una excepción estándar.    |
| `throw std::runtime_error("Error");` | Lanza una excepción personalizada. |

---

## Comandos avanzados: STL (Standard Template Library)

| Concepto/Comando                                        | Descripción                             |
|---------------------------------------------------------|-----------------------------------------|
| `#include <algorithm>` `std::sort(v.begin(), v.end());` | Ordena un vector.                       |
| `#include <map>` `std::map<int, string> m;`             | Declara un mapa (clave-valor).          |
| `m[1] = "uno";`                                         | Asigna un valor a una clave en el mapa. |
| `#include <set>` `std::set<int> s;`                     | Declara un conjunto (sin duplicados).   |
| `#include <queue>` `std::queue<int> q;`                 | Declara una cola FIFO.                  |
| `#include <stack>` `std::stack<int> st;`                | Declara una pila LIFO.                  |

---

## Comandos avanzados: Plantillas (Templates)

| Concepto/Comando                                             | Descripción       |
|--------------------------------------------------------------|-------------------|
| `template <typename T>` `T suma(T a, T b) { return a + b; }` | Función genérica. |
| `template <class T>` `class MiClase { T dato; };`            | Clase genérica.   |

---

## Comandos avanzados: Gestión de memoria (C++11+)

| Concepto/Comando                                           | Descripción                                     |
|------------------------------------------------------------|-------------------------------------------------|
| `#include <memory>` `std::unique_ptr<int> up(new int(5));` | Puntero único (libera memoria automáticamente). |
| `std::shared_ptr<int> sp = std::make_shared<int>(5);`      | Puntero compartido (contador de referencias).   |
| `auto`                                                     | Deducción automática de tipos (C++11).          |
| `nullptr`                                                  | Puntero nulo moderno (reemplaza `NULL`).        |

---

## Comandos avanzados: Concurrencia (C++11+)

| Concepto/Comando                           | Descripción                           |
|--------------------------------------------|---------------------------------------|
| `#include <thread>` `std::thread t(func);` | Crea un hilo para ejecutar `func`.    |
| `t.join();`                                | Espera a que el hilo termine.         |
| `#include <mutex>` `std::mutex mtx;`       | Declara un mutex para sincronización. |
| `mtx.lock();` `mtx.unlock();`              | Bloquea y desbloquea el mutex.        |

