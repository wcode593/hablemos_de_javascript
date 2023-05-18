<!-- # Hablemos de Git & GitHub -->

<h1 style="text-align:center; color: lightpink;">Hablemos de <i><b>Git & GitHub<i><b>😍</h1>

[![Git](https://img.shields.io/badge/Git-2.37+-f14e32?style=for-the-badge&logo=git&logoColor=white&labelColor=101010)](https://git-scm.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Web-blue?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/)

Git es un software de control de versiones distribuido y descentralizado que permite a un equipo de desarrolladores trabajar sobre el mismo código.

Se denomina "distribuido" porque cada miembro del equipo dispone de una copia completa del código.

Los miembros del equipo pueden enviarse código, recibirlo y desarrollar funcionalidades de forma conjunta y separada del servidor central.

![git es distribuido](https://jonmircha.com/img/blog/git-centr-decentr.png "git es distribuido")

## Ventajas

- Es el estándar actual.
- Código colaborativo, versionado y distribuido.
- Recuperación de archivos.
- Mayor control.
- Shorcuts y plugins.
- Mejora la productividad.

## Git y GitHub son lo mismo

![git y gitHub no son lo mismo](https://jonmircha.com/img/blog/git-github.png "git es diferente a gitHub")

## Flujo básico

El flujo de Git, consta de tres estados locales, es decir en la computadora donde se esta trabajando y uno más de forma remota cuando accedemos al codigo centralizado en plataformas como GitHub

1. **Working Directory**:
   Es el área correspondiente al estado modified y es la carpeta local de tu computadora donde almacenas los archivos de tu proyecto.
1. **Staging Area**: Es el área correspondiente al estado staged también se le llama index por que es el área donde git indexa y agrega los cambios realizados en los archivos previos a comprometerlos en su registro.
1. **Local Repository**: Es el área correspondiente al estado committed, donde los cambios ya se han registrado en el repositorio de git también se le llama HEAD por que indica en qué cambio se encuentra el puntero del repositorio.

1. **Remote Repository**: Es el área correspondiente al estado remote y es el directorio remoto donde almacenamos los archivos del proyecto en alguna plataforma web como GitHub, GitLab, BitBucket. Git denomina origin al repositorio remoto

![flujo de Git](https://jonmircha.com/img/blog/git-flow.png "flujo básico para trabajar con GIT")

## De master a main

Con los desafortunados acontecimientos del 25 de mayo de 2020 en los Estados Unidos que culminaron con el asesinato del afroamericano George Floyd a manos de policias de la ciudad de Mineápolis, se intensificó de manera global el movimiento #BlackLivesMatter.

Con dicho movimiento muchas industrias y empresas comenzaron a tomar acciones para erradicar el racismo.

En la industria de la tecnología por años se han empleado palabras como master, slave, whitelist, blacklist entre otras que actualmente no son bien vistas por el contexto y la semántica que implican.

Al respecto Microsoft empresa propietaria de GitHub decidió comenzar una campaña para reemplazar el nombre de la rama principal de los repositorios de master a main; como lo han explicado en este [documento](https://github.com/github/renaming):

> "El 1 de octubre de 2020, cualquier nuevo repositorio que crees utilizará 'main' como la
> rama por defecto, en lugar de 'master'. Este cambio no afecta a ninguno de tus repositorios
> existentes: los repositorios existentes continuarán teniendo la misma rama por defecto que
> tienen ahora".

Este cambio implica agregar una par de líneas de comandos adicionales para crear la rama 'main' y hacerla principal en el repositorio.

Entonces el flujo básico quedaría de la siguiente manera:

## Para repositorios nuevos

```git
git init
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main
```

## Para repositorios existentes

```git
git branch -M main
git remote add origin https://github.com/usuario/repositorio.git
git push -u origin main
```

## Para reemplazar la rama _master_ por **main** en Git

```git
git config --global init.defaultBranch main
```

## Ramas

Una rama nos permite aislar una nueva funcionalidad en nuestro código que después podremos añadir a la versión principal.

## Fusiones

Une dos ramas. Para hacer una fusión necesitamos:

1. Situarnos en la rama que se quedará con el contenido fusionado.
1. Fusionar.

Cuando se **fusionan** ramas se pueden dar 2 resultados diferentes:

- Fast-Forward: La fusión se hace automática, no hay conflictos por resolver.
- Manual Merge: La fusión hay que hacerla manual, para resolver conflictos de duplicación de contenido.

<b><u>Muy bonito y todo pero Vamos al Código</u> :sunglasses:</b>
