
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