# Gestión de Archivos
---
## Borrar achivos
- `rm archivo.txt` eliminaremos el archivo en local y al status veremos que el archivo sigue estando y su nombre sale en **rojo**, para que se borre debremos añadirlo al stage con `git add` lo que pasará a estar en **verde** y tras eso haremos un commit para que se apliquen los cambios y finalmenete se borre en la rama principal

Para ahorarnos unos segundo tambien podemos usar:
- `git rm archivo.txt` borra el archivo y lo pasa directamente a la etapa de stage en **verde**

## Restaurar Archivos Borrados
Para traer un archivo borrado que esta en la tapa de stage tanto en **rojo** como en **verde** usaremos los sigunietes comandos

>**NOTA**: si commiteas un archivo borrado **NO** podemos restaurarlo

- `git restore archivo.txt` restautra un archivo borrado en local, este estaba en **rojo** en estatus
- `git restore --staged archivo.txt` restaura un archivo borrado que estaba en **verde** en stage

## Renombrar en Git

- `mv archivo.txt nuevo_Archivo.txt` Usaremos este comando para renombrar archivos. Si hacemos un status podemos ver que hay 1 archivo eliminado y uno pendiente de ser añadido a stage.
Tras eso añadiremos ambos a stegae, y luego se realizará el commit.

- `git mv archivo.txt nuevo_Archivo.txt` renombra al archivo y lo mete directamente en stage (el eliminado y el nuevo)

## Ignorar archivos y directorios
Crearemos un archivo cullo nombre es **.gitignore**0 fichero donde se especifica los archivos o rutas de los archivos que vamos a ignorar. Al darle a status no saldrán los archivos, pero este archivo hay que añadirlo a stage para commitearlo después.
Dentro de este archivo se suelen guardar contraseñas varibales importante para hacer pruebas, ya que este archivo **no se sube**