Deshacer el último commit (perdiendo los cambios realizados en el working copy) 

git reset --hard HEAD ~ 1

--------------------------------------------------------------------------------------------------------------------------------------

12) Rehacer el último commit (el que acabamos de deshacer)

git reflog
git reset --hard 66eb956

--------------------------------------------------------------------------------------------------------------------------------------

13) Hacer un merge con ‘main’ (styled absorbe a main)

git merge main

--------------------------------------------------------------------------------------------------------------------------------------

19) Hacer un merge de “htmlify” en “styled” (styled absorbe a htmlify)

git checkout styled
git merge htmlify

--------------------------------------------------------------------------------------------------------------------------------------

21) Desde “main”, hacer un merge con “styled”

git checkout main
git merge styled

--------------------------------------------------------------------------------------------------------------------------------------

25) Dibujar el diagrama

git log --graph --decorate --pretty=oneline

--------------------------------------------------------------------------------------------------------------------------------------

26) Hacer un merge “no fast-forward” de “title” en “main” (main absorbe a title)

git merge --no-ff title

--------------------------------------------------------------------------------------------------------------------------------------

27) Deshacer el merge (sin perder los cambios del working copy)

git reset HEAD~1

--------------------------------------------------------------------------------------------------------------------------------------

28) Descartar los cambios

git restore .

--------------------------------------------------------------------------------------------------------------------------------------

29) Eliminar la rama “title”

git branch -D title

--------------------------------------------------------------------------------------------------------------------------------------

30) Rehacer el merge que hemos deshecho

git reflog
git checkout 1684ed8
git checkout -b title
git checkout main
git merge --no-ff title

--------------------------------------------------------------------------------------------------------------------------------------

32) Volver al commit inicial cuando se creó el poema

git log
git checkout 66eb956b9e21e5ca35b7d1a11193a9bf4667c84f

--------------------------------------------------------------------------------------------------------------------------------------

33) Volver al estado final, cuando pusimos título al poema

git log
git checkout 1684ed802d034b7b185dc3727c71a4b7b2497f73

--------------------------------------------------------------------------------------------------------------------------------------
