---
marp: true
paginate: true
title: IA orientada a la investigación en marketing
---

<!--
Presentación de la sesión. Cada diapositiva va separada por una línea "---".
Compatible con Marp (extensión "Marp for VS Code"): se puede proyectar o exportar a PDF/PPTX.
Los comentarios HTML son notas del orador.
-->

# IA orientada a la investigación en marketing

**De la pregunta a la publicación abierta en cuatro horas**
Con métodos transparentes y verificables

Seminario práctico de investigación
**Máster Universitario en Dirección de Marketing Digital y Social**
Facultad de Ciencias Sociales y de la Comunicación · Universidad de Cádiz
5 de noviembre de 2026

<!-- Bienvenida. Hoy cada grupo hará una investigación completa, de principio a fin. No hace falta saber programar ni haber usado antes estas herramientas. -->

---

## Objetivo de la sesión: un proyecto de investigación completo

| Análisis real | IA transparente | Ciencia abierta |
|---|---|---|
| Análisis de contenido de **32 publicaciones de Instagram** de **4 marcas** comparables | **Gemini** como asistente declarado, con un **diario de prompts** | Artículo, datos y web publicados en **GitHub Pages** |

> **Regla fundamental:** la IA apoya el proceso, pero **nunca firma como autora**.

---

## Al terminar la sesión sabréis…

1. Usar la IA generativa para formular preguntas, explorar un tema y analizar datos, y **comprobar lo que responde**.
2. Buscar, verificar y citar **bibliografía real** con un gestor de referencias.
3. Recoger y analizar **datos propios** con criterios que otra persona pueda repetir.
4. Escribir un **artículo breve** con estructura científica y **declarar el uso de IA**.
5. Comunicar el estudio en una **presentación** y en una **web pública** con datos abiertos.

---

## El proyecto, paso a paso

1. **Pregunta** — sector, 4 marcas, una pregunta y dos hipótesis. Gema revisora.
2. **Literatura** — al menos 6 artículos académicos reales, comprobados, en Zotero.
3. **Datos** — 32 publicaciones (8 por marca) codificadas con las mismas reglas.
4. **Análisis** — la IA analiza; vosotros comprobáis cada cifra con fórmulas.
5. **Artículo** — estructura científica, citas automáticas y declaración de IA.
6. **Presentación** — 3 minutos, 6 diapositivas.
7. **Web** — resumen, hallazgo y archivos descargables en GitHub Pages.

<!-- Ejemplo de pregunta: ¿qué formato (reel, carrusel o imagen) genera más interacción en las marcas de moda sostenible? -->

---

## Marco ético: el semáforo de la IA

| 🟢 Verde: libre | 🟠 Ámbar: verificar | 🔴 Rojo: prohibido |
|---|---|---|
| Lluvia de ideas | Analizar datos | Inventar o completar datos |
| Revisar estilo y ortografía | Resumir artículos | Citar fuentes no comprobadas |
| Dar formato | Sugerir dónde buscar | Redactar resultados y discusión |
| Generar el código de la web | **Todo se verifica** | |

Cada uso importante se anota en el **diario de prompts**:
hora · herramienta · prompt · para qué · color · cómo se verificó

---

## La cadena de herramientas

La salida de un bloque es la entrada del siguiente.

**Gemini y Gemas** → **Zotero** → **Google Sheets** → **Google Docs + plantilla DYNA** → **Slides** · **Gemini Canvas** → **GitHub Pages**

| Herramienta | Para qué sirve hoy |
|---|---|
| Gemini | Explorar el tema, analizar datos, generar código |
| Gemini Gems | Un revisor con instrucciones fijas |
| Zotero | Guardar, comprobar y citar referencias |
| Google Sheets | Registrar, analizar y verificar los datos |
| Google Docs / Slides | Escribir el artículo / presentarlo |
| Gemini Canvas + HTML, CSS, JS | Construir la web |
| GitHub y GitHub Pages | Guardar con historial y publicar |

<!-- Todo es gratuito o está incluido en la cuenta de Google de la UCA. Overleaf, como complemento opcional. -->

---

## Gemini: qué hay que saber

- Es un **modelo de lenguaje**: genera la respuesta más probable, no consulta una base de datos de verdades.
- Escribe **con la misma seguridad cuando acierta que cuando se equivoca**.
- Puede **inventar referencias muy creíbles** y **equivocarse en cálculos**.

**Cómo usarlo bien:** dad contexto al principio del prompt (quiénes sois, qué tenéis, qué queréis) y **verificad todo lo que sea un dato o una cita**.

---

## La Gema revisora

Una versión de Gemini con **instrucciones permanentes**.

- **Papel:** actúa como revisor/a ciego/a de una revista científica.
- **Función:** señala puntos fuertes y débiles, afirmaciones sin cita y conclusiones que van más allá de los datos.
- **Límite estricto:** **no redacta** párrafos por vosotros.

> Prueba de fuego: pedidle «Escríbeme la introducción». Debe negarse.

Sus comentarios son sugerencias: el grupo decide cuáles aplica y anota por qué.

---

## Literatura real con Zotero

- **Mínimo:** 6 artículos académicos reales, con DOI, en una **biblioteca de grupo**.
- **Gemini sugiere dónde buscar; las fuentes las encontráis y comprobáis vosotros.**
- Cada referencia:
  - ✅ existe (el DOI lleva a la web de la revista),
  - ✅ tiene los datos correctos en Zotero,
  - ✅ dice lo que vais a citar,
  - ✅ lleva una **nota de lectura** de tres líneas.
- Citas insertadas desde el **menú Zotero de Google Docs**: nada de citas a mano.

---

## Datos: análisis de contenido verificado

1. **Desplegables cerrados** en Sheets: nadie escribe «reel», «Reels» y «vídeo» para lo mismo.
2. **Libro de códigos** común: una definición para cada categoría.
3. **Fiabilidad:** dos personas codifican las mismas 5 publicaciones → **acuerdo mínimo del 80 %**.
4. **Verificación con fórmulas:** cada cifra de Gemini se repite con `CONTAR.SI`, `PROMEDIO.SI` o `MEDIANA`.

> **Si Gemini y la fórmula no coinciden, manda la fórmula.**

---

## Ética y privacidad de los datos

- Solo **cuentas públicas de marcas** y **observación manual**: el scraping incumple las condiciones de Instagram.
- **No** se anotan nombres de usuarios particulares ni se copian sus comentarios.
- **No** se introducen datos personales en la IA ni en el repositorio.
- Si falta un dato, **la celda queda vacía**: nunca se rellena con IA.
- Con 32 publicaciones los resultados son **exploratorios**: «las publicaciones analizadas», no «las marcas de moda».

---

## La revista de referencia: DYNA

Trabajamos con las **normas y la plantilla oficial** de una revista real:
[revistas.unal.edu.co/index.php/dyna/about](https://revistas.unal.edu.co/index.php/dyna/about)

- Título, resumen (máx. 150 palabras) y palabras clave **en inglés y en español**.
- Apartados numerados, **tres niveles como máximo**.
- Citas **numéricas entre corchetes**: `[1,2]`, `[1-3]`.
- Figuras **sin color** (escala de grises), título debajo y fuente.
- Biografías de autores con **ORCID**.

<!-- DYNA es una revista de ingeniería: la usamos como ejercicio de formato. Para un envío real habría que elegir una revista de marketing o comunicación. -->

---

## Organización: cuatro roles por grupo

| Coordinación y datos | Literatura | Redacción | Difusión |
|---|---|---|---|
| Pregunta inicial | Biblioteca Zotero | Estructura del artículo | Repositorio GitHub |
| Hoja de codificación | Citas y DOI | Coherencia global | Web con Canvas |
| Análisis y fórmulas | Marco teórico | Revisión con la Gema | |
| Presentación oral | | | |

En la recogida de datos, **las cuatro personas codifican** (8 publicaciones cada una, una marca por persona).

---

## Plan de las 4 horas

| Hora | Bloque | Resultado |
|---|---|---|
| 0:00–0:15 | Presentación, grupos y roles | Roles repartidos |
| 0:15–0:45 | 0. Cuentas e instalaciones (por roles) | Drive, Zotero y GitHub listos |
| 0:45–1:05 | 1. Pregunta de investigación | Pregunta, 2 hipótesis y Gema |
| 1:05–1:30 | 2. Literatura | ≥ 6 referencias comprobadas |
| 1:30–2:05 | 3. Recogida de datos | 32 publicaciones y fiabilidad |
| 2:05–2:15 | *Descanso* | |
| 2:15–2:45 | 4. Análisis | Cifras verificadas y `figura1.png` |
| 2:45–3:40 | 5, 6 y 7. Producción en paralelo | Artículo, presentación y web |
| 3:40–4:00 | Presentaciones de 3 min y cierre | Enlace entregado |

---

## Primero: cuentas e instalaciones (30 min, en paralelo)

| Quién | Qué prepara |
|---|---|
| **Todo el grupo** | Cuenta en zotero.org · acceso a Instagram (vale la app del móvil) |
| **Coordinación y datos** | Carpeta en Drive, «Artículo», «Datos» y diario de prompts |
| **Literatura y Redacción** | Zotero de escritorio + Connector en Chrome · biblioteca de grupo · cita de prueba en Google Docs |
| **Difusión** | Cuenta de GitHub (correo personal, usuario profesional) |

- Quien instale Zotero, mejor en su **portátil**: el aula puede no dejar instalar.
- **Plan B** sin instalación: referencias por DOI en zotero.org y bibliografía con zbib.org.
- Tened el **móvil a mano**: llegan códigos de verificación.

<!-- Ir pasando por los grupos: Zotero y la conexión con Google Docs es lo que más se atasca. La verificación en dos pasos de GitHub, si no la exige en el momento, se deja para casa (anexo de la guía). -->

---

## Entregables: un único enlace

| Producto | Formato final |
|---|---|
| Artículo breve (1.500–2.000 palabras, plantilla DYNA) | `articulo.pdf` |
| Datos y análisis | `datos.csv` y hoja compartida |
| Figura del hallazgo principal (escala de grises) | `figura1.png` |
| Presentación de 3 minutos | `presentacion.pdf` |
| Web del artículo | Página en GitHub Pages |
| Transparencia | Diario de prompts y declaración de IA |

> Se entrega **la dirección de la web en GitHub Pages**: desde ella se llega a todo lo demás.

---

## Evaluación

| Criterio | Qué se valora | Peso |
|---|---|---|
| Datos y análisis | Libro de códigos, fiabilidad, cifras verificadas | **25 %** |
| Literatura | ≥ 6 referencias reales citadas con Zotero | **20 %** |
| Pregunta y coherencia | Pregunta respondible, hipótesis claras | **15 %** |
| Redacción | Normas DYNA, conclusiones ajustadas a los datos | **15 %** |
| Transparencia | Diario de prompts, declaración de IA, datos abiertos | **15 %** |
| Difusión | Web funcional y presentación en 3 minutos | **10 %** |

---

## ¡Comenzamos!

1. Formad los **grupos de 4**, repartid los **roles** y elegid el **sector**.
2. Empezad el **bloque 0**: cada rol prepara sus cuentas e instalaciones.
3. Coordinación crea la **carpeta compartida** (con el profesor como editor) y el **diario de prompts**.

Tenéis todos los pasos y prompts en la **guía de la actividad**.

> Lo que produce la IA es un borrador hasta que una persona lo comprueba con una fuente independiente.
