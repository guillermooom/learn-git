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
Todos lo cambios realizados en local se verán en stage en **rojo** y cuando esten en stage ya cambiara su color a **verde**.
Para ello debe pasar de local a stage, lugo a commit y despues a server.
Todo esto sin saltarse fases, no podemos pasar de *LOCAL* a *COMMIT* ya que no se nos permitirá

## Inicializar un Repositorio
Para iniciar un repositorio deberemos colocarnos en la carpeta que vamos a querer que sea el repositorio, para ello vamos ponernos dentro de la carpeta y pondremos lo siguintes `git init`, la rama principal será **master**.

Dentro del repositorio iniciado se creará el archivo `.git` la cual será ignorada por todos los repositorios y dentro tendrá archivos para gestionar los proyectos como contraseñas o usuarios.

- `code .` abre la carpeta en nuestro editor de texto (VS Code que es el que tenemos configurado)

### Estado de los archivos

- `git status` ver el estado actual de nuestro repositorio incluye la rama e indica ficheros en stage y los que no estan allí. Los **untracked files**
    - `git status -s` muestra resumida la informacino de git status
    > *M* (Rojo) archivo modificado en mi pc
    > *M* (Verde) archivo modificado estado en etapa de stage
    > *??* No ha sido agregadoi al stage (archivo nuevo)
    > *A* (Verde) archivo que estamos agregando (archivo nuevo)
    

### Stage
Esta es la etapa entre el commit y local, todos los cambios realizados en local ha de pasar a esta fase para depues ser commiteados y ser subidos mas tarde al server.

- `git add archivo.txt` añade los cambios realizados en local a stage
    - `git add *.md` añade todos los arhcivos terminados en *.md*

>**NOTA**: Si cuando un archivo esta en stage en verde y realizamos un cambio en local este cambiara su color otra vez a rojo.

### Commit
Esta estapa es la que guarda los cambios que realizamos, aqui se lleva un registro de los cambios que se realizan y se guardan. Cuando commiteamos todos los archivos de stage se quitaran de alli y pasaran a formar parte de los cambios permanentes.
- `git commit -m "Primer commit"` se realiza el commit con los archivos que estavben en stage
#### Peor forma de hacer commits
- `git commit` te abre en el editor de texter que tengamos configurado un archivo (arriba de este irá el texto sin nada) luego guardamos y cerramos, al cerrarlo se realizará el commit automaticamente.

### Server
Para añadir archivos al server partimos de la base que tenemos configurado ant5es nuestra carpeta local con un repositorio de github, cuando lo tengamos vamos a subir archivos con el siguinte comando;
- `git push` se subiran los commits al server