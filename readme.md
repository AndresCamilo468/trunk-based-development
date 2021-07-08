# Trunk Based Development

*Repositorio de prueba para entender el manejo de branches usado en Trunk Based Development*


## Rebase para actualizar feature-branch 

Si se tienen cambio en el trunk (rama principal) y se desea actualizar la rama actual y simular una historia perfecta, se usa rebase.

```
#actualizar repositorio local (pull: mala practica)
git fetch --all -p

#rebase
git rebase origin/master


#si aparecen conflictos solucionarlos y usar
git add .
git rebase --continue

```



## Stash para cambios pendientes
Si se necesita realizar una integracion, pero hay cambios pendientes se puede usar stash

```
#guardar cambios
git stash

#realizar Integracion
git fetch --all -p
git rebase origin/master

#recuperar cambios
git stash pop


#atajos
git rebase origin/master --autostash
```





