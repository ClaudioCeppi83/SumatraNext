# Contexto del Proyecto "SumatraNext"

Este documento sirve como guía interna y bitácora para el desarrollo de "SumatraNext", un fork modernizado de SumatraPDF.

## Misión del Proyecto
Modernizar el lector de documentos SumatraPDF, añadiendo funcionalidades clave y mejorando la experiencia de usuario, sin comprometer su ligereza y rendimiento.

## Roadmap General
El roadmap detallado se gestiona a través de los Issues de GitHub. Las fases principales son:
1.  **Fase 0: Fundación y Estrategia** (Actual)
2.  **Fase 1: Refactorización Técnica**
3.  **Fase 2: Mejoras de UI/UX**
4.  **Fase 3: Modernización y Futuro**

---

## Estado Actual

### **Fase Actual:** Fase 1: Refactorización Técnica
### **Hito Actual:** Hito 1: Migración a CMake

### **Decisiones Clave Tomadas:**
*   **Nombre del Proyecto:** SumatraNext
*   **Repositorio:** Público en GitHub (`https://github.com/ClaudioCeppi83/SumatraNext`)
*   **Estrategia de Ramas:** `main` (estable), `develop` (desarrollo principal).
*   **Versionamiento:** Semántico (SemVer).
*   **Documentación:** `README.md` (público), `CHANGELOG.md` (historial de cambios), `context.md` (guía interna).
*   **Entorno de Desarrollo:** Visual Studio Build Tools 2022 (compilación por línea de comandos con MSBuild).

---

## Siguiente Paso Concreto

El siguiente paso es continuar con la migración a CMake. Esto implica analizar los proyectos de la solución de Visual Studio (`.vcxproj`) para identificar sus archivos fuente, dependencias y configuraciones, y replicarlos en archivos `CMakeLists.txt` secundarios.

---

## Historial de Acciones Recientes
*   **Fase 0 completada:** Entorno de desarrollo validado y artefactos de compilación limpiados.
*   Inicio de la Fase 1: Creado el archivo `CMakeLists.txt` raíz como primer paso de la migración.
*   Migración de `zlib` a CMake completada con éxito.
*   Corregido el error de rutas de inclusión en `libwebp` CMakeLists.txt.
*   Migración de `libwebp` a CMake completada con éxito.
*   Migración de `bzip2` a CMake completada con éxito.
*   Migración de `lzma` a CMake completada con éxito.
*   Migración de `unarrlib` a CMake completada con éxito.
*   Migración de `CHMLib` a CMake completada con éxito.
*   Migración de `libjpeg-turbo` a CMake completada con éxito.
*   Migración de `libdjvu` a CMake completada con éxito.
