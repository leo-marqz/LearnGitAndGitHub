
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

#### Buenas practicas
- Al crear un commit es necesario agregar un mensaje que nos de contexto, si se corrigio un error, se agrego nueva funcionalidad, etc.
- los mensajes deben ser cortos y explicar lo que hace lo que describe el commit, no lo que tu mismo hiciste.
- Tomando en cuenta lo antes mencionado, habra ocasiones donde sea necesario mayor contexto y se permiten los mensajes multilineas aunque lo ideas se mensajes cortos y concisos.
- Se recomienda usar herramientas de seguimiento las cuales generan codigos por bugs o tareas, asi puedes agregar un commit: [BUG-182849], asi despues puedes agrupar los commits realizados en relacion a una tarea o commit.