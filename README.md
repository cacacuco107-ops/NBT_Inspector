# NBT Inspector

Editor web de `level.dat` para **Minecraft Java Edition** y **Bedrock Edition**.
Lee, muestra en árbol y permite editar el NBT binario directamente en el navegador — sin subir el archivo a ningún servidor.

**Demo en vivo:** `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`
(reemplaza con tu usuario y el nombre real del repo una vez publicado)

## Qué hace

- Detecta automáticamente si el archivo es Java (NBT comprimido con gzip, big-endian) o Bedrock (NBT little-endian con cabecera de versión).
- Árbol expandible/colapsable de todos los tags NBT, coloreados por tipo.
- Edición de valores numéricos, strings, arrays (byte/int/long) y renombrado de tags.
- Añadir o eliminar tags dentro de compounds y listas.
- Búsqueda por nombre de tag.
- Exporta un `level.dat` nuevo, reconstruyendo el binario exacto (gzip para Java, cabecera de longitud para Bedrock).

Todo el procesamiento ocurre 100% en el navegador (JavaScript puro, sin dependencias ni backend).

## Uso local

Solo necesitas abrir `index.html` en un navegador (Chrome, Edge, Firefox o Safari recientes). No requiere instalación ni servidor.

## Publicar en GitHub Pages

1. Sube este repo a GitHub (ver sección siguiente si aún no lo hiciste).
2. En el repo, ve a **Settings → Pages**.
3. En "Source" (o "Build and deployment"), elige la rama `main` y la carpeta `/ (root)`.
4. Guarda. En un par de minutos tu sitio quedará disponible en:
   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`

## Subir este repo a GitHub desde cero

```bash
cd nbt-inspector-repo
git init
git add .
git commit -m "NBT Inspector: editor de level.dat para Java y Bedrock"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/NOMBRE-DEL-REPO.git
git push -u origin main
```

Luego sigue los pasos de "Publicar en GitHub Pages" de arriba.

## Requisitos del navegador

Usa `CompressionStream` / `DecompressionStream` nativos (para el gzip de Java Edition). Disponibles en Chrome/Edge, Firefox 113+ y Safari 16.4+, tanto en PC como en Android.

## Nota sobre Bedrock en Android/consolas

Para editar el `level.dat` real de un mundo con la app de Minecraft Bedrock, primero tienes que extraerlo de la carpeta del juego (con un explorador de archivos con permisos adecuados) y luego volver a colocarlo ahí tras editarlo.

## Licencia

Úsalo, modifícalo y compártelo libremente.
