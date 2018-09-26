# Tutorial de Git

## Configuracion incial

1. **Nombre del administrador:**
`git config --global user.name "Francisco Berchez Moreno"`

2. **Correo electronico:**
`git config --global user.email i72bemof@uco.es`

3. **Editor de texto:**
`git config --global core.editor "gedit"`

4. **Color de la interfaz:**
`git config --global color.ui true`

5. **Listado de la configuracion:**
`git config --list`


## Comandos basicos I

1. **Iniciar repositorio en un directorio:**
`git init`

2. **Agregar cambios al area de *staging*:**
`git add`

3. **Validar cambios en el repositorio:**
`git commit -m "Mensaje"`

4. **Hacer los dos pasos anteriores en uno:**
`git commit -am "Mensaje"`

5. **Historial de commits:**
`git log`


# Comandos basicos II

1. **Ayuda del listado anterior:**
`git help log`

2. **Listar los 5 commits más recientes:**
`git log -n 5`

3. **Listar los commits desde una fecha:**
`git log --since=2018-09-18`

4. **Listar los commits por autor:**
`git log --author="Francisco"`

5. **Ver cambios en el directorio:**
`git status`

## Comandos basicos III

1. **Ver diferencia entre ficheros en el directorio y el repositorio de git:**
`git diff`

2. **Ver diferencia entre ficheros en el staging y el repositorio:**
`git diff --staged`

3. **Eliminar archivos:**
   ~~~
   git rm archivo
   git commit -m "Mensaje"
   ~~~

4. **Mover o renombrar archivos:**
   ~~~
   git mv antiguo nuevo
   git commit -m "Mensaje"
   ~~~


## Comandos basicos IV

1. **Deshacer cambios con git:**
`git checkout -- nombre_fichero`

2. **Retirar archivos del *staging*:**
`git reset HEAD nombre_fichero`

3. **Completar último commit:**
`git commit --amend -m "Mensaje"`

4. **Recuperar version de un fichero de commit antiguo:**
`git checkout <id_commit> -- nombre_archivo`

5. **Revertir un commit:**
`git revert <id_commit>`

## Comandos básicos V

1. **Deshacer múltiples cambios en el repositorio:**
   ~~~
   git reset --soft <id_commit>
   git reset --mixed <id_commit>
   git reset --hard <id_commit>
   ~~~

2. **Listar archivos que git no controla:**
`git clean -n`

3. **Eliminar archivos que git no controla:**
`git clean -f`

4. **Ignorar archivos en el repositorio:**
`gitignore`

## Comandos básicos VI

1. **Examinar el contenido de un commit:**
   ~~~
   git ls-tree master
   git ls-tree master^^^
   git ls-tree master~3
   ~~~

2. **Log en una línea:**
`git log --oneline`

3. **Log con los tres últimos commits en una línea:**
`git log --oneline -3`

4. **Para más opciones consultar documentación de git.**

## Comandos básicos VII

1. **Examinar contenido de un commit:**
`git show <id>`

2. **Comparar un commit con el actual:**
`git diff <id> nombre_archivo`

3. **Comparar dos commits:**
`git diff id..id nombre_archivo`

# Ramas o *Branches*

## Comandos Ramas I

1. **Ver listado de ramas:**
`git branch`

2. **Crear una rama:**
`git branch nombre_rama`

3. **Cambiarnos a una rama:**
`git checkout nombre_rama`

4. **Crear una rama y moverse en un paso:**
`git checkout -b nombre_rama`

5. **Comparar ramas:**
`git diff nombre_rama..nombre_rama`

## Comandos Ramas II

1. **Ver ramas idénticas a la actual:**
`git branch --merged`

2. **Renombrar ramas:**
`git branch -m nombre_antiguo nombre_nuevo`

3. **Eliminar ramas:**
   ~~~
   git branch -d nombre_rama
   git branch -D nombre_rama
   ~~~

4. **Integrar ramas a la actual:**
`git merge nombre_rama`

5. **Resolver conflictos *(se suele hacer manualmente)*:**
`git merge --abort`

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

# Operaciones con *branches* remotos

* **Creación**
	* Crear *branch* local.
	* Hacer cambios en dicho *branch*.
	* Hacer commit.
	* Copiar el *branch* al repositorio remoto:
	`git push -u origin branch_remoto`

* **Copia:**
`git checkout -b local remoto`

* **Eliminación:**
`git push origin --delete branch_remoto`
	

