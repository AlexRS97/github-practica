11) Deshacer el último commit (perdiendo los cambios realizados en el working copy) 

git reset --hard HEAD ~ 1

¿Qué comando utilizaste en el paso 11? ¿Por qué?

Utilice el comando git reset --hard HEAD ~ 1 porque deshace el último commit realizado eliminando los cambios que hay en el working copy

--------------------------------------------------------------------------------------------------------------------------------------

12) Rehacer el último commit (el que acabamos de deshacer)

git reflog
git reset --hard 66eb956

¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

uso git reflog para poder ver todo el trabajo que hemos realizado y asi poder localizar el identificador que quiero para poder volver al punto del commit anterior, y con el comando git reset --hard 66eb956 vuelvo a ese punto asi vuelvo
al commit que habia deshecho

--------------------------------------------------------------------------------------------------------------------------------------

13) Hacer un merge con ‘main’ (styled absorbe a main)

git merge main

El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

estando en la rama styled ejecutamos git merge main para que styled absorba la rama main

--------------------------------------------------------------------------------------------------------------------------------------

19) Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)

git checkout styled
git merge htmlify

El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si creo un conflicto, al mergear las ramas ya que ambas tienen el archivo git-nuestro.md, pero en el caso de la rama htmlify este archivio estaba modificado y por lo tanto los archivos eran distintos.

--------------------------------------------------------------------------------------------------------------------------------------

21) Desde “main”, hacer un merge con “styled”

git checkout main
git merge styled

El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

Creo recordar que el archivo que habia en al rama main y el que hay en la rama styled, no eran el mismo, por lo cual si que creo un conflicto al hacer el merge.

--------------------------------------------------------------------------------------------------------------------------------------

25) Dibujar el diagrama

¿Qué comando o comandos utilizaste en el paso 25?

use el siguiente comando git log --graph --decorate --pretty=oneline

--------------------------------------------------------------------------------------------------------------------------------------

26) Hacer un merge “no fast-forward” de “title” en “main” (main absorbe a title)

git merge --no-ff title

El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí podría ser fast fordware por que en la rama main no teníamos un commit por encima que se quedase fuera y provocase una bifurcación, sino que directamente en la rama main al crear una rama nueva llamada title, esto hace que pudieses haber escalado por esa misma rama usando el fast forward.

--------------------------------------------------------------------------------------------------------------------------------------

27) Deshacer el merge (sin perder los cambios del working copy)

¿Qué comando o comandos utilizaste en el paso 27?

git reset HEAD~1 este comando consigue deshacer los cambios sin perder lo que teniamos en el working copy

--------------------------------------------------------------------------------------------------------------------------------------

28) Descartar los cambios

¿Qué comando o comandos utilizaste en el paso 28?

git restore . se utiliza para restaurar todos los archivos modificados en tu directorio de trabajo a su último estado confirmado

--------------------------------------------------------------------------------------------------------------------------------------

29) Eliminar la rama “title”

¿Qué comando o comandos utilizaste en el paso 29?

git branch -D title este comando borra la rama title

--------------------------------------------------------------------------------------------------------------------------------------

30) Rehacer el merge que hemos deshecho

¿Qué comando o comandos utilizaste en el paso 30?

git reflog // con este comando compruebo todo el trabajo que se ha realizado para poder localizar el identificador que necesito
git checkout 1684ed8 // con este comando voy al paso al que quiero volver
git checkout -b title // creo la rama title y me muevo hacia ella
git checkout main // vuelvo a main
git merge --no-ff title // hago un merge no fast-forward con title

--------------------------------------------------------------------------------------------------------------------------------------

32) Volver al commit inicial cuando se creó el poema

¿Qué comando o comandos usaste en el paso 32?

git log // compruebo la lista de commits realizados
git checkout 66eb956b9e21e5ca35b7d1a11193a9bf4667c84f // me muevo al commit solicitado

--------------------------------------------------------------------------------------------------------------------------------------

33) Volver al estado final, cuando pusimos título al poema

¿Qué comando o comandos usaste en el punto 33?

git log // compruebo la lista de commits realizados
git checkout 1684ed802d034b7b185dc3727c71a4b7b2497f73 // me muevo al commit solicitado

FIN

--------------------------------------------------------------------------------------------------------------------------------------
