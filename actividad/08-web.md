[🏠 Índice](../actividad-alumnos.md) · [← Bloque 6](07-presentacion.md) · [Cierre →](09-cierre.md)

# Bloque 7. Web con Gemini Canvas y GitHub

| ⏱️ Horario | 👥 Quién | 🧰 Herramientas |
|---|---|---|
| 2:45–3:45, en paralelo con los bloques 5 y 6 | Difusión | Gemini Canvas, GitHub, GitHub Pages |

**🎯 Resultado:** repositorio público con artículo, datos y figura, y una web en GitHub Pages.

> [!NOTE]
> Este bloque se hace **a la vez que los bloques [5](06-articulo.md) y [6](07-presentacion.md)**: mientras el resto escribe el artículo y la presentación, Difusión construye la web. Difusión puede crear el repositorio antes, durante el bloque 0 o el 4, para ganar tiempo.

## Parte A. El repositorio

1. En github.com → **+** → New repository → nombre `articulo-[sector]-grupo[n]` (sin espacios ni tildes) → **Public** → **Add a README file** → Create repository.
2. Add file → Upload files → `figura1.png` y `datos.csv` → mensaje `Datos y figura` → Commit changes.
   Para obtener `datos.csv`: en «Datos», con la pestaña Respuestas abierta → Archivo → Descargar → Valores separados por comas (.csv). Se descarga como «Datos - Respuestas.csv»: **renombradlo como `datos.csv`**.
3. Editad `README.md` (lápiz): título, pregunta, método en tres líneas y lista de archivos → Commit changes.

## Parte B. La web con Canvas, en tres versiones

1. **Versión 1.** En gemini.google.com, nueva conversación → activad **Canvas** → pegad este prompt y, debajo, la plantilla:

   > Te paso el index.html de la web de un artículo de investigación. Rellena únicamente las zonas ESTILOS, CABECERA, RESUMEN y PIE con estos textos, sin añadir otros: [título, autores, «Máster Universitario en Dirección de Marketing Digital y Social, Facultad de Ciencias Sociales y de la Comunicación, Universidad de Cádiz», resumen, palabras clave]. Diseño sobrio de publicación académica, muy legible y adaptado al móvil, solo con HTML y CSS. No borres ninguna marca ni cambies nada fuera de esas zonas. Devuélveme el archivo completo.

   ```html
   <!DOCTYPE html>
   <html lang="es">
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1">
     <title>[Título del artículo]</title>
     <style>
       /* ===== INICIO: ESTILOS ===== */
       /* ===== FIN: ESTILOS ===== */
     </style>
   </head>
   <body>
     <!-- INICIO: CABECERA --> <!-- FIN: CABECERA -->
     <!-- INICIO: RESUMEN --> <!-- FIN: RESUMEN -->
     <!-- INICIO: HALLAZGO --> <!-- FIN: HALLAZGO -->
     <!-- INICIO: DESCARGAS --> <!-- FIN: DESCARGAS -->
     <!-- INICIO: CÓMO CITAR --> <!-- FIN: CÓMO CITAR -->
     <!-- INICIO: DECLARACIÓN IA --> <!-- FIN: DECLARACIÓN IA -->
     <!-- INICIO: PIE --> <!-- FIN: PIE -->
   </body>
   </html>
   ```

2. **Revisad la vista previa:** que no haya textos ni datos inventados. Si los hay: «Quita [lo que sobre]; usa solo mis textos».
3. **Subid la versión a GitHub.** En Canvas, pestaña de código → copiad todo. En el repositorio: Add file → Create new file → `index.html` → pegad → mensaje `v1: cabecera y resumen` → Commit changes. (No uséis Descargar de Canvas.)
4. **Activad GitHub Pages** (solo la primera vez): Settings → Pages → Source: Deploy from a branch → Branch: `main`, carpeta `/ (root)` → Save. En uno o dos minutos la web está en `https://[usuario].github.io/[repositorio]/`.
5. **Versiones 2 y 3.** Partid siempre del `index.html` que hay en GitHub (Raw → copiad todo), pegadlo en Canvas y pedid: «Modifica únicamente lo que está entre `<!-- INICIO: [ZONA] -->` y `<!-- FIN: [ZONA] -->`…».

   | Versión | Zonas | Contenido | Mensaje de commit |
   |---|---|---|---|
   | 2 | Hallazgo | `figura1.png` con texto alternativo y la frase del hallazgo | `v2: hallazgo principal` |
   | 3 | Descargas, Cómo citar, Declaración IA | Enlaces a `articulo.pdf`, `presentacion.pdf` y `datos.csv`; referencia en formato DYNA; declaración de IA | `v3: descargas y citación` |

6. **Para actualizar:** abrid `index.html` en GitHub → lápiz → seleccionad todo → pegad la versión nueva → Commit changes.
7. **Comprobad cada commit** en el historial: las líneas en verde y rojo deben estar solo en las zonas de esa versión.

> [!TIP]
> **Opcional (Difusión): ayuda de GitHub Copilot Chat**
>
> Si algo de la web no funciona, podéis preguntar sin salir de GitHub. Con la sesión iniciada, abrid el repositorio y pulsad el **icono de Copilot** (arriba, junto a la barra de búsqueda). Cualquier cuenta tiene **Copilot Free**, con un número limitado de mensajes al mes. Si os lo pide, activadlo en Settings → Copilot.
>
> Usos recomendados 🟠, siempre comprobando el resultado en la web publicada:
> - «¿Por qué no se ve la imagen `figura1.png` en mi `index.html`?»
> - «Explícame qué ha cambiado en mi último commit de `index.html`.»
> - «¿Por qué mi web en GitHub Pages muestra un error 404?»
>
> Copilot **explica y propone**, pero el texto de la web sigue saliendo de vuestros documentos, y los cambios se hacen igual que antes: Canvas → copiar → editar `index.html` → commit. Anotad cada consulta en el diario de prompts y añadid Copilot a la declaración de uso de IA si lo usáis.

## ✅ Comprobación
- ☐ Repositorio público con README, `datos.csv` y `figura1.png`.
- ☐ Tres commits de `index.html` (v1, v2 y v3).
- ☐ Web visible en GitHub Pages, también en el móvil.

---

[🏠 Índice](../actividad-alumnos.md) · [← Bloque 6](07-presentacion.md) · [Cierre →](09-cierre.md)
