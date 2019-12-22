# Trackear Archivos en Git

1. [Añadir cambios + mensaje para commit en la misma orden](#añadir-cambios-+-mensaje-para-commit-en-la-misma-orden)
2. [Ver listado de archivos trackeados](#ver-listado-de-archivos-trackeados)
3. [Añadir ficheros paso a paso](#añadir-ficheros-paso-a-paso)
4. [Uso de add](#uso-de-add)
5. [Añadir ficheros y carpetas recursivamente](#añadir-ficheros-y-carpetas-recursivamente)

## Añadir cambios + mensaje para commit en la misma orden
Los pasos con ficheros para ser trackear ficheros en Git son:

1. Crear o modificar un fichero
2. Añadir **add** fichero para ser trackearlo / **Ahora este fichero está en el Staging Area**
3. Commiteamos el fichero / **Ahora este fichero se encuentra en el Local Ropository**

### Realizar estas dos últimas acciones a la vez

Para crear un fichero desde la terminal, *en mi caso uso Visual Studio Code*. Para lanzar visual solo hay que añadir *code*

```
code ruta/nombre-del-fichero.md
```

Con esto lanzamos un fichero nuevo con el nombre que le hemos dado dentro de visual. Añadimos contenido y guardamos el* fichero. Si ahora hacemos un **git status** veremos que tenemos un nuevo fichero y que este no ha sido añadido a *.git*

```
commit -am "mensaje que queremos para el commit"
```
## Ver listado de archivos trackeados

con la orden **ls-files** podemos ver el listado de ficheros que Git está trackeando

```
git ls-files
```

## Añadir ficheros paso a paso

1. Añadir ficheros **git add nombre-fichero.md**
2. Commitear fichero **git commit -m "mensaje para el commit"**

## Uso de add

Cada vez que usamos **add** estamos añadiendo cambios al Stagin Area, es la forma que tenemos de sumar cambios, todos los cambios que queremos. Con Commit estamos subiendo todos estos cambios a nuestro Local Repository. 

Podemos tener uno o varios documentos sin commitear a nuestro Local Repository y hacer cambios, cada uno de esos cambios los podemos añadir **add** al Staging Area sin que se suba aún nuestro fichero al repositorio local.

## Añadir ficheros y carpetas recursivamente

Si tengo varios niveles de carpetas, con varios ficheros dentro y los quiero añadir todos a la vez, **con add en la terminal solo te enseñará el primer nivel de carpetas**. Solo hay que utilizar la siguiente orden en la terminal.

```
git add .
```

Con esta orden, verás al hacer commit todo el listado de ficheros y carpetas que estarás añadiendo al repositorio local.