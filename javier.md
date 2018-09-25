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

##Comando básicos VI

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

#Ramas o *Branches*

##Comandos Ramas I

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




