

# 🌐 Dashboard de Escenarios 3D interactivos

> **Proyecto Académico para la materia de Graficación** > Desarrollado por **Michell Ostria Martinez ** (*Abril 2026*)
> 🎓 *Instituto Tecnológico de Pachuca (TECNM)* | Ingeniería en Sistemas Computacionales

---

## 🧭 Resumen del Sistema

Este proyecto es una plataforma web interactiva construida bajo el concepto de **Single Page Application (SPA)** que sirve como catálogo y entorno de pruebas para diversas capacidades de **WebGL** mediante **Three.js**.

Para garantizar un rendimiento óptimo y evitar la colisión de scripts, el sistema utiliza un núcleo centralizado que renderiza cada escenario mediante **iframes dinámicos**. Esto aísla los recursos `.js` y `.css`, permitiendo que cada escena funcione de forma independiente pero integrada.

---

## 🎬 Catálogo de Escenarios Incluidos

La aplicación se divide en 5 módulos interactivos, cada uno diseñado para demostrar una faceta específica de la manipulación 3D:

| Escena | Tipo de Demostración | Características Clave |
| --- | --- | --- |
| 🧱 **Geometry - Minecraft** | Vóxeles y Geometría | Replicación de un entorno voxelizado con navegación básica. |
| 🗺️ **Controls - Map** | Navegación 2.5D / Plana | Controles estilo mapa interactivo (paneo, arrastre y zoom). |
| 🔄 **Controls - Orbit** | Enfoque de Objeto | Cámara orbital que rota de manera fluida alrededor de un objetivo central. |
| 🕹️ **Controls - PointerLock** | Primera Persona (FPS) | Navegación de juego en primera persona con bloqueo de puntero y físicas básicas de salto/colisión. |
| 🛠️ **Controls - Transform** | Manipulación Directa | Interfaz para trasladar, rotar y escalar objetos tridimensionales en tiempo real. |

---

## 🏗️ Arquitectura y Tecnologías

El stack tecnológico fue seleccionado para ofrecer una experiencia responsiva, modular y de última generación:

* **Núcleo 3D:** `Three.js` (Motor WebGL) utilizando *importmaps* para la gestión nativa de módulos ES6+.
* **Interfaz de Usuario (UI):** `Bootstrap 5` para el diseño del Dashboard adaptativo y `CSS3` personalizado con la tipografía *Inter* (Google Fonts) e iconos vectoriales.
* **Lógica de Integración:** `JavaScript (ES6+)` para la manipulación dinámica del DOM y la inyección de contextos en el contenedor principal.

> 💡 **Nota de Optimización:** Cada escena incluye un script de escucha (`resize`) que ajusta dinámicamente el *canvas* 3D al 100% del contenedor del iframe, eliminando barras de scroll y manteniendo el aspecto de pantalla completa dentro del visualizador.

---

## 🚀 Despliegue Local

Debido a que el proyecto implementa módulos de JavaScript (`type="module"`) y carga recursos de forma externa, **no se puede abrir directamente el archivo HTML en el navegador**. Sigue estos pasos para montarlo en un servidor local:

### Requisitos Previos

* Un editor de código (Se recomienda **Visual Studio Code**).
* Una extensión de servidor local (Ej. **Live Server** para VS Code).

### Pasos para Ejecución

1. **Descarga:** Clona este repositorio o descarga los archivos fuente en tu equipo.
2. **Apertura:** Abre la carpeta raíz del proyecto desde tu editor de código.
3. **Lanzamiento:** Haz clic derecho sobre el archivo `index.html` y selecciona **"Open with Live Server"** (o arranca tu servidor HTTP preferido en ese directorio).
4. **Exploración:** Utiliza el menú lateral interactivo del Dashboard para conmutar entre las diferentes demos en tiempo real.
