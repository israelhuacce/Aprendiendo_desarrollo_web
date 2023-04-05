# Curso de Git y Github

## Comandos básicos para guardar en local
- "git add ."   Con este comando trackeamos los cambios
- "git commit"  Con este comando el cambio está oficializado. Pero es necesario entrar al editor de texto para establecerle un nombre
- "git commit -m" "Nombre del cambio" : ya no es necesario escribir el nombre del cambio en otra pestaña todo lo hace desde el gitbash.
Ya hicimos nuestro primer commit con solo la subida de los 2 archivos
Realizaremos la siguiente pero ahora usando "-m"

## Subir a github
- Crear repositorio en tu cuenta de github.
Ejecutar los comandos que están en mi segundo cerebro con el nombre git, lo que ocurrió fue lo siguiente : 
- Al momento de realizar me pidió autorización del github hasta con el celular.
- Al ejecutar el código `git push -u origin master` , petó mi visual studio code.

El anterior comando solo se realiza la primera vez : después se hace el siguiente comando `git push`

## Descargar cambios 
En la terminal ejecutamos el comando `git pull`

# Master o main?
Se puede trabajar con master. pero la industria de la tecnolgía lo que hizo es cambiar los nombres de palabras que puedan ser ofensivas en este caso es la palabra master por main a raiz de movimientos racitas.

Para realizar el cambio en un repositorio ya existente.

# Para crear un repositorio con main iniciado

```bash
git init
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/usuario/ruta del repositorio # Aqui poner el enlace que te da a la hora de crear un nuevo repositorio.
git push -u origin main
```
# Ignorar archivos

En el archivo .gitignore incluimos todo lo que NO queramos incluir en nuestro repositorio. Lo podemos crear manualmente o con gitignore.io.
```
# esto es un comentario
archivo.ext
carpeta
/archivo_desde_raiz.ext
# ignorar todos los archivos que terminen en .log
*.log
# excepto production.log
!production.log
# ignorar los archivos terminados en .txt dentro de la carpeta doc,
# pero no en sus subcarpetas
doc/*.txt
# ignorar todos los archivos terminados en .txt dentro de la carpeta doc
# y también en sus subcarpetas
doc/**/*.txt
```
# Clonar archivos
Ubicarnos en el lugar donde el repositorio se pondrá.
```
git clone https://github.com/usuario/repositorio.git
```
# Ramas
Pequeñas realidades simultáneas de tu proyecto. Una rama nos permite aislar una nueva funcionalidad en nuestro código que después podremos añadir a la versión principal.

Tener versiones alternas en la línea del tiempo. 

```bash
# crear rama
git branch nombre-rama

# cambiar de rama
git checkout nombre-rama

# crear una rama y cambiarte a ella (atajo de los 2 anteriores)
git checkout -b rama

# eliminar rama
git branch -d nombre-rama

# eliminar ramas remotas
git push origin --delete nombre-rama

#eliminar rama (forzado)
git branch -D nombre-rama

# listar todas las ramas del repositorio
git branch

# lista ramas no fusionadas a la rama actual
git branch --no-merged

# lista ramas fusionadas a la rama actual
git branch --merged

# rebasar ramas
git checkout rama-secundaria
git rebase rama-principal
```
