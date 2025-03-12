---
title: Apache HTTP Server
---

Apache HTTP Server es un servidor web de código abierto desarrollado por la Apache Software Foundation. 
Es una herramienta que permite alojar y distribuir contenido en la web, como páginas HTML, imágenes o 
aplicaciones, al procesar solicitudes HTTP de los navegadores. Es altamente personalizable, compatible 
con múltiples sistemas operativos (como Windows y Linux) y soporta módulos que extienden sus funciones, 
como seguridad o manejo de lenguajes de programación. Es uno de los servidores web más utilizados en 
internet por su robustez y flexibilidad. 

A continuación se presentan referencias rápidas con los comandos y configuraciones más esenciales de Apache, 
organizada por categorías.

---

## Configuración y básicos

| Comando/Concepto                                 | Descripción                                                                     |
|--------------------------------------------------|---------------------------------------------------------------------------------|
| `httpd` o `apache2`                              | Binario principal de Apache (varía según el sistema).                           |
| `/etc/apache2/` (Linux) o `/etc/httpd/` (CentOS) | Directorio principal de configuración.                                          |
| `apache2ctl -v` o `httpd -v`                     | Muestra la versión de Apache instalada.                                         |
| `# Comentario`                                   | Comentario en archivos de configuración.                                        |
| `Listen 80`                                      | Especifica el puerto en el que Apache escucha (en `httpd.conf` o `ports.conf`). |

---

## Comandos de gestión (Linux)

| Comando                          | Descripción                                            |
|----------------------------------|--------------------------------------------------------|
| `sudo systemctl start apache2`   | Inicia el servidor Apache (Ubuntu/Debian).             |
| `sudo systemctl stop apache2`    | Detiene el servidor Apache.                            |
| `sudo systemctl restart apache2` | Reinicia el servidor Apache.                           |
| `sudo systemctl reload apache2`  | Recarga la configuración sin interrumpir conexiones.   |
| `sudo apache2ctl configtest`     | Verifica la sintaxis de los archivos de configuración. |
| `sudo systemctl enable apache2`  | Habilita Apache para iniciar con el sistema.           |

---

## Archivos principales de configuración

| Archivo                       | Descripción                                               |
|-------------------------------|-----------------------------------------------------------|
| `httpd.conf` o `apache2.conf` | Archivo de configuración principal.                       |
| `ports.conf`                  | Define los puertos en los que escucha Apache.             |
| `sites-available/`            | Carpeta para configuraciones de sitios (Ubuntu).          |
| `sites-enabled/`              | Enlaces simbólicos a sitios activos (Ubuntu).             |
| `conf.d/` o `conf/`           | Configuraciones adicionales (CentOS).                     |
| `.htaccess`                   | Configuración a nivel de directorio (si está habilitada). |

---

## Configuración de sitios virtuales (Virtual Hosts)

| Estructura                                       | Descripción                              |
|--------------------------------------------------|------------------------------------------|
| `<VirtualHost *:80>`                             | Define un sitio virtual en el puerto 80. |
| `ServerName dominio.com`                         | Nombre del dominio del sitio.            |
| `DocumentRoot /var/www/sitio`                    | Directorio raíz del contenido del sitio. |
| `ErrorLog /var/log/apache2/error.log`            | Ruta del archivo de errores.             |
| `CustomLog /var/log/apache2/access.log combined` | Ruta del archivo de acceso con formato.  |
| `</VirtualHost>`                                 | Cierra la definición del sitio virtual.  |

---

## Habilitar/deshabilitar sitios (Ubuntu/Debian)

| Comando                         | Descripción                                                 |
|---------------------------------|-------------------------------------------------------------|
| `sudo a2ensite nombre_sitio`    | Habilita un sitio virtual (crea enlace en `sites-enabled`). |
| `sudo a2dissite nombre_sitio`   | Deshabilita un sitio virtual.                               |
| `sudo systemctl reload apache2` | Aplica los cambios tras habilitar/deshabilitar.             |

---

## Módulos

| Comando/Concepto                                   | Descripción                                |
|----------------------------------------------------|--------------------------------------------|
| `sudo a2enmod nombre_modulo`                       | Habilita un módulo (ej. `rewrite`, `ssl`). |
| `sudo a2dismod nombre_modulo`                      | Deshabilita un módulo.                     |
| `apache2ctl -M` o `httpd -M`                       | Lista los módulos cargados actualmente.    |
| `LoadModule rewrite_module modules/mod_rewrite.so` | Carga un módulo en `httpd.conf`.           |

---

## Directivas comunes

| Directiva                       | Descripción                                           |
|---------------------------------|-------------------------------------------------------|
| `DirectoryIndex index.html`     | Especifica el archivo por defecto (página principal). |
| `AllowOverride All`             | Permite el uso de `.htaccess` en un directorio.       |
| `Options -Indexes`              | Desactiva el listado de directorios.                  |
| `ServerAdmin admin@dominio.com` | Correo del administrador del servidor.                |
| `Redirect /vieja /nueva`        | Redirige una URL a otra.                              |

---

## Configuración de SSL/TLS

| Comando/Concepto                      | Descripción                                       |
|---------------------------------------|---------------------------------------------------|
| `sudo a2enmod ssl`                    | Habilita el módulo SSL.                           |
| `<VirtualHost *:443>`                 | Configura un sitio virtual en HTTPS (puerto 443). |
| `SSLEngine on`                        | Activa SSL para el sitio virtual.                 |
| `SSLCertificateFile /ruta/cert.pem`   | Ruta al certificado SSL.                          |
| `SSLCertificateKeyFile /ruta/key.pem` | Ruta a la clave privada SSL.                      |
| `sudo systemctl restart apache2`      | Reinicia para aplicar cambios SSL.                |

---

## Archivos de log

| Comando/Concepto              | Descripción                      |
|-------------------------------|----------------------------------|
| `/var/log/apache2/error.log`  | Log de errores (Ubuntu/Debian).  |
| `/var/log/apache2/access.log` | Log de accesos (Ubuntu/Debian).  |
| `/var/log/httpd/error_log`    | Log de errores (CentOS/RHEL).    |
| `/var/log/httpd/access_log`   | Log de accesos (CentOS/RHEL).    |
| `tail -f /ruta/log`           | Monitorea un log en tiempo real. |

---

## Configuración de .htaccess

| Directiva                             | Descripción                                              |
|---------------------------------------|----------------------------------------------------------|
| `RewriteEngine On`                    | Activa el motor de reescritura (requiere `mod_rewrite`). |
| `RewriteRule ^vieja$ /nueva [R=301]`  | Redirige permanentemente una URL.                        |
| `ErrorDocument 404 /404.html`         | Define una página personalizada para errores 404.        |
| `Order deny,allow` `Deny from all`    | Restringe acceso a un directorio.                        |
| `AuthType Basic` `Require valid-user` | Configura autenticación básica.                          |

---

## Comandos avanzados: Rendimiento

| Directiva/Concepto                  | Descripción                                                     |
|-------------------------------------|-----------------------------------------------------------------|
| `KeepAlive On`                      | Habilita conexiones persistentes.                               |
| `MaxKeepAliveRequests 100`          | Número máximo de solicitudes por conexión.                      |
| `Timeout 300`                       | Tiempo máximo de espera (segundos).                             |
| `MPM (Multi-Processing Module)`     | Configura el modelo de procesamiento (ej. `prefork`, `worker`). |
| `sudo apache2ctl -t -D DUMP_VHOSTS` | Muestra los sitios virtuales configurados.                      |

---

## Comandos avanzados: Monitoreo y diagnóstico

| Comando                       | Descripción                                             |
|-------------------------------|---------------------------------------------------------|
| `sudo netstat -tulnp grep 80` | Verifica si Apache está escuchando en el puerto 80.     |
| `ps aux grep apache`          | Lista los procesos de Apache en ejecución.              | 
| `sudo apache2ctl status`      | Muestra el estado del servidor (requiere `mod_status`). |
| `htop`                        | Monitorea el uso de recursos del servidor.              |

---

## Instalación (Ubuntu/Debian)

| Comando                        | Descripción                                |
|--------------------------------|--------------------------------------------|
| `sudo apt update`              | Actualiza la lista de paquetes.            |
| `sudo apt install apache2`     | Instala Apache en el sistema.              |
| `sudo ufw allow 'Apache Full'` | Permite tráfico HTTP/HTTPS en el firewall. |

