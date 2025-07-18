
# Aprendiendo Git, GitHub y GitHub Action
> Aprendiendo las bases de git, almacenamiento local y remoto de un repositorio, asi como la compilacion y despliegue de una aplicacion usando GitHub Actions.

## Git
> Sistema de Control de Versiones, usando principalmente para darle seguimiento a proyectos de codigo.

#### Principales Comandos Git

- git init: inicializacion de un repositorio.
- git add README.md: agregando archivo al area de staying.
- git add *.txt: agregando multiples archivos usando patrones.
- git add confidencial/: agregando carpetas completas al staying, dejandolos listos para el commit.
- git add .: agrega todos los cambios existentes al area de staying.
- git commit -m "": comando para mover del staying al reposotirio los cambios y agregando un mensaje. Persiste los datos.
- git commit -am "": permite agregar los cambios y persistirlos a la vez, la condicion es que solo aplica para archivos a los que ya anteriormente se les da seguimiento, no para archivos nuevos.
- git log: muestras nuestros commits con detalles.
- git log --oneline: muestra los commits sin detalles y en una sola linea por commit.
- git log -n 2: permite limitar la cantidad de commits que deseamos visualizar.
- git log README.md: me permite visualizar los commits sobre este archivo.
- git commit --amend: nos permite enmendar un error o corregir el mensaje de commit.
- git add . luego git commit --amend: esto es para casos en los que se nos olvido agregar uno de dos archivos al staying para luego persistirlos, primero agregamos el archivo faltante y luego corregimos el commit.
- git show: permite visualizar los cambios del ultimo commit.
- git show HEAD~1: permite visualizar los cambios del commit anterior al ultimo realizado.
- git restore info.txt: nos permite resturar cambios por ejemplo contenido en uno o mas archivos (sin commits).
- git reset info.txt: se usa cuando deseamos sacar del staying los cambios de un archivo. al hacer commit no se tomara en cuenta los cambios de este archivo hasta que los llevemos al staying y hagamos commit.
- git reset --soft HEAD~1: nos permite deshacer commits, en este caso lo hacemos con el commit anterior al actual(HEAD). remueve el commit.
- git revert HEAD: nos permite revertir un commit creando un nuevo commit, eso nos evita darle problemas a otros desarrolladores, no afectamos el historias de commits.
- git revert --continue: este comando nos ayuda a seguir con una reversion cuando al ejecutar el comando anterior tenemos algun tipo de conflicto (conflictos de union).
- git diff --staged: nos permite visualizar que archivos o que cambios estan en el area de preparacion (Que ha cambiado?).
- git branch <nombre_rama>: nos permite crear una rama aparte para agregar nuevas funcionalidad sin afectar a los archivos originales.
- git branch: los listas las ramas existentes y nos muestra en cual nos encontramos actualmente.
- git switch <nombre_rama>: moverse entre ramas.
- git switch -c <nombre_rama>: crea una nueva rama y te mueve hacia ella despues de crearla.
- git branch -d <nombre_rama>: Eliminar rama.
- git log --oneline --graph: nos permite ver los commits e historicos de cambios mostrando las ramas.
- git rebase <nombre_rama>: usado comunmente para traernos los posibles nuevos cambios de la rama main o master hacia nuestra rama de desarrollo, antes de realizar un merge de la rama en desarrollo con la main o master.
- git rebase -i HEAD~3: Este comando nos permite aplastar o hacer de muchos commits a uno solo. Aqui indicamos que tome en cuenta desde HEAD hacia atras, 3 commits, los cuales convertiriamos en uno solo.
- git stash: guardar cambios si necesidad de crear un commit, los cambios no se comparten con los demas que tambien trabajen en el mismo projecto, eso sucedera hasta que hagas un commit y un pull request. el guardado de stash es en local.
- git stash list: nos permite lo que tenemos guardado con stash.
- git stash pop: nos devuelve los cambios de stash hacia el espacio normal de trabajo y borra el contenido de stash, dejando listo el contenido o cambios para agregarlos a staying y luego al repositorio.
- git cherry-pick <commit_id>: nos permite tomar algunos commits de un conjunto de commits y aplicarlo a distintas ramas. usualmente usado para corregir errores en diferentes ramas y asi evitar hacer commits para corregir el mismo error en diferentes ramas.
- git log <nombre_rama> -n 1: con este comando podemos visualizar logs en diferentes ramas, en esta ocasion visualizamos el ultimo commit de una rama.
- git tag -a <version_o_nombre_etiqueta> -m <mensaje>: nos permite crear una etiqueta, comunmente usado para versionar software final ejemplo: dotnet 8.1.101, etc.
- git tag: nos devuelve la ultima etiqueta creada.
- git clone add <url_repository>: nos permite clonar o crear una copia de un repositorio.
- git branch -a: me permite ver todas las ramas, incluso las remotas.
- git switch <nombre_rama>: si tenemos una rama <nombre_rama> en remoto y ejectuamos el comando actual, y la rama se llama igual a una de las ramas en remoto, esta se crea en base a esa rama remota.

#### Buenas practicas
- Al crear un commit es necesario agregar un mensaje que nos de contexto, si se corrigio un error, se agrego nueva funcionalidad, etc.
- los mensajes deben ser cortos y explicar lo que hace lo que describe el commit, no lo que tu mismo hiciste.
- Tomando en cuenta lo antes mencionado, habra ocasiones donde sea necesario mayor contexto y se permiten los mensajes multilineas aunque lo ideas se mensajes cortos y concisos.
- Se recomienda usar herramientas de seguimiento las cuales generan codigos por bugs o tareas, asi puedes agregar un commit: [BUG-182849], asi despues puedes agrupar los commits realizados en relacion a una tarea o commit.
- Es recomendable usar el archivo .gitignore para evitar enviar al repositorio compilaciones o archivos pesados o paquetes que pueden ser facilmente recreados a ejecutar un comando de instalacion o para evitar subir claves o secretos a un repositorio de codigo en especial si es publico.

#### Git Flow
- Consiste en tener ramas clasificadas con propositos especificos para tener un orden de trabajo.
- Rama Principal (master o main)
- Rama de Desarrollo (dev)
- Ramas por Funcionalidades
- Ramas de Errores.
- Ramas de Errores Graves.
- Ramas de Lanzamiento (util cuando se tienen muchas versiones de un mismo software)

## Apriendiendo sobre Markdown

> Insertamos una url a mi perfil de [LinkedIn](https://www.linkedin.com/in/leomarqz)

> Insertamos una imagen:
<img width="225" height="225" alt="git" src="https://github.com/user-attachments/assets/85e5bc47-6592-4a3f-a645-970d432e8075" />


> Insertamos una tabla

|Id|Name|Email|Actions|
|--|----|-----|-------|
|1001|Elmer Marquez|leomarqz2020@gmail.com|`Edit` `Delete`|
|1002|Leonel Marquez|leomarqz@gamil.com|`Edit` `Delete`|


