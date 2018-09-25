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
