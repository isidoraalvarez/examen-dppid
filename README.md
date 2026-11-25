# Portafolio — Isidora Álvarez

## 1. Links

| | Link |
|---|---|
| Figma | [Portafolio-Isidora-Alvarez](https://www.figma.com/design/ADbrbFWVOeJkBakvKcFPj6/Portafolio-Isidora-Alvarez) |
| Sitio en GitHub Pages | [isidoraalvarez.github.io/examen-dppid](https://isidoraalvarez.github.io/examen-dppid/) |
| Repositorio | [github.com/isidoraalvarez/examen-dppid](https://github.com/isidoraalvarez/examen-dppid) |

---

## Portafolio

En mi portafolio verás los trabajos que he hecho durante la carrera de Diseño Industrial y, a través de ellos, cuento cómo he ido creciendo como diseñadora.

Siempre me ha gustado fabricar cosas con las manos. En mi primer año de carrera empecé trabajando en lo conceptual, como llevar a cabo ideas y mezclar conceptos. Poco a poco empecé a meterme en el trabajo manual; ya en mi segundo año empecé fuerte con el trabajo en madera, armando sillas, bancas y objetos que se pueden tocar y usar, como la Chair Ele, la Banca estructural, el Banquito zapatero y Mimus Thenca, una tenca chilena que mueve las alas al jalar de su tirador. En mi tercer año me encontré con la electrónica y descubrí lo entretenido que es hacer sonar algo que una misma construyó, como el Sin-te o la Tostadora inestable. Y en estos últimos meses llegué a la web, donde aprendí que lo digital también se puede sentir, con proyectos como Multirealidades y Contrapresión.

Cada trabajo me enseñó algo y me llevó al siguiente. Este portafolio es mi forma de mostrar ese camino, lo que me gusta y lo que me mueve a diseñar, que al final es crear cosas que se usan y se habitan.

---

| Página | Contenido |
|---|---|
| `index.html` | Portada con el titular dinámico, mi avatar y una foto mía de fondo. Desde ahí se entra a los trabajos, una lista de los 12 proyectos (Sin-te, Tostadora inestable, Multirealidades, Traductor de bits, Contrapresión, Diseño Abierto, Banquito zapatero, Chair Ele, Banca estructural, Mimus Thenca, Comedero para Mascotas y Lámpara) con filtros y la ficha de cada uno, y al contacto |
| `sobre-mi.html` | Sobre mí, herramientas, trayectoria y contacto |

La página está hecha con HTML, CSS y JavaScript normales, sin usar React. Las dos páginas comparten el diseño (`style.css`) y las animaciones (`script.js`). Para el efecto pixelado del fondo de la portada usé un shader de Shaders.com, y las letras las traje desde Google Fonts. Las fotos están en la carpeta [imagenes](imagenes/) y los videos en [videos portafolio](videos%20portafolio/).

### **Tipografías.** El sitio usa cuatro tipografías, todas de Google Fonts con licencia SIL Open Font License 1.1.

| Tipografía | Dónde la uso |
|---|---|
| [Dancing Script](https://fonts.google.com/specimen/Dancing+Script) (700) | Títulos grandes en cursiva pixelada ("hola, diseño para lo que se *usa / habita*", "trabajos", el nombre de cada proyecto, "sobre mí y contacto" y "contacto"). La convierto en píxeles cuadrados con código, y el texto real queda en la página para los lectores de pantalla |
| [Pixelify Sans](https://fonts.google.com/specimen/Pixelify+Sans) | Logo, botones, número de cada trabajo en el índice, herramientas de software y enlaces del contacto |
| [DM Mono](https://fonts.google.com/specimen/DM+Mono) | Menú, reloj, etiquetas y categorías. Dentro de cada proyecto es la única tipografía (ficha, descripción, créditos y botones) |
| [DM Sans](https://fonts.google.com/specimen/DM+Sans) | Textos de lectura, como la presentación de la portada, la bio y la trayectoria |
| <img width="537" height="760" alt="image" src="https://github.com/user-attachments/assets/bc996875-3d3f-4ee0-898a-648fa1536eeb" /> |

Para la cursiva pixelada comparé varias cursivas convertidas en píxeles y me quedé con Dancing Script, porque es la que mejor se lee al pixelarla.

### **Paleta.** Fondo blanco con tonos de azul, celeste y beige, a partir de una paleta de referencia que me gustó. Le da más blanco y aire a la página.

| Color | Hex | Variable en `style.css` | Dónde lo uso |
|---|---|---|---|
| **Azul petróleo** | `#567C8D` | `--pixel` y `--acero` | Títulos en cursiva pixelada, etiquetas, trama de las fotos y el árbol pixelado |
| Azul marino | `#2F4156` | `--oxford` | Textos y botón principal |
| Celeste | `#C8D9E6` | `--escarcha`, `--celeste` y `--lavanda` | Manchas del fondo, líneas y hover del índice |
| Beige | `#F5EFEB` | `--luna` | Paneles y pie de página |
| Blanco | `#FFFFFF` | `--papel` | Fondo de la página |
| <img width="1007" height="80" alt="image" src="https://github.com/user-attachments/assets/fbd164ea-adf8-4ed3-a5fd-512df1b7dc7a" /> |

---

## Cómo se ve

| Foto 1 | Foto 2 |
|---|---|
| <img width="823" height="723" alt="image" src="https://github.com/user-attachments/assets/63f069b3-47ec-4840-8a6b-c2e124f2c3b6" /> | <img width="370" height="662" alt="image" src="https://github.com/user-attachments/assets/45c1100c-fec8-4b39-a272-f69d5c533b49" /> |
| Foto 3 | Foto 4 |
| <img width="1890" height="866" alt="image" src="https://github.com/user-attachments/assets/c07b150d-62a6-44c3-a28a-b3f997cf8f27" /> | <img width="1903" height="868" alt="image" src="https://github.com/user-attachments/assets/78881c81-9fc0-48c6-9e1e-2ef4515f5a65" /> |
| Foto 5 | Foto 6 |
| <img width="1903" height="866" alt="image" src="https://github.com/user-attachments/assets/0b0af37f-a1f3-4b36-a94d-01f924b5787a" /> | <img width="1880" height="858" alt="image" src="https://github.com/user-attachments/assets/48f97778-eaef-4c50-b6ab-1d405041aac6" /> |

---

## 2. Diseño y evolución del proyecto

### Concepto

El portafolio mezcla el **pixel art** con dos fotos mías que uso de fondo, una playa en la portada y el corte de un tronco en trabajos. A las dos les apliqué un filtro con los colores de mi paleta y una opacidad baja. Encima van los títulos en cursiva pixelada y mi avatar en pixel art. Lo que une todo es la grilla de píxeles y una paleta suave de tonos azules, celeste y beige sobre fondo blanco, con mucho aire para que los trabajos sean los protagonistas.

El sitio tiene dos páginas. `index.html` tiene la portada y los trabajos, y se recorre como si fueran páginas separadas, y `sobre-mi.html` es la página de Sobre mí. Al entrar lo primero que se ve es la portada, con el título dinámico "hola, diseño para lo que se *usa / habita*", mi avatar y la foto pixelada de la playa de fondo. Desde ahí, el botón "ver trabajos" o el menú llevan a los **trabajos**, una lista de los 12 proyectos ordenados por categoría (electrónica, web y diseño de objetos) y por año. Al pasar el cursor por el nombre de un trabajo aparece la foto del proyecto, y al hacer clic se abre su ficha con su descripción, y con imágenes y videos que muestran su proceso. El botón "sobre mí" lleva a su propia página, con mi presentación, mi foto, herramientas y trayectoria. El contacto está siempre al final de cada vista.

En la portada tengo la frase "diseño para lo que se usa" o "diseño para lo que se habita". Elegí esas dos palabras porque así es como yo pienso que es la mejor forma de describir lo que hago:
- ***usa*.** El diseño como algo funcional, pensado para el uso diario, tanto en los objetos (el Comedero para Mascotas, el Banquito zapatero) como en las interfaces web.
- ***habita*.** Los objetos y espacios donde se vive, como el mobiliario (la Chair Ele, la Banca estructural), y también las experiencias digitales donde uno entra y se queda.

### Versiones que tuve

Antes de llegar al diseño actual pasé por distintas versiones del portafolio que me sirvieron para probar ideas, descartar lo que no me representaba y ajustar cómo mostrar mis trabajos:

| Versión | Cómo era | Qué cambié después | Registro |
|---|---|---|---|
| **Versión 1** | Estética de estampillas en 3 columnas con paleta de colores grises y azules. La página era solo una y todo se veía de corrido, alargándose mucho. | Moví "Sobre mí" hacia el final para dar prioridad a los proyectos. Descarté exportar como PDF porque el encargo pide un sitio interactivo en GitHub Pages. Pasé a una versión 2 Y2K con ventanas flotantes, dock y estampillas en una fila con scroll horizontal. | <img width="530" height="632" alt="image" src="https://github.com/user-attachments/assets/27fd91c6-9a0b-4086-97a9-eb2772a9d48b" /> <img width="327" height="461" alt="image" src="https://github.com/user-attachments/assets/40b46df2-7a01-42b2-aa62-6c3c729d76d2" /> |
| **Versión 2 y 3** | Estética de estampillas con más azules y el gris en segundo plano, en una sola columna con carrusel horizontal y estilo Y2K. Ninguna lograba que sintiera mi esencia en ella. | Adapté cada foto a su propia proporción sin franjas grises ni recortes, agregué los créditos de colaboradores y autores originales, y cambié hacia una estética propia con pixel art, cursiva pixelada, mi avatar y fondos con fotos propias. | <img width="1135" height="682" alt="image" src="https://github.com/user-attachments/assets/a7f98316-7e55-4c6e-965f-22995c56146a" /> <img width="1137" height="678" alt="image" src="https://github.com/user-attachments/assets/b6af84a9-bfc1-4744-9f0d-56631c13e1c4" /> |
| **Versión actual** | Estética editorial con pixel art, cursiva pixelada, avatar animado, fondos con fotos propias (playa pixelada con Shaders.com y tronco), índice limpio desplegable con filtros y Figma ordenado en cinco páginas (Boceto, Wireframes, UI Kit, Desktop y Mobile). | Logra que la página se sienta mía, ordena los 12 proyectos sin saturar y funciona tanto en desktop como en mobile. | <img width="823" height="723" alt="image" src="https://github.com/user-attachments/assets/63f069b3-47ec-4840-8a6b-c2e124f2c3b6" /> |

### Decisiones de diseño

| Decisión | Por qué |
|---|---|
| **Portada primero y secciones que se abren con botones** | Al entrar solo se ve la portada, trabajos aparece al apretar su botón y Sobre mí tiene su propia página (`sobre-mi.html`). Así la página no se siente tan sobrecargada y se entiende que hay que entrar a cada sección. |
| **Fotos propias de fondo, con filtro de la paleta y suaves** | La playa (pixelada con Shaders.com y respaldo en CSS) en la portada y el tronco en "trabajos" acompañan sin opacar el texto. Además hacen que la página se sienta más mía, porque son momentos bonitos de mi vida. |
| **Títulos en cursiva pixelada** | Inspirada en la estética de píxeles, que va con mis gustos. Es una letra cursiva hecha con píxeles, igual que el resto del sitio. <img width="707" height="190" alt="image" src="https://github.com/user-attachments/assets/20c35c0b-a778-4517-ad87-3c3fcd78c7db" /> |
| **Portada simple y titular compacto** | Solo el titular ("hola, diseño para lo que se *usa / habita*" con líneas juntas para leerse como un solo bloque), una descripción corta, los botones y yo como avatar, para que se entienda rápido de qué se trata el portafolio. |
| **Menú a la izquierda, con botones grandes** | Los trabajos, sobre mí y contacto van junto al logo, como botones con borde para que se note que hay que entrar a cada sección. En el celular quedan visibles en una segunda fila. |
| **Lista de trabajos que se abre con la foto** | Cada trabajo aparece como una franja con bordes redondeados y su nombre y, al pasar el cursor, se abre y muestra su foto. Así la lista se mantiene limpia aunque sean 12 proyectos. |
| **Filtros y orden por categoría y año** | Filtros (todo, electrónica, web y diseño de objetos) y proyectos ordenados dentro de cada categoría del más reciente al más antiguo. |
| **Cada proyecto se abre en un panel sobre el índice** | Permite volver al índice sin perder el lugar. |
| **Tonos de azul sobre blanco** | Elegí una paleta suave de azules, celeste y beige sobre fondo blanco, para que la página no se sienta tan cargada y los trabajos se lean bien. <img width="927" height="152" alt="image" src="https://github.com/user-attachments/assets/2450ab81-8100-40bd-a618-3bea0f8335c8" /> |
| **Avatar en pixel art** en la portada | Me presenta de forma propia y cercana, con mis rasgos y mi ropa, sin usar una foto. |
| **Fotos de proceso completas y detalle de naturaleza** | La foto abierta toma su propia proporción sin recortarse, y detrás de trabajos y el pie de página agregué un árbol pixelado muy suave de fondo. |
| **Proceso de cada proyecto y diseño responsive** | Al abrir un trabajo aparecen directo las fotos de proceso, las casillas de ficha, links, descripción, créditos y video(s). Todo se adapta al celular sin scroll lateral. |

---

## 3. Código, HTML, CSS, JavaScript y MQTT

La página está hecha con HTML, CSS y JavaScript, en cuatro archivos. `index.html` tiene la portada y los trabajos, `sobre-mi.html` la página Sobre mí, `style.css` el diseño y `script.js` las animaciones y lo que pasa al hacer clic. Las fotos están en la carpeta `imagenes` y los videos en `videos portafolio`.

### HTML: estructura

**Qué es.** Nos ayuda a definir qué elementos existen, como los títulos, imágenes, botones.

**Cómo lo usé.** Cada sección de `index.html` es un `<section>` con su `id` (`#inicio`, `#trabajos`), y Sobre mí está en su propia página, `sobre-mi.html`, enlazada desde el menú. La lista de trabajos queda vacía en el HTML y JavaScript la llena con los 12 proyectos.

```html
<section class="seccion trabajos" id="trabajos">
  <h2 class="titulo-xl" data-puntos>trabajos</h2>
  <div class="filtros" data-filtros>…</div>
  <ol class="indice" id="indice" aria-label="Trabajos"></ol>
</section>
```

### CSS, el diseño

**Qué es.** CSS es el lenguaje en el que se le define la apariencia visual, como lo es la tipografía,color, espaciado.

**Cómo lo usé.** Guardé la paleta y las tipografías en **variables** dentro de `:root`, así si cambio un color se actualiza en todo el sitio.

```css
:root {
  --pixel:    #567C8D;   /* azul petróleo */
  --oxford:   #2F4156;   /* azul marino */
  --celeste:  #C8D9E6;
  --luna:     #F5EFEB;   /* beige */
  --papel:    #FFFFFF;   /* blanco */

  --f-pixel: "Pixelify Sans", "DM Mono", monospace;
  --f-sans:  "DM Sans", system-ui, sans-serif;
  --f-mono:  "DM Mono", ui-monospace, monospace;
}

/* dentro de cada proyecto se usa una sola tipografía */
.win--detalle, .win--detalle * { font-family: var(--f-mono) !important; }
```

### JavaScript, la interacción

**Qué es.** 
JavaScript es la Interactividad de la pagina, los cambios con un clic, botones que responden.

**Cómo lo usé.** Los 12 proyectos están guardados como una lista de datos. Con esa lista, JavaScript arma el índice y la ventana de detalle de cada trabajo, con sus fotos, video y créditos.

```js
{
  id: "chair-ele", categoria: "objetos", titulo: "Chair Ele", anio: "2025",
  carpeta: "trabajo-silla", portada: "silla.jpeg",
  proceso: ["silla-a.jpeg", "silla-b.jpeg", …],
  creditos: [ANN], video: "videos portafolio/trabajo-silla/silla.mp4"
}
```

### MQTT, mensajes entre el teléfono y la pantalla

**Qué es.** MQTT comunica datos entre distitintos dispositivos con recursos limitados .

**Para qué lo usé.** En Contrapresión cada teléfono funciona como control, el teléfono le manda a la pantalla lo que hace la persona (inclinarlo, tocarlo, soplar) y la pantalla le puede responder, por ejemplo haciéndolo vibrar. Cada partida tiene su propio código de sala, así no se mezclan los mensajes.

```js
async function conectar() {
  base = `tacto/${sala}/${dev}`;
  const will = { topic: `${base}/status`, payload: JSON.stringify({ online: false, name: nombre, caps: { rol } }), qos: 1, retain: true };
  const o = await Tacto.open({ clientId: 'tel-' + dev, will });
  client = o.client;
  client.on('connect', () => { client.subscribe(`${base}/cmd`); publicarEstado(); });
}

const pub = (kind, obj, qos = 0, retain = false) =>
  client && client.connected && client.publish(`${base}/${kind}`, JSON.stringify(obj), { qos, retain });
```

---

## 4. Reflexión del semestre

### Principales aprendizajes




### Desafíos y cómo los resolviste

También hubo desafíos más prácticos: mostrar mis trabajos sin que la página se viera sobrecargada me hizo pensar en qué necesita ver alguien primero, y por eso cada trabajo muestra solo su nombre hasta que lo eliges. Las librerías que se recomendaron funcionaban casi todas con React, así que tuve que buscar una que pudiera usar a mi manera, y la encontré en Shaders.com. Y subir todo a GitHub me enseñó a tener paciencia y a ordenar mis carpetas, porque las fotos y videos pesaban demasiado y tuve que subirlos por partes.

| Problema | Causa | Solución |
|---|---|---|
| El link de GitHub Pages mostraba una página en blanco con el README | Pages publicó primero el repositorio solo con README, antes de subir `index.html` | Subí `index.html` a la raíz y esperé el ✔ verde de Pages |
| Después de subir cambios seguía viendo la versión antigua | El navegador guarda los archivos un tiempo (caché) | Recargué con Ctrl + F5 o abrí la página en una ventana privada |
| Las imágenes salían cortadas o con franjas | La imagen se estiraba más que su marco y el panel tenía un ancho fijo | Ajusté el código para que la foto principal mantenga su propia proporción y para que, en el acordeón, el panel abierto tome la forma de cada foto |
| La imagen grande desapareció de todos los proyectos | Una regla de mi código ocultaba la portada si también figuraba en la lista de proceso | La portada va primero en el acordeón y se salta en la lista de proceso |
| El título "trabajos" se cortaba en el celular | El tamaño de letra era fijo y más ancho que la pantalla | Ajusté el cálculo del tamaño según el ancho de la pantalla |
| GitHub no dejaba subir la carpeta `imagenes` | El navegador acepta máximo 100 archivos por subida | Saqué los videos a su propia carpeta para que `imagenes` quedara bajo 100 archivos |
| "Commit failed, the file is too large" | Los videos juntos pesaban demasiado para una sola subida | Subí los videos en tandas, en la carpeta `videos portafolio/` |
| El GIF de la Lámpara no se veía en la página publicada | El archivo no estaba subido a GitHub y el reproductor solo aceptaba `.mp4` | Lo subí a `videos portafolio/trabajo-lampara/`, habilité que se muestren GIF y programé que si un video no carga la sección se oculte |
| El sitio tenía una sola página | Sobre mí era una sección dentro de `index.html` | Lo separé en `sobre-mi.html`, enlazada desde la navegación |
| VS Code mostraba "1 problem" en `style.css` | `-webkit-line-clamp` sin su propiedad estándar | Agregué `line-clamp: 2;` |
| La cursiva pixelada no se leía bien | Sacramento es una letra muy fina y al engrosarla para pixelarla se tapaban letras como la "a" y la "o" | Comparé varias cursivas convertidas en píxeles y elegí Dancing Script, que tiene trazo propio y se lee sin engrosarla |
| La "j" de "trabajos" se cortaba | El alto de cada título era fijo y no alcanzaba para las letras con cola | Ajusté el código para medir el alto real del texto antes de pixelarlo |
| Se cargaba una tipografía que ya no se usaba | Instrument Serif quedó en el enlace de Google Fonts después del cambio de estética | La saqué del enlace para que la página cargue más rápido |
| El video de Multirealidades pesaba 34 MB | GitHub no deja subir archivos de más de 25 MB desde la web | Usé una versión más liviana del video, de 3,2 MB |

### Créditos (código, componentes, tipografías, imágenes y sonidos)

#### Código y componentes

Tomé las ideas de los referentes y las hice a mi manera, menos Shaders.com, que sí se puede usar directo.

| Componente | Autor / Fuente | Licencia | Qué hice en el portafolio |
|---|---|---|---|
| Pixelate e ImageTexture | [shaders.com](https://shaders.com) | Licencia MIT | **Integrado.** El efecto que pixela la foto de la playa en la portada (con respaldo en CSS) |
| Skiper 53 | Gurvinder Singh · [skiper-ui.com/v1/skiper53](https://skiper-ui.com/v1/skiper53) | Uso libre con atribución | **Adaptado.** La lista de trabajos que se abre con la foto, reescrita sin React |
| Acordeón de imágenes | [skiper-ui.com](https://skiper-ui.com) · [bencho.dev](https://bencho.dev) | Uso libre / inspiración | Las fotos de proceso dentro de cada proyecto |
| Matrix Trail | [ui.aceternity.com](https://ui.aceternity.com) | Licencia MIT | Inspiración para el rastro de píxeles que sigue al cursor |
| Text Effect / Transitions | [motion-primitives.com](https://motion-primitives.com) | Licencia MIT | Inspiración para el desenfoque de la palabra que cambia en el titular |

#### Tipografías

Todas cargadas desde [Google Fonts](https://fonts.google.com) bajo licencia **SIL Open Font License 1.1**:
- **Dancing Script** (autor: Impallari Type)
- **Pixelify Sans** (autor: Stefie Justprince)
- **DM Mono** (autor: Colophon Foundry)
- **DM Sans** (autor: Colophon Foundry)

#### Imágenes y videos

Las fotos de los proyectos están en la carpeta [imagenes](imagenes/), con una carpeta por trabajo, y los videos en [videos portafolio](videos%20portafolio/). Son fotos y videos tomados por Camila Ramirez, Dayana Pañitrur y yo, menos los de Sin-te. Las fotos de fondo (la playa y el tronco) son mías. La foto de Sobre mí (`imagenes/ui/foto-perfil.jpg`) también la saqué yo.

#### Sonidos

Este portafolio no usa sonidos. Los sonidos de *Contrapresión* y de *Traductor de bits* están acreditados en el README de cada repositorio [si usaste algún sonido de terceros con licencia específica en los proyectos del curso, puedes mencionarlo aquí].

#### Referentes y recursos de consulta

| Referente / Recurso | Link | Qué tomé |
|---|---|---|
| Bill Guo | [billguo.me](https://billguo.me) | Proyectos como colección, jerarquía tipográfica (primera etapa) |
| Cindy Ly | [cindyly.design](https://www.cindyly.design/) | Navegación lúdica tipo escritorio y elementos arrastrables (primera etapa) |
| Feather Computer | [feather.computer](https://feather.computer/) | Contenido ordenado como archivos en un escritorio (primera etapa) |
| Nicolás Miranda (compañero) | [nicolas-miranda1312.github.io](https://nicolas-miranda1312.github.io/) | La organización del portafolio, con la portada primero y cada sección aparte, y los filtros de los trabajos |
| Effepinna Studio (Fabio Pinna) | [effepinnastudio.com](https://effepinnastudio.com) | Un personaje propio como presentación |
| 21st.dev | [21st.dev/community/components](https://21st.dev/community/components) | Consulta de componentes |
| save.design | [save.design/explore](https://save.design/explore) | Consulta de referentes |
| Designeer | [designeer.xyz](https://designeer.xyz) | Consulta de referentes |
| mesh3d | [mesh3d.gallery](https://mesh3d.gallery) | Consulta de referentes |

### Uso de IA a lo largo del semestre

**Herramientas:** Claude, como apoyo en la programación para avanzar más rápido, armar y ajustar funciones en HTML, CSS y JavaScript, integrar el acordeón de fotos de proceso de cada proyecto, resolver errores al subir los archivos al repositorio y apoyar en la interactividad del componente "Fila del índice" en Figma.

**Dónde no usé IA:** No usé IA para generar el sitio completo ni en las decisiones de diseño del portafolio (elección de trabajos, estética, paleta, estructura y contenidos). Fui programando el sitio por mi cuenta y recurriendo a Claude como apoyo puntual cuando necesitaba destrabar partes que se me complicaban, adaptar componentes de librerías externas sin React o depurar errores específicos.

| Etapa | Qué le pedí | Qué me entregó | Qué decidí yo |
|---|---|---|---|
| Avatar pixel art <img width="220" height="537" alt="image" src="https://github.com/user-attachments/assets/15c69e48-91fe-4dc6-ba75-903ab6c47214" /> | Que me ayudara a crear mi avatar en pixel art a partir de mis fotos y a animarlo | Una base de mi avatar dibujado en una grilla de píxeles, que respira, parpadea, mira hacia el cursor y saluda | Elegí las referencias, ajusté el código e iteré para darle más detalle y sombras en la cara, el pelo y la ropa |
| Portada y secciones | Apoyo para estructurar que al entrar se vea solo la portada y que Trabajos y Sobre mí se abran con sus botones | Sugerencias de lógica para mostrar y ocultar las secciones como páginas | Elegí esta organización para que no se viera saturada la página y la integré en mi código |
| Fondos | Apoyo para aplicar un filtro con los colores de mi paleta sobre mis fotos de la playa y del tronco | La lógica de filtrado y pixelado para la playa en la portada y el tronco en trabajos | Elegí mis propias fotos, definí la paleta, ajusté la opacidad y programé el respaldo en CSS |
| Lista de trabajos <img width="1180" height="767" alt="image" src="https://github.com/user-attachments/assets/c307643e-706f-4208-9139-76acece8f68a" /> | Ayudarme a adaptar el componente Skiper 53 sin React para que al pasar el cursor por el nombre aparezca la foto | Una base en JavaScript vanilla para abrir la fila con la foto y los filtros por categoría | Integré el código en mi página, ajusté los estilos y definí que mostrara solo el nombre y la foto al pasar el cursor |
| Figma <img width="1151" height="492" alt="image" src="https://github.com/user-attachments/assets/fe112749-925a-4530-94cc-1699a496200e" /> | Ayuda para configurar la interactividad de la fila de índice de los trabajos | Guía para armar los estados interactivos que muestran la portada del trabajo | Implementé el prototipo, corroboré que funcionara igual que la web y apliqué lo aprendido en el resto de las pantallas |

Importante recalcar que la IA fue un apoyo para agilizar el desarrollo, mientras iba programando, cuando alguna parte se me complicaba o el código no funcionaba como debía, le pedía que identificara el error, me explicara cuál era el problema y cómo corregirlo para aplicarlo y seguir avanzando.

#### Creación del personaje

- **Prompt 1.** "Quiero crear un personaje que me represente para la portada de mi portafolio. Te paso dos fotos mías para que tome mi pelo largo negro, mi cara y mi ropa, una polera negra de malla y jeans anchos oscuros. Quiero que sea animado, que respire, parpadee, salude y apunte a mis trabajos."
- **Prompt 2.** "No me convence el estilo de caricatura. Hazlo en pixel art, que se parezca a mí, con un contorno oscuro como en las referencias de personajes pixel art que te mando."
- **Prompt 3.** "Mejora más mi personaje, mejorar la calidad y el funcionamiento del personaje." Elegí que tuviera más detalle y sombras.
- **Qué me entregó.** Una base de avatar en pixel art dibujado con código (36 × 76 píxeles, que respira, parpadea, mira hacia el cursor, saluda y habla) que fui ajustando e iterando hasta lograr una versión con más detalle (cejas, nariz, labios en dos tonos, gargantilla, brillo en el pelo y pliegues en el pantalón).
- **Qué ajusté y por qué.** Pasé de la caricatura al pixel art porque calzaba mejor con la letra pixelada, y mantuve mi ropa real en el avatar para que se pareciera a mí.

<img width="222" height="520" alt="image" src="https://github.com/user-attachments/assets/861ccd90-67c8-4fa6-a2bc-9cae6e90b56e" />

#### Transiciones de las imágenes en la descripción de cada proyecto

- **Prompt 1.** "En la ficha de cada proyecto quiero que las fotos de proceso se vean como un acordeón. Al pasar el mouse o hacer clic, la foto elegida se abre a color y las demás quedan angostas y en gris, con una transición suave."
- **Prompt 2.** "Cuando abro un proyecto desde la lista, quiero que la ventana crezca desde la fila donde hice clic, en vez de aparecer de golpe."
- **Qué me entregó.** La base del acordeón de fotos con la transición de apertura, la animación de ventana creciendo desde la fila del índice y un ajuste para que el panel abierto tome la proporción de cada foto, que luego fui afinando en mi código.
- **Qué ajusté y por qué.** Ajusté el código para que la foto principal de cada proyecto fuera la primera del acordeón y no se repitiera en el proceso.

<img width="1181" height="777" alt="image" src="https://github.com/user-attachments/assets/dee44b14-6450-4309-8782-a1df1fbc2a23" />

#### Lista de trabajos que muestra la foto

- **Prompt.** "Para la sección de trabajos quiero que aplique el código que te doy… quiero que sea el nombre del proyecto, pases el cursor y te salga la foto del proyecto." Le pasé el componente Skiper 53 de Skiper UI.
- **Qué me entregó.** Una adaptación sin React del componente para que cada trabajo muestre su nombre y, al pasar el cursor, se abra y aparezca su foto, que integré y ajusté en mi página.
- **Qué ajusté y por qué.** Ajusté la vista para que no se vieran las fotos de los trabajos hasta pasar el cursor, logrando que la lista quedara limpia.


#### Reflexión sobre el uso de IA y la creación de mi portafolio

Usar IA me ayudó a facilitar el proceso de crear mi portafolio: cuando tenía una idea, me servía para saber si lo que quería era posible de lograr en la página y cómo podía hacerlo, antes de invertir tiempo en algo que quizás no iba a funcionar. También me ayudó a organizarme, a ordenar los pasos y a no perderme entre tantos cambios. Lo que más me sirvió fue aprender a explicarme bien, porque para que el resultado fuera lo que yo imaginaba tenía que describir con claridad lo que quería, y eso me obligó a tener mis ideas más claras. Aun así, la IA no decidió por mí: revisé cada versión, pedí corregir lo que no me representaba y muchas veces cambié lo que me proponía, porque al final el portafolio tenía que sentirse mío.

Crear un portafolio que tenga mi esencia fue más difícil de lo que pensé. No se trata solo de ordenar trabajos y elegir colores, sino de mirarme hacia adentro y preguntarme qué es lo que de verdad me gusta, qué me representa y qué quiero mostrar. En el camino probé muchas estéticas, paletas y formas de presentarme, y en cada cambio tuve que revisar si eso era realmente yo o solo algo que se veía bien.

Lo más complicado fue pensar en cómo me iban a ver los demás. Quería que quien entrara pudiera conocer quién soy y viera a una persona confiable, capaz de lograr buenas cosas. Eso es aún más difícil, porque en cierta parte no es fácil creerse el cuento de que eres buena en lo que haces. Mostrar mis proyectos, contar cómo los hice y poner mi nombre en ellos me obligó a mirar mi trabajo con otros ojos y a reconocer lo que he logrado.

Al final, el portafolio también terminó siendo un ejercicio personal: me ayudó a ordenar lo que he hecho, a entender hacia dónde quiero ir y a confiar un poco más en lo que sé hacer.

---

## 5. Trabajos y con quién los hice

Los trabajos están ordenados por **categoría** y, dentro de cada una, por **año** (del más reciente al más antiguo), igual que en el sitio.

| Nº | Categoría | Trabajo | Año | Con quién lo hice | ¿Tiene video? |
|---|---|---|---|---|---|
| 01 | Electrónica | Sin-te | 2026 | Camila Ramirez y Dayana Pañitrur · expuesto en INÉDITO Universitario, Design Week México 2026 ([publicación](https://www.instagram.com/p/DeecHSEESYF/)) | sí |
| 02 | Electrónica | Tostadora inestable | 2026 | Dayana Pañitrur, Carla Pino Barrios y Camila Ramirez | sí, dos |
| 03 | Web | Multirealidades | 2026 | Dayana Pañitrur · proyecto original de Felipe Roa | sí, video de uso (`uso-multirealidades.mp4`) |
| 04 | Web | Traductor de bits | 2026 | Camila Ramirez | sí |
| 05 | Web | Contrapresión | 2026 | Dayana Pañitrur | sí |
| 06 | Web | Diseño Abierto | 2026 | Belén Castillo y Horacio García | no |
| 07 | Diseño de objetos | Banquito zapatero | 2025 | Dayana Pañitrur | no |
| 08 | Diseño de objetos | Chair Ele | 2025 | Sola · réplica de una silla de Ann Demeulemeester | sí |
| 09 | Diseño de objetos | Banca estructural | 2025 | Camila Ramirez, Dayana Pañitrur y Jiamin Huang | no |
| 10 | Diseño de objetos | Mimus Thenca | 2025 | Camila Ramirez, Dayana Pañitrur y Jiamin Huang | sí |
| 11 | Diseño de objetos | Comedero para Mascotas | 2025 | Sola | no |
| 12 | Diseño de objetos | Lámpara | 2025 | Camila Ramirez, Dayana Pañitrur y Jiamin Huang | sí, un GIF |

**Créditos de colaboradores.** Son los mismos que aparecen en la ficha de cada trabajo.

| Persona | Rol | GitHub | Trabajos |
|---|---|---|---|
| Dayana Pañitrur | colaboración | [dayanapanitrur](https://github.com/dayanapanitrur) | Sin-te, Tostadora inestable, Multirealidades, Contrapresión, Banquito zapatero, Banca estructural, Mimus Thenca, Lámpara |
| Camila Ramirez | colaboración | [Estrabismx](https://github.com/Estrabismx) | Sin-te, Tostadora inestable, Traductor de bits, Banca estructural, Mimus Thenca, Lámpara |
| Carla Pino Barrios | colaboración | [Coff4](https://github.com/Coff4) | Tostadora inestable |
| Jiamin Huang | colaboración | [jiamin-huang-wu](https://github.com/jiamin-huang-wu) | Banca estructural, Mimus Thenca, Lámpara |
| Belén Castillo | colaboración | [bombobby](https://github.com/bombobby) | Diseño Abierto |
| Horacio García | colaboración | [horaciogarcia-cell](https://github.com/horaciogarcia-cell) | Diseño Abierto |
| Felipe Roa | creador | [fefeliperoar](https://github.com/fefeliperoar) | Multirealidades (proyecto original) |
| Ann Demeulemeester | diseño original | — | Chair Ele (réplica de su silla) |

**Links de los proyectos web**

| Trabajo | Repositorio | Página (GitHub Pages) |
|---|---|---|
| Multirealidades | [github.com/isidoraalvarez/Multirealidades](https://github.com/isidoraalvarez/Multirealidades) | [isidoraalvarez.github.io/Multirealidades](https://isidoraalvarez.github.io/Multirealidades/) |
| Traductor de bits | [github.com/isidoraalvarez/traductor-de-bits](https://github.com/isidoraalvarez/traductor-de-bits) | [isidoraalvarez.github.io/traductor-de-bits](https://isidoraalvarez.github.io/traductor-de-bits/) |
| Contrapresión | [github.com/isidoraalvarez/contrapresion](https://github.com/isidoraalvarez/contrapresion) | [isidoraalvarez.github.io/contrapresion](https://isidoraalvarez.github.io/contrapresion/) |
| Diseño Abierto | [github.com/isidoraalvarez/dis-abierto-solemne](https://github.com/isidoraalvarez/dis-abierto-solemne) | [isidoraalvarez.github.io/dis-abierto-solemne](https://isidoraalvarez.github.io/dis-abierto-solemne/) |

En el sitio, estos links aparecen como botones ("repositorio GitHub" y "ver experiencia") en la ficha de cada proyecto.

- **Multirealidades.** Página web de arte y tecnología con estética Y2K / Windows XP que explora cómo la presencia y el movimiento del cuerpo pueden alterar la realidad digital a través de la cámara web. Combina tres sistemas simultáneos: OpenCV (movimiento y quietud), MediaPipe (manos y gestos) y Three.js (modelo 3D hecho en Blender).
- **Traductor de bits.** Página web que traduce cualquier fotografía en sonido en tiempo real según el brillo, el color y la distribución de sus píxeles. El sonido se puede descargar y volver a subir para generar una imagen a partir de él, y así sucesivamente. Se controla con la mano mediante MediaPipe o con un controlador MIDI, y su estética toma los menús de la Nintendo Wii.
- **Contrapresión.** Juego web que usa el teléfono como mando (de 2 a 4 teléfonos y una pantalla compartida, conectados por MQTT). No se puede jugar de a una persona, siempre hay un POC y al menos un ciudadano. Tres ciudadanos corren por la Alameda perseguidos por el carro lanzaaguas del POC, una institución ficticia; solo los tres escudos juntos detienen el chorro.
- **Diseño Abierto.** Página web de una sola página para Diseño Abierto 2026, la muestra de fin de año de la Escuela de Diseño UDP. Muestra qué es la muestra, los proyectos de cada mención con sus ramos y estudiantes, y la ubicación y los horarios. La diseñamos primero en Figma y tiene un botón "VISÍTANOS" que se expande y un menú lateral para el celular. La hice para la Solemne 2 de Interfaces Web, no para este curso.

**Proyectos sin video**

Estos trabajos no tienen video porque no grabé su uso. En su ficha se muestran con fotos de proceso y del resultado.

| Trabajo | Qué muestra su ficha |
|---|---|
| Diseño Abierto | Foto de la página. Es de la Solemne 2 de Interfaces Web, fuera de este curso, y se puede probar directo en su página publicada |
| Banquito zapatero | Fotos de proceso y del resultado, y el plano |
| Banca estructural | Fotos de proceso y del resultado |
| Comedero para Mascotas | Fotos de proceso y del resultado |

**Diseños de otras personas**

| Trabajo | Autor/a original | Detalle |
|---|---|---|
| Multirealidades | Felipe Roa — [github.com/fefeliperoar](https://github.com/fefeliperoar) | Es el creador del proyecto; nosotras hicimos nuestra propia versión. |
| Chair Ele | Ann Demeulemeester | Réplica de su silla, el diseño original le pertenece a ella. |

En el sitio, cada trabajo tiene su sección **"créditos"** con el rol de cada persona (colaboración, creador o diseño original) y el link a su GitHub.
