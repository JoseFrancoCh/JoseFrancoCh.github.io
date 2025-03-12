---
tile: GIT
---

Git es un sistema de control de versiones distribuido que permite rastrear cambios en el código, 
colaborar en equipo y gestionar proyectos de manera eficiente. Es la base de plataformas como 
GitHub y GitLab, ideal para desarrolladores. Esta es una referencia rápida con los comandos más 
esenciales y avanzados de Git, organizada por categorías.

---

## Configuración inicial

| Comando                                         | Descripción                                  |
|-------------------------------------------------|----------------------------------------------|
| `git config --global user.name "Tu Nombre"`     | Configura tu nombre de usuario globalmente.  |
| `git config --global user.email "tu@email.com"` | Configura tu correo electrónico globalmente. |
| `git config --list`                             | Muestra la configuración actual de Git.      |

---

## Iniciar y clonar repositorios

| Comando           | Descripción                                              |
|-------------------|----------------------------------------------------------|
| `git init`        | Inicia un nuevo repositorio Git en el directorio actual. |
| `git clone <url>` | Clona un repositorio remoto a tu máquina local.          |

---

## Trabajo básico con cambios

| Comando                    | Descripción                                                       |
|----------------------------|-------------------------------------------------------------------|
| `git status`               | Muestra el estado actual del repositorio (cambios, staged, etc.). |
| `git add <archivo>`        | Añade un archivo específico al área de staging.                   |
| `git add .`                | Añade todos los archivos modificados al staging.                  |
| `git commit -m "Mensaje"`  | Confirma los cambios en el repositorio con un mensaje.            |
| `git commit -am "Mensaje"` | Combina `add` y `commit` para archivos ya rastreados.             |

---

## Historial y revisión

| Comando             | Descripción                                           |
|---------------------|-------------------------------------------------------|
| `git log`           | Muestra el historial de commits.                      |
| `git log --oneline` | Muestra el historial en una línea por commit.         |
| `git diff`          | Muestra las diferencias entre cambios no confirmados. |
| `git show <commit>` | Muestra detalles de un commit específico.             |

---

## Ramas (Branches)

| Comando                    | Descripción                                     |
|----------------------------|-------------------------------------------------|
| `git branch`               | Lista todas las ramas locales.                  |
| `git branch <nombre>`      | Crea una nueva rama.                            |
| `git checkout <nombre>`    | Cambia a una rama específica.                   |
| `git checkout -b <nombre>` | Crea y cambia a una nueva rama al mismo tiempo. |
| `git merge <rama>`         | Fusiona la rama especificada en la actual.      |
| `git branch -d <nombre>`   | Elimina una rama local (si ya está fusionada).  |

---

## Trabajo con repositorios remotos

| Comando                       | Descripción                                         |
|-------------------------------|-----------------------------------------------------|
| `git remote add origin <url>` | Conecta el repositorio local a uno remoto.          |
| `git push origin <rama>`      | Sube los cambios de una rama al repositorio remoto. |
| `git pull origin <rama>`      | Descarga y fusiona cambios del repositorio remoto.  |
| `git fetch`                   | Descarga datos del remoto sin fusionarlos.          |

---

## Deshacer cambios

| Comando               | Descripción                                            |
|-----------------------|--------------------------------------------------------|
| `git reset <archivo>` | Saca un archivo del área de staging.                   |
| `git reset --hard`    | Revierte todos los cambios no confirmados.             |
| `git revert <commit>` | Crea un nuevo commit que deshace un commit anterior.   |
| `git stash`           | Guarda cambios temporales y limpia el área de trabajo. |
| `git stash pop`       | Recupera los cambios guardados en el stash.            |

---

## Extras útiles

| Comando                  | Descripción                                    |
|--------------------------|------------------------------------------------|
| `git rm <archivo>`       | Elimina un archivo y lo prepara para commit.   |
| `git mv <viejo> <nuevo>` | Renombra un archivo y lo prepara para commit.  |
| `git clean -f`           | Elimina archivos no rastreados del directorio. |

---

## Comandos avanzados: Reescritura de historial

| Comando                     | Descripción                                                                  |
|-----------------------------|------------------------------------------------------------------------------|
| `git rebase <rama>`         | Reescribe el historial aplicando commits sobre otra rama.                    |
| `git rebase -i <commit>`    | Inicia un rebase interactivo para editar, combinar o eliminar commits.       |
| `git commit --amend`        | Modifica el último commit (puede añadir cambios o cambiar el mensaje).       |
| `git reset --soft <commit>` | Mueve la rama a un commit anterior, manteniendo cambios en staging.          |
| `git reset --hard <commit>` | Resetea completamente al commit especificado, descartando todo lo posterior. |

---

## Comandos avanzados: Selección y combinación

| Comando                     | Descripción                                                 |
|-----------------------------|-------------------------------------------------------------|
| `git cherry-pick <commit>`  | Aplica un commit específico de otra rama en la rama actual. |
| `git merge --no-ff <rama>`  | Fuerza un merge con un commit de fusión (no fast-forward).  |
| `git merge --squash <rama>` | Combina una rama en un solo commit antes de fusionarla.     |

---

## Comandos avanzados: Inspección y depuración

| Comando                    | Descripción                                                      |
|----------------------------|------------------------------------------------------------------|
| `git blame <archivo>`      | Muestra quién modificó cada línea de un archivo y en qué commit. |
| `git bisect start`         | Inicia una búsqueda binaria para encontrar un commit con error.  |
| `git bisect good <commit>` | Marca un commit como bueno durante el bisect.                    |
| `git bisect bad <commit>`  | Marca un commit como malo durante el bisect.                     |
| `git bisect reset`         | Termina el proceso de bisect y regresa al estado inicial.        |

---

## Comandos avanzados: Gestión de remotos

| Comando                             | Descripción                                  |
|-------------------------------------|----------------------------------------------|
| `git remote -v`                     | Lista los repositorios remotos con sus URLs. |
| `git remote rename <viejo> <nuevo>` | Renombra un remoto existente.                |
| `git remote remove <nombre>`        | Elimina un remoto del repositorio local.     |
| `git push origin --delete <rama>`   | Elimina una rama del repositorio remoto.     |

---

## Comandos avanzados: Stash avanzado

| Comando                     | Descripción                                |
|-----------------------------|--------------------------------------------|
| `git stash list`            | Lista todos los stashes guardados.         |
| `git stash apply <stash>`   | Aplica un stash específico sin eliminarlo. |
| `git stash drop <stash>`    | Elimina un stash específico.               |
| `git stash branch <nombre>` | Crea una rama a partir de un stash.        |

---

## Comandos avanzados: Tags

| Comando                            | Descripción                             |
|------------------------------------|-----------------------------------------|
| `git tag <nombre>`                 | Crea un tag ligero en el commit actual. |
| `git tag -a <nombre> -m "Mensaje"` | Crea un tag anotado con un mensaje.     |
| `git push origin <tag>`            | Sube un tag específico al remoto.       |
| `git push origin --tags`           | Sube todos los tags al remoto.          |
| `git tag -d <nombre>`              | Elimina un tag localmente.              |


