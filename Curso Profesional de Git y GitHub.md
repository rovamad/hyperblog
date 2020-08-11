# Curso Profesional de Git y GitHub
### Introducción a la terminal y línea de comandos

Lista de comandos basicos para el uso del terminal.

| Comando | Descripción |
| ------ | ------ |
| cd + ~ o cd / | Ruta principal del user. |
| ctrl + L | Para borrar. |
| ls -al | Argumento o traer argumento.|
| cd ("direccion de ka carpeta seguido de un /") | Para la moverte entre directorios|
| ls  | Abrir  directorios.|
| cd .. | Para retroceder.|
| pwd | Para saber en que carpeta estoy.|
| mkdir ("el nombre de la carpeta") | Para crear una carpeta.|
| clear o ls | Limpiar la consoala.|
| touch (vacio.txt) | Crear un archivo nuevo.|
| cat ("nombre del archivo") |  Muestra el contenido del archivo.|
| history | Log de comandos escritos. |
| !("numero del comando que deseas repetir") | Repetir el comando o accion.|
| rm ("archivo que quieres borrar") | Borrar archivos.|
| rm -rf ("carpeta quieres borrar") | Borrar carpetas con todos sus archivos.|
| rm --help | Muestra un resument del uso de cada comando.|

### Conceptos Basicos de Git

- Master: Esta es la rama donde se inicia siempre por defecto (se le puede asignar cualquier nombre), a partir de esta rama se crean todas las ramas, en esta rama estan todos los cambios de tus archivos.
- Commit: Cada vez que haces una nueva rama lo único que se hace es que copias un commit, que pasa a la rama de a lado, en la cual puedes continuar trabajando sin afectar el flujo de trabajo principal que esta en la rama master. cambios para después probarlo en tu rama master.
- Checkout: Crea una nueva rama.
- Merge: Une dos ramas

##### Comandos Basicos de git

Lista de comandos basico que debes manejar al empezar git.

| Comando | Descripción |
| ------ | ------ |
| $git init  | inicializar el repositorio. |
| $git add nombre_de_archivo.extencion  | Agregar el archivo al repositorio. |
| $git commit -m “Mensaje” |  Agregamos los cambios para el repositorio. |
| $git add . |  Agregar los cambios de la carpeta en la que nos encontramos agregar todo. |
| $git status  |  visualizar cambios. |
| $git log nombre_de_archivos.extencion  | historico de cambios con detalles. |
| $git push  | envia a otro repositorio remoto lo que estamos haciendo. |
| $git pull  | traer repositorio remoto. |
| $ checkout  | traer cambios realizado. |
| $git rm --cached archivo.extencion | se usa para devolver el archivo que se tiene en ram cuando escribimos git add lo devuleve a estado natural mientra esta en staging. |
| $git config --list  | muestra la lista de configuracion de git. |
| $git config --list --show-origin | rutas de acceso a la configuración de git. |
| $git log archivo.extencion  | muestra la historia del archivo. |
| $git rm --cached  | Elimina los archivos del área de Staging y del próximo commit pero los mantiene en nuestro disco duro. |
| $git rm --force  | Elimina los archivos de Git y del disco duro. Git siempre guarda todo, por lo que podemos acceder al registro de la existencia de los archivos, de modo que podremos recuperarlos si es necesario (pero debemos usar comandos más avanzados). |

```$git diff _tag1_ _tag2_```
- Hace la comparativa de cambios entre el archivo en su etapa en el commit del tag1 y del tag2. Considera al más reciente como tag2 y al anterior como tag1, SI IMPORTA EL ORDEN DE LOS TAGS

### Volver en el tiempo nuestro Repositorio utilizando reset y checkout

```git reset #commit --soft```
- Volvemos nuestro archivo a la versión del commit indicada, pero sin borrar los commits usados anteriormente. Mantenemos lo que tengamos en stagin ($git add) disponible para un siguiente commit.

```git reset #commit --hard```
- ES MUY PELIGROSO, Volvemos nuestro archivo a la versión del commit indicada, BORRANDO TODOS los commits usados anteriores a la versión del commit indicado.

```git reset HEAD```
- Este es el comando para sacar archivos del área de Staging. No para borrarlos ni nada de eso, solo para que los últimos cambios de estos archivos no se envíen al último commit, a menos que cambiemos de opinión y los incluyamos de nuevo en staging con git add, por supuesto.

```$git checkout #commit archivo.txt```
- Volvemos nuestro archivo a la versión del commit indicado, sin cambiar nada en el Staging.

##### Ver y personalizar mas detalles en $git log

Algunos comandos que pueden ayudar cuando colaboren con proyectos muy grandes de github:

git log --oneline - Te muestra el id commit y el título del commit.
git log --decorate- Te muestra donde se encuentra el head point en el log.
git log --stat - Explica el número de líneas que se cambiaron brevemente.
git log -p- Explica el número de líneas que se cambiaron y te muestra que se cambió en el contenido.
git shortlog - Indica que commits ha realizado un usuario, mostrando el usuario y el titulo de sus commits.
git log --graph --oneline --decorate y
git log --pretty=format:"%cn hizo un commit %h el dia %cd" - Muestra mensajes personalizados de los commits.
git log -3 - Limitamos el número de commits.
git log --after=“2018-1-2” ,
git log --after=“today” y
git log --after=“2018-1-2” --before=“today” - Commits para localizar por fechas.
git log --author=“Name Author” - Commits realizados por autor que cumplan exactamente con el nombre.
git log --grep=“INVIE” - Busca los commits que cumplan tal cual está escrito entre las comillas.
git log --grep=“INVIE” –i- Busca los commits que cumplan sin importar mayúsculas o minúsculas.
git log – index.html- Busca los commits en un archivo en específico.
git log -S “Por contenido”- Buscar los commits con el contenido dentro del archivo.
git log > log.txt - guardar los logs en un archivo txt

### Introduccion a las ramas o branches de Git

$git commit -am “MENSAJE” = Agrega y manda el mensaje es decir hace la función de "$git add" y "$git commit -m" al mismo tiempo, este solo aplica para archivos ya trackeados en el repositorio.
$git branch nombre_rama = Se crea la rama teniendo en cuenta que uno se debe de posicionar en la rama que se necesita copiar.
$git branch -l = Lista todas las ramas que existen.
$git branch -d nombre_rama = Elimina la rama nombre_rama. Con -D se fuerza el borrado.
$git branch -m nombre_rama rama_nueva = Permite renombrar una rama nombre_rama por rama_nueva.
$git checkout nombre_rama = Aqui se cambia la rama que se le indico.

### Fusión de ramas con Git merge

Desde la Rama en la que estoy me traigo los cambios de otra rama con:
$git merge nombre_de_la_rama

Algunos comandos que están en el libro Pro Git de utilidad

$git branch –v // muestra el último commit de cada rama
$git branch --merged // lista las ramas que se fusionaron conla rama actual
$git branch --no-merged // lista las ramas que nose han fusionado conla rama actual
$git merge --abort // anula el merge y devuelve todo a como estaba antes

### Uso de GitHub

$git remote add origin (url)
$git remote (muestra el origen)
$git remote -v (es verval)
$git pull origin master --allow-unrelated-histories (Fuerza la union de las diferentes historias)
$git pull origin master (Descarga cambios)
$git push (origin) (master) (Sube Cambios)