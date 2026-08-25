# Mi Estudio de Cábala — PWA

Aplicación personal, sin dependencias y preparada para instalarse desde Safari o Chrome. Incluye una ruta de 40 lecciones, Lección 1 completa, estados de progreso, notas, tarjetas, examen, temporizador, tema claro/oscuro y respaldo de datos.

## Publicar con GitHub Pages

1. Descomprime el ZIP.
2. Sube **los archivos del interior** a la raíz de un repositorio público de GitHub.
3. En **Settings → Pages**, selecciona **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
4. Abre la dirección publicada. En iPhone: Safari → Compartir → Agregar a Inicio.

También puede publicarse en cualquier alojamiento estático con HTTPS. El service worker necesita HTTPS, salvo en `localhost`.

## Privacidad y respaldo

El progreso y las notas se guardan en `localStorage`, dentro del navegador del dispositivo. No se envían a ningún servidor. Usa **Respaldo → Exportar progreso** periódicamente y guarda el archivo JSON en un lugar seguro.

## Archivos

- `index.html`: interfaz, contenido y lógica.
- `manifest.json`: instalación PWA.
- `service-worker.js`: uso sin conexión y caché.
- `icon-192.png` y `icon-512.png`: iconos de instalación.

Para publicar una actualización, reemplaza los archivos existentes. Si modificas recursos y el dispositivo conserva una versión anterior, cambia el nombre de `CACHE` en `service-worker.js`.
