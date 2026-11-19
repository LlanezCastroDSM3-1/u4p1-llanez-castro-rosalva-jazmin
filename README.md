# U4S7 — Llanez Castro Rosalva Jazmín

## Demo en vivo (producción)
https://u4s7-llanez-castro-rosalva-jazmin.onrender.com

## Semana 7 — Pulido funcional y UX
Paginación, búsqueda simple y estado vacío agregados al listado.
Hallazgos de la UI review corregidos: Se mejoró el contraste de los textos secundarios en gris claro (cambiando text-slate-400 a text-slate-600), se aumentó el área táctil de los enlaces de «Editar» y «Eliminar» en móvil, y se verificó el desplazamiento horizontal de la tabla en pantallas de 375px.
## Correcciones u4p1

1. **Protección de credenciales y archivo `.env`:** En el video de entrega anterior el archivo `.env` quedó abierto en pantalla mostrando datos sensibles. Para proteger la aplicación, restablecí la contraseña de la base de datos en Aiven (`DB_PASSWORD`), generé una nueva clave secreta de Django (`SECRET_KEY`) y actualicé ambos valores tanto en mi entorno local como en las variables de entorno de Render. Tambien, oculté el archivo en VS Code para evitar exponerlo por accidente.
2. **Corrección de `.env.example`:** Eliminé `.env.example` del `.gitignore` para que Git lo rastreara correctamente, lo renombré agregándole el punto inicial (`env.example` a `.env.example`) y reemplacé el `SECRET_KEY` real que había quedado guardado por valores ficticios de ejemplo.
3. **Simulacro de Live Coding:** Agregué el campo booleano `disponible` (con `default=True`) al modelo `Servicio` en `models.py`, lo incluí en los campos del formulario en `forms.py` y generé y apliqué la migración correspondiente en vivo, comprobando que los registros anteriores se mantuvieron intactos y que la casilla funciona correctamente en la vista de edición.
