# Tutorial Git
1. [Comandos básicos](#Comandos-básicos)
..* [Antes de empezar](#Antes-de-empezar)
..* [Configurar Git](#Configurar-Git)
..* [Clonar un repositorio](#Clonar-un-repositorio)
2. [Empezar con un proyecto desde cero](#Empezar-con-un-proyecto-desde-cero)
..* [Añadir un fichero](#Añadir-un-fichero)
3. [Añadir Git a un proyecto existente](#Añadir-Git-a-un-proyecto-existente)

Comandos básicos
----------------------

### Antes de empezar
Si quieres conocer el directorio en el que te encuentras, escribe:
```
pwd
```
### Configurar Git

Para operar con git tenemos que dejar el mismo nombre y dirección de correo en git en el terminal. **2 órdenes**
```
git config --global user.name “Nombre de usuario”
git config --global user.email “nombre@email.com”
```

Para ver que esas dos órdenes han tenido efecto y todos los parametros que puedes configurar
```
git config -- global --list
```

Para limpiar la pantalla y tener una terminal limpia
```
clear
```

Para obtener ayuda de Git y la segunda para obtener ayuda sobre un tema en concreto.
```
git help
git help commit
``` 

### Clonar un repositorio

```
git clone URL DEL REPOSITORIO
```

### Añadir un fichero

```
echo "Texto que aparecerá al inicio del fichero" >> NombreFiechero.md
```
Para ver el contenido del fichero
```
cat NombreFiechero.md
```
Si hacemos un git status nos dirá que hay **Untraked files**. Esto quiere decir que este fichero está en nuestro **working directory** pero aún no está añadido a Git para ser trackeado. Para añadir este nuevo fichero a git usar la orden **add**
```
git add NombreFiechero.md
```
Ahora este fichero está en el Staging Area. Este area está diseñada para que podamos hacer añadidos o modificaciones incrementales y finalmente añadir mediante un commit todos los cambios realizados a nuestro **Local Ropository** (aún en nuestro ordenador) y finalmente subirlo al **Remote Repository**, en nuestro caso GitHub.
```
git commit -m "mensaje del commit con el resumen de lo que hayamos hecho"
```
Ahora si hacemos un git status la terminal nos informará de que nuestro **working directory** está limpio y que (en nuestro caso) master branch está por delante del master en por un commit. Es decir, podemos ir añadiendo commits en nuestro Local Repository para luego añadirlos al **Remote Repository**.

Para subir nuestro fichero y nuestros cambios al **Remote Repository** solo tenemos que hacer
```
git push origin master
```
En este caso **origin** es nuestro repositorio en GitHub (podemos acceder a esta información en la parte de config) y **master** se refiere a nuestra, de momento, única rama en el repositorio.


Empezar con un proyecto desde cero
----------------------

### Crear un proyecto desde cero
Para crear desde cero un proyecto con un repositorio de GIT. Para hacer esto necesitamos utilizar el comando **init**
```
git init nombre-del-proyecto
```
Con esto habremos creado una carpeta vacia (sin ficheros visibles) que será el repositorio local que git controlará. Al hacer un **ls** en el terminal veremos que se ha creado una carpeta. Al entrar en ella con el comando **cd** y ejecutar de nuevo el comando **ls** vemos que no existe ningún fichero visible. Ahora si queremos ver los ficheros ocultos:
```
ls -al
```
Ahora podemos ver que existe una carpeta oculta **.git** si accedemos a ella a través de **cd** y listamos su contenido podemos ver la estructura del repostorio de git. Al vover a la carpeta donde se encuentra el **working repository** con **cd ..** podemos crear un fichero desde cero.

```
touch nombre-fichero.md
open nombre-fichero.md
```

Con **touch** creamos un fichero y con **open** lo abrimos con las herramienta que tengamos configurada por defecto para trabajar con ese tipo de fichero.

Si preguntamos con **git status** se nos informará de que existe un nuevo fichero en el **working directory** que aún no está siendo trackeado **staging area** por git. Lo tendremos que añadir mediante **add**

```
git commit
```

Podemos hacer un commit de varias líneas, pero vas a realizarlo por defecto dentro de la terminal, para salir de esta vision. Presiona primero **escape** y luego:

```
:wq
```
**:** entra en el modo de comando, **w** es para "escribir" (guardar) y, **q** es para salir.  
Con esto hemos pasado el fichero al repositorio Git y habrá un historial de commits que posteriormente podremos recuperar.

Ahora simplemente vamos a eliminar todo el proyecto y el repositorio de git, para ello nos tenemos que situar en la carpeta origen del proyecto y ejecutar la orden
```
rm -rf nombre-del-projecto/
```


Añadir Git a un proyecto existente
----------------------

