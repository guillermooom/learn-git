# Historial  y Cambios
---
## Ver Cambios realizados

- `git diff` nos muestra lso cambios realizadosy en cual archivo se ha realizado (salen todos los archivos que nosotros hemos modificado). Saldrá en rojo la linea que no hemos modificado **x** significará lo que habia antes en el archivo.
Los numeros nos indican desde donde comienza y las lineas que se han añadido.
Si metemos el archivo modificado enj stage al hacer `git diff` no saldrán los cambios
> **NOTA**: Para salir del diff se sale con la tecla *Q*

- `git diff --stay` te saldrán los cambios en los archivos que se encuentren el la etapa de stage

## Historial de Git
- `git log` muetra con mucho detalle el historial de commits (con el autor, su email, la fecha, el texto del commit y un código de identificación)

    - `git log --oneline` te muestra los commits con su codigo y el mensaje. Esta opción resume el texto que sale con el comando de arriba

## Ramas  y Branches 

Cuando inicamos un proyecto lo normla es que nuestras ramas se llamen o main o master
- `git branch` ve todas las rampas pero la rama que tiene **`*`** en la cual estamos trabajando
- `git checkout -b rama1` crea una nueva rama y nos pone en ella
    - `git checkout rama1` te cambia a la rama1

>**NOTA**: Cuando hacemos un commit en una nueva rama vamos a poder ver en *git log* el commit en la rama que fue hecho y **HEAD** significa el ultimo codigo hecho y donde nos encontramos

- `cat archivo.txt` ver archivoe n el historial
> **NOTA**: Lo veremos en la rama en la que nos encontramos, si cambiamos de rama y hacemos de nuevo el *cat* veremos el código de esa rama y no como estaba (en la otra rama)

- `git merge rama1` combinamos la rama que especificamos con la rama en la que nos encontramos, metiendo los cambios de la rama indicada en la que estamos actualmente

## Conexión con GitHub
- `git remote add origin URL-SITE` conecta mi repositorio local con github donde irá el codigo y de donde se sacará
- `git push -u origin rama1` subimos la rama que estamos trabajando en local y se creará en github si no existe

> **NOTA**: Para subir archivo al servidor solo usaremos `git push` si la rama ya esta creada ya que si lo subimos con la opción de *-u origin* nos adara error