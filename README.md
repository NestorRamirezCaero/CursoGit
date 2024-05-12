# CursoGit

# # Clase 1: Introducción a Git

## ¿Qué es Git?

Git es un sistema de control de versiones distribuido que te permite rastrear cambios en archivos de código fuente durante el desarrollo de software. Es especialmente útil para colaborar en proyectos con otros desarrolladores, ya que permite trabajar de manera eficiente en equipo y mantener un historial completo de los cambios realizados en un proyecto.

## Comandos Básicos de Git

### git -h

El comando `git -h` muestra una lista de los comandos Git más comunes y su descripción básica. Es útil para obtener una descripción general de los comandos disponibles en Git y su sintaxis básica.

```bash
git -h
```

# 

## Git init

El comando `git init` se utiliza para inicializar un nuevo repositorio Git en un directorio. Convierte una carpeta normal en un repositorio Git, permitiendo rastrear los cambios en los archivos de ese directorio.

## Git status

El comando `git status` proporciona información sobre el estado actual del repositorio Git. Muestra los archivos modificados desde el último commit, los archivos que están siendo rastreados por Git pero aún no han sido preparados para el commit, y los archivos listos para ser confirmados.

## Git commit

El comando `git commit` se utiliza para confirmar los cambios realizados en el repositorio. Después de preparar los cambios con `git add`, se utiliza este comando para guardar los cambios en el historial de versiones de Git. Se debe proporcionar un mensaje descriptivo para el commit.

## Estados en Git

| Estado    | Descripción                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| Modified  | Archivos modificados desde el último commit, pero no preparados para el commit.  |
| Staged    | Archivos preparados para el commit con `git add`, pero no confirmados.           |
| Committed | Archivos confirmados mediante un commit, registrados de forma permanente en Git. |

Estos estados representan las diferentes etapas por las que pasan los archivos en un repositorio Git: desde ser modificados en el directorio de trabajo, luego preparados para el commit, hasta finalmente ser confirmados en el historial de versiones del repositorio.

## Git restore --staged

El comando `git restore --staged` se utiliza para eliminar cambios de la zona de preparación (staging area) en Git. Esto significa que los cambios que han sido preparados para el commit con `git add` volverán al estado modificado, es decir, serán eliminados de la zona de preparación sin eliminar los cambios en sí.

## Git add

El comando `git add` se utiliza para añadir cambios al área de preparación (staging area) en Git. Esto permite preparar cambios específicos para ser incluidos en el próximo commit. Puedes añadir archivos individuales (`git add nombre_archivo`) o todos los archivos modificados (`git add .`).

## Git commit --amend

El comando `git commit --amend` se utiliza para modificar el commit más reciente en Git. Permite agregar cambios adicionales al commit más reciente o cambiar su mensaje. Es útil para corregir errores de escritura en el mensaje del commit o para incluir cambios olvidados en el commit anterior.

## Git log

El comando `git log` se utiliza para ver el historial de commits en un repositorio Git. Muestra una lista de todos los commits realizados.





# Clase 2: Ramas en Git

En esta clase, exploraremos el concepto de ramas en Git y cómo pueden ser utilizadas para organizar y gestionar el desarrollo de software de manera efectiva.

## ¿Qué es una rama en Git?

Una rama en Git es una línea independiente de desarrollo que permite trabajar en nuevas características, correcciones de errores o experimentos sin afectar el código en otras ramas. Cada repositorio Git comienza con una rama principal predeterminada, comúnmente denominada `master` o `main`, y a partir de ahí se pueden crear y fusionar ramas adicionales según sea necesario.

Las ramas en Git ofrecen varias ventajas, incluyendo:

- **Aislamiento de cambios**: Permite trabajar en nuevas características o experimentos sin afectar el código principal del proyecto.
- **Facilidad para la colaboración**: Varios desarrolladores pueden trabajar en diferentes características simultáneamente sin interferir entre sí.
- **Experimentación segura**: Las ramas proporcionan un entorno seguro para probar nuevas ideas o soluciones sin arriesgar la estabilidad del proyecto principal.



# ![Aprendiendo git: Ramas](https://res.cloudinary.com/snyk/images/f_auto,q_auto/w_1240,h_384,c_scale/v1/wordpress-sync/image1-11/image1-11-1240x384.png)

Las ramas son una parte fundamental del flujo de trabajo en Git y son ampliamente utilizadas en el desarrollo de software para gestionar cambios de manera eficiente y colaborativa.

# Comandos para Ramas



## Git branch

El comando `git branch` se utiliza para listar todas las ramas en el repositorio actual. Muestra una lista de las ramas existentes y resalta la rama actual con un asterisco (`*`). Es útil para visualizar todas las ramas disponibles en el proyecto.

<img src="https://miro.medium.com/v2/resize:fit:1400/1*vOgcWxc9PW10b-E6VndtLQ.png" title="" alt="𝐆𝐢𝐭 𝐁𝐫𝐚𝐧𝐜𝐡 𝐂𝐨𝐦𝐦𝐚𝐧𝐝 | by Meghasharmaa | Medium" width="499">

## Git branch [nombre_rama]

El comando `git branch [nombre_rama]` se utiliza para crear una nueva rama en el repositorio. Al proporcionar un nombre de rama, se crea una nueva línea de desarrollo independiente a partir del punto en el que te encuentras. 

<img src="https://docs.github.com/assets/cb-26429/images/help/desktop/new-branch-button-mac.png" title="" alt="Administración de ramas en GitHub Desktop - Documentación de GitHub" width="371">

## Git switch

El comando `git switch` se utiliza para cambiar entre ramas en el repositorio. Puedes cambiar a una rama existente proporcionando su nombre como argumento. Es una forma rápida y conveniente de moverte entre diferentes líneas de desarrollo en el proyecto.

## Git checkout

El comando `git checkout` se utiliza para cambiar entre ramas en el repositorio. Puedes cambiar a una rama existente proporcionando su nombre como argumento. Además, puedes usar `git checkout -b [nombre_rama]` para crear una nueva rama y cambiar a ella al mismo tiempo. Es útil para moverte entre diferentes ramas y crear nuevas ramas en el proyecto.

## Git merge

El comando `git merge` se utiliza para fusionar cambios de una rama a otra. Por lo general, se utiliza para integrar cambios de una rama secundaria en la rama principal del proyecto. Es útil para combinar el trabajo realizado en diferentes ramas y mantener la coherencia en el código base.

![Gif conflictos](https://camo.githubusercontent.com/9ce9843f5609e7b93781dedfeb13b7d84f26db23500e9c65531afbde879822e0/68747470733a2f2f7374617469632e6a61766174706f696e742e636f6d2f7475746f7269616c2f6769742f696d616765732f6769742d6d657267652d616e642d6d657267652d636f6e666c6963742e706e67)