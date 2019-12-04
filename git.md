# Tutorial Git
1 [Antes de empezar](#Antes-de-empezar)
2 [Configurar Git](#Configurar-Git)
3 [Clonar un repositorio](#Clonar-un-repositorio)
4 [Añadir un fichero](#Añadir-un-fichero)

### Antes de empezar
Si quieres conocer el directorio en el que te encuentras, escribe:
```
pwd
```
Configurar Git
-------------------

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

Clonar un repositorio
-------------------

```
git clone URL DEL REPOSITORIO
```

Añadir un fichero
-------------------

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