# Trunk Based Development

*Repositorio de prueba para entender el manejo de branches usado en Trunk Based Development*

Se tiene a merge como la principal herramienta para mezclar cambios, esta es util pero suele tener problemas a la hora de realizar la mezcla. Para evitar errores del merge, se puede primero actualizar la rama del feature (usando rebase) con los cambios de la rama principal, aqui se solucionan los conflictos y cuando se esta seguro se realiza el merge, esto evita conflictos.

**Before:** 
  1. Merge (con conflicto)
  
**After:** 
  1. Rebase (actualizacion -> conflictos -> solventarlos)
  2. Merge (sin conflictos)

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

## Rebase Interactivo
Si se tienen muchos commit en la feature branch es posible que se busque limpiar la historia
para esto se usa rebase interactivo, interactive me permite actualziar la historia a mi manera

```
#usar rebase interactive
git rebase -i

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








