# Proyecto AR - Instrucciones

## Qué contiene este proyecto
- `index.html` — la escena de realidad aumentada con 3 marcadores de ejemplo (salvación, tesoros, nombre).
- `markers/` — aquí van los archivos `.patt` de tus marcadores (debes crear esta carpeta y agregar tus archivos).

## Cómo agregar tus marcadores reales

1. Prepara cada imagen con un marco negro grueso alrededor (necesario para que AR.js pueda leerla como patrón).
2. Sube cada imagen a: https://ar-js-org.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
3. Descarga el `.patt` generado.
4. Crea una carpeta llamada `markers` junto a tu `index.html`.
5. Guarda ahí tus archivos con estos nombres exactos (o cambia el nombre en el HTML si prefieres otros):
   - `markers/salvacion.patt`
   - `markers/titulos.patt`
   - `markers/nombre.patt`

## Cómo agregar los 9 temas restantes

Por cada tema nuevo:
1. Genera su `.patt` (mismo proceso de arriba) y guárdalo en `markers/`.
2. Copia dentro de `index.html` uno de los bloques `<a-marker> ... </a-marker>` completo.
3. Cambia el `url="markers/tuarchivo.patt"` por el nuevo archivo.
4. Cambia el texto dentro de `<a-text value="...">` por la información de ese tema.
   - Usa `\n\n` dentro del texto para saltos de línea.

## Cómo probarlo

**En tu computadora (sin cámara todavía, solo para revisar que no haya errores):**
```
python -m http.server 8000
```
Abre `http://localhost:8000` en el navegador.

**En tu celular (con cámara, ya funcional):**
Necesitas subir el proyecto a un hosting con HTTPS, por ejemplo GitHub Pages:
1. Crea un repositorio en GitHub.
2. Sube `index.html` y la carpeta `markers/`.
3. Ve a Settings > Pages, activa GitHub Pages sobre la rama principal.
4. Espera unos minutos y abre el link que te da (algo como `https://tuusuario.github.io/tu-repo/`) desde el navegador de tu celular.
5. Da permiso de cámara cuando te lo pida.

## Notas útiles

- Imprime los marcadores lo más grande posible dentro del espacio de tu cartulina (mínimo 5x5 cm) — entre más grande, mejor detección.
- Evita imprimir los marcadores muy brillantes o plastificados: el reflejo de la luz puede dificultar que la cámara los reconozca.
- Prueba siempre con buena iluminación antes de tu exposición.
- Si un marcador no se reconoce bien, intenta con una imagen de mayor contraste (blanco y negro puro suele funcionar mejor que colores).
