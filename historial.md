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