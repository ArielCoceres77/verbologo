# El Verbólogo

Humano digital de **DIA (Didáctica con IA)** y **Adustiones Libertarias** (El Colorado, Formosa): un personaje 3D de caricatura que conversa por voz (agente de ElevenLabs) y aparece en **realidad aumentada** en la cámara del celular, **sin lámina**: se lo llama con el botón de su cara.

Pelo y barba verdes, cabeza grande, ojos y orejas de caricatura, anteojos con un cristal rosa y otro celeste, chaleco con letras, brazos robóticos con circuitos, manos enormes, jean arremangado, zapatillas y letras de colores que flotan alrededor.

Es experto en **palabras** (verbos, verboides, voseo, neologismos, préstamos, siglas y vocabulario de la inteligencia artificial con sus alternativas en español) y en **libros y discos**: Umberto Eco, literatura latinoamericana, argentina, regional (Van Bredam, Ayala Gauna, Roa Bastos) y anarquista (Kropotkin, Emma Goldman, Arshinov, Christian Ferrer, Frank Mintz, Bayer), los libros de Ariel Cóceres, punk y música de todos los géneros, vinilos, casetes y CD.

- Agente de ElevenLabs: `agent_5201m5jaz92gfj8vbdry430rs5ma`
- Prueba solo de voz: https://elevenlabs.io/app/talk-to?agent_id=agent_5201m5jaz92gfj8vbdry430rs5ma

## Cómo se usa
1. **Llamar al Verbólogo** (el botón con su cara): se abre la cámara y aparece de pie en la imagen. Tocá «Hablar» y conversá, o escribile.
2. **Leer la tapa**: con la cámara abierta, enfocá cualquier libro, vinilo, CD o casete y tocá «Leer la tapa». La página lee el texto de la tapa y el Verbólogo identifica la obra y te la cuenta. «Guardar en la estantería» la deja cargada.
3. **Mi estantería (colaborativa)**: sacale una foto a la tapa o **elegila de la galería** del celular, y cargá sus datos. Con «Compartirla en el estante en vivo» marcado, la tapa sube a la **estantería compartida** y aparece en todos los celulares y tablets que abran el mismo enlace. Al enfocarla, el Verbólogo salta, se para **sobre la tapa** y te la cuenta solo. Cada persona puede quitar solo las tapas que subió ella; las de otros se pueden ocultar en el propio dispositivo.
4. **Moverlo**: con la cámara abierta, arrastralo con el dedo adonde quieras y cambiale el tamaño con dos dedos (o con − y +). El botón con su cara lo vuelve a llamar.
5. **Ver mejor**: en la barra de la cámara, ese botón pone fondos oscuros sólidos y letras grandes para que la interfaz se lea bien sobre cualquier imagen. Queda recordado.

## Publicarla
1. Creá un repositorio en GitHub y subí el contenido de esta carpeta.
2. Settings → Pages → Branch `main` / root → Save.
3. Abrí `https://TU-USUARIO.github.io/REPO/` en el celular.

La cámara y el micrófono **solo funcionan con https** (GitHub Pages o Netlify).

## La estantería compartida (sin cuentas ni Firebase)
Tiene dos partes que se ven juntas en «Mi estantería»:

**1. Estante en vivo (colaborativo).** Cuando alguien comparte su primera tapa, la página crea sola un estante en [jsonblob.com](https://jsonblob.com), un servicio gratuito que no pide cuenta. Arriba de la estantería aparece su estado y dos botones:
- **Copiar enlace para otro dispositivo**: copia la dirección de la página con el código del estante (`…/humano-digital/?estante=CÓDIGO`). Abrila en la tablet, o pasásela a tus estudiantes: todas las tapas que suba cualquiera con ese enlace aparecen en todos los dispositivos (se actualiza sola cada 30 segundos).
- **Usar un código de estante**: para pegar el código o el enlace a mano.

Si me pasás el código de tu estante, lo dejo fijo en la página para que se abra sin enlace.

**2. Estantería fija (`estanteria.json`).** Las tapas que estén en este archivo aparecen siempre, en todos los dispositivos, y nadie las puede borrar desde la página. Para sumar tapas: en «Mi estantería» tocá **Exportar**, y subí ese archivo a esta carpeta con el nombre `estanteria.json` (o pasámelo y lo subo yo).

Cada dispositivo puede quitar solo las tapas que subió; las demás se pueden **ocultar** en ese dispositivo. Las tapas que ya tenías cargadas tienen un botón **Compartir** para subirlas al estante en vivo.

## Lo que conviene saber
- Necesita internet: la voz es el agente de ElevenLabs (cada charla consume créditos) y «Leer la tapa» descarga el lector de texto la primera vez.
- Sin tapas cargadas, el Verbólogo aparece flotando delante de la cámara (no queda pegado a un objeto). Sobre una tapa de la estantería sí queda parado encima y la sigue.
- Las tapas con mucho detalle y buena luz se reconocen mejor; los estuches de CD brillan: inclinalos un poco.
- Cada dispositivo prepara las tapas compartidas la primera vez que abre la cámara (unos segundos por tapa); después quedan guardadas.
- Las tapas compartidas son públicas para quien tenga el enlace: no subas fotos de personas, especialmente de estudiantes.
- El estante en vivo depende de un servicio gratuito externo (jsonblob.com): si algún día no responde, la página avisa y sigue funcionando con la estantería fija y las tapas del propio dispositivo.

## Archivos
| Archivo | Para qué |
| --- | --- |
| `index.html` | La página completa: figura 3D, voz, cámara, botón de llamado y estantería |
| `prompt-del-agente.txt` | Las instrucciones del agente en ElevenLabs |
| `base-de-conocimiento.txt` | Lo que sabe: libros y discos + palabras, neologismos e IA (en ElevenLabs son dos documentos) |

(ɔ) Copyleft — Adustiones Libertarias, El Colorado, Formosa. Se permite y se alienta copiar, adaptar y compartir citando la fuente.
