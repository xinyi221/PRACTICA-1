# BASICOS DE GIT E INVESTIGACIÓN DE GIT

## ¿QUÉ ES GIT?
- **Git** es un **sistema de control de versiones distribuido** creado en 2005 por **Linus Torvalds** (el creador del kernel de Linux). Su función principal es registrar el historial completo de cambios realizados en un conjunto de archivos a lo largo del tiempo, permitiendo volver a versiones anteriores, comparar modificaciones y colaborar en equipo sin sobrescribir el trabajo de los demás.

- A diferencia de los sistemas centralizados antiguos, Git es **distribuido:** cada desarrollador tiene en su computadora una copia íntegra del proyecto y de todo su historial, por lo que puede trabajar sin conexión a internet y sincronizar los cambios cuando lo necesite.

<img width="2816" height="1536" alt="licensed-image" src="https://github.com/user-attachments/assets/3c344346-2ec8-48a6-aed4-dd1a00d1c1ac" />


## LOS 3 ESTADOS FUNDAMENTALES DE GIT
Para entender cómo funciona Git, hay que conocer las tres zonas por las que pasan tus archivos en tu máquina local (más el servidor remoto):
- **Working Directory (Directorio de trabajo):** Es la carpeta normal de tu proyecto donde editas, creas o borras archivos.
- **Staging Area (Área de preparación / Index):** Es una zona intermedia donde seleccionas y preparas exactamente qué cambios quieres incluir en la próxima foto del proyecto.
- **Local Repository (Repositorio local):** Es la base de datos oculta (.git) donde Git guarda de forma permanente las instantáneas (commits) de tu proyecto.
- **Remote Repository (Repositorio remoto):** Una copia alojada en un servidor (como GitHub, GitLab o Bitbucket) para respaldar el código y compartirlo con otras personas.

## FLUJO DE TRABAJO Y COMANDOS BÁSICOS
1. **Iniciar o clonar un repositorio**
     *Solo se ejecuta una vez por proyecto*
Crea un repositorio nuevo en tu carpeta actual con git init, o descarga uno ya existente desde internet con git clone <url-del-repositorio>.
2. **Revisar el estado de los archivos:**
Ejecuta git status para ver qué archivos han sido modificados, cuáles son nuevos y cuáles están listos para guardarse.
3. **Preparar los cambios (Staging):**
Usa git add <archivo> (o git add . para incluir todos los cambios) para mover las modificaciones del *Working directory* al *Staging area*.
4. **Guardar una instantánea (Commit):**
Ejecuta git commit -m "Descripción clara del cambio" para registrar permanentemente los archivos preparados en tu *Local repository*.
5. **Sincronizar con el repositorio remoto:**
Descarga los cambios recientes de tus compañeros con git pull y sube tus propios commits al servidor con git push.

## OTROS COMANDOS ESENCIALES DEL DÍA
| Comando | Qué hace |
| :--- | ---: |
| git log | Muestra el historial cronológico de todos los commits realizados, con autor, fecha e identificador único. |
| git branch | Lista las ramas existentes. Usar git branch <nombre> crea una línea paralela de desarrollo sin afectar el código principal. |
| git checkout <rama>  git switch <rama> | Cambia de una rama a otra para trabajar en distintas funcionalidades por separado. |
| git init | Crea un nuevo repositorio de Git vacío en la carpeta actual, generando la carpeta oculta `.git` donde se almacenará todo el historial. |
| git clone <url> | Descarga una copia completa de un repositorio remoto a tu equipo local, incluyendo todos sus archivos, ramas e historial de cambios. |
| git status | Muestra el estado actual del directorio de trabajo y del área de preparación, indicando qué archivos fueron modificados, añadidos o están sin seguimiento. |
| git add <archivo> | Pasa los cambios específicos del directorio de trabajo al área de preparación (*Staging Area*). Usar `git add .` añade todos los archivos modificados de una vez. |
| git commit -m "mensaje" | Guarda una instantánea permanente de los cambios preparados en el repositorio local, asociándola a un mensaje descriptivo de lo que se hizo. |
| git checkout <rama> / git switch <rama> | Cambia de una rama a otra para trabajar en distintas funcionalidades por separado. |
| git merge <rama> | Fusiona el historial y los cambios de una rama específica dentro de la rama en la que te encuentras actualmente. |
| git push | Envía y sube tus commits confirmados desde tu repositorio local hacia el repositorio remoto para compartirlos con el equipo. |
| git pull | Descarga los cambios más recientes desde el repositorio remoto y los fusiona automáticamente con tu copia local. |

## FLUJO DE TRABAJO DIARIO (RESUMEN PRÁCTICO)
En el día a día, casi el 90% de tu interacción con Git sigue este ciclo repetitivo:
1. **Modificas** archivos en tu editor de código.
2. **Revisas** qué cambió con *git status*.
3. **Preparas** los archivos que quieres guardar con *git add .*
4. **Guardas** la versión en tu historial local con *git commit -m* "Añade validación de usuario".
5. **Sincronizas** con el equipo trayendo cambios (*git pull*) y subiendo los tuyos (*git push*).
