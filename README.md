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

# Eliminación de Ramas en Git

En esta sección, discutiremos la importancia de eliminar ramas obsoletas en Git y los comandos asociados para hacerlo de manera segura.

## ¿Por qué eliminar ramas?

Es importante eliminar ramas obsoletas en un repositorio Git por varias razones:

- **Mantenimiento del repositorio**: Eliminar ramas obsoletas ayuda a mantener un repositorio limpio y organizado, lo que facilita la navegación y la comprensión del historial de cambios.
- **Evitar confusión**: Al eliminar ramas que ya no son necesarias, se evita la confusión sobre qué ramas están activas y cuáles están obsoletas.
- **Ahorro de recursos**: Al reducir el número de ramas en un repositorio, se ahorran recursos y se mejora el rendimiento de Git.

## Comandos para eliminar ramas

![Eliminar todas las ramas locales en Git | Delft Stack](https://www.delftstack.com/img/Git/feature-image---git-delete-all-local-branches.webp)

### git branch -d [nombre_rama]

El comando `git branch -d [nombre_rama]` se utiliza para eliminar una rama en Git de forma segura. Este comando solo eliminará la rama si todos los cambios de la rama a eliminar ya han sido fusionados en otra parte del proyecto. Es útil para eliminar ramas que ya han cumplido su propósito y ya no son necesarias.

### git branch -D [nombre_rama]

El comando `git branch -D [nombre_rama]` se utiliza para forzar la eliminación de una rama en Git, incluso si hay cambios en la rama que no se han fusionado. Esto puede ser útil si estás seguro de que no necesitas los cambios de la rama y deseas eliminarla de todos modos.

## Otros comandos útiles

### git log --one-line

El comando `git log --one-line` se utiliza para mostrar el historial de commits en una sola línea por cada commit. Proporciona una vista compacta del historial de cambios, que puede ser útil para tener una visión general rápida del proyecto.

### git log --graph

El comando `git log --graph` se utiliza para mostrar el historial de commits en forma de gráfico ASCII. Muestra las relaciones entre ramas y commits, lo que facilita la visualización del flujo de trabajo del proyecto.

Estos comandos son útiles para mantener un repositorio Git limpio y organizado, así como para visualizar y comprender el historial de cambios de manera efectiva.

![how to add author info onto git log --oneline --graph - Stack Overflow](https://i.stack.imgur.com/SUERW.jpg)

# Clase 3: Introducción a GitHub

En esta clase, exploraremos GitHub, una plataforma de alojamiento de repositorios de código que facilita la colaboración en proyectos de desarrollo de software.

<img src="data:image/png;base64,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" title="" alt="GitHub - Wikipedia" data-align="center">

## ¿Qué es GitHub?

GitHub es una plataforma en línea que permite alojar y gestionar repositorios de código fuente utilizando el sistema de control de versiones Git. Permite a los desarrolladores colaborar en proyectos, realizar seguimiento de cambios, gestionar problemas y mucho más, todo en un entorno centralizado y accesible desde cualquier lugar.

## ¿Cómo funciona GitHub?

GitHub funciona mediante la creación y gestión de repositorios de código fuente. Cada proyecto en GitHub tiene su propio repositorio, que puede contener todos los archivos y carpetas relacionados con el proyecto, así como su historial de cambios y ramificaciones.

Los desarrolladores pueden clonar repositorios existentes, realizar cambios en el código y enviar esas modificaciones de vuelta al repositorio original mediante "pull requests". 

## Comandos básicos de Git para interactuar con GitHub

### git remote add origin [link_del_repo]

El comando `git remote add origin [link_del_repo]` se utiliza para conectar un repositorio Git local con un repositorio remoto en GitHub. Establece un "remoto" llamado `origin` que apunta al repositorio remoto en la URL especificada. Esto permite enviar y recibir cambios entre el repositorio local y el repositorio en GitHub.

<img title="" src="https://www.classicpress.net/wp-content/uploads/2020/02/map-initial-github-desktop-tutorial.png" alt="Github Desktop Tutorial – A Really, Really Simple Guide" data-align="center" width="381">

### git remote -v

El comando `git remote -v` se utiliza para mostrar una lista de los remotos configurados en el repositorio Git local, junto con sus URLs asociadas. Proporciona una forma rápida de verificar la configuración de los remotos y asegurarse de que el repositorio esté correctamente conectado a GitHub.

<img title="" src="file:///C:/Users/Usuario/AppData/Roaming/marktext/images/2024-05-11-23-03-22-image.png" alt="" data-align="center" width="423">