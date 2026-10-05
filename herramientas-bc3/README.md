# Herramientas BC3

Auditor y visor de presupuestos en formato FIEBDC-3 (.bc3), como páginas web estáticas.
Todo se procesa en el navegador: el BC3 no se sube a ningún servidor.

- `index.html`: página de inicio
- `auditor.html`: auditoría automática con 22 reglas e informe Excel
- `visor.html`: árbol del presupuesto, descompuestos, mediciones y recursos
- `lib/`: librería de Excel (SheetJS 0.18.5, Apache 2.0), incluida para no depender de un CDN
- `manifest.webmanifest` e iconos: para añadirla a la pantalla de inicio del móvil

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub, por ejemplo `herramientas-bc3`.
2. Sube **el contenido** de esta carpeta a la raíz del repositorio (no la carpeta en sí):
   en la página del repositorio, *Add file → Upload files* y arrastra todos los archivos,
   incluida la carpeta `lib`. Pulsa *Commit changes*.
3. Ve a *Settings → Pages*. En *Build and deployment*, elige *Deploy from a branch*,
   rama `main` y carpeta `/ (root)`. Guarda.
4. En uno o dos minutos estará en `https://TU-USUARIO.github.io/herramientas-bc3/`.

El archivo `.nojekyll` es oculto; si al arrastrar no se sube, no pasa nada: las páginas funcionan igual.

Con una cuenta gratuita de GitHub, Pages solo funciona con repositorios **públicos**.
Eso hace público el código de la herramienta, no tus presupuestos: los BC3 nunca se guardan en el repositorio.
No subas BC3 de obras reales al repositorio.

## Actualizar

Sube la nueva versión del archivo que cambie (por ejemplo `auditor.html`) con *Add file → Upload files*.
GitHub Pages tarda un minuto en publicarla. Si el navegador sigue mostrando la anterior, recarga con Ctrl+F5.

## Uso local

También funciona sin publicar: abre `index.html` con doble clic. Solo necesita internet para la tipografía;
sin conexión se usa la del sistema y todo lo demás funciona.
