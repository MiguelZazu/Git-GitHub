# EJERCICIO 1

1. cd /RUTA CARPETA PRACTICA DONDE SE CLONA EL REPOSITORIO
git clone https://github.com/MiguelZazu/Git-GitHub

2. notepad git-nuestro.md
(entro en el notepad y copio el texto)
3. git add git-nuestro.md
git status

4. git commit -m "Añado git-nuestro"
git status

5. git branch styled

6. git branch

7. git checkout styled

8. git branch

9. (entro en el notepad y copio el texto)

10. git add git-nuestro.md
git commit -m "Estilo el git-nuestro"
git log

11. git reset --hard HEAD~1
git log
git branch
(miro el log y veo los commits, el head está en la creación de styled por lo que hay que moverlo al anterior y se hace con el comando git reset --hard HEAD~1. --hard porque queremos perder los cambios en el working copy, es decir, tener la carpeta sin el nuevo estilo)

12. git reflog
git reset --hard 78889e5
git log
(miro el reflog y veo los commits y cambios historicos de la carpeta para ver el codigo del commit al que nos queremos mover. Me muevo con el git reset y el codigo del commit es 78889e5 y añado --hard para ver el cambio en el working copy).

13. git merge main
(Already up to date.)
(No muestra ningún conflicto porque simplemente estoy moviendome entre commits y no he modificado el notepad).

14. git checkout main

15. git branch htmlify

16. git checkout htmlify

17. (entro en el notepad y copio el texto)

18. git add git-nuestro.md 
git commit -m "HTML git-nuestro"

19. git checkout styled
git merge htmlify
CONFLICT (content): Merge conflict in git-nuestro.md
Automatic merge failed; fix conflicts and then commit the result.
(Existe conflicto porque git encuentra 2 versiones del notepad, la de styled y la de htmlify, por lo que hay que eliminar del archivo la parte de styled y quedarse con la de htmify.)

20. Modifico el archivo git-nuestro.md dejando solo la parte de styled (HEAD).
git add git-nuestro.md
git commit

21. git checkout main
git merge styled
(No existe conflicto porque styled es una rama de htmlify que a su vez es y tiene el mismo archivo)

22. git branch title
git checkout title

23. git branch
(entro en el notepad y añado un titulo)
git add git-nuestro.md
git commit -m "Añado Titulo git-nuestro"

24. git checkout main

25. git log --graph --decorate --pretty=oneline

26. git merge --no-ff title
(si se podría hacer merge fast forward por que hay una ruta lineal desde el main hasta title)

27. git log
git reset d5e95ff

28. git reflog
git reset HEAD~1

29. git branch -d title

30. git reset --hard 1e1916d

31. git checkout main
git branch
git branch -d htmlify
git branch -d styled

32. git reflog
git reset --hard 3d5cc99

33. git reflog
git reset --hard 1e1916d

34. git reflog
git reset 3d5cc99
git tag inicial
git reflog
git reset 78889e5
git tag styled
git reflog
git reset ffee5b4
git tag htmlify
git reflog
git reset 1e1916d
git tag title

35. git checkout htmlify

36. git checkout main

37. git push -u origin main
git push origin --tags
