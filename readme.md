# Trunk Based Development
*Repositorio de prueba para entender el manejo de branches usado en Trunk Based Development*



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
