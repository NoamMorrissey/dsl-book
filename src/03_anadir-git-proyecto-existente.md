# Añadir Git a un proyecto existente

1. [Situarte en el directorio que quieras desde la raiz](#situarte-en-el-directorio-que-quieras-desde-la-raiz)
2. [Inicializar Git](#inicializar-Git)
3. [Añadir fichero](#añadir-fichero)
4. [Commit fichero](#commit-fichero)
5. [Eliminar repositorio](#eliminar-repositorio)

## Situarte en el directorio que quieras desde la raiz

Si tienes un proyecto y este aún no está siendo versionado por Git. Para situarte desde cualquier punto en el que estés en el directorio que quieras:
```
cd ~/ruta/nombre-del-directorio-que buscas
```
En donde **~** es la raiz de mi usuario. P.E. Si mi carpeta se encuentra en Documents la ruta sería la siguiente 
```
cd ~/Documents/Nombre-de-la-carpeta/
```
## Inicializar Git

Para inicializar el uso de Git en ese proyecto y comenzar con el versionado utilizaremos el comando **init**
```
git init
```
Git inicialará un repositorio en esa carpeta, como working directory. Para ver que temos la carpeta **.git** que está oculta podemos listar todos los elementos dentro de esa carpeta, los visibles y los ocultos.
```
ls -al
```
## Añadir fichero

En este caso tenemos una carpeta con muchos ficheros, para añadir todos estos ficheros a la vez al **staging area** no necesitamos **add** añadirlos uno a uno. Para hacer esto lo realizamos mediante el siguiente comando.
```
git add . 
```
## Commit fichero

Lo único que nos falta es realizar nuestro primer commit de la manera que ya sabemos realizarlo
```
git commit -m "Mi prirmer commit"
```
## Eliminar repositorio

Ya estamos funcionando con un repositorio de git. Para dejar de tener versionado este proyecto lo único que tenmos que hacer es eliminar la carpeta **.git** de la carpeta para hacer esto basta con borrarla
```
rm -rf .git
```
