# 🧬 Quizzes de Lulú — Biología 3.º A

Plataforma de exámenes de práctica para estudiar desde el celular.

**Link del sitio:** https://agerbilsky.github.io/Lulu_biologia/

**29 exámenes · 340 preguntas · 2 unidades**

Todos los archivos son HTML autónomos: no cargan fuentes, scripts ni imágenes de afuera.
Por eso abren bien incluso desde el navegador interno de WhatsApp en el iPhone.

---

## 😤 Si el sitio muestra una versión vieja

Es caché del navegador, no un problema del repo. Por orden:

1. Abrir el link con un parámetro al final, que saltea el caché:
   `https://agerbilsky.github.io/Lulu_biologia/?v=3` (cambiar el número cada vez)
2. Si así se ve bien, limpiar el caché de verdad:
   **Ajustes → Safari → Borrar historial y datos de sitios web**
3. Si sigue igual, revisar el deploy: pestaña **Actions** del repo. El último
   *pages build and deployment* tiene que tener el check verde.

GitHub Pages tarda entre 30 segundos y 2 minutos en publicar después de cada commit,
y su CDN cachea unos 10 minutos. Mirar enseguida de subir algo siempre muestra lo anterior.

---

## 🔄 Cómo actualizar un examen

1. Editar o reemplazar el `.html` que corresponda.
2. **Importante:** abrir `index.html` y cambiar la fecha en todos los links
   (`?v=20260913` → la fecha del día). Es lo que obliga al navegador de Lulú a bajar
   la versión nueva en vez de servir la guardada.
3. Commit y esperar el check verde en **Actions**.

El `index.html` además trae etiquetas `Cache-Control` en el `<head>`. Ayudan en algunos
navegadores, pero **no son confiables por sí solas** (no son estándar y Safari suele
ignorarlas). Lo que realmente funciona es el `?v=` del paso 2.

---

## 📁 Qué hay en el repo

### Unidad 1 — Biomoléculas y Célula (16 exámenes · 176 preguntas)

| Versión 1 (12 preg. c/u) | Versión 2 (10 preg. c/u) | Tema |
|---|---|---|
| `quiz-inorganicas.html` | `quiz-inorganicas-v2.html` | Biomoléculas inorgánicas |
| `quiz-proteinas.html` | `quiz-proteinas-v2.html` | Proteínas |
| `quiz-glucidos.html` | `quiz-glucidos-v2.html` | Glúcidos |
| `quiz-lipidos.html` | `quiz-lipidos-v2.html` | Lípidos |
| `quiz-acidos-nucleicos.html` | `quiz-acidos-nucleicos-v2.html` | Ácidos nucleicos |
| `quiz-componentes-celula.html` | `quiz-componentes-celula-v2.html` | Componentes comunes a todas las células |
| `quiz-procariotas.html` | `quiz-procariotas-v2.html` | Células procariotas |
| `quiz-eucariotas.html` | `quiz-eucariotas-v2.html` | Células eucariotas |

### Unidad 2 — Genética y División Celular (13 exámenes · 164 preguntas)

Un examen por cada dos capítulos del resumen.

| Versión 1 | Versión 2 | Caps. | Tema |
|---|---|---|---|
| `gen-e1.html` | `gen-e1-v2.html` | 1–2 | Niveles de organización y ADN |
| `gen-e2.html` | `gen-e2-v2.html` | 3–4 | Genes, genoma y bases nitrogenadas |
| `gen-e3.html` | `gen-e3-v2.html` | 5–6 | Transcripción, traducción y expresión génica |
| `gen-e4.html` | `gen-e4-v2.html` | 7–8 | Un gen una proteína · Genotipo y fenotipo |
| `gen-e5.html` | `gen-e5-v2.html` | 9–10 | Mitosis, meiosis y herencia mendeliana |
| `gen-e6.html` | `gen-e6-v2.html` | 11–12 | Cromosomas sexuales y trisomías |

12 preguntas cada uno. La V2 no repite ninguna pregunta de la V1: mismos temas,
otro ángulo (más preguntas de aplicación y de razonamiento).

**`gen-integrador.html`** — 20 preguntas de los 12 capítulos mezclados, tipo prueba real.

### Otros

- `index.html` — la portada, con dos solapas: 🔬 Biomoléculas y Células y 🧬 Genética.
  Cada solapa está organizada internamente por versiones.
- `Clave-respuestas-genetica.pdf` — las 164 respuestas correctas de los 13 exámenes de
  genética, con su explicación. Para tomar oral sin abrir los quizzes.

---

## ⚙️ Cómo funcionan los exámenes

Cada archivo es autónomo y trae:

- Una pregunta por pantalla, con 4 opciones.
- Corrección inmediata: marca la correcta en verde, la elegida en rojo si falló,
  y muestra la explicación del porqué.
- Barra de progreso y contador de aciertos.
- Pantalla final con el puntaje y la lista de repaso ✅/❌.
- **Modo repaso de errores**: si falló alguna, aparece un botón naranja que rehace
  solo las preguntas falladas, no las 12 de nuevo. Se puede encadenar: si en el repaso
  vuelve a errar algunas, el botón ofrece repasar solo esas.
- Botón para rehacer el examen completo.

Las respuestas correctas están repartidas en partes iguales entre A, B, C y D,
en orden mezclado. No hay patrón para adivinar.

---

Armado con 💜 por papá.
