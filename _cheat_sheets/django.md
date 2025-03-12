---
title: Django
---

Django es un framework de Python de alto nivel para desarrollar aplicaciones web rápidas y seguras, 
basado en el principio "no te repitas" (DRY). Simplifica tareas como manejo de bases de datos, 
autenticación y rutas con su estructura MTV (Modelo-Template-Vista). Esta es una referencia rápida con
los comandos y estructuras más esenciales de Django, organizada por categorías.

---

## Configuración y básicos

| Comando/Concepto                   | Descripción                                                 |
|------------------------------------|-------------------------------------------------------------|
| `pip install django`               | Instala Django en tu entorno Python.                        |
| `django-admin startproject nombre` | Crea un nuevo proyecto Django.                              |
| `python manage.py startapp nombre` | Crea una nueva aplicación dentro del proyecto.              |
| `python manage.py runserver`       | Inicia el servidor local (por defecto en `localhost:8000`). |
| `settings.py`                      | Archivo principal de configuración del proyecto.            |
| `INSTALLED_APPS`                   | Lista de aplicaciones activas en `settings.py`.             |

---

## Comandos de gestión

| Comando                            | Descripción                                        |
|------------------------------------|----------------------------------------------------|
| `python manage.py makemigrations`  | Genera migraciones basadas en cambios en modelos.  |
| `python manage.py migrate`         | Aplica las migraciones a la base de datos.         |
| `python manage.py createsuperuser` | Crea un usuario administrador.                     |
| `python manage.py shell`           | Abre una consola interactiva de Python con Django. |
| `python manage.py test`            | Ejecuta las pruebas unitarias del proyecto.        |
| `python manage.py collectstatic`   | Recolecta archivos estáticos en `STATIC_ROOT`.     |

---

## Estructura de un proyecto

| Directorio/Archivo        | Descripción                                      |
|---------------------------|--------------------------------------------------|
| `manage.py`               | Script principal para gestionar el proyecto.     |
| `nombre_proyecto/urls.py` | Define las rutas URL del proyecto.               |
| `nombre_app/models.py`    | Define los modelos de datos (tablas de BD).      |
| `nombre_app/views.py`     | Define las vistas (lógica de las páginas).       |
| `nombre_app/templates/`   | Carpeta para plantillas HTML.                    |
| `nombre_app/static/`      | Carpeta para archivos estáticos (CSS, JS, etc.). |

---

## Modelos (Models)

| Concepto/Estructura                                                     | Descripción                                                |
|-------------------------------------------------------------------------|------------------------------------------------------------|
| `from django.db import models`                                          | Importa el módulo de modelos.                              |
| `class MiModelo(models.Model):`                                         | Define un modelo (clase).                                  |
| `campo = models.CharField(max_length=100)`                              | Campo de texto (otros: `IntegerField`, `DateField`, etc.). |
| `foreign_key = models.ForeignKey(OtroModelo, on_delete=models.CASCADE)` | Relación uno a muchos.                                     |
| `Meta: db_table = "nombre"`                                             | Personaliza opciones del modelo (ej. nombre de tabla).     |
| `def __str__(self): return self.nombre`                                 | Representación en string del modelo.                       |

---

## Vistas (Views)

| Concepto/Estructura                                         | Descripción                                      |
|-------------------------------------------------------------|--------------------------------------------------|
| `from django.http import HttpResponse`                      | Respuesta HTTP básica.                           |
| `def mi_vista(request): return HttpResponse("Hola")`        | Vista simple basada en función.                  |
| `from django.shortcuts import render`                       | Renderiza plantillas.                            |
| `return render(request, 'template.html', {'clave': valor})` | Pasa datos a la plantilla.                       |
| `class MiVista(View):`                                      | Vista basada en clase (usa `get`, `post`, etc.). |

---

## URLs

| Concepto/Estructura                                   | Descripción                                |
|-------------------------------------------------------|--------------------------------------------|
| `from django.urls import path`                        | Importa el módulo para definir rutas.      |
| `urlpatterns = [path('ruta/', vista, name='nombre')]` | Define una URL con su vista asociada.      |
| `path('ruta/<int:id>/', vista)`                       | Ruta con parámetro dinámico (ej. ID).      |
| `from django.urls import include`                     | Incluye URLs de otra aplicación.           |
| `path('', include('app.urls'))`                       | Redirige a las URLs de una app específica. |
 
---

## Formularios (Forms)

| Concepto/Estructura              | Descripción                                   |
|----------------------------------|-----------------------------------------------|
| `from django import forms`       | Importa el módulo de formularios.             |
| `class MiForm(forms.Form):`      | Define un formulario simple.                  |
| `campo = forms.CharField()`      | Campo de texto (otros: `IntegerField`, etc.). |
| `class MiForm(forms.ModelForm):` | Formulario basado en un modelo.               |
| `Meta: model = MiModelo`         | Vincula el formulario a un modelo específico. |
| `form.is_valid()`                | Valida los datos enviados por el usuario.     |

---

## Archivos estáticos y media

| Concepto/Comando                           | Descripción                                                   |
|--------------------------------------------|---------------------------------------------------------------|
| `STATIC_URL = '/static/'`                  | Define la URL base para archivos estáticos en `settings.py`.  |
| `STATICFILES_DIRS = [BASE_DIR / "static"]` | Directorios adicionales de archivos estáticos.                |
| `load static`                              | Carga la etiqueta para usar archivos estáticos en plantillas. |
| `static 'css/estilo.css'`                  | Ruta a un archivo estático en una plantilla.                  |
| `MEDIA_URL = '/media/'`                    | URL para archivos subidos por usuarios.                       |
| `MEDIA_ROOT = BASE_DIR / 'media'`          | Directorio donde se guardan los archivos media.               |


---

## Base de datos (ORM)

| Concepto/Comando                       | Descripción                                                    |
|----------------------------------------|----------------------------------------------------------------|
| `MiModelo.objects.all()`               | Obtiene todos los registros del modelo.                        |
| `MiModelo.objects.get(id=1)`           | Obtiene un registro específico (lanza excepción si no existe). |
| `MiModelo.objects.filter(campo=valor)` | Filtra registros según condiciones.                            |
| `obj = MiModelo(campo=valor)`          | Crea una nueva instancia del modelo.                           |
| `obj.save()`                           | Guarda la instancia en la base de datos.                       |
| `MiModelo.objects.delete()`            | Elimina registros que cumplen una condición.                   |

---

## Comandos avanzados: Configuración

| Concepto/Comando        | Descripción                                                           |
|-------------------------|-----------------------------------------------------------------------|
| `DATABASES = {...}`     | Configura la base de datos en `settings.py` (ej. SQLite, PostgreSQL). |
| `MIDDLEWARE = [...]`    | Lista de middleware en `settings.py` (seguridad, sesiones, etc.).     |
| `TEMPLATES = [{...}]`   | Configura directorios y opciones de plantillas.                       |
| `ALLOWED_HOSTS = ['*']` | Permite hosts específicos para el servidor.                           |

---

## Comandos avanzados: Desarrollo

| Comando/Concepto            | Descripción                                   |
|-----------------------------|-----------------------------------------------|
| `python manage.py check`    | Verifica errores en el proyecto sin ejecutar. |
| `python manage.py dumpdata` | Exporta datos de la BD a un archivo JSON.     |
| `python manage.py loaddata` | Importa datos desde un archivo JSON a la BD.  |
| `DEBUG = True`              | Activa el modo depuración en `settings.py`.   |

---

## Despliegue

| Concepto/Comando                         | Descripción                                         |
|------------------------------------------|-----------------------------------------------------|
| `gunicorn nombre.wsgi`                   | Inicia el proyecto con Gunicorn (servidor WSGI).    |
| `STATIC_ROOT = BASE_DIR / 'staticfiles'` | Directorio para recolectar estáticos en producción. |
| `DEBUG = False`                          | Desactiva depuración en producción.                 |
| `python manage.py collectstatic`         | Recolecta estáticos para el servidor.               |
