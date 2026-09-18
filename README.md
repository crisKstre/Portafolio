# Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub (puede ser público, es requisito para el plan gratuito).
2. Sube `index.html` a la raíz del repositorio.
3. Ve a **Settings → Pages**.
4. En "Source" elige la rama `main` y la carpeta `/root`, luego guarda.
5. En un par de minutos tu sitio queda disponible en `https://tu-usuario.github.io/nombre-del-repo/`.

## Cómo editar el contenido (sin tocar HTML ni CSS)

Abre `index.html`, ve hasta el final del archivo y busca este bloque, marcado claramente con comentarios:

```
EDITAR AQUÍ — esta es la única parte que necesitas tocar...
```

Ahí hay tres listas simples:

- **`CERTIFICACIONES`**: agrega o quita objetos `{ nombre, emisor, anio, archivo }`, uno por certificación. `archivo` es la ruta al PDF de tu certificado (por ejemplo `certificados/mi-certificado.pdf`) — el nombre queda como link a ese archivo. Sube tus PDFs a una carpeta `certificados/` junto a `index.html` en el repositorio. Si dejas `archivo` vacío o lo borras, el nombre se muestra como texto normal, sin link.
- **`PUNTOS_DE_VENTA`**: agrega o quita objetos `{ nombre, ciudad }`, uno por instalación activa. Se acomodan solos en el recuadro — no hay coordenadas que calcular.
- **`PAGINAS_WEB`**: igual que el anterior, pero para tus sitios web entregados.

Para agregar una entrada, copia una línea existente dentro de la lista y cambia el texto. Para quitar una, borra la línea completa. El resto de la página se genera solo a partir de estas listas.

## Otros detalles a personalizar

- **Encabezado y nombre**: busca `tu<span>nombre</span>` en el HTML.
- **Contacto**: correo, WhatsApp y GitHub están al final del archivo, en la sección `#contacto`.

El archivo es autónomo (un solo `index.html`), así que no necesitas ningún build ni dependencias — solo subirlo tal cual.
