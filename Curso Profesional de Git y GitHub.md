# Curso Profesional de Git y GitHub
### Introducción a la terminal y línea de comandos

Lista de comandos basicos para el uso del terminal.

| Comando | Descripción |
| ------ | ------ |
| ```$cd + ~``` o ```cd /``` | Ruta principal del user. |
| ctrl + L | Para borrar. |
| ```$ls -al``` | Argumento o traer argumento.|
| ```$cd ("direccion de ka carpeta seguido de un /")``` | Para la moverte entre directorios|
| ```$ls``` | Abrir  directorios.|
| ```$cd ..``` | Para retroceder.|
| ```$pwd``` | Para saber en que carpeta estoy.|
| ```$mkdir ("el nombre de la carpeta")``` | Para crear una carpeta.|
| ```$clear``` o ```$ls``` | Limpiar la consoala.|
| ```$touch (vacio.txt)``` | Crear un archivo nuevo.|
| ```$cat ("nombre del archivo")``` |  Muestra el contenido del archivo.|
| ```$history``` | Log de comandos escritos. |
| ```!("numero del comando que deseas repetir")``` | Repetir el comando o accion.|
| ```$rm ("archivo que quieres borrar")``` | Borrar archivos.|
| ```$rm -rf ("carpeta quieres borrar")``` | Borrar carpetas con todos sus archivos.|
| ```$rm --help``` | Muestra un resument del uso de cada comando.|

### Conceptos Basicos de Git

- Master: Esta es la rama donde se inicia siempre por defecto (se le puede asignar cualquier nombre), a partir de esta rama se crean todas las ramas, en esta rama estan todos los cambios de tus archivos.
- Commit: Cada vez que haces una nueva rama lo único que se hace es que copias un commit, que pasa a la rama de a lado, en la cual puedes continuar trabajando sin afectar el flujo de trabajo principal que esta en la rama master. cambios para después probarlo en tu rama master.
- Checkout: Crea una nueva rama.
- Merge: Une dos ramas

##### Comandos Basicos de git

Lista de comandos basico que debes manejar al empezar git.

| Comando | Descripción |
| ------ | ------ |
| ```$git init```  | inicializar el repositorio. |
| ```$git add nombre_de_archivo.extencion```  | Agregar el archivo al repositorio. |
| ```$git commit -m “Mensaje”``` |  Agregamos los cambios para el repositorio. |
| ```$git add .``` |  Agregar los cambios de la carpeta en la que nos encontramos agregar todo. |
| ```$git status``` |  visualizar cambios. |
| ```$git log nombre_de_archivos.extencion``` | historico de cambios con detalles. |
| ```$git push```  | envia a otro repositorio remoto lo que estamos haciendo. |
| ```$git pull``` | traer repositorio remoto. |
| ```$git checkout``` | traer cambios realizado. |
| ```$git rm --cached archivo.extencion``` | se usa para devolver el archivo que se tiene en ram cuando escribimos git add lo devuleve a estado natural mientra esta en staging. |
| ```$git config --list``` | muestra la lista de configuracion de git. |
| ```$git config --list --show-origin``` | rutas de acceso a la configuración de git. |
| ```$git log archivo.extencion``` | muestra la historia del archivo. |
| ```$git rm --cached``` | Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro. |
| ```$git rm --force``` | Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados). |

```$git diff _tag1_ _tag2_```
- Hace la comparativa de cambios entre el archivo en su etapa en el commit del tag1 y del tag2. Considera al más reciente como tag2 y al anterior como tag1, SI IMPORTA EL ORDEN DE LOS TAGS

### Volver en el tiempo nuestro Repositorio utilizando reset y checkout

```$git reset #commit --soft```
- Volvemos nuestro archivo a la versión del commit indicada, pero sin borrar los commits usados anteriormente. Mantenemos lo que tengamos en stagin ($git add) disponible para un siguiente commit.

```$git reset #commit --hard```
- ES MUY PELIGROSO, Volvemos nuestro archivo a la versión del commit indicada, BORRANDO TODOS los commits usados anteriores a la versión del commit indicado.

```$git reset HEAD```
- Este es el comando para sacar archivos del área de Staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con git add, por supuesto.

```$git checkout #commit archivo.txt```
- Volvemos nuestro archivo a la versión del commit indicado, sin cambiar nada en el Staging.

##### Ver y personalizar mas detalles en $git log

Algunos comandos que pueden ayudar cuando colaboren con proyectos muy grandes de github:

| Comando | Descripción |
| ------ | ------ |
| ```$git log --oneline``` | Te muestra el id commit y el título del commit|
| ```$git log --decorate``` | Te muestra donde se encuentra el head point en el log.|
| ```$git log --stat``` | Explica el número de líneas que se cambiaron brevemente.|
| ```$git log -p``` | Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido. |
| ```$git shortlog```| Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits. |
| ```$git log --graph --oneline --decorate``` y ```$git log --pretty=format:"%cn hizo un commit %h el dia %cd"``` | Muestra mensajes personalizados de los commits. |
| ```$git log -3``` | Limitamos el número de commits. |
| ```$git log --after=“2018-1-2”```, ```$git log --after=“today”``` y ```$git log --after=“2018-1-2” --before=“today”``` | Commits para localizar por fechas.|
| ```$git log --author=“Name Author”``` | Commits realizados por autor que cumplan exactamente con el nombre. |
| ```$git log --grep=“INVIE”``` | Busca los commits que cumplan tal cual está escrito entre las comillas. |
| ```$git log --grep=“INVIE” –i``` | Busca los commits que cumplan sin importar mayúsculas o minúsculas. |
| ```$git log – index.html``` | Busca los commits en un archivo en específico|
| ```$git log -S “Por contenido”``` | Buscar los commits con el contenido dentro del archivo. |
| ```$git log > log.txt``` | Guardar los logs en un archivo txt. |

### Introduccion a las ramas o branches de Git

| Comando | Descripción |
| ------ | ------ |
| ```$git commit -am “MENSAJE”``` | Agrega y manda el mensaje es decir hace la función de ```$git add``` y ```$git commit -m``` al mismo tiempo, este solo aplica para archivos ya trackeados en el repositorio. |
| ```$git branch nombre_rama``` | Se crea la rama teniendo en cuenta que uno se debe de posicionar en la rama que se necesita copiar. |
| ```$git branch -l``` | Lista todas las ramas que existen. |
| ```$git branch -d nombre_rama``` | Elimina la rama nombre_rama. Con -D se fuerza el borrado. |
| ```$git branch -m nombre_rama rama_nueva``` | Permite renombrar una rama nombre_rama por rama_nueva. |
| ```$git checkout nombre_rama``` | Aqui se cambia la rama que se le indico. |

### Fusión de ramas con Git merge

Desde la Rama en la que estoy me traigo los cambios de otra rama con:
$git merge nombre_de_la_rama

Algunos comandos que están en el libro Pro Git de utilidad

| Comando | Descripción |
| ------ | ------ |
| ```$git branch –v``` | Muestra el último commit de cada rama. |
| ```$git branch --merged``` | Lista las ramas que se fusionaron conla rama actual. |
| ```$git branch --no-merged``` | Lista las ramas que nose han fusionado conla rama actual. |
| ```$git merge --abort``` | Anula el merge y devuelve todo a como estaba antes. |

### Uso de GitHub

| Comando | Descripción |
| ------ | ------ |
| ```$git remote add origin (url)```| |
| ```$git remote``` | Muestra el origen |
| ```$git remote -v``` | Es verval |
| ```$git pull origin master --allow-unrelated-histories``` | Fuerza la union de las diferentes historias |
| ```$git pull origin master``` | Descarga cambios |
| ```$git push (origin) (master)``` | Sube Cambios |

### Tags y versiones en Git y GitHub

| Comando | Descripción |
| ------ | ------ |
| ```$git tag -a nombre-del-tag id-del-commit``` | Crear un nuevo tag y asignarlo a un commit |
| ```$git tag -d nombre-del-tag``` | Borrar un tag en el repositorio local |
| ```$git tag o $git show-ref --tags``` | Listar los tags de nuestro repositorio local |
| ```$git push origin --tags``` | Publicar un tag en el repositorio remoto |
| ```$git tag -d nombre-del-tag``` y ```$git push origin :refs/tags/nombre-del-tag``` | Borrar un tag del repositorio remoto |

###Pull request

Es una funcionalidad de github (en gitlab llamada merge request y en bitbucket push request), en la que un colaborador pide que revisen sus cambios antes de hacer merge a una rama, normalmente master.

Al hacer un pull request se genera una conversación que pueden seguir los demás usuarios del repositorio, así como autorizar y rechazar los cambios.

El flujo del pull request es el siguiente

1. Se trabaja en una rama paralela los cambios que se desean (```$git checkout -b <rama>```)
2. Se hace un commit a la rama (```$git commit -am '<Comentario>'```)
3. Se suben al remoto los cambios (```$git push origin <rama>```)
4. En GitHub se hace el pull request comparando la rama master con la rama del fix.
5. Uno, o varios colaboradores revisan que el código sea correcto y dan feedback (en el chat del pull request)
6. El colaborador hace los cambios que desea en la rama y lo vuelve a subir al remoto (automáticamente jala la historia de los cambios que se hagan en la rama, en remoto)
7. Se aceptan los cambios en GitHub
8. Se hace merge a master desde GitHub
**Importante**: Cuando se modifica una rama, también se modifica el pull request.

### Stashed

El stashed nos sirve para guardar cambios para después, Es una lista de estados que nos guarda algunos cambios que hicimos en Staging para poder cambiar de rama sin perder el trabajo que todavía no guardamos en un commit
Ésto es especialmente útil porque hay veces que no se permite cambiar de rama, ésto porque porque tenemos cambios sin guardar, no siempre es un cambio lo suficientemente bueno como para hacer un commit, pero no queremos perder ese código en el que estuvimos trabajando.

El stashed nos permite cambiar de ramas, hacer cambios, trabajar en otras cosas y, más adelante, retomar el trabajo con los archivos que teníamos en Staging pero que podemos recuperar ya que los guardamos en el Stash.

#####git stash

El comando git stash guarda el trabajo actual del Staging en una lista diseñada para ser temporal llamada Stash, para que pueda ser recuperado en el futuro.

Para agregar los cambios al stash se utiliza el comando:
```$git stash```
Podemos poner un mensaje en el stash, para asi diferenciarlos en git stash list por si tenemos varios elementos en el stash. Ésto con:
```$git stash save "mensaje identificador del elemento del stashed"```

#####Obtener elelmentos del stash

El stashed se comporta como una Stack de datos comportándose de manera tipo LIFO (del inglés Last In, First Out, «último en entrar, primero en salir»), así podemos acceder al método pop.

El método pop recuperará y sacará de la lista el último estado del stashed y lo insertará en el staging area, por lo que es importante saber en qué branch te encuentras para poder recuperarlo, ya que el stash será agnóstico a la rama o estado en el que te encuentres, siempre recuperará los cambios que hiciste en el lugar que lo llamas.

Para recuperar los últimos cambios desde el stash a tu staging area utiliza el comando:

```$git stash pop```

Para aplicar los cambios de un stash específico y eliminarlo del stash:

```$git stash pop stash@{<num_stash>}```

Para retomar los cambios de una posición específica del Stash puedes utilizar el comando:

```$git stash apply stash@{<num_stash>}```
Donde el <num_stash> lo obtienes desden el git stash list

#####Listado de elementos en el stash

Para ver la lista de cambios guardados en Stash y así poder recuperarlos o hacer algo con ellos podemos utilizar el comando:

```$git stash list```

Retomar los cambios de una posición específica del Stash || Aplica los cambios de un stash específico

#####Crear una rama con el stash

Para crear una rama y aplicar el stash mas reciente podemos utilizar el comando

```$git stash branch <nombre_de_la_rama>```

Si deseas crear una rama y aplicar un stash específico (obtenido desde git stash list) puedes utilizar el comando:

```$git stash branch nombre_de_rama stash@{<num_stash>}```

Al utilizar estos comandos crearás una rama con el nombre <nombre_de_la_rama>, te pasarás a ella y tendrás el stash especificado en tu staging area.

#####Eliminar elementos del stash

Para eliminar los cambios más recientes dentro del stash (el elemento 0), podemos utilizar el comando:

```$git stash drop```

Pero si en cambio conoces el índice del stash que quieres borrar (mediante git stash list) puedes utilizar el comando:

```$git stash drop stash@{<num_stash>}```

Donde el <num_stash> es el índice del cambio guardado.
Si en cambio deseas eliminar todos los elementos del stash, puedes utilizar:

```$git stash clear```

Consideraciones:

El cambio más reciente (al crear un stash) SIEMPRE recibe el valor 0 y los que estaban antes aumentan su valor.

Al crear un stash tomará los archivos que han sido modificados y eliminados. Para que tome un archivo creado es necesario agregarlo al Staging Area con git add [nombre_archivo] con la intención de que git tenga un seguimiento de ese archivo, o también utilizando el comando git stash -u (que guardará en el stash los archivos que no estén en el staging).
Al aplicar un stash este no se elimina, es buena práctica eliminarlo.

### Git Clean: limpiar tu proyecto de archivos no deseados

A veces creamos archivos cuando estamos realizando nuestro proyecto que realmente no forman parte de nuestro directorio de trabajo, que no se deberían agregar y lo sabemos.

- Para saber qué archivos vamos a borrar tecleamos ```$git clean --dry-run```
- Para borrar todos los archivos listados (que no son carpetas) tecleamos ```$git clean -f```
- Para borrar todos los archivos y carpetas listadas tecleamos ```$git clean -df```

### Git cherry-pick: traer commits viejos al head de un branch

Este comando permite coger uno o varios commits de otra rama sin tener que hacer un merge completo. Así, gracias a cherry-pick, podríamos aplicar los commits relacionados con nuestra funcionalidad de Facebook en nuestra rama master sin necesidad de hacer un merge.

Para demostrar cómo utilizar git cherry-pick, supongamos que tenemos un repositorio con el siguiente estado de rama:

```
a - b - c - d   Master
         \
           e - f - g Feature
```
El uso de git cherry-pick es sencillo y se puede ejecutar de la siguiente manera:

```$git checkout master```

En este ejemplo, commitSha es una referencia de confirmación. Puedes encontrar una referencia de confirmación utilizando el comando git log. En este caso, imaginemos que queremos utilizar la confirmación ‘f’ en la rama master. Para ello, primero debemos asegurarnos de que estamos trabajando con esa rama master.

```$git cherry-pick f```

Una vez ejecutado, el historial de Git se verá así:

```
a - b - c - d - f   Master
         \
           e - f - g Feature
```

La confirmación f se ha sido introducido con éxito en la rama de funcionalidad

### Reconstruir commits en Git con amend

Puede modificar el commit más reciente (enmendar) en la misma rama ejecutando:

```$
$git add -A # Para hacer uso de ammend los archivos deben de estar en staging
$git commit --amend # Remendar último commit
```
Este comando sirve para agregar archivos nuevos o actualizar el commit anterior y no generar commits innecesarios.

También es una forma sencilla de editar o agregar comentarios al commit anterior porque abrirá la consola para editar el commit anterior.

Nota: Es una mala práctica hacer ammend de un commit que ya ha sido pusheado o pulleado del repositorio remoto, al momento de hacer ammend con algún commit que esté en remoto va a generar un conflicto que se va a arreglar haciendo un commit adicional y se perderá el beneficio del ammend.

### Git Reset y Reflog: úsese en caso de emergencia

##### Git nunca olvida, git reflog

Git guarda todos los cambios aunque decidas borrarlos, al borrar un cambio lo que estás haciendo sólo es actualizar la punta del branch, para gestionar éstas puntas existe un mecanismo llamado registros de referencia o reflogs.

La gestión de estos cambios es mediante los hash’es de referencia (o ref) que son apuntadores a los commits.

Los recoges registran cuándo se actualizaron las referencias de Git en el repositorio local (sólo en el local), por lo que si deseas ver cómo has modificado la historia puedes utilizar el comando:

```$git reflog```

Muchos comandos de Git aceptan un parámetro para especificar una referencia o “ref”, que es un puntero a una confirmación sobre todo los comandos:
git checkout Puedes moverte sin realizar ningún cambio al commit exacto de la ref

```$git checkout eff544f```

git reset: Hará que el último commit sea el pasado por la ref, usar este comando sólo si sabes exactamente qué estás haciendo

```
$git reset --hard eff544f # Perderá todo lo que se encuentra en staging y en el Working directory y se moverá el head al commit eff544f
$git reset --soft eff544f # Te recuperará todos los cambios que tengas diferentes al commit eff544f, los agregará al staging area y moverá el head al commit eff544f
```

git merge: Puedes hacer merge de un commit en específico, funciona igual que con una branch, pero te hace el merge del estado específico del commit mandado

```
$git checkout master
$git merge eff544f # Fusionará en un nuevo commit la historia de master con $el momento específico en el que vive eff544f
```

### Buscar en archivos y commits de Git con Grep y log

| Comando | Descripción |
| ------ | ------ |
|```$git grep color``` | Use la palabra color |
|```$git grep la``` | Donde use la palabra la |
|```$git grep -n color``` | En que lineas use la palabra color |
|```$git grep -n platzi``` | En que lineas use la palabra platzi |
|```$git grep -c la``` | Cuantas veces use la palabra la |
|```$git grep -c paltzi``` | Cuantas veces use la palabra platzi |
|```$git grep -c “<p>”``` | Cuantas veces use la etiqueta <p> |
|```$git log-S “cabecera”``` | Cuantas veces use la palabra cabecera en
todos los commits.|
|grep| Para los archivos|
|log | Para los commits.|

### Comandos y recursos colaborativos en Git y GitHub

| Comando | Descripción |
| ------ | ------ |
|```$git shortlog```| Ver cuantos commits a hecho los miembros del equipo|
|```$git shortlog -sn```| Las personas que han hecho ciertos commits|
|```$git shortlog -sn --all```| Todos los commits (también los borrados)|
|```$git shortlog -sn --all --no-merges```| muestra las estadisticas de los comigs del repositorio donde estoy|
|```$git config --global alias.<nombre_del_alias> “<comando_a_invocar_con_alias>”```| configura el comando, ejemplo para ```$git config --global alias.stats “shortlog -sn --all --no-merges”``` “shortlog -sn --all --no-merges” en un Alias en las configuraciones globales de git del pc|
|```$git blame -c blogpost.html```| Muestra quien ha hecho cambios en dicho archivo identado|
|```$git blame --help```| Muestra en el navegador el uso del comando|
|```$git blame archivo -L 35, 60 -c```| Muestra quien escribio el codigo con informacion de la linea 35 a la 60, EJ: git blame css/estilos.css -L 35, 60 -c|
|```$git branch -r```| Muestra las Ramas remotas de GitHub|
|```$git branch -a```| Muestra todas las Ramas del repo y remotas de GitHub|