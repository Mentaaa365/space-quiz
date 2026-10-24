# Órbita — Quiz de exploración espacial

Órbita es un quiz interactivo en español sobre exploración espacial. Incluye
preguntas de opción múltiple, seguimiento del progreso y la puntuación,
explicaciones para las respuestas y la posibilidad de volver a jugar.

## Ejecutar en local

No se necesitan dependencias ni un proceso de compilación. Abre `index.html`
directamente en un navegador. También puedes servir el directorio con Python:

```sh
python -m http.server 8000
```

Después, visita <http://localhost:8000>.

## Publicación

El sitio se publica en GitHub Pages mediante GitHub Actions. Cada pull request
comprueba que exista el archivo `index.html` y prepara el artefacto estático; al
integrar cambios en `main`, el workflow despliega el sitio.
