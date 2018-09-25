## Comandos Ramas III

1. **Almacenar cambios temporales:**
`git stash save "Mensaje"`

2. **Listar cambios:**
`git stash list`

3. **Ver contenido de un cambio temporal:**
`git stash show -p nombre_stash`

4. **Eliminar un cambio temporal:**
`git stash drop nombre_stash`

5. **Aplicar cambio del stash:**
   ~~~
   git stash apply nombre_stash
   git stash pop nombre_stash
   ~~~
