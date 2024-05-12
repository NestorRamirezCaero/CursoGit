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