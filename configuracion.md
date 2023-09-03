# Instalación de Git
---
Para bajarnos el ejecutable de descarga, para cualquier SO, usaremo el sigunte enlace [Descargar Git](https://git-scm.com/downloads)

### Ejecutable
Al iniciar el ejecutable no habrá que tocar apenas nada de configuracion est todo sigunte, lo unico que si quieres cambiar seria la ruta de dunde se ubicaria o si queremos el acceso directo, por lo demas no tocamos anada
> **Nota**: Para windows al terminar la ejecución tendremos el git_bash y el git_cmd.
> Deberemos usar el git_bash es mucho mas comodo y es el mismo shell que usa mac y linux

## Comandos de la Configuracion

Para conocer la versión usararemos `git -v` o también `git  --version`
Para que las modificaciones se apliquen **en global y no en global** `git config --global`

### Configuracion de usuario y correo
`git config --global user.name "Guille"` Configura el nombre de usuario
`git config --global user.email "correo@mail.com"` Configura el correo electronico

## Configurar con VS Code
Para indicar que VS Code será nuestro editor por defecto lo haremos de la siguinte manera
`git config --global core.editor "code --wait"`
>**Nota**: La parte entre comillas significa que cuando cerremos el terminal espere cuando cerremos el editor

`git config --global -e` Si el anterorio comando está bien copnfigurado se nos abrirá el editor 

### Compatibilidad Linux/MAC y Windows
Linux y Windows tienen el sistema de salto de linea diferente, en linux tenemos el LF(Line Feed o salto de linea) mientras que en Windows está el CRLF (Control de Carro en el salto de linea) ambos son diferentes y a la hora de compartir codigo estos chocan entre sí para ello vamos a configurarlo para todos los sistemas
##### Windows
`git config --global core.autocrlf true`

##### Linux/MAC
`git config --global core.autocrlf input`
