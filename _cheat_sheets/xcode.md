---
title: XCode
---

Xcode es el entorno de desarrollo integrado (IDE) oficial de Apple, utilizado para crear aplicaciones 
para iOS, macOS, watchOS y tvOS con lenguajes como Swift y Objective-C. Incluye herramientas como
simuladores y un editor gráfico para interfaces. Esta es una referencia rápida con los comandos y 
atajos más esenciales de Xcode, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando         | Descripción                                          |
|--------------------------|------------------------------------------------------|
| `xcode-select --install` | Instala las herramientas de línea de comandos (CLI). |
| `xcodebuild`             | Compila un proyecto desde la terminal.               |
| `open archivo.xcodeproj` | Abre un proyecto en Xcode desde la terminal.         |
| `Cmd + N`                | Crea un nuevo archivo.                               |
| `Cmd + Shift + O`        | Abre rápidamente un archivo (Quick Open).            |
| `Cmd + B`                | Compila el proyecto (Build).                         |

---

## Navegación en el editor

| Atajo/Comando    | Descripción                                   |
|------------------|-----------------------------------------------|
| `Cmd + 0`        | Muestra/esconde el Navigator (izquierda).     |
| `Cmd + Opt + 0`  | Muestra/esconde el Inspector (derecha).       |
| `Ctrl + 6`       | Abre el menú de símbolos (jump bar).          |
| `Cmd + Click`    | Salta a la definición de una función/clase.   |
| `Opt + Click`    | Muestra la documentación rápida (Quick Help). |
| `Cmd + Ctrl + J` | Salta a la línea seleccionada en el jump bar. |
| `Cmd + L`        | Salta a una línea específica.                 |

---

## Edición de código

| Atajo/Comando     | Descripción                                      |
|-------------------|--------------------------------------------------|
| `Cmd + /`         | Comenta o descomenta líneas seleccionadas.       |
| `Ctrl + I`        | Reformatea (indentación) el código seleccionado. |
| `Cmd + ]`         | Indenta a la derecha.                            |
| `Cmd + [`         | Indenta a la izquierda.                          |
| `Cmd + D`         | Duplica la línea o selección actual.             |
| `Cmd + Shift + F` | Busca en todo el proyecto (Find in Project).     |

---

## Depuración (Debugging)

| Atajo/Comando   | Descripción                           |
|-----------------|---------------------------------------|
| `Cmd + R`       | Compila y ejecuta la app (Run).       |
| `Cmd + .`       | Detiene la ejecución de la app.       |
| `Cmd + Y`       | Activa/desactiva breakpoints.         |
| `F6`            | Avanza al siguiente paso (Step Over). |
| `F7`            | Entra en una función (Step Into).     |
| `F8`            | Sale de una función (Step Out).       |
| `Cmd + Opt + B` | Muestra todos los breakpoints.        |

---

## Interfaz gráfica (Interface Builder)

| Atajo/Comando       | Descripción                                     |
|---------------------|-------------------------------------------------|
| `Cmd + Shift + L`   | Abre la biblioteca de objetos (Object Library). |
| `Cmd + Opt + Enter` | Abre el Assistant Editor (vista dividida).      |
| `Ctrl + Arrastrar`  | Crea una conexión (IBOutlet o IBAction).        |
| `Cmd + =`           | Ajusta el tamaño al contenido (Size to Fit).    |
| `Opt + Cmd + 0`     | Muestra el Inspector de atributos.              |

---

## Gestión de proyectos

| Atajo/Comando         | Descripción                                   |
|-----------------------|-----------------------------------------------|
| `Cmd + 1` a `Cmd + 9` | Cambia entre pestañas del Navigator.          |
| `Cmd + Shift + K`     | Limpia el build (Clean Build Folder).         |
| `Cmd + Shift + J`     | Selecciona el archivo actual en el Navigator. |
| `Cmd + Shift + Y`     | Muestra/esconde la consola de depuración.     |
| `Cmd + T`             | Abre una nueva pestaña en Xcode.              |

---

## Pruebas (Testing)

| Atajo/Comando          | Descripción                                       |
|------------------------|---------------------------------------------------|
| `Cmd + U`              | Ejecuta todas las pruebas (Unit/UI Tests).        |
| `Cmd + Opt + U`        | Ejecuta pruebas específicas en el archivo actual. |
| `Ctrl + Opt + Cmd + G` | Repite la última prueba ejecutada.                |
| `Cmd + Shift + U`      | Muestra el Test Navigator.                        |

---

## Control de versiones (Git integrado)

| Atajo/Comando           | Descripción                           |
|-------------------------|---------------------------------------|
| `Cmd + Opt + C`         | Realiza un commit desde Xcode.        |
| `Cmd + Opt + Shift + C` | Muestra el historial de commits.      |
| `Cmd + Opt + Shift + D` | Compara cambios en el archivo actual. |
| `Cmd + 2`               | Abre el Source Control Navigator.     |

---

## Comandos avanzados: Refactorización

| Atajo/Comando          | Descripción                                                  |
|------------------------|--------------------------------------------------------------|
| `Ctrl + Cmd + E`       | Renombra una variable en todo el ámbito (Refactor > Rename). |
| `Ctrl + Cmd + Opt + E` | Extrae código a una función (Refactor > Extract).            |
| `Cmd + Opt + /`        | Genera documentación automática (Swift).                     |

---

## Comandos avanzados: Simulador

| Atajo/Comando            | Descripción                                       |
|--------------------------|---------------------------------------------------|
| `Cmd + Shift + H`        | Vuelve a la pantalla de inicio del simulador.     |
| `Cmd + 1` a `Cmd + 5`    | Cambia el tamaño del simulador (100%, 75%, etc.). |
| `Cmd + S`                | Toma una captura de pantalla del simulador.       |
| `Cmd + R` (en simulador) | Rota el simulador.                                |

---

## Comandos avanzados: Productividad

| Atajo/Comando                 | Descripción                                        |
|-------------------------------|----------------------------------------------------|
| `Cmd + Shift + O`             | Busca y abre rápidamente cualquier archivo.        |
| `Cmd + Shift + D`             | Abre la documentación de Xcode.                    |
| `Cmd + Ctrl + Espacio`        | Abre el selector de emojis y símbolos.             |
| `Cmd + Opt + Shift + [` o `]` | Cambia entre archivos .h/.m o .swift relacionados. |

---

## Personalización

| Concepto/Comando                     | Descripción                                                           |
|--------------------------------------|-----------------------------------------------------------------------|
| `Xcode > Preferences > Key Bindings` | Personaliza atajos de teclado.                                        |
| `Code Snippets Library`              | Añade fragmentos de código reutilizables (arrastrar a la biblioteca). |
| `Behaviors > Edit Behaviors`         | Configura acciones personalizadas (ej. al compilar).                  |

