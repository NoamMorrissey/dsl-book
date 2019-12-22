# Descartar Cambios

Al trabajar sobre **un mismo fichero esté puede tener diferentes versiones del mismo**:

1. Puede haber una versión en el repositorio local
2. Este también puede estar en Staging Area con una versión diferente


En esta página vamos a explicar cómo tener este escenario:

1. **Un fichero está commiteado en el Local Repository**

    ![Fichero commiteado en el Repositorio Local](img/file-local-repository.png)

2. **Hacemos nuevas modificaciones en ese mismo fichero**

3. **Añadimos estas nuevas modificaciones al Staging Area**

    ![Fichero en el Staging Area](img/file-staging-area.png)

4. **Queremos eliminar las morificaciones añadidas al Stagging Area**

    ![Git reset HEAD](img/git-reset-head.png)
    ```
    git reset HEAD nombre-del-fichero.md
    ```
    
    Entonces el fichero vuelve a estar dentro del Working Directory

    ![Fichero en Working Directory](img/file-working-directory.png)

5. Recuperar el fichero commiteado al Local Ropository

    ![Git checkout --](img/git-checkout.png)
    ```
    git checkout -- nombre-del-fichero.md
    ```
