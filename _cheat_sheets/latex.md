---
title: LaTeX
---

LaTeX es un sistema de composición tipográfica diseñado para crear documentos de alta calidad, 
especialmente en matemáticas, ciencias y publicaciones académicas, gracias a su precisión en 
fórmulas y formato. Funciona con comandos que estructuran texto y ecuaciones. Esta es una referencia
rápida con los comandos y estructuras más esenciales de LaTeX, organizada por categorías.

---

## Estructura básica

| Comando/Estructura        | Descripción                                                |
|---------------------------|------------------------------------------------------------|
| `\documentclass{article}` | Define el tipo de documento (article, book, report, etc.). |
| `\usepackage{paquete}`    | Importa un paquete (ej. `utf8x`, `geometry`).              |
| `\begin{document}`        | Inicia el contenido del documento.                         |
| `\end{document}`          | Finaliza el contenido del documento.                       |
| `% Comentario`            | Añade un comentario (ignorado al compilar).                |

---

## Configuración del documento

| Comando                                      | Descripción                                        |
|----------------------------------------------|----------------------------------------------------|
| `\title{Título}`                             | Define el título del documento.                    |
| `\author{Autor}`                             | Define el autor del documento.                     |
| `\date{Fecha}`                               | Define la fecha (puede dejarse vacío para omitir). |
| `\maketitle`                                 | Genera el título con la información previa.        |
| `\usepackage[utf8]{inputenc}`                | Permite caracteres UTF-8 (acentos, ñ, etc.).       |
| `\usepackage[a4paper, margin=1in]{geometry}` | Configura márgenes y tamaño del papel.             |

---

## Secciones y estructura

| Comando                  | Descripción                                   |
|--------------------------|-----------------------------------------------|
| `\section{Título}`       | Crea una sección (nivel 1).                   |
| `\subsection{Título}`    | Crea una subsección (nivel 2).                |
| `\subsubsection{Título}` | Crea una subsubsección (nivel 3).             |
| `\chapter{Título}`       | Crea un capítulo (solo en `book` o `report`). |
| `\tableofcontents`       | Genera la tabla de contenido automáticamente. |

---

## Texto básico

| Comando             | Descripción                             |
|---------------------|-----------------------------------------|
| `\textbf{Texto}`    | Texto en negrita.                       |
| `\textit{Texto}`    | Texto en cursiva.                       |
| `\underline{Texto}` | Texto subrayado.                        |
| `\texttt{Texto}`    | Texto en fuente de máquina de escribir. |
| `\\`                | Forzar un salto de línea.               |
| `\newpage`          | Forzar un salto de página.              |

---

## Listas

| Comando/Estructura                                                      | Descripción                      |
|-------------------------------------------------------------------------|----------------------------------|
| `\begin{itemize}` `\item Elemento` `\end{itemize}`                      | Lista con viñetas (no numerada). |
| `\begin{enumerate}` `\item Elemento` `\end{enumerate}`                  | Lista numerada.                  |
| `\begin{description}` `\item[Etiqueta] Descripción` `\end{description}` | Lista descriptiva con etiquetas. |

---

## Matemáticas (Modo matemático)

| Comando                | Descripción                           |
|------------------------|---------------------------------------|
| `$x + y$`              | Modo matemático en línea.             |
| `\[ x + y \]`          | Modo matemático centrado (display).   |
| `\usepackage{amsmath}` | Paquete para matemáticas avanzadas.   |
| `x^2`                  | Superíndice (exponente).              |
| `x_2`                  | Subíndice.                            |
| `\frac{a}{b}`          | Fracción (numerador/denominador).     |
| `\sqrt{x}`             | Raíz cuadrada.                        |
| `\sum_{i=1}^{n}`       | Suma con límites inferior y superior. |
| `\int_{a}^{b}`         | Integral con límites.                 |

---

## Tablas

| Comando/Estructura                                      | Descripción                                              |
|---------------------------------------------------------|----------------------------------------------------------|
| `\begin{tabular}{c c c}` `a & b & c \\` `\end{tabular}` | Tabla básica (c = centrado, l = izquierda, r = derecha). |
| `\hline`                                                | Línea horizontal en una tabla.                           |
| `\multicolumn{2}{c}{Texto}`                             | Combina 2 columnas y centra el texto.                    |
| `\multirow{2}{*}{Texto}`                                | Combina 2 filas (requiere paquete `multirow`).           |

---

## Figuras e imágenes

| Comando/Estructura                                                            | Descripción                             |
|-------------------------------------------------------------------------------|-----------------------------------------|
| `\usepackage{graphicx}`                                                       | Paquete para incluir imágenes.          |
| `\includegraphics[opciones]{archivo}`                                         | Inserta una imagen (ej. `[width=5cm]`). |
| `\begin{figure}[h]` `\includegraphics{imagen} \caption{Texto}` `\end{figure}` | Figura con leyenda (h = aquí).          |

---

## Referencias y citas

| Comando/Estructura                                                                   | Descripción                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| `\usepackage{bibentry}`                                                              | Paquete para bibliografía simple.            |
| `\begin{thebibliography}{9}` `\bibitem{clave} Autor, Título` `\end{thebibliography}` | Bibliografía manual.                         |
| `\cite{clave}`                                                                       | Cita una referencia de la bibliografía.      |
| `\label{etiqueta}`                                                                   | Define una etiqueta para referencia cruzada. |
| `\ref{etiqueta}`                                                                     | Referencia a una sección, figura, etc.       |

---

## Comandos avanzados: Entornos

| Comando/Estructura                               | Descripción                                    |
|--------------------------------------------------|------------------------------------------------|
| `\begin{center}` `Texto` `\end{center}`          | Centra el contenido.                           |
| `\begin{flushleft}` `Texto` `\end{flushleft}`    | Alinea el contenido a la izquierda.            |
| `\begin{flushright}` `Texto` `\end{flushright}`  | Alinea el contenido a la derecha.              |
| `\begin{equation}` `E=mc^2` `\end{equation}`     | Ecuación numerada automáticamente.             |
| `\begin{align}` `a &= b \\ c &= d` `\end{align}` | Alinea varias ecuaciones (requiere `amsmath`). |

---

## Comandos avanzados: Personalización

| Comando                                    | Descripción                              |
|--------------------------------------------|------------------------------------------|
| `\newcommand{\nombre}{definición}`         | Define un nuevo comando personalizado.   |
| `\renewcommand{\nombre}{nueva_definición}` | Redefine un comando existente.           |
| `\usepackage{xcolor}`                      | Paquete para usar colores.               |
| `\textcolor{red}{Texto}`                   | Texto en color rojo (requiere `xcolor`). |
| `\setlength{\parskip}{1em}`                | Ajusta el espaciado entre párrafos.      |

---

## Comandos avanzados: Matemáticas adicionales

| Comando                      | Descripción                                        |
|------------------------------|----------------------------------------------------|
| `\infty`                     | Símbolo de infinito (∞).                           |
| `\alpha`, `\beta`, `\gamma`  | Letras griegas.                                    |
| `\cdot`                      | Punto de multiplicación (·).                       |
| `\pm`                        | Símbolo de más/menos (±).                          |
| `\left( \frac{a}{b} \right)` | Paréntesis que se ajustan al tamaño del contenido. |

