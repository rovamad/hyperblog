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
| $ git log archivo.extencion  | muestra la historia del archivo. |

```$git diff _tag1_ _tag2_```
- Hace la comparativa de cambios entre el archivo en su etapa en el commit del tag1 y del tag2. Considera al más reciente como tag2 y al anterior como tag1, SI IMPORTA EL ORDEN DE LOS TAGS

### Volver en el tiempo nuestro Repositorio utilizando reset y checkout

```git reset #commit --soft```
- Volvemos nuestro archivo a la versión del commit indicada, pero sin borrar los commits usados anteriormente. Mantenemos lo que tengamos en stagin ($git add) disponible para un siguiente commit.

```git reset #commit --hard```
- ES MUY PELIGROSO, Volvemos nuestro archivo a la versión del commit indicada, BORRANDO TODOS los commits usados anteriores a la versión del commit indicado.

```$git checkout #commit archivo.txt```
- Volvemos nuestro archivo a la versión del commit indicado, sin cambiar nada en el Staging.