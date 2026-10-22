# El Verbólogo

Humano digital de **DIA (Didáctica con IA)** y **Adustiones Libertarias** (El Colorado, Formosa): un personaje 3D de caricatura que conversa por voz (agente de ElevenLabs) y aparece en **realidad aumentada** en la cámara del celular, **sin lámina**: se lo llama con el botón de su cara.

Pelo y barba verdes, cabeza grande, ojos y orejas de caricatura, anteojos con un cristal rosa y otro celeste, chaleco con letras, brazos robóticos con circuitos, manos enormes, jean arremangado, zapatillas y letras de colores que flotan alrededor.

Es experto en **palabras** (verbos, verboides, voseo, neologismos, préstamos, siglas y vocabulario de la inteligencia artificial con sus alternativas en español) y en **libros y discos**: Umberto Eco, literatura latinoamericana, argentina, regional (Van Bredam, Ayala Gauna, Roa Bastos) y anarquista (Kropotkin, Emma Goldman, Arshinov, Christian Ferrer, Frank Mintz, Bayer), los libros de Ariel Cóceres, punk y música de todos los géneros, vinilos, casetes y CD.

- Agente de ElevenLabs: `agent_5201m5jaz92gfj8vbdry430rs5ma`
- Prueba solo de voz: https://elevenlabs.io/app/talk-to?agent_id=agent_5201m5jaz92gfj8vbdry430rs5ma

## Cómo se usa
1. **Llamar al Verbólogo** (el botón con su cara): se abre la cámara y aparece de pie en la imagen. Tocá «Hablar» y conversá, o escribile.
2. **Leer la tapa**: con la cámara abierta, enfocá cualquier libro, vinilo, CD o casete y tocá «Leer la tapa». La página lee el texto de la tapa y el Verbólogo identifica la obra y te la cuenta. «Guardar en la estantería» la deja cargada.
3. **Mi estantería**: sacale una foto de frente a cada tapa y cargá sus datos. Desde ahí, al enfocarla, el Verbólogo salta y se para **sobre la tapa** y te la cuenta solo. Hasta 24 tapas; se pueden exportar e importar para compartir con estudiantes.

## Publicarla
1. Creá un repositorio en GitHub y subí el contenido de esta carpeta.
2. Settings → Pages → Branch `main` / root → Save.
3. Abrí `https://TU-USUARIO.github.io/REPO/` en el celular.

La cámara y el micrófono **solo funcionan con https** (GitHub Pages o Netlify).

## Lo que conviene saber
- Necesita internet: la voz es el agente de ElevenLabs (cada charla consume créditos) y «Leer la tapa» descarga el lector de texto la primera vez.
- Sin tapas cargadas, el Verbólogo aparece flotando delante de la cámara (no queda pegado a un objeto). Sobre una tapa de la estantería sí queda parado encima y la sigue.
- Las tapas con mucho detalle y buena luz se reconocen mejor; los estuches de CD brillan: inclinalos un poco.

## Archivos
| Archivo | Para qué |
| --- | --- |
| `index.html` | La página completa: figura 3D, voz, cámara, botón de llamado y estantería |
| `prompt-del-agente.txt` | Las instrucciones del agente en ElevenLabs |
| `base-de-conocimiento.txt` | Lo que sabe: libros y discos + palabras, neologismos e IA (en ElevenLabs son dos documentos) |

(ɔ) Copyleft — Adustiones Libertarias, El Colorado, Formosa. Se permite y se alienta copiar, adaptar y compartir citando la fuente.
