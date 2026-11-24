# PASOS PARA HACER PULL REQUEST

Una Pull Request (PR) en GitHub sirve para proponer que los cambios realizados en una rama (branch) se integren en otra, normalmente en `main` o `develop`.

Estos son los pasos para crear una Pull Request desde cero.

## 1. Actualizar tu repositorio local

Primero, descarga los últimos cambios del repositorio:

bash

```bash
git checkout main
git pull origin main
```

## 2. Crear una nueva rama

Crea una rama para trabajar en tu tarea o funcionalidad:

bash

```bash
git checkout -b feature/nombre-de-la-tarea
```

Por ejemplo:

bash

```bash
git checkout -b feature/login
```

## 3. Realizar los cambios

Modifica los archivos de tu proyecto y comprueba qué archivos has cambiado:

bash

```bash
git status
```

## 4. Añadir los cambios (stage)

Añade los archivos que quieres incluir en el commit:

bash

```bash
git add .
```

O un archivo concreto:

bash

```bash
git add src/login.js
```

## 5. Hacer un commit

Guarda los cambios con un mensaje descriptivo:

bash

```bash
git commit -m "feat: add login functionality"
```

## 6. Subir la rama a GitHub

Sube tu nueva rama al repositorio remoto:

bash

```bash
git push origin feature/login
```

## 7. Crear la Pull Request en GitHub

1. Entra en tu repositorio de GitHub.
2. Busca el botón Compare & pull request (normalmente aparece después de subir la rama).
3. Si no aparece, ve a la pestaña Pull requests.
4. Haz clic en New pull request.
5. Selecciona las ramas:
   - Base: rama donde quieres integrar los cambios (`main`).
   - Compare: rama donde has realizado los cambios (`feature/login`).

## 8. Completar la Pull Request

Pull Request Guide - Imageomics Guide

[imageomics.github.io](<https://imageomics.github.io/Imageomics-guide/wiki-guide/The-GitHub-Pull-Request-Guide/?utm_source=chatgpt.com>)

Rellena los campos:

- Title: título descriptivo, por ejemplo: `Add login functionality`.
- Description: explica qué cambios has realizado.
- Reviewers: selecciona las personas que deben revisar el código (si corresponde).
- Assignees: asigna responsables si es necesario.

Finalmente, pulsa Create pull request.

## 9. Revisión y merge

Una vez creada la PR:

1. Los compañeros revisan el código.
2. Pueden aprobarla (Approve) o solicitar cambios (Request changes).
3. Si solicitan cambios, los realizas en tu misma rama.
4. Haces otro commit y un `git push`.
5. Los cambios aparecerán automáticamente en la Pull Request.
6. Cuando esté aprobada, se puede pulsar Merge pull request.

## Resumen del flujo completo

1. Actualizar `main`
   `git pull origin main`
2. Crear una rama
   `git checkout -b feature/login`
3. Realizar cambios en el código
4. Añadir y guardar cambios
   `git add .`
   `git commit -m "feat: add login"`
5. Subir la rama
   `git push origin feature/login`
6. Crear la Pull Request en GitHub
7. Revisar y aprobar
8. Hacer Merge
