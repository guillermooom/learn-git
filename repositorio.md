#  Gestionar un repositorio
---
Para gestionar un repositior antes hemos de comocer algunos de los comandos basicos de bash
## Comandos Básicos
- `ls` lista todos los archivos que tenemos en el terminal
    - `ls -a` para listar archibos ocultos también
- `pwd` directorio actual en el q estamos
- `cd` se usa para moverse entre directorios
- `mkdir` crear una carpeta
- `rm` borrar o un archivo o una carpeta
## Flujo entre archivos
Para enterder como funciona la metodoliga de git y como se ve en el terminal hemos de determinar 4 fases: 
- *LOCAL*
- *STAGE*
- *COMMIT*
- *SERVER*

Cuando creamos un archivo o modifiquemos en local estos cambios no se reflejan en el server, pero tampoco en la etapa de stage.
Para ello debe pasar de local a stage, lugo a commit y despues a server.
Todo esto sin saltarse fases, no podemos pasar de *LOCAL* a *COMMIT* ya que no se nos permitirá

## Inicializar un Repositorio
Para iniciar un repositorio deberemos colocarnos en la carpeta que vamos a querer que sea el repositorio, para ello vamos ponernos dentro de la carpeta y pondremos lo siguintes `git init`, la rama principal será **master**.

Dentro del repositorio iniciado se creará el archivo `.git` la cual será ignorada por todos los repositorios y dentro tendrá archivos para gestionar los proyectos como contraseñas o usuarios.

- `code .` abre la carpeta en nuestro editor de texto (VS Code que es el que tenemos configurado)

- `git status` ver el estado actual de nuestro repositorio incluye la rama e indica ficheros en stage y los que no estan allí. Los **untracked files**
    - `git status -s` muestra resumida la informacino de git status