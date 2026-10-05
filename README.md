# El Verbólo — asistente visual contextual

<img src="desktop/verbolo-retrato.jpg" width="220" align="right" alt="El Verbólo">

El Verbólo, personaje de **DIA (Didáctica con IA) — «Aprendé jugando»**, vive en una ventanita flotante que **mira tu pantalla cuando vos se lo pedís**, entiende qué estás haciendo y te ayuda en cualquier aplicación. Funciona en **PC** (Windows, Linux y Mac) y en **celulares Android**.

- **Offline**: con [Ollama](https://ollama.com) y un modelo con visión corriendo en tu PC, nada sale de tu red.
- **En la nube**: con una clave de la API de Anthropic (Claude), más inteligente, pero cada captura viaja a internet.
- **Ética por diseño**: nunca mira en segundo plano. Solo captura al tocar «Mirar» o al usar el atajo, y se esconde para no salir en su propia foto.

---

## 1. Subirlo a GitHub (una sola vez)

1. Creá un repositorio nuevo en GitHub (por ejemplo `el-verbolo`), público.
2. Subí **todo** el contenido de esta carpeta, incluida la carpeta oculta `.github`.
   - Con Git: `git init && git add . && git commit -m "El Verbólo" && git branch -M main && git remote add origin https://github.com/TU-USUARIO/el-verbolo.git && git push -u origin main`
   - Desde la web: *Add file → Upload files* y arrastrá las carpetas. Si la carpeta `.github` no se sube (en Mac suele estar oculta), creala a mano con *Add file → Create new file*, escribiendo como nombre `.github/workflows/compilar.yml` y pegando el contenido.
3. Andá a **Releases → Draft a new release**, creá la etiqueta `v1.0.0` y tocá **Publish release**.
4. En la pestaña **Actions** vas a ver cómo se compila todo (tarda unos 10 minutos). Al terminar, la Release tiene los instaladores:

| Archivo | Para |
|---|---|
| `Verbolo-Setup-1.0.0.exe` | Windows (instalador) |
| `Verbolo-Portable-1.0.0.exe` | Windows (portable, sin instalar) |
| `Verbolo-1.0.0.AppImage` | Linux |
| `Verbolo-1.0.0.dmg` | Mac |
| `Verbolo-android.apk` | Android |

Para sacar una versión nueva, cambiá el número en `desktop/package.json` y `android/app/build.gradle.kts`, y publicá otra Release.

---

## 2. Instalar en la PC

1. Bajá el archivo de tu sistema desde la Release.
   - **Windows**: si aparece «Windows protegió tu PC», tocá *Más información → Ejecutar de todas formas* (el programa no está firmado).
   - **Linux**: dale permiso de ejecución (`chmod +x Verbolo-*.AppImage`) y abrilo.
   - **Mac**: clic derecho → *Abrir*. Después dale permiso en *Ajustes del Sistema → Privacidad → Grabación de pantalla*.
2. Elegí el cerebro en **⚙ Ajustes**.
3. Usalo: escribí una pregunta (o dejala vacía) y tocá **Mirar**, o apretá **Ctrl+Shift+Espacio** desde cualquier programa.

### Cerebro offline con Ollama
1. Instalá Ollama desde https://ollama.com
2. En una terminal: `ollama pull gemma3:4b` (liviano). Con 16 GB de RAM o una buena placa de video podés probar `qwen2.5vl:7b`.
3. En El Verbólo, elegí *Ollama* y poné el nombre del modelo.

---

## 3. Instalar en Android

1. Desde el celular, bajá `Verbolo-android.apk` de la Release y abrilo. Android te va a pedir permitir «instalar apps de origen desconocido»; si Play Protect avisa, elegí *Instalar de todas formas*.
2. Abrí El Verbólo, elegí el cerebro y tocá **▶ Despertar al Verbólo**. Te va a pedir tres permisos:
   - **Notificaciones** (para mostrar que está activa y el botón Detener).
   - **Mostrar sobre otras apps** (para la burbuja con su cara).
   - **Captura de pantalla** (Android lo pregunta cada vez que lo despertás).
3. Aparece la burbuja con la cara del Verbólo: arrastrala donde quieras, tocala para abrir el panel y tocá **Mirar**.

### Usar el celular con el Ollama de tu PC (sin internet)
1. En la PC, cerrá Ollama y abrilo así:
   - Windows (PowerShell): `$env:OLLAMA_HOST="0.0.0.0"; ollama serve`
   - Linux/Mac: `OLLAMA_HOST=0.0.0.0 ollama serve`
2. Averiguá la IP de la PC (`ipconfig` en Windows, `ip a` en Linux), por ejemplo `192.168.0.15`.
3. En El Verbólo del celular poné `http://192.168.0.15:11434`. PC y celular tienen que estar en el mismo wifi. Si no conecta, permití el puerto 11434 en el firewall.

---

## Su personalidad

El Verbólo te dice qué aplicación ve, te guía con pasos claros (con verbos en imperativo, cómo no) y cierra cada respuesta con un guiño: el verbo clave de lo que estás haciendo, con una mini definición o un dato curioso. Para cambiar su forma de ser, editá el texto `SISTEMA` en `desktop/main.js` y en `android/app/src/main/java/ar/adustiones/lupa/Cerebro.kt`. Para cambiar su cara, reemplazá `desktop/verbolo-cara.png`, `desktop/build/icon.png` y los PNG de `android/app/src/main/res/drawable-nodpi/`.

## Probar el código sin compilar en GitHub

- PC: `cd desktop && npm install && npm start`
- Android: abrí la carpeta `android` con Android Studio y tocá ▶.

## Privacidad

El Verbólo no guarda capturas. Recuerda solo el texto de las últimas 3 preguntas y respuestas mientras está abierta (botón ↺ / «Olvidar» para borrar). Con el cerebro Claude, la captura se envía a Anthropic para responder. Con Ollama, todo queda en tu equipo o tu red.

## Licencia

Copyleft — GPL-3.0-or-later. Copiá, estudiá, modificá y compartí, siempre con la misma libertad.
