---
title: Virtual Studio Code
---

Visual Studio Code (VS Code) es un editor de código fuente ligero y altamente personalizable 
desarrollado por Microsoft, popular entre desarrolladores por su soporte para múltiples 
lenguajes, extensiones y herramientas integradas como Git. Esta es una referencia rápida 
con los comandos y atajos más esenciales de VS Code, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando                             | Descripción                                      |
|----------------------------------------------|--------------------------------------------------|
| `code --version`                             | Muestra la versión de VS Code (terminal).        |
| `code .`                                     | Abre VS Code en el directorio actual (terminal). |
| `Ctrl + N` (Windows/Linux) / `Cmd + N` (Mac) | Crea un nuevo archivo.                           |
| `Ctrl + S` / `Cmd + S`                       | Guarda el archivo actual.                        |
| `Ctrl + Shift + N` / `Cmd + Shift + N`       | Abre una nueva ventana de VS Code.               |
| `Ctrl + B` / `Cmd + B`                       | Muestra/esconde la barra lateral (Sidebar).      |

---

## Navegación en el editor

| Atajo/Comando                          | Descripción                                       |
|----------------------------------------|---------------------------------------------------|
| `Ctrl + P` / `Cmd + P`                 | Busca y abre rápidamente un archivo (Go to File). |
| `Ctrl + Tab` / `Cmd + Tab`             | Cambia entre pestañas abiertas.                   |
| `Ctrl + G` / `Cmd + G`                 | Salta a una línea específica.                     |
| `Ctrl + Shift + O` / `Cmd + Shift + O` | Busca símbolos en el archivo (Go to Symbol).      |
| `Ctrl + Click` / `Cmd + Click`         | Salta a la definición de una función/clase.       |
| `Alt + Left/Right`                     | Navega hacia atrás/adelante en el historial.      |

---

## Edición de código

| Atajo/Comando                          | Descripción                                        |
|----------------------------------------|----------------------------------------------------|
| `Ctrl + /` / `Cmd + /`                 | Comenta o descomenta líneas seleccionadas.         |
| `Alt + Up/Down`                        | Mueve la línea o bloque seleccionado arriba/abajo. |
| `Ctrl + D` / `Cmd + D`                 | Selecciona la siguiente ocurrencia del texto.      |
| `Ctrl + L` / `Cmd + L`                 | Selecciona la línea actual.                        |
| `Ctrl + Shift + F` / `Cmd + Shift + F` | Busca en todo el proyecto (Find in Files).         |
| `Ctrl + H` / `Cmd + H`                 | Reemplaza texto en el archivo actual.              |
| `F12`                                  | Salta a la definición (Go to Definition).          |

---

## Depuración (Debugging)

| Atajo/Comando                            | Descripción                           |
|------------------------------------------|---------------------------------------|
| `F5`                                     | Inicia/continúa la depuración.        |
| `Shift + F5`                             | Detiene la depuración.                |
| `F10`                                    | Avanza al siguiente paso (Step Over). |
| `F11`                                    | Entra en una función (Step Into).     |
| `Shift + F11`                            | Sale de una función (Step Out).       |
| `F9`                                     | Activa/desactiva un breakpoint.       |
| `Ctrl + Shift + F5` / `Cmd + Shift + F5` | Reinicia la depuración.               |

---

## Terminal y ejecución

| Atajo/Comando                          | Descripción                                               |
|----------------------------------------|-----------------------------------------------------------|
| `Ctrl + `` (backtick)` / `Cmd + ``     | Abre/cierra la terminal integrada.                        |
| `Ctrl + Shift + C` / `Cmd + Shift + C` | Abre una terminal externa.                                |
| `Ctrl + Shift + P` / `Cmd + Shift + P` | Abre la paleta de comandos (Command Palette).             |
| `Tasks: Run Task`                      | Ejecuta una tarea definida en `tasks.json`.               |
| `Run Code`                             | Ejecuta el código (requiere extensión, como Code Runner). |

---

## Gestión de archivos y proyectos

| Atajo/Comando                           | Descripción                              |
|-----------------------------------------|------------------------------------------|
| `Ctrl + Shift + E` / `Cmd + Shift + E`  | Muestra/esconde el Explorer (archivos).  |
| `Ctrl + Shift + G` / `Cmd + Shift + G`  | Abre la pestaña de Source Control (Git). |
| `Ctrl + W` / `Cmd + W`                  | Cierra la pestaña actual.                |
| `Ctrl + Shift + T` / `Cmd + Shift + T`  | Reabre la última pestaña cerrada.        |
| `Ctrl + K Ctrl + S` / `Cmd + K Cmd + S` | Abre la configuración de atajos.         |

---

## Control de versiones (Git integrado)

| Atajo/Comando                              | Descripción                                   |
|--------------------------------------------|-----------------------------------------------|
| `Ctrl + Shift + G G` / `Cmd + Shift + G G` | Abre la vista de Git.                         |
| `Ctrl + Enter` / `Cmd + Enter`             | Realiza un commit desde el mensaje de commit. |
| `Git: Pull` (Command Palette)              | Actualiza el repositorio desde el remoto.     |
| `Git: Push` (Command Palette)              | Sube los cambios al repositorio remoto.       |
| `Ctrl + Shift + G H` / `Cmd + Shift + G H` | Muestra el historial de Git.                  |

---

## Ventanas y paneles

| Atajo/Comando                          | Descripción                                               |
|----------------------------------------|-----------------------------------------------------------|
| `Ctrl + Shift + D` / `Cmd + Shift + D` | Muestra/esconde la pestaña Debug.                         |
| `Ctrl + J` / `Cmd + J`                 | Muestra/esconde el panel inferior (Output, Terminal).     |
| `Ctrl + Shift + U` / `Cmd + Shift + U` | Muestra/esconde la pestaña Output.                        |
| `Ctrl + Shift + M` / `Cmd + Shift + M` | Muestra/esconde la pestaña Problems.                      |
| `Ctrl + K Z` / `Cmd + K Z`             | Activa el modo Zen (pantalla completa sin distracciones). |

---

## Comandos avanzados: Productividad

| Atajo/Comando                           | Descripción                                         |
|-----------------------------------------|-----------------------------------------------------|
| `Ctrl + Shift + P` / `Cmd + Shift + P`  | Abre la paleta de comandos (Command Palette).       |
| `Ctrl + K Ctrl + T` / `Cmd + K Cmd + T` | Cambia el tema de color.                            |
| `F2`                                    | Renombra una variable en todo el ámbito (Refactor). |
| `Ctrl + Shift + L` / `Cmd + Shift + L`  | Selecciona todas las ocurrencias del texto.         |
| `Alt + Shift + Drag`                    | Edita múltiples líneas con cursores (multi-cursor). |

---

## Comandos avanzados: Extensiones

| Concepto/Comando                       | Descripción                                       |
|----------------------------------------|---------------------------------------------------|
| `Ctrl + Shift + X` / `Cmd + Shift + X` | Abre el marketplace de extensiones.               |
| `Extensions: Install Extensions`       | Busca e instala extensiones desde la paleta.      |
| `Python`                               | Extensión recomendada para soporte de Python.     |
| `Live Server`                          | Extensión para previsualizar HTML en tiempo real. |
| `GitLens`                              | Extensión para mejorar la integración con Git.    |

---

## Comandos avanzados: Configuración de tareas y lanzamiento

| Concepto/Comando                       | Descripción                                  |
|----------------------------------------|----------------------------------------------|
| `Ctrl + Shift + B` / `Cmd + Shift + B` | Ejecuta una tarea de construcción (build).   |
| `.vscode/tasks.json`                   | Define tareas personalizadas (ej. compilar). |
| `.vscode/launch.json`                  | Configura opciones de depuración.            |
| `Terminal > Configure Tasks`           | Configura tareas desde el menú.              |

---

## Comandos avanzados: Inspección y análisis

| Atajo/Comando                           | Descripción                                    |
|-----------------------------------------|------------------------------------------------|
| `F8`                                    | Salta al siguiente error o advertencia.        |
| `Shift + F8`                            | Salta al error o advertencia anterior.         |
| `Ctrl + Shift + I` / `Cmd + Shift + I`  | Muestra información de un símbolo (Hover).     |
| `Ctrl + K Ctrl + I` / `Cmd + K Cmd + I` | Muestra detalles del cursor (Peek Definition). |

---

## Personalización

| Concepto/Comando                          | Descripción                            |
|-------------------------------------------|----------------------------------------|
| `Ctrl + ,` / `Cmd + ,`                    | Abre la configuración de usuario.      |
| `File > Preferences > Keyboard Shortcuts` | Personaliza los atajos de teclado.     |
| `.vscode/settings.json`                   | Configuración específica del proyecto. |
| `Code > Preferences > Color Theme`        | Cambia el tema visual de VS Code.      |

