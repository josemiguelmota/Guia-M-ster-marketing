[🏠 Índice](../actividad-alumnos.md) · [← Bloque 3](04-datos.md) · [Bloque 5 →](06-articulo.md)

# Bloque 4. Análisis: de los gráficos de Forms a vuestros propios cálculos

| ⏱️ Horario | 👥 Quién | 🧰 Herramientas |
|---|---|---|
| 2:15–2:45 (después del descanso) | Todo el grupo (lidera Coordinación) | Google Forms, Google Sheets, Gemini |

**🎯 Resultado:** columnas calculadas y pestaña Análisis con fórmulas generadas con Gemini y comprobadas, y la figura `figura1.png`.

## 1. Lo que os da Forms, y lo que no (3 min)

Abrid el formulario → **Respuestas** → **Resumen**. Forms dibuja **un gráfico por pregunta**: cuántas publicaciones hay de cada formato, de cada marca, con personas o sin ellas…

Pero cada gráfico mira **una sola pregunta por separado**: no relaciona unas respuestas con otras. Forms no puede deciros:
- qué formato obtiene **más interacción** (eso cruza Formato con Me gusta y Comentarios),
- la **tasa de interacción**, la **media** o la **mediana**,
- si la diferencia se mantiene **dentro de cada marca**.

Es decir, no puede responder a vuestras hipótesis. Además, sus gráficos son en color y DYNA no los admite. Por eso los datos están vinculados a una hoja de cálculo: allí haréis **vuestros propios cálculos**.

> [!TIP]
> 👉 **Anotad los recuentos de Formato y de Marca** que muestra el resumen: os servirán para comprobar vuestras fórmulas.

## 2. Pedid a Gemini fórmulas, no resultados 🟠

Si Gemini os da directamente un número, no sabéis de dónde sale. Si os da una **fórmula**, podéis leerla, comprobarla y dejarla en la hoja: se recalcula sola si cambian los datos, y cualquiera puede repetir vuestro análisis.

Abrid Gemini en el panel de la hoja (icono ✦, arriba a la derecha) o en gemini.google.com y empezad dándole el contexto:

> Trabajo en Google Sheets configurado en español (nombres de funciones en español y punto y coma como separador). La pestaña «Respuestas» se rellena con un formulario de Google y tiene estas columnas: A marca temporal, B ID de la publicación, C marca, D seguidores, E fecha de publicación, F formato (Imagen, Carrusel o Reel), G tema principal, H aparecen personas (Sí/No), I llamada a la acción (Sí/No), J me gusta (puede estar vacía si la marca los oculta), K comentarios, L código de codificador/a (C1–C4), M enlace de la publicación. Las celdas vacías son datos no disponibles, no ceros. Cuando te pida un cálculo, dame la fórmula, dime en qué celda pegarla y explícame qué hace cada parte. No me des el resultado numérico: lo calcularé yo con la fórmula.

## 3. Columnas calculadas en la pestaña Respuestas

El formulario añade una fila nueva con cada respuesta, y una fórmula escrita fila a fila no se copia sola a las filas nuevas. Hay que pedir una fórmula que se aplique a toda la columna:

> Necesito dos columnas calculadas en la pestaña «Respuestas» que se rellenen solas cuando llegue una respuesta nueva del formulario: en N, «Interacción» = me gusta + comentarios (vacía si no hay me gusta); en O, «Tasa de interacción (%)» = interacción ÷ seguidores × 100. Quiero una única fórmula por columna, en la fila 1, que incluya el encabezado.

Pegad las fórmulas en N1 y O1. **Comprobadlas:** elegid dos filas y haced la cuenta con la calculadora del móvil.

## 4. Pestaña Análisis: un cálculo por prompt

Cread una pestaña **Análisis**. Pedid a Gemini una fórmula para cada cálculo, de lo descriptivo a lo interpretativo, con este patrón:

> En la pestaña «Análisis», escríbeme una fórmula que calcule [lo que necesitáis] a partir de la pestaña «Respuestas».

1. Número de publicaciones de cada formato y de cada marca.
2. Tasa de interacción **media** y **mediana** según la variable de vuestra H1 (por ejemplo, el formato), y después según la de vuestra H2.
3. La tasa media **por marca y formato**: ¿se mantiene la diferencia dentro de cada marca, o la provoca una sola marca?
4. Y una pregunta de interpretación, sin fórmula: «¿Qué prueba estadística sería adecuada para comparar estos grupos con esta muestra? Explica por qué y qué limitaciones tendría».

El cálculo 3 es la clave: si la marca con más seguidores publica casi todos los reels, la diferencia puede deberse a la marca y no al formato.

## 5. Comprobad cada fórmula antes de fiaros de ella

| Qué comprobar | Cómo |
|---|---|
| Los recuentos | Deben coincidir con el resumen de Forms que anotasteis |
| Las sumas, tasas y medias | Repetid la cuenta a mano con 2 o 3 filas |
| Que la fórmula mira las columnas correctas | Pinchad en la celda: Sheets colorea los rangos que usa |
| Un error (`#N/A`, `#¡VALOR!`, `#ERROR!`) | Pegad en Gemini la fórmula y el mensaje, y pedid que os explique la causa antes de cambiar nada |

> [!IMPORTANT]
> Si Gemini os da una cifra que no coincide con la de vuestra fórmula comprobada, **manda la fórmula**. Anotad en el diario cada prompt, la fórmula obtenida y cómo la comprobasteis.

<details>
<summary>Si Gemini se atasca: fórmulas de referencia (con el formato como variable)</summary>

| Cálculo | Fórmula |
|---|---|
| Interacción (N1) | `={"Interacción";ARRAYFORMULA(SI(B2:B="";"";SI(J2:J="";"";J2:J+K2:K)))}` |
| Tasa de interacción (O1) | `={"Tasa de interacción (%)";ARRAYFORMULA(SI(N2:N="";"";N2:N/D2:D*100))}` |
| Número de reels | `=CONTAR.SI(Respuestas!F:F;"Reel")` |
| Tasa media de los reels | `=PROMEDIO.SI(Respuestas!F:F;"Reel";Respuestas!O:O)` |
| Mediana de los reels | `=MEDIANA(FILTER(Respuestas!O2:O;Respuestas!F2:F="Reel";Respuestas!O2:O<>""))` |
| Tasa media de los reels de una marca | `=PROMEDIO.SI.CONJUNTO(Respuestas!O:O;Respuestas!F:F;"Reel";Respuestas!C:C;"[marca]")` |

</details>

## 6. Tabla dinámica y figura

1. **Cruzad marca y formato.** Seleccionad los datos de Respuestas → Insertar → **Tabla dinámica** → Hoja nueva. Filas: Marca; Columnas: Formato; Valores: Tasa de interacción resumida por AVERAGE, y otra vez por COUNTA para saber cuántas publicaciones hay detrás de cada media. Comparad sus cifras con las de vuestras fórmulas.
2. **Haced la figura** a partir de vuestra tabla de Análisis, no del resumen de Forms: Insertar → Gráfico → **Gráfico de columnas**. En Personalizar → Serie, barras en gris o negro. Título con el hallazgo y eje con la unidad, por ejemplo «Tasa de interacción media por formato (%)». Menú ⋮ del gráfico → Descargar → Imagen PNG. El archivo se descarga con el título del gráfico: **renombradlo como `figura1.png`**.

> [!NOTE]
> Con 32 publicaciones los resultados son **exploratorios**: hablad de «las publicaciones analizadas», no de «las marcas de moda» en general.

## ✅ Comprobación
- ☐ Columnas Interacción y Tasa de interacción que se rellenan solas.
- ☐ Pestaña Análisis con cada cifra del artículo calculada con una fórmula comprobada.
- ☐ Prompts, fórmulas y comprobaciones anotados en el diario.
- ☐ `figura1.png` descargada.

---

[🏠 Índice](../actividad-alumnos.md) · [← Bloque 3](04-datos.md) · [Bloque 5 →](06-articulo.md)
