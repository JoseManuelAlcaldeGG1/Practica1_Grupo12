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



