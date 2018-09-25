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

# GitHub

![Imagen github](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRuW2rqf0Lw3E_kvxt7EFX9Y7C0o6Fba2UNpi_NCQayJ13AC0GI8Q)

## Comandos GitHub I

1. **Añadir repositorio remoto:**
`git remote add origin url`

2. **Ver repositorios remotos:**
`git remote -v`

3. **Eliminar repositorio remoto:**
`git remote rm origin`

4. **Añadir cambios del repositorio local al remoto:**
`git push -u origin master`

5. **Añadir cambios del repositorio remoto al local:**
`git pull`

## Comandos GitHub II

1. **Ver branches remotos:**
`git branch -r`

2. **Ver todos los *branches*:**
`git branch -a`

3. **Clonar un repositorio remoto:**
`git clone url`

# Dar seguimiento a todos los *branches*:

* **LOCAL --> REMOTO**
	* Cambios en el repositorio local.
	* Commit de los cambios.
	* Añadir cambios de un repositorio remoto:
	`git push`

* **REMOTO --> LOCAL**
	* Sincronización y unión:
	~~~
	git fetch origin
	git merge origin/master
	~~~
	* En un solo paso:
	`git pull`
	

