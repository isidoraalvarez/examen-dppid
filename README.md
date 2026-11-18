# Portafolio — Isidora Álvarez

**Examen final · Dispositivos periféricos y plataformas para la interacción digital (DPPID) · Escuela de Diseño UDP · 2026**

En mi portafolio vas a ver las distintas etapas de mi carrera como diseñadora industrial. Empecé explorando el mobiliario y los objetos en madera, como la silla, la banca y el banquito zapatero, después me metí en la electrónica con sintetizadores como el Sin-Te y la Tostadora inestable, y en el último tiempo llegué a la web, creando experiencias interactivas como Multirealidades.sys (Dos realidades) y Contrapresión (Tocar la imagen).

Cada etapa me dejó algo distinto, y aquí las junto todas para mostrar cómo fui creciendo y lo que me mueve al diseñar: crear cosas que se tocan, se usan, se habitan y se sostienen.

---

## Dirección visual

El portafolio se construye como un **escritorio de autora**: una interfaz que mezcla el lenguaje de los sistemas operativos clásicos con el de los afiches y fanzines digitales.

- **Paleta de azules (inspirada en hortensias):** marino `#0E1B38`, azul rey `#164A96`, azul medio `#4A84C6`, azul claro `#84AEE2` y celeste `#B4CFF2`, sobre un fondo blanco azulado muy suave `#EEF3FB`. El azul rey es el protagonista: barra superior, barras de las ventanas, títulos, etiquetas, chips, cinta y pie de página. No hay tonos rosados.
- **Tipografías:** **Pixelify Sans** para los títulos y botones, **Instrument Serif** en cursiva para los acentos ("hola," y la palabra que rota), **DM Sans** para los textos y **DM Mono** para las etiquetas y metadatos.
- **Ventanas flotantes (`.win`):** cada bloque de información es una ventana con barra de título azul y nombre de archivo (`sobre-mi`, `herramientas — software`, `E03_sin-te`). Se pueden arrastrar con el mouse o el dedo.
- **Texturas:** retícula de líneas azul, grano de fotocopia y un **follaje en trama de puntos**: ramas y hojas generadas con código y convertidas en puntos, muy tenues, en el fondo de la portada, los trabajos y el pie. Es un toque sutil de árbol y naturaleza.
- **Avatar en pixel art:** en la portada aparece mi avatar dibujado píxel a píxel, con mis rasgos (pelo largo negro con partidura al medio, ojos oscuros) y mi outfit real (polera negra de malla ajustada, pantalones anchos oscuros y zapatos negros). Está animado por cuadros: respira, parpadea, mira hacia el lado del cursor, saluda, habla en un globo de diálogo y apunta a la ventana `trabajos`. Una versión mini acompaña el recorrido en la esquina de la pantalla.
- **Sticker de About Me:** un sticker sin marco, con borde blanco, pegado en la esquina de la ventana de herramientas. **Se puede arrastrar por la pantalla** y vuelve a su lugar con doble clic o al recargar. Muestra mi avatar sentado frente a un **monitor de escritorio** con teclado negro y mesa de madera, **escribiendo en bucle** mientras aparecen líneas de código en la pantalla. Esta animación existe solo en esa sección.
- **Cursor propio:** el puntero del sitio es un corazón azul pixelado.

**Estructura del sitio:** portada con titular dinámico ("hola, diseño para lo que se *toca / usa / habita / sostiene*") → índice de los 12 trabajos → detalle de cada proyecto en una ventana flotante → About Me al final, dentro de la ventana `sobre-mi` → contacto en el pie.

El sitio está hecho en **HTML, CSS y JavaScript sin frameworks**, organizado en tres archivos: `index.html`, `style.css` y `script.js`.

---

## 1. Conceptos técnicos

> [Revisa estas explicaciones y ajústalas con tus palabras: la rúbrica pide que estén redactadas por ti.]

### 1.1 Variables de CSS

**Qué es:** una variable de CSS guarda un valor (un color, una tipografía, una medida) con un nombre, para usarlo en muchas partes sin repetirlo.

**Para qué la usé:** para definir la paleta y las tipografías en un solo lugar. Si cambio un color en `:root`, cambia en todo el sitio.

```css
:root {
  --marino:  #0E1B38;
  --rey:     #164A96;   /* azul protagonista */
  --medio:   #4A84C6;
  --claro:   #84AEE2;
  --celeste: #B4CFF2;
  --papel:   #EEF3FB;

  --f-pixel: "Pixelify Sans", "DM Mono", monospace;
  --f-script: "Instrument Serif", Georgia, serif;
}
```

### 1.2 Pixel art con código: grilla y SVG

**Qué es:** un dibujo en pixel art es una grilla donde cada celda tiene un color. Con JavaScript se puede guardar esa grilla y convertirla en rectángulos SVG.

**Para qué lo usé:** para dibujar mi avatar de la portada y la miniatura de About Me. Pinto cada parte (pelo, cara, polera, mesa, monitor, teclado) en una grilla, y el código agrega solo el contorno oscuro alrededor de cada parte, como en el pixel art hecho a mano.

```js
function Lienzo(w, h) { this.w = w; this.h = h; this.c = new Array(w * h).fill(null); }
Lienzo.prototype.rect = function (x, y, w, h, col) {
  for (var j = 0; j < h; j++) for (var i = 0; i < w; i++) this.set(x + i, y + j, col);
};

var monitor = new Lienzo(72, 58);
monitor.rect(7, 10, 31, 22, "#2B3138");   // marco
monitor.rect(9, 12, 27, 18, "#161B21");   // pantalla
```

### 1.3 Animación por cuadros con `steps()`

**Qué es:** en CSS, `steps()` hace que una animación salte de un estado a otro sin transición suave, como los cuadros de un dibujo animado o de un videojuego.

**Para qué lo usé:** en la escena de About Me hay dos dibujos de los brazos (manos arriba y manos abajo) que se alternan cada 0,36 segundos, así se ve que estoy escribiendo. Las líneas de código de la pantalla aparecen una por una.

```css
.escena__brazos--a { animation: tecleoA .36s steps(1) infinite; }
.escena__brazos--b { animation: tecleoB .36s steps(1) infinite; }
@keyframes tecleoA { 0% { opacity: 1; } 50% { opacity: 0; } }
@keyframes tecleoB { 0% { opacity: 0; } 50% { opacity: 1; } }
```

### 1.4 Manipulación del DOM: titular dinámico

**Qué es:** el DOM es la estructura de la página que JavaScript puede leer y cambiar. Con `classList` se agregan o quitan clases de CSS, y `setTimeout` espera un tiempo antes de ejecutar algo.

**Para qué lo usé:** para que la última palabra del titular cambie sola cada 1,8 segundos, con un desenfoque al salir y al entrar.

```js
palabra.classList.add("sale");
setTimeout(function () {
  palabra.textContent = lista[i];
  palabra.classList.remove("sale");
  palabra.classList.add("entra");
  void palabra.offsetWidth;
  palabra.classList.remove("entra");
}, 380);
```

### 1.5 Pointer events: ventanas arrastrables

**Qué es:** los *pointer events* son eventos que funcionan igual con mouse, dedo y lápiz (`pointerdown`, `pointermove`, `pointerup`).

**Para qué lo usé:** para que las ventanas se puedan arrastrar desde su barra de título, en computador y en celular.

```js
barra.addEventListener("pointermove", function (e) {
  if (!activo) return;
  x = Math.min(limites.maxX, Math.max(limites.minX, e.clientX - inicioX));
  y = Math.max(limites.minY, e.clientY - inicioY);
  win.style.translate = x + "px " + y + "px";
});
```

### 1.6 Canvas: vista previa que se arma por píxeles

**Qué es:** `<canvas>` es un lienzo donde JavaScript dibuja píxel a píxel.

**Para qué lo usé:** al pasar el mouse por un trabajo del índice aparece su foto, primero en pocos píxeles grandes y después nítida. Dibujo la imagen muy chica y luego la amplío sin suavizado.

```js
var NIVELES = [6, 12, 24, 48, 96, 0];
ctx.imageSmoothingEnabled = n === 0;
tmp.width = cols; tmp.height = filas;
t.drawImage(img, 0, 0, cols, filas);
ctx.drawImage(tmp, 0, 0, W, H);
```

### 1.7 Rutas con `#hash`: detalle de cada proyecto

**Qué es:** el `#` de una URL (por ejemplo `#proyecto/sin-te`) se puede leer con JavaScript sin recargar la página.

**Para qué lo usé:** cada proyecto se abre en una ventana flotante según la dirección, así funcionan los botones atrás y adelante del navegador y se puede compartir el link directo a un proyecto.

```js
function segunDireccion() {
  var m = location.hash.match(/^#proyecto\/(.+)$/);
  var i = m ? buscar(decodeURIComponent(m[1])) : -1;
  if (i !== -1) abrir(i); else cerrar();
}
window.addEventListener("hashchange", segunDireccion);
```

### 1.8 Flexbox: acordeón de fotos de proceso

**Qué es:** con `flex` se reparte el espacio entre elementos. Si uno tiene más `flex` que los otros, ocupa más espacio.

**Para qué lo usé:** las fotos de proceso de cada proyecto están en franjas; la elegida se abre y se ve completa y a color, y las demás quedan angostas y en gris.

```css
.acordeon__panel { flex: 1 1 0; transition: flex .55s; }
.acordeon__panel.activo { flex: 7 1 0; }
.acordeon__panel.activo img { object-fit: contain; filter: none; }
```

### 1.9 [Otro concepto de mis proyectos: WebGL / Shaders / MediaPipe / MQTT]

**Qué es:** [explicación con tus palabras]

**Para qué lo usé:** [en qué proyecto: por ejemplo Gestos, Dos realidades o Tocar la imagen]

```js
[pega aquí un fragmento de ese proyecto]
```

---

## 2. Reflexión del semestre

### 2.1 Aprendizajes

[Escribe aquí tu reflexión personal. Algunas preguntas guía:]
- [¿Qué cambió en tu forma de diseñar al pasar del Figma al código?]
- [¿Qué aprendiste al documentar procesos de objetos físicos en un formato web?]
- [¿Qué te llevas del trabajo en equipo con Camila y Dayana?]

### 2.2 Desafíos y cómo los resolví

Los desafíos técnicos están en detalle en la [Bitácora · Problemas y soluciones](#4-problemas-y-soluciones). Los más importantes fueron:

- **Mostrar 12 proyectos sin saturar la pantalla:** pasé por estampillas en tres filas, después en una sola fila con scroll horizontal, y llegué a un índice limpio donde cada trabajo se ve al pasar el mouse y se abre en una ventana.
- **Mostrar las fotos sin cortarlas ni dejar franjas grises:** la imagen principal se adapta a su propia proporción, y las fotos de proceso se ven completas en el acordeón.
- **Que los cambios se vieran publicados:** aprendí cómo funciona la memoria (caché) del navegador y de GitHub Pages.
- [desafío propio]

### 2.3 Créditos

**Colaboradoras**

| Proyecto | Persona | GitHub |
|---|---|---|
| Gestos | Dayana | [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Dos realidades (Multirealidades.sys) | Dayana | [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Escuchar la imagen (Oír la luz) | Camila | [github.com/Estrabismx](https://github.com/Estrabismx) |
| Tocar la imagen (Contrapresión) | Dayana | [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Banquito zapatero modular | Dayana | [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Sintetizador modular Sin-Te | Camila y Dayana | [github.com/Estrabismx](https://github.com/Estrabismx) · [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Tostadora inestable | Camila y Dayana | [github.com/Estrabismx](https://github.com/Estrabismx) · [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Banca | Camila y Dayana | [github.com/Estrabismx](https://github.com/Estrabismx) · [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Ave | Camila y Dayana | [github.com/Estrabismx](https://github.com/Estrabismx) · [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Lámpara | Camila y Dayana | [github.com/Estrabismx](https://github.com/Estrabismx) · [github.com/dayanapanitrur](https://github.com/dayanapanitrur) |
| Silla | individual | — |
| Comedero | individual | — |

**Código y componentes**

El sitio está escrito en HTML, CSS y JavaScript sin frameworks ni librerías externas. Las librerías del curso están hechas para React, así que no instalé su código: hice versiones propias en JavaScript, inspiradas en ellas.

| Inspiración | Fuente | Qué hice en el portafolio |
|---|---|---|
| *Matrix Trail* · *Image Particles* (Aceternity UI) | [ui.aceternity.com](https://ui.aceternity.com) | Rastro de píxeles que sigue al cursor y vista previa del índice que se arma por píxeles. |
| Acordeón de imágenes (Skiper UI / Bencho) | [skiper-ui.com](https://skiper-ui.com) · [bencho.dev](https://bencho.dev) | Acordeón de fotos de proceso en el detalle de cada proyecto. |
| Ventanas y transiciones (Aceternity UI / Motion Primitives) | [ui.aceternity.com](https://ui.aceternity.com) · [motion-primitives.com](https://motion-primitives.com) | Ventanas flotantes arrastrables y el desenfoque de la palabra que rota. |

**Tipografías** (todas desde Google Fonts, licencia SIL Open Font License 1.1)

| Tipografía | Uso |
|---|---|
| [Pixelify Sans](https://fonts.google.com/specimen/Pixelify+Sans) | Títulos, botones, índice |
| [Instrument Serif](https://fonts.google.com/specimen/Instrument+Serif) | Acentos en cursiva |
| [DM Sans](https://fonts.google.com/specimen/DM+Sans) | Textos |
| [DM Mono](https://fonts.google.com/specimen/DM+Mono) | Etiquetas y metadatos |

**Imágenes**

| Imagen | Autoría | Licencia |
|---|---|---|
| Fotos de los proyectos (`imagenes/`) | [confirmar: fotos propias o de quién] | [licencia] |
| Capturas de los proyectos web (`multirealidades.png`, `wii.png`, `contrapresion.png`) | [confirmar] | [licencia] |
| Íconos y borde troquelado (`imagenes/ui/`) | Diseño propio, exportados desde mi archivo de Figma | [licencia] |
| Avatar pixel art y miniatura de About Me | Dibujo propio hecho con código, basado en mis fotos (las fotos no se publican) y en imágenes de referencia de pixel art | [licencia] |
| Cursor de corazón pixelado (`imagenes/ui/cursor-corazon.png`) | Adaptado de una imagen de referencia: [autor / fuente] | [licencia] |
| Composición de la escena (monitor, teclado y mesa) | Redibujada a partir de una ilustración de referencia: [autor / fuente] | [licencia] |
| Follaje en trama de puntos | Generado con código, sin imágenes externas | — |
| Fondo de cuadritos de la sección trabajos (`imagenes/ui/fondo-trabajos.jpg`) | [autor / fuente] | [licencia] |

**Sonidos:** este portafolio no usa sonidos.

### 2.4 Uso de IA durante el semestre

El resumen está aquí y el detalle con los prompts en la [Bitácora · Uso de IA](#3-uso-de-ia). Usé IA en dos etapas:

- **Diseño:** para ordenar ideas a partir de mis referentes, elegir una paleta y construir el componente de estampilla en Figma.
- **Programación:** con **Claude** (Claude Code) para escribir y ajustar el HTML, CSS y JavaScript del sitio a partir de mi Figma y de mis instrucciones.

Las decisiones de diseño fueron mías: qué proyectos mostrar, los referentes, la paleta, la estética, qué se quedaba y qué se descartaba, y cada corrección pedida después de revisar el resultado.

---

## Bitácora de proceso

### 1. Links principales

| | Link |
|---|---|
| Figma (acceso de lectura) | [figma.com/design/ADbrbFWVOeJkBakvKcFPj6/Portafolio-Isidora-Alvarez](https://www.figma.com/design/ADbrbFWVOeJkBakvKcFPj6/Portafolio-Isidora-Alvarez) — [confirmar que esté compartido como "cualquiera con el link puede ver"] |
| Sitio en GitHub Pages | [isidoraalvarez.github.io/portafolio](https://isidoraalvarez.github.io/portafolio/) — [confirmar que esté publicada la versión final] |
| Repositorio | [link del repositorio] |

### 2. Registro por avances

#### Avance 1

- **Qué presenté:** [describe qué mostraste: Figma, estampillas, primera versión web…]
- **Comentarios recibidos:**
  - Mover la sección "Sobre mí" al final de la página.
  - Asegurar que el diseño se mantuviera al exportar la página como PDF.
- **Cambios realizados:**
  - Moví "Sobre mí" al final. Ahora el recorrido parte con la portada, sigue con los trabajos y cierra con "Sobre mí" y el contacto, así los proyectos tienen el protagonismo.
  - **No apliqué** la sugerencia del PDF. La rúbrica pide un desarrollo interactivo y funcional en GitHub Pages, y un PDF no puede mostrar ventanas que se arrastran, animaciones ni transiciones. Preferí dedicar el tiempo a que la experiencia web funcione bien en desktop y en mobile.

#### Avance 2

- **Qué presenté:** [describe qué mostraste]
- **Comentarios recibidos:** [confirmar si estas correcciones de la profesora fueron en el Avance 2]
  - Agregar créditos de las personas con las que hice cada trabajo, con link a su GitHub.
  - Ajustar las imágenes para que no se perdiera el objeto central.
- **Cambios realizados:**
  - Agregué en el detalle de cada proyecto el apartado **"créditos — trabajo en colaboración"**, con el nombre y GitHub de Camila y Dayana. En los proyectos individuales (Silla y Comedero) no aparece.
  - Reorganicé las imágenes: la foto principal se muestra completa en su proporción y las fotos de proceso se ven completas en el acordeón.

#### Después del Avance 2 (hacia el examen)

- Unifiqué todo el código en tres archivos (`index.html`, `style.css`, `script.js`), sin subcarpetas de código.
- Incorporé los 12 proyectos y una vista de detalle para cada uno, con descripción, links, video, fotos de proceso y créditos.
- Cambié la presentación de los trabajos: de estampillas a un **índice** con vista previa por píxeles.
- Rediseñé la estética a partir de mis nuevos referentes (afiches pixel, fanzines, paletas invernales).
- Diseñé y animé mi **avatar** para la portada, primero como caricatura 2D y después en **pixel art**.
- Agregué en About Me la escena de mi avatar **escribiendo en un laptop isométrico** y un **cursor de corazón pixelado** para todo el sitio.
- Reemplacé la ventana de contacto de "Sobre mí" por **herramientas**, con el software que uso: Illustrator, AutoCAD, Rhino, Inventor, KiCad, HTML, CSS, JavaScript, VS Code y GitHub. El contacto quedó en el pie de página.
- **Ajuste final de estética:**
  - Quité el sufijo `.exe` de todas las ventanas.
  - Cambié la paleta: primero un azul con grises de complemento, y al final una paleta solo de azules (de marino a celeste), con el azul rey como protagonista. Eliminé el rosado.
  - Subí el titular de la portada para que no quede tan abajo.
  - Cambié la escena del laptop por una **miniatura** con un monitor de escritorio, debajo del recuadro de mi foto de perfil, que sigue vacío hasta que ponga mi imagen.
  - Agregué un follaje tenue en trama de puntos como toque de naturaleza.
  - Probé una versión sin letra pixelada y sin avatar en la portada, pero la descarté porque perdía la identidad que buscaba. Mantuve Pixelify Sans, el avatar y la ubicación de las herramientas.

### 3. Uso de IA

**Herramientas:**

| Etapa | Prompt (resumen de lo que pedí) | Qué me entregó | Qué ajusté o decidí yo |
|---|---|---|---|
| Ideas y paleta | [prompt] | Ideas a partir de mis referentes y una paleta basada en mis imágenes de Pinterest | Elegí la paleta A porque me gusta el azul. Descarté el llavero colgante de la portada porque se parecía demasiado al de Cindy Ly. Pedí agregar elementos de *junk journaling*. |
| Estampilla en Figma | "Ayúdame a crear una estampilla en Figma para este proyecto, con borde perforado, inclinada como en Bill Guo, con estado hover y versión desktop y mobile." | Componente con variantes desktop/mobile y estados Default, Hover y Pressed, borde perforado y propiedades editables | Le di una inclinación distinta a cada estampilla. |
| Primera versión web | Escribir el CSS y JavaScript del portafolio según mi Figma (ventanas flotantes, titular dinámico, fila de estampillas) | El HTML, CSS y JS del sitio | Pedí agregar la sección "proceso — bocetos y croquis", que faltaba. |
| Organización del código | Dejar todo en tres archivos y sin subcarpetas | Proyecto unificado en `index.html`, `style.css` y `script.js` | Elegí el nombre `script.js`. |
| 12 proyectos | Incluir los 12 trabajos oficiales con su subpágina | Fichas y vista de detalle de cada proyecto | Definí qué fotos van en cada proyecto y cuál es la principal. |
| Correcciones de la profesora | Agregar créditos y ajustar el encuadre de las imágenes | Apartado de créditos y nuevo ajuste de imágenes | Indiqué con quién hice cada proyecto. Pedí que las fotos no se cortaran ni tuvieran franjas grises. |
| Rediseño | Cambiar a una estética de escritorio Y2K y luego a una de autora basada en mis nuevos referentes | Nuevas versiones de la interfaz | Pedí más impacto en el titular, quité la frase del pie que no me gustaba, el recuadro de la palabra que rota y el texto bajo el personaje. Pedí alejarme de la estética anterior. |
| Avatar (primera versión) | Personaje animado estilo caricatura 2D basado en mis fotos | Personaje en SVG con brazos articulados y animaciones | Pedí que interactuara con la interfaz (agarrar ventanas, apuntar a los trabajos). Después lo cambié a pixel art. |
| Avatar pixel art y escena de escritura | Ver el prompt completo más abajo | Avatar pixel art animado por cuadros, escena del laptop con animación de escritura, cursor de corazón | Elegí las referencias (mis fotos, el laptop isométrico, el corazón y los personajes pixel art) y decidí que la animación de escritura fuera solo en About Me. |
| Ajuste final de estética | Quitar `.exe`, eliminar el rosado de la paleta, reubicar el titular, rehacer la escena de About Me con el computador de la referencia y agregar un toque sutil de naturaleza | Una primera versión cambió también la tipografía, sacó el avatar y movió las herramientas | Rechacé esa versión porque cambiaba cosas que no pedí. Pedí volver atrás, que el azul fuera el protagonista, que la escena fuera una miniatura bajo mi foto y que la naturaleza fuera solo una textura de fondo. |
| Bitácora y README | Redactar la bitácora y este README | Estructura y redacción base | [revisa y reescribe con tus palabras lo que corresponda] |

#### IA para el avatar pixel art y la animación de escritura

Usé asistencia de IA (Claude, en Claude Code) para programar mi avatar en pixel art y lograr que se moviera, en especial la animación de escritura en el laptop de la sección About Me. Le entregué como referencia dos fotos mías (para el outfit y para la cara y el pelo), una imagen de un corazón azul pixelado, una ilustración de un laptop gris en perspectiva isométrica y dos ejemplos de personajes en pixel art.

**Prompt utilizado:**

> Necesito que actualices el código de mi portafolio aplicando exactamente las siguientes modificaciones de diseño e interactividad:
>
> 1. **Cursor personalizado:** configura el cursor del sitio web utilizando la imagen del corazón azul pixelado provista en los recursos (`cursor: url('...'), auto;`).
> 2. **Personaje pixel art personalizado (avatar):** el personaje principal de la web debe ser un avatar en estilo pixel art que me represente fielmente con mis rasgos físicos (cabello largo negro, ojos, expresión) y mi ropa real (polera negra/malla y pantalones anchos o jeans oscuros, basándose en las referencias visuales).
> 3. **Sección About Me con animación de escritura (tipeo):** en la sección About Me, incorpora a mi personaje pixel art trabajando frente a un computador. El modelo de laptop debe ser exactamente el diseño de la imagen de referencia (portátil gris claro pixel art en perspectiva isométrica). El personaje debe estar animado, realizando el gesto continuo de escribir en el teclado (movimiento de manos/brazos en bucle). Esta animación del personaje escribiendo debe aparecer exclusivamente en la sección About Me.

**Qué me entregó:**
- Un pequeño motor en JavaScript para dibujar pixel art en una grilla y convertirlo a SVG, con contorno automático.
- Mi avatar de pie (36 × 76 píxeles), con cuadros para respirar, parpadear, mirar hacia el cursor, saludar, hablar y apuntar.
- La escena del laptop isométrico en un escritorio de madera, con mis brazos alternando sobre el teclado y líneas de código que aparecen en la pantalla.
- *Actualización:* en el ajuste final cambié el laptop por el monitor de escritorio de una nueva imagen de referencia y convertí la escena en una miniatura debajo de mi foto de perfil.
- El cursor de corazón, convertido a una imagen de 32 × 32 px con fondo transparente.

**Qué ajusté o decidí yo:**

**Reflexión sobre el uso de IA:** 

### 4. Problemas y soluciones

| Problema | Causa | Solución |
|---|---|---|
| El link de GitHub Pages mostraba una página en blanco con el README | Pages publicó primero el repositorio solo con README, antes de subir `index.html` | Subí `index.html` a la raíz y esperé el ✔ verde de Pages |
| Después de subir cambios seguía viendo la versión antigua | El navegador guarda los archivos por 10 minutos (caché) | Agregué un número de versión a los archivos (`style.css?v=7`, `script.js?v=7`) y probé en ventana privada |
| Las imágenes salían cortadas o con franjas grises | La imagen principal se estiraba más que su caja y el `object-fit` recortaba las fotos verticales | La imagen principal ahora usa su propia proporción con un alto máximo, y las fotos de proceso se ven completas |
| La imagen grande desapareció de todos los proyectos | Una regla ocultaba la portada si también estaba en la lista de proceso | La portada siempre se muestra en grande, y se salta en la lista de proceso para no repetirla |
| No se veía el borde perforado de las estampillas | El navegador tenía guardada una versión fallida del SVG | Agregué número de versión también a la URL del SVG |
| VS Code mostraba "1 problem" en `style.css` | `-webkit-line-clamp` sin su propiedad estándar | Agregué `line-clamp: 2;` |
| Las estampillas en tres filas no me convencían | Demasiada información a la vez | Las pasé a una sola fila con scroll horizontal y después a un índice |
| El código estaba repartido en subcarpetas | Estructura inicial con carpetas `css/` y `js/` | Unifiqué todo en tres archivos en la raíz |
| La vista previa del índice quedaba pegada al hacer scroll | No se ocultaba si el mouse no salía de la lista | La vista previa se oculta al hacer scroll o al abrir un proyecto |

### 5. Aprendizajes del semestre

[Reflexión de cierre personal sobre el proceso de diseño y prototipado. Por ejemplo: cómo se relaciona prototipar un objeto físico con prototipar una interfaz, qué significó documentar el proceso, qué harías distinto.]

### 6. Recursos y referentes visuales

#### Imágenes de proceso

Registro de la creación de las piezas (las mismas fotos aparecen en el acordeón de proceso de cada proyecto):

| Proyecto | Proceso |
|---|---|
| Sintetizador modular Sin-Te | ![](imagenes/sin_te.jpeg) ![](imagenes/sintes.jpeg) ![](imagenes/sinte.jpeg) |
| Banquito zapatero modular | ![](imagenes/banco_zapatero.jpeg) ![](imagenes/banco_zapatero2.jpeg) |
| Banca | ![](imagenes/banca2.jpeg) ![](imagenes/plano_banca.jpeg) |
| Ave | ![](imagenes/ave2.jpeg) ![](imagenes/ave3.jpeg) ![](imagenes/ave4.jpeg) |
| Comedero | ![](imagenes/comedero4.jpeg) ![](imagenes/comedero2.jpeg) |
| Lámpara | ![](imagenes/lampara2.jpeg) ![](imagenes/lampara3.jpeg) ![](imagenes/lampara4.jpeg) |
| Gestos, Dos realidades, Escuchar la imagen, Tocar la imagen, Tostadora inestable, Silla | [por agregar fotos de proceso] |

#### Referentes de diseño

| Referente | Link | Qué tomé |
|---|---|---|
| Danilo De Marco | [link] | Composición editorial y minimalismo de autor [ajustar] |
| Niccolò Miranda | [link] | [qué tomaste] |
| Ollivere | [link] | Concepto de periódico: cabecera, etiquetas y jerarquía de títulos [ajustar] |
| Thibaut Crépelle | [link] | [qué tomaste] |
| 2xA Studio | [link] | Mostrar el proceso de cada pieza, no solo el resultado |
| bleibtgleich | [link] | [qué tomaste] |
| Bulbs · Simon Dupety | [link] | Inmersión y dinamismo: movimiento constante y personaje interactivo [ajustar] |
| Bill Guo | [billguo.me](https://billguo.me) | Proyectos como colección, jerarquía tipográfica (primera etapa) |
| Cindy Ly | [cindyly.design](https://www.cindyly.design/) | Navegación lúdica tipo escritorio y elementos arrastrables (primera etapa) |
| Feather Computer | [feather.computer](https://feather.computer/) | Contenido ordenado como archivos en un escritorio (primera etapa) |
| Imágenes de inspiración | [autores] | Afiches pixel en damero, fanzines con grano y retícula, contraste entre letra pixel y script, paletas invernales |

#### Librerías de componentes y recursos web

| Recurso | Link | Uso en el portafolio |
|---|---|---|
| Aceternity UI | [ui.aceternity.com](https://ui.aceternity.com) | Inspiración: rastro de píxeles, vista previa por píxeles, ventanas |
| Bencho | [bencho.dev](https://bencho.dev) | Inspiración: acordeón de fotos de proceso |
| Skiper UI | [skiper-ui.com](https://skiper-ui.com) | Inspiración: acordeón de fotos de proceso |
| Motion Primitives | [motion-primitives.com](https://motion-primitives.com) | Inspiración: desenfoque del titular y transiciones |
| Shaders | [shaders.com](https://shaders.com) | [no usado en esta versión / indicar uso] |
| 21st.dev | [21st.dev/community/components](https://21st.dev/community/components) | Consulta |
| save.design | [save.design/explore](https://save.design/explore) | Consulta de referentes |
| Designeer | [designeer.xyz](https://designeer.xyz) | Consulta de referentes |
| mesh3d | [mesh3d.gallery](https://mesh3d.gallery) | Consulta de referentes |
| Google Fonts | [fonts.google.com](https://fonts.google.com) | Tipografías |

---

