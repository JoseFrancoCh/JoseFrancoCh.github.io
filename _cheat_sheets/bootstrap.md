---
title: Bootstrap 5
---

Bootstrap es un framework de código abierto que agiliza el diseño de sitios web responsivos usando HTML, 
CSS y JavaScript. Ofrece componentes predefinidos —como botones, formularios y cuadrículas— para crear 
interfaces modernas sin partir de cero. Esta es una referencia rápida con las clases y componentes
más esenciales de Bootstrap 5, organizada por categorías.

---

## Configuración y básicos

| Concepto/Comando                                                                                         | Descripción                                   |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| `<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">` | Incluye CSS de Bootstrap vía CDN.             |
| `<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>`   | Incluye JS de Bootstrap (con Popper).         |
| `class="container"`                                                                                      | Contenedor centrado con márgenes automáticos. |
| `class="container-fluid"`                                                                                | Contenedor de ancho completo.                 |
| `<!-- Comentario -->`                                                                                    | Comentario en HTML.                           |

---

## Sistema de rejilla (Grid)

| Clase                     | Descripción                                                 |
|---------------------------|-------------------------------------------------------------|
| `class="row"`             | Define una fila en la rejilla.                              |
| `class="col"`             | Columna de ancho automático.                                |
| `class="col-md-6"`        | Columna de 6 unidades (50%) en pantallas medianas (≥768px). |
| `class="col-12 col-md-4"` | 12 unidades (100%) en móvil, 4 (33%) en mediano.            |
| `class="g-3"`             | Espaciado entre columnas/filas (gutter).                    |
| `class="offset-md-2"`     | Desplaza la columna 2 unidades a la derecha (mediano).      |

---

## Tipografía y texto

| Clase                       | Descripción                               |
|-----------------------------|-------------------------------------------|
| `class="h1"` a `class="h6"` | Estilos de encabezados (h1 a h6).         |
| `class="text-center"`       | Alinea el texto al centro.                |
| `class="text-primary"`      | Aplica color primario (azul por defecto). |
| `class="fw-bold"`           | Texto en negrita (font-weight).           |
| `class="fs-4"`              | Tamaño de fuente (1 = mayor, 6 = menor).  |
| `class="text-uppercase"`    | Convierte texto a mayúsculas.             |

---

## Colores y fondos

| Clase                  | Descripción                      |
|------------------------|----------------------------------|
| `class="bg-primary"`   | Fondo azul (primario).           |
| `class="bg-success"`   | Fondo verde (éxito).             |
| `class="text-bg-dark"` | Texto blanco sobre fondo oscuro. |
| `class="bg-gradient"`  | Añade un gradiente al fondo.     |
| `class="opacity-50"`   | Reduce la opacidad al 50%.       |

---

## Botones

| Clase                               | Descripción                      |
|-------------------------------------|----------------------------------|
| `class="btn btn-primary"`           | Botón azul básico.               |
| `class="btn btn-outline-secondary"` | Botón con borde gris, sin fondo. |
| `class="btn btn-lg"`                | Botón grande.                    |
| `class="btn btn-sm"`                | Botón pequeño.                   |
| `<button class="btn" disabled>`     | Botón deshabilitado.             |
| `class="btn-group"`                 | Agrupa botones horizontalmente.  |

---

## Formularios

| Clase                      | Descripción                              |
|----------------------------|------------------------------------------|
| `class="form-control"`     | Estilo para inputs, selects y textareas. |
| `class="form-label"`       | Estilo para etiquetas de formulario.     |
| `class="form-check"`       | Checkbox o radio button.                 |
| `class="form-check-input"` | Input dentro de un checkbox/radio.       |
| `class="form-check-label"` | Etiqueta para checkbox/radio.            |
| `class="input-group"`      | Agrupa un input con un botón o texto.    |

---

## Alertas

| Clase                                                         | Descripción                  |
|---------------------------------------------------------------|------------------------------|
| `class="alert alert-success"`                                 | Alerta verde (éxito).        |
| `class="alert alert-danger"`                                  | Alerta roja (error).         |
| `class="alert alert-dismissible"`                             | Alerta cerrable con botón.   |
| `<button class="btn-close" data-bs-dismiss="alert"></button>` | Botón para cerrar la alerta. |

---

## Tarjetas (Cards)

| Clase                  | Descripción                                |
|------------------------|--------------------------------------------|
| `class="card"`         | Contenedor de tarjeta.                     |
| `class="card-body"`    | Contenido principal de la tarjeta.         |
| `class="card-title"`   | Título dentro de la tarjeta.               |
| `class="card-img-top"` | Imagen en la parte superior de la tarjeta. |
| `class="card-footer"`  | Pie de la tarjeta.                         |

---

## Navegación (Navbar)

| Clase                                                       | Descripción                                          |
|-------------------------------------------------------------|------------------------------------------------------|
| `class="navbar navbar-expand-lg"`                           | Barra de navegación expansible en pantallas grandes. |
| `class="navbar-brand"`                                      | Logo o nombre del sitio en la navbar.                |
| `class="nav-link"`                                          | Enlace dentro de la navbar.                          |
| `<button class="navbar-toggler" data-bs-toggle="collapse">` | Botón para menú colapsable.                          |
| `class="collapse navbar-collapse"`                          | Contenido colapsable de la navbar.                   |

---

## Modales (Modals)

| Estructura                                                  | Descripción                            |
|-------------------------------------------------------------|----------------------------------------|
| `<div class="modal">`                                       | Contenedor del modal.                  |
| `class="modal-dialog"`                                      | Define el tamaño y posición del modal. |
| `class="modal-content"`                                     | Contenido interno del modal.           |
| `<button data-bs-toggle="modal" data-bs-target="#idModal">` | Botón que abre el modal.               |
| `class="modal-header"`                                      | Encabezado del modal.                  |

---

## Utilidades (Utilities)

| Clase                       | Descripción                                            |
|-----------------------------|--------------------------------------------------------|
| `class="m-3"`               | Margen exterior de 1rem (ajustable: `m-0` a `m-5`).    |
| `class="p-2"`               | Padding interior de 0.5rem (ajustable: `p-0` a `p-5`). |
| `class="d-none d-md-block"` | Oculta en móvil, visible en mediano y superior.        |
| `class="text-end"`          | Alinea texto a la derecha.                             |
| `class="rounded"`           | Bordes redondeados.                                    |
| `class="shadow"`            | Añade sombra al elemento.                              |

---

## Componentes avanzados: Carrusel

| Clase                                | Descripción                        |
|--------------------------------------|------------------------------------|
| `class="carousel slide"`             | Contenedor del carrusel.           |
| `class="carousel-inner"`             | Contiene los ítems del carrusel.   |
| `class="carousel-item"`              | Cada diapositiva del carrusel.     |
| `<button data-bs-slide="prev/next">` | Botones para avanzar o retroceder. |

---

## Componentes avanzados: Acordeón

| Clase                      | Descripción                           |
|----------------------------|---------------------------------------|
| `class="accordion"`        | Contenedor del acordeón.              |
| `class="accordion-item"`   | Cada sección del acordeón.            |
| `class="accordion-header"` | Encabezado clickable de cada sección. |
| `class="accordion-body"`   | Contenido colapsable de cada sección. |

---

## Breakpoints (Puntos de ruptura)

| Prefijo         | Rango de ancho (px)            |
|-----------------|--------------------------------|
| `(sin prefijo)` | <576px (extra pequeño, móvil). |
| `sm-`           | ≥576px (pequeño).              |
| `md-`           | ≥768px (mediano).              |
| `lg-`           | ≥992px (grande).               |
| `xl-`           | ≥1200px (extra grande).        |
| `xxl-`          | ≥1400px (extra extra grande).  |

