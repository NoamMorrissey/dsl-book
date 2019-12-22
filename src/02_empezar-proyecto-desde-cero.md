# Empezar con un proyecto desde cero

1. [Crear un proyecto desde cero](#crear-un-proyecto-desde-cero)
2. [Listado mostrando carpetas ocultas](#listado-mostrando-carpetas-ocultas)
3. [Git commit](#git-commit)
4. [Eliminar proyecto](#eliminar-proyecto)

## Crear un proyecto desde cero

Para crear desde cero un proyecto con un repositorio de GIT. Para hacer esto necesitamos utilizar el comando **init**
```
git init nombre-del-proyecto
```
## Listado mostrando carpetas ocultas

Con esto habremos creado una carpeta vacia (sin ficheros visibles) que será el repositorio local que git controlará. Al hacer un **ls** en el terminal veremos que se ha creado una carpeta. Al entrar en ella con el comando **cd** y ejecutar de nuevo el comando **ls** vemos que no existe ningún fichero visible. Ahora si queremos ver los ficheros ocultos:
```
ls -al
```
## Crear fichero desde la terminal

Ahora podemos ver que existe una carpeta oculta **.git** si accedemos a ella a través de **cd** y listamos su contenido podemos ver la estructura del repostorio de git. Al vover a la carpeta donde se encuentra el **working repository** con **cd ..** podemos crear un fichero desde cero.

```
touch nombre-fichero.md
open nombre-fichero.md
```

Con **touch** creamos un fichero y con **open** lo abrimos con las herramienta que tengamos configurada por defecto para trabajar con ese tipo de fichero.

Si preguntamos con **git status** se nos informará de que existe un nuevo fichero en el **working directory** que aún no está siendo trackeado **staging area** por git. Lo tendremos que añadir mediante **add**

## Git commit

```
git commit
```

Podemos hacer un commit de varias líneas, pero vas a realizarlo por defecto dentro de la terminal, para salir de esta vision. Presiona primero **escape** y luego:

```
:wq
```
**:** entra en el modo de comando, **w** es para "escribir" (guardar) y, **q** es para salir.  
Con esto hemos pasado el fichero al repositorio Git y habrá un historial de commits que posteriormente podremos recuperar.

## Eliminar proyecto

Ahora simplemente vamos a eliminar todo el proyecto y el repositorio de git, para ello nos tenemos que situar en la carpeta origen del proyecto y ejecutar la orden
```
rm -rf nombre-del-projecto/
```