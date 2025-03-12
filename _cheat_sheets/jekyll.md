---
title: Jekyll
---

Jekyll es un generador de sitios estáticos basado en Ruby que transforma contenido en Markdown, HTML y 
Liquid en páginas web rápidas y seguras, ideal para blogs y sitios simples. No requiere bases de datos y 
se integra bien con GitHub Pages. Esta es una referencia rápida con los comandos y estructuras más esenciales 
de Jekyll, organizada por categorías.

---

## Instalación y configuración inicial

| Comando/Concepto                   | Descripción                                           |
|------------------------------------|-------------------------------------------------------|
| `gem install jekyll bundler`       | Instala Jekyll y Bundler (requiere Ruby).             |
| `jekyll new nombre_sitio`          | Crea un nuevo sitio Jekyll con una estructura básica. |
| `cd nombre_sitio` `bundle install` | Instala las dependencias definidas en el `Gemfile`.   |
| `_config.yml`                      | Archivo principal de configuración del sitio.         |
| `baseurl: "/nombre"`               | Define la URL base del sitio en `_config.yml`.        |
| `url: "https://ejemplo.com"`       | Define la URL absoluta del sitio en `_config.yml`.    |

---

## Comandos básicos

| Comando                    | Descripción                                                 |
|----------------------------|-------------------------------------------------------------|
| `jekyll serve`             | Inicia el servidor local (por defecto en `localhost:4000`). |
| `jekyll serve --watch`     | Inicia el servidor y regenera al detectar cambios.          |
| `jekyll build`             | Genera el sitio estático en la carpeta `_site`.             |
| `jekyll serve --drafts`    | Sirve el sitio incluyendo borradores (`_drafts`).           |
| `jekyll clean`             | Limpia la carpeta `_site` y archivos generados.             |
| `bundle exec jekyll serve` | Ejecuta Jekyll usando las dependencias del `Gemfile`.       |

---

## Estructura de directorios

| Directorio/Archivo | Descripción                                                  |
|--------------------|--------------------------------------------------------------|
| `_posts/`          | Carpeta para publicaciones (formato `YYYY-MM-DD-título.md`). |
| `_pages/`          | Carpeta opcional para páginas estáticas.                     |
| `_layouts/`        | Carpeta para plantillas reutilizables.                       |
| `_includes/`       | Carpeta para fragmentos de código reutilizables.             |
| `_data/`           | Carpeta para datos en formato YAML, CSV o JSON.              |
| `_site/`           | Carpeta generada con el sitio estático final.                |
| `assets/`          | Carpeta común para CSS, JS, imágenes, etc.                   |

---

## Front Matter (Metadatos)

| Concepto/Estructura                          | Descripción                                        |
|----------------------------------------------|----------------------------------------------------|
| `---` `title: "Título"` `layout: post` `---` | Define metadatos al inicio de un archivo Markdown. |
| `permalink: /ruta/personalizada/`            | Personaliza la URL de una página o post.           |
| `date: 2025-03-10 12:00:00`                  | Especifica la fecha de publicación.                |
| `categories: blog tech`                      | Añade categorías al post.                          |
| `tags: [jekyll, ruby]`                       | Añade etiquetas al post.                           |

---

## Plantillas y layouts

| Comando/Estructura             | Descripción                          |
|--------------------------------|--------------------------------------|
| `_layouts/default.html`        | Plantilla base para el sitio.        |
| `<!DOCTYPE html>` `<html>` ... | Estructura HTML típica en un layout. |

---

## Publicaciones (Posts)

| Concepto/Estructura              | Descripción                                          |
|----------------------------------|------------------------------------------------------|
| `2025-03-10-mi-post.md`          | Nombre de archivo típico para un post.               |
| `_posts/`                        | Carpeta predeterminada para posts.                   |
| `_drafts/mi-borrador.md`         | Borradores (sin fecha en el nombre).                 |
| `excerpt_separator: <!--more-->` | Define un separador para extractos en `_config.yml`. |

---

## Datos personalizados

| Concepto/Estructura            | Descripción                                    |
|--------------------------------|------------------------------------------------|
| `_data/datos.yml`              | Archivo YAML para datos (ej. `nombre: valor`). |
| `{{ site.data.datos.nombre }}` | Accede a datos desde `_data/datos.yml`.        |
| `_data/lista.csv`              | Datos en formato CSV accesibles con Liquid.    |

---

## Comandos avanzados: Configuración

| Comando/Concepto                         | Descripción                                         |
|------------------------------------------|-----------------------------------------------------|
| `exclude: [node_modules, README.md]`     | Excluye archivos o carpetas en `_config.yml`.       |
| `collections:` `proyectos:`              | Define colecciones personalizadas en `_config.yml`. |
| `defaults:` `- scope:` `type: proyectos` | Configura valores predeterminados para colecciones. |
| `sass:` `sass_dir: _sass`                | Configura Sass para estilos en `_config.yml`.       |

---

## Comandos avanzados: Desarrollo

| Comando                            | Descripción                                       |
|------------------------------------|---------------------------------------------------|
| `jekyll serve --host 0.0.0.0`      | Sirve el sitio accesible en red local.            |
| `jekyll serve --port 8080`         | Cambia el puerto del servidor local.              |
| `jekyll build --destination /ruta` | Cambia la carpeta de salida del sitio generado.   |
| `jekyll serve --incremental`       | Regeneración incremental para builds más rápidos. |

---

## Integración con GitHub Pages

| Concepto             | Descripción                                        |
|----------------------|----------------------------------------------------|
| `gem "github-pages"` | Añade esta línea al `Gemfile` para compatibilidad. |
| `docs/`              | Carpeta común para publicar en GitHub Pages.       |
| `_config.yml`        | Configura `baseurl` y `url` para GitHub Pages.     |
