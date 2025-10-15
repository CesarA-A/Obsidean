# Git: Guía Completa

## ¿Qué es Git?

Git es un **sistema de control de versiones distribuido** que permite:

- Guardar y versionar el historial de tus archivos.
- Trabajar en equipo sin perder información.
- Volver a estados anteriores de tu proyecto.

Git es diferente de GitHub. **Git** es la herramienta local y **GitHub** es un servicio remoto para almacenar repositorios.

---

## Conceptos clave

- **Repositorio (repo):** Carpeta que Git controla.
- **Commit:** Guardar un conjunto de cambios en el repositorio.
- **Branch (rama):** Línea de desarrollo independiente.
- **Merge:** Combinar cambios de una rama a otra.
- **Remote:** Repositorio remoto (ej: GitHub, GitLab).
- **Clone:** Copiar un repositorio remoto localmente.
- **Pull:** Traer cambios desde el remoto.
- **Push:** Enviar cambios locales al remoto.
- **Stage / Index:** Área temporal donde agregas cambios antes de hacer commit.

---

## Configuración inicial

```bash
# Nombre y correo del usuario
git config --global user.name "Tu Nombre"
git config --global user.email "tu.email@dominio.com"

# Evitar problemas de saltos de línea entre Windows y Linux
git config --global core.autocrlf input

# Ver configuración
git config --global --list

|Comando|Para qué sirve|
|---|---|
|`git status`|Ver archivos modificados|
|`git add .`|Preparar archivos para commit|
|`git commit -m "mensaje"`|Guardar cambios localmente|
|`git push origin main`|Subir cambios a GitHub|
|`git pull origin main`|Traer cambios de GitHub|
```
