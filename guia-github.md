# Guía: cómo publicar Pizarrón en GitHub (gratis, con GitHub Pages)

Esta guía te lleva paso a paso desde "no tengo nada" hasta tener tu app
funcionando en una dirección web pública, del estilo:

```
https://tu-usuario.github.io/pizarron/
```

No hace falta saber programar ni usar la terminal: todo se puede hacer
desde el navegador.

---

## Lo que vas a necesitar

- Los archivos de la app: `index.html`, `styles.css`, `app.js`,
  `examples.js`, `engine.browser.js`, `manifest.json` (los que te generé
  antes, dentro de la carpeta `pizarron`).
- Una cuenta de GitHub (gratuita).

---

## Paso 1 — Crear una cuenta en GitHub

1. Entrá a **https://github.com**
2. Hacé clic en **Sign up** (Registrarse).
3. Completá correo electrónico, contraseña y un nombre de usuario
   (ese nombre va a formar parte de la dirección de tu app, elegilo
   simple, sin espacios).
4. Verificá tu correo cuando GitHub te lo pida.

Si ya tenés cuenta, pasá directo al paso 2.

---

## Paso 2 — Crear el repositorio (la "carpeta" del proyecto)

1. Una vez logueado, hacé clic en el botón verde **New** (o el ícono
   **+** arriba a la derecha → **New repository**).
2. Completá:
   - **Repository name**: por ejemplo `pizarron`
   - **Description** (opcional): "Editor de pseudocódigo interactivo"
   - Dejalo en **Public** (tiene que ser público para usar GitHub Pages
     gratis).
   - **NO** actives "Add a README file" (para no complicar la subida de
     archivos; lo podés agregar después).
3. Hacé clic en **Create repository**.

---

## Paso 3 — Subir los archivos

1. En la página del repositorio recién creado, buscá el link
   **uploading an existing file** (o el botón **Add file** →
   **Upload files**).
2. Arrastrá **todos** estos archivos juntos a la ventana del navegador
   (no los metas dentro de otra carpeta, tienen que quedar sueltos en
   la raíz del repositorio):
   - `index.html`
   - `styles.css`
   - `app.js`
   - `examples.js`
   - `engine.browser.js`
   - `manifest.json`
3. Abajo de todo, en **Commit changes**, dejá el mensaje que ya viene
   puesto (algo como "Add files via upload") y hacé clic en el botón
   verde **Commit changes**.

> 💡 Si en algún momento querés actualizar un archivo (por ejemplo,
> después de modificar `app.js`), volvé a "Add file → Upload files" y
> subilo de nuevo: GitHub lo reemplaza automáticamente respetando el
> mismo nombre.

---

## Paso 4 — Activar GitHub Pages

1. Dentro del repositorio, andá a la pestaña **Settings** (arriba, en
   el menú del repositorio, no el de tu perfil).
2. En el menú de la izquierda, hacé clic en **Pages**.
3. En **Build and deployment → Source**, elegí **Deploy from a
   branch**.
4. En **Branch**, elegí `main` (o `master`, según cómo se llame la
   tuya) y la carpeta `/ (root)`. Hacé clic en **Save**.
5. Esperá uno o dos minutos y volvé a entrar a **Settings → Pages**:
   arriba va a aparecer un mensaje verde con la dirección de tu sitio,
   algo así:

   ```
   Your site is live at https://tu-usuario.github.io/pizarron/
   ```

6. Entrá a esa dirección: ahí está tu app, funcionando para cualquiera
   que tenga el link, desde PC o celular.

---

## Paso 5 — Compartir el link con tus alumnos

Copiá la URL de GitHub Pages y compartila como quieras (WhatsApp,
classroom, cartelera, etc.). Funciona en cualquier navegador moderno
(Chrome, Firefox, Safari, Edge) y se adapta a pantallas de celular.

Si querés, en el celular se puede "instalar" como si fuera una app:
al entrar al link, el navegador suele ofrecer la opción **Agregar a
pantalla de inicio** (gracias al archivo `manifest.json` que ya está
incluido).

---

## Cómo actualizar la app más adelante

Cada vez que quieras cambiar algo (agregar un ejemplo, corregir un
texto, cambiar colores):

1. Editá el archivo correspondiente en tu computadora.
2. Entrá al repositorio en GitHub → **Add file → Upload files**.
3. Subí el archivo modificado (mismo nombre) → **Commit changes**.
4. GitHub Pages se actualiza solo, en general en menos de un minuto.
   Si no ves el cambio, hacé un refresco forzado del navegador
   (Ctrl+Shift+R en PC, o borrá caché en el celular).

---

## Problemas comunes

| Problema | Causa probable | Solución |
|---|---|---|
| Aparece una página en blanco | Los archivos no quedaron en la raíz del repositorio, sino dentro de una subcarpeta | Volvé a subirlos arrastrándolos sueltos, sin carpeta contenedora |
| "404 - There isn't a GitHub Pages site here" | Todavía no pasaron unos minutos desde que activaste Pages, o el branch elegido está mal | Esperá 1-2 minutos y revisá que el branch en Settings → Pages sea el correcto |
| No carga la tipografía y se ve con una fuente distinta | No hay conexión a internet (la fuente se trae de Google Fonts) | No afecta el funcionamiento, solo el estilo; es normal sin internet |
| Subí un archivo con otro nombre y no cambia nada | El `index.html` sigue apuntando al nombre viejo | Los nombres de archivo tienen que ser exactamente: `index.html`, `styles.css`, `app.js`, `examples.js`, `engine.browser.js`, `manifest.json` |

---

## Opcional: usar un nombre de dominio propio

Si más adelante comprás un dominio (por ejemplo `pizarron.com`), en
**Settings → Pages → Custom domain** podés escribirlo y seguir las
instrucciones que te muestra GitHub para configurar los DNS. No es
necesario para que la app funcione: el link gratuito de
`github.io` ya es público y estable.
