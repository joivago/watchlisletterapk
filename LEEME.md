# LB Watchlist

App de Android que añade películas a tu watchlist de Letterboxd. Escribes o pegas
una lista (una película por línea), pulsas «Añadir» y la app busca cada una en
la web de Letterboxd y pulsa el botón de Watchlist por ti.

## Qué puedes escribir

```
Dune
The Thing (1982)
Perfect Days, 2023
https://letterboxd.com/film/past-lives/
https://boxd.it/xxxx
```

- El año es opcional; ponlo entre paréntesis o tras una coma cuando haya varias
  películas con el mismo título.
- Se aceptan enlaces de Letterboxd directamente.
- Viñetas y numeración («1.», «-», «•») se ignoran.
- También puedes usar **Compartir** desde cualquier app (notas, WhatsApp, el
  navegador…) y elegir «LB Watchlist».

Al terminar, en la caja de texto quedan solo las que fallaron, para corregirlas
y volver a intentarlo.

## Cómo conseguir el APK

### Opción A · Sin instalar nada (GitHub)
1. Crea una cuenta gratuita en github.com y un repositorio nuevo (puede ser privado).
2. Sube todo el contenido de esta carpeta (botón «Add file → Upload files»;
   incluye la carpeta `.github`, que en algunos sistemas está oculta).
3. Entra en la pestaña **Actions**: la compilación arranca sola y tarda unos 3–5 minutos.
4. Abre la ejecución terminada y descarga **LB-Watchlist-apk** (un .zip con el .apk dentro).
5. Pásalo al móvil, ábrelo y permite «instalar apps de origen desconocido» cuando lo pida.

### Opción B · Android Studio
1. Instala Android Studio y elige **Open** sobre esta carpeta.
2. Espera a que termine la sincronización (la primera vez descarga cosas).
   Si te propone actualizar versiones de Gradle o del plugin, puedes aceptar.
3. Conecta el móvil con la depuración USB activada y pulsa ▶ Run,
   o usa **Build → Build APK(s)**.

## Primer uso
1. Abre la app y pulsa **Mi cuenta** para iniciar sesión en Letterboxd en la
   página de abajo. La sesión se queda guardada.
2. **Importante:** el inicio de sesión con Google o Apple no funciona dentro de
   apps (Google lo bloquea). Usa usuario y contraseña. Si tu cuenta se creó con
   Google, ponle una contraseña desde «Forgotten password» en la web de Letterboxd.

## Si algo falla
- Si la app no encuentra el botón de Watchlist en una película, se pausa:
  añádela tú tocando la página de abajo y pulsa **Siguiente**.
- Si Letterboxd cambia el diseño de su web y deja de funcionar en general, el
  único archivo que hay que ajustar es `app/src/main/assets/lbw.js`.
- La app no usa la API oficial (es privada); funciona como si fueras tú pulsando
  los botones. Úsala con listas razonables y sin prisas.
