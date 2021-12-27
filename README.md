# _Git y Github_

## ¿Qué es Git?   
Es un Sistema que “Controla Versiones” (Version Control System - VCS)   
Un software que permite seguir y manipular distintas versiones de un mismo archivo.
En resumen, permite manejar distintas versiones de un programa, archivo, etc para poder acceder a las distintas versiones, combinarlas, deshacer cambios.



## ¿Qué es Github?  
Es un servicio que contiene distintos repositorios Git en una nube, permite trabajar en conjunto con otras personas y utilizar sus versiones de archivos y/o programas.  

****
***
***
***

* ## _Comandos de terminal_:
  * ls – muestra el contenido de la dirección en la que estamos (carpeta)
  * pwd – muestra la dirección en la que estamos  
  * open . – Abre una ventana de la dirección en la que estamos
  * start .  – Lo mismo que open . pero para Windows.
  * cd – Permite navegar entre las direcciones.
  * cd .. – Volvemos una dirección atrás.
  * touch – crear archivos
  * mkdir – crear carpetas
  * rm – Eliminar permanentemente archivos.
  * rm -rf – Elimina permanentemente carpetas.

  

* ## _[Comandos de GIT](https://git-scm.com/docs)_:
  * ### _Inicio y revision:_
    * **git init** – Inicia un repositorio (archivos GIT)
    * **git status** – Muestra el estado de los archivos que analiza el repositorio
  * ### _Guardados o checkpoints (commit):_
    * **git add** – Agrega cambios realizados en los archivos a la lista previa al “commit”
    * **git commit** – Realiza el “guardado” de los archivos modificados, una especie de checkpoint.
    * **git commit** –a –m <Nombre> - Realiza el “add” y el “commit” poniendo un nombre al commit
    * **git commit** –amend – Permite agregar cambios al ULTIMO punto “commit” realizado.
    * **git log** – Permite ver todos los puntos commit en el repositorio (Con todos los datos como dirección en la memoria, comentarios, etc.)
    * **git log** – – oneline – Permite ver los cambios en el repositorio de forma resumida.
  * ### _Creacion y manejo de ramas (branches):_
    * **git branch** – Muestra los “Branch” (Ramas) del proyecto.
    * **git branch <Nombre>** - Crea un “Branch” nuevo en el proyecto.
    * **git branch –m <Nombre>** - Renombrar un Branch
    * **git branch –d <Nombre>** - Borra el Branch
    * **git switch <Nombre>** - Cambia el HEAD (Puntero) a la dirección del Branch seleccionado.
  * ### _Comparacion (Diff):_
    * **git diff**  - Muestra las diferencias entre el “stage” y los cambios en proceso.
    * **git diff HEAD**- Muestra todos los cambios dentro y fuera del stage
    * **git diff - - staged**- Muestra solo los cambios en stage
    * **git diff <Nombre archivo>**- Muestra solo los cambios de un archivo entre el stage y los actuales
    * **git diff < branch1 >. .< branch2>** - Analiza los cambios de todos los archivos de 2 branches
    * **git diff < Commit1 >. .< Commit2>** - Analiza los cambios de todos los archivos de 2 Commits
  * ### _Ocultando/Guardando/Posponiendo (Stashing)_
    * **git stash** - "Guarda" o almacena los archivos que aun no se guardaron en un commit en una "carpeta" o direccion de almacenamiento oculta. Esconde archivos.  
    * **git stash pop** - Devuelve y saca los archivos guardados en modo stash.
    * **git stash apply** - Devuelve los archivos pero sin sacarlos de la carpeta stash (copia y pega)
    * **git stash list** - Muestra la lista de los diferentes "stashings" hechos. Se puede acumular varias veces. 
    * **git stash drop "direccion"** - Elimina algun Stash realizado.
    * **git stash clear** - Elimina todos los stash.
 
  * ### _Rebasing (reconstruir un branch)_
    * **git rebase "nombre del branch"** - Reconstruye el historial de commits creados entre 2 ramas. La rama mas actualizada agrupa sus commits, y luego de ese punto final se inicia la otra rama en la que estoy trabajando. (Nota: usar primero git switch)

    * **git rebase -i HEAD~5** - Permite visualizar la cantidad indicada de commits anteriores, y manipularlos de distintas maneras.

  * ### _Tags (etiquetas)_
    * **git tag** - Muestra los tags
    * **git tag -l "*Nombre*"** - Muestras los tags con el nombre 
    * **git checkout "nombre del tag"** - Viaja hasta el tag
    * **git diff "tag" "otro tag"** - Diferencia entre tags
    * **git tag "Nombre"** - Crea un tag con el nombre. Son tags cortos.
    * **git tag -a "nombre"** - Crea un tag especial con el nombre (con mas detalles)
    * **git show "nombre"** - Muestra toda la informacion del tag
    * **git tag -a "nombre" #direccion del commit** - Tag para un commit especifico
     * **git tag -a "nombre" #direccion del commit -f** - Fuerza a un tag a moverse a la otra direccion
     * **git tag -d "nombre"** - Borra el tag
     * **git push --tags** - Agrega todos los tags al repositorio de github

  * ### _Config_
  * **git config usar.name "nombre"** - Configura el repositorio agregandole el nombre que se coloque
  * **git config usar.email "email"** - Configura el repositorio agregandole el email que se coloque

