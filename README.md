# Diario de Cristina

App web para el seguimiento diario de salud: ejercicio, comidas, medicación, energía y evolución de analíticas. Funciona en el móvil como una app (se instala en la pantalla de inicio, va a pantalla completa y funciona sin conexión).

Es una app estática (solo HTML, CSS y JavaScript). No necesita servidor ni base de datos: los datos se guardan en el propio móvil.

## Archivos

- `index.html` — la aplicación completa.
- `manifest.json` — datos de instalación (nombre, icono, color).
- `service-worker.js` — permite el uso sin conexión y la instalación.
- `icon.svg` / `icon-192.png` / `icon-512.png` / `apple-touch-icon.png` — el icono de la app.
- `README.md` — este archivo.

Todos deben estar en la **misma carpeta** (la raíz del repositorio).

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `diario-cristina`).
2. Sube todos los archivos de esta carpeta a la raíz del repositorio.
3. En el repositorio: **Settings → Pages**.
4. En **Source**, elige la rama `main` y la carpeta `/root`. Guarda.
5. Espera un minuto. GitHub te dará una dirección del tipo
   `https://TU-USUARIO.github.io/diario-cristina/`.

## Instalar en el móvil

Abre esa dirección en el navegador del móvil y añádela a la pantalla de inicio:

- **iPhone (Safari):** botón Compartir → *Añadir a pantalla de inicio*.
- **Android (Chrome):** menú de tres puntos → *Instalar aplicación* / *Añadir a pantalla de inicio*.

Aparecerá con el icono y se abrirá a pantalla completa, como una app normal.

## Los datos

Se guardan solo en el móvil donde se usa (no se envían a ningún sitio). Por eso:

- No se sincronizan entre dispositivos.
- Si se borra el navegador o los datos del sitio, se pierden.

Conviene exportar/copiar de vez en cuando si os interesa conservarlos a largo plazo (aún no implementado; se puede añadir).

## Actualizar la app más adelante

Cuando cambies `index.html`, sube el nuevo archivo y **sube también el número de versión** en `service-worker.js` (la línea `const CACHE = 'diario-cristina-v1'` → `v2`, `v3`…). Así el móvil coge la versión nueva en lugar de la guardada.

## Nota

Es una herramienta de apoyo a hábitos, no un dispositivo médico. La medicación, las analíticas y cualquier decisión de salud deben confirmarse siempre con el médico correspondiente.
