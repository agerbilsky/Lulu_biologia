# 🧬 Quizzes de Lulú — Biología 3.º A

Plataforma de exámenes de práctica para estudiar desde el celular.

**Link del sitio:** https://agerbilsky.github.io/Lulu_biologia/

**31 exámenes · 380 preguntas · 2 unidades**

Todos los archivos son HTML autónomos: no cargan fuentes, scripts ni imágenes de afuera.
Por eso abren bien incluso desde el navegador interno de WhatsApp en el iPhone.

---

## 😤 Si el sitio muestra una versión vieja

Es caché del navegador, no un problema del repo. Por orden:

1. Normalmente se arregla solo: el índice detecta que hay versión nueva y se recarga.
   Si no, abrir el link con un parámetro al final, **cambiando el número cada vez**:
   `https://agerbilsky.github.io/Lulu_biologia/?v=8`
2. Si así se ve bien, limpiar el caché de verdad:
   **Ajustes → Safari → Borrar historial y datos de sitios web**
3. Si sigue igual, revisar el deploy: pestaña **Actions** del repo. El último
   *pages build and deployment* tiene que tener el check verde.

GitHub Pages tarda entre 30 segundos y 2 minutos en publicar después de cada commit,
y su CDN cachea unos 10 minutos. Mirar enseguida de subir algo siempre muestra lo anterior.

---

## 🔄 Cómo actualizar un examen

1. Editar o reemplazar el `.html` que corresponda.
2. Cambiar la versión en **dos lugares**, siempre al mismo valor:
   - `version.json` → el campo `"v"`
   - `index.html` → la constante `var MIA` (al final, en el script de auto-versión)
     y la fecha de los links `?v=...`
3. Commit y esperar el check verde en **Actions**.

El botón "Volver al inicio" de cada examen **no hay que tocarlo**: se versiona solo
con la fecha del día, por JavaScript.

### Cómo funciona el auto-chequeo de versión

Al abrir el índice, un script consulta `version.json` pidiéndolo sin caché. Si la versión
publicada no coincide con la que trae la copia guardada, el índice se recarga solo
apuntando a una URL nueva, y eso fuerza una descarga fresca.

Por eso el paso 2 es obligatorio: si `version.json` no cambia, el auto-chequeo no se entera
de que hay algo nuevo.
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

### Unidad 2 — Genética y División Celular (15 exámenes · 204 preguntas)

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

**Integradores** — 20 preguntas cada uno, los 12 capítulos mezclados, tipo prueba real.
Los tres cubren los mismos temas pero no comparten ni una sola pregunta entre sí.

| Archivo | |
|---|---|
| `gen-integrador.html` | Integrador 1 |
| `gen-integrador-v2.html` | Integrador 2 |
| `gen-integrador-v3.html` | Integrador 3 |

### Otros

- `version.json` — dice cuál es la versión publicada. Lo lee el índice para saber
  si la copia guardada del navegador quedó vieja.
- `index.html` — la portada, con dos solapas: 🔬 Biomoléculas y Células y 🧬 Genética.
  Cada solapa está organizada internamente por versiones.
- `Clave-respuestas-genetica.pdf` — las 204 respuestas de los 15 exámenes de genética
  (23 páginas). El práctico para la prueba de genética.
- `Clave-respuestas-completa.pdf` — las 380 respuestas de los 31 exámenes, las dos
  unidades (46 páginas). El de referencia.

Los dos traen, para cada pregunta, la respuesta correcta con su letra (A/B/C/D, la misma
que se ve en pantalla) y la explicación. Sirven para tomar oral sin abrir los quizzes.

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
- **Guarda la nota**: al terminar, queda registrado el mejor puntaje de cada examen y
  el índice lo muestra como una chapa de color en cada tarjeta (verde 80%+, amarillo
  60%+, rojo abajo de eso), más un resumen arriba con cuántos hizo y el promedio.
  El repaso de errores no pisa la nota, porque tiene menos preguntas.

### ⚠️ Sobre las notas guardadas

Se guardan **en el navegador de cada dispositivo**, no en la nube. Consecuencias:

- Las notas de Lulú se ven en el teléfono de Lulú, no en el de papá.
- Si borra los datos de Safari (el mismo truco que se usa para el caché), se borran.
- El navegador interno de WhatsApp puede no guardarlas. Conviene abrir el link en Safari.
- Si el navegador bloquea el guardado, el examen funciona igual: simplemente no anota.

Hay un botón **Borrar mi progreso** en el índice para empezar de cero.

Las respuestas correctas están repartidas en partes iguales entre A, B, C y D,
en orden mezclado. No hay patrón para adivinar.

---

Armado con 💜 por papá.
