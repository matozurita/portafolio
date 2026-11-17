# Cómo publicar tu portafolio

Esta carpeta ya tiene todo lo que necesita la página. Solo hay que subirla a GitHub, conectarla a Cloudflare Pages y, si quieres, comprar el dominio.

## Qué hay en esta carpeta

| Archivo | Para qué sirve |
| --- | --- |
| `index.html` | La página completa del portafolio |
| `img/` | Todos los artes, portadas de video y la imagen para compartir |
| `favicon.svg` | El ícono "mz" que se ve en la pestaña del navegador |
| `robots.txt` | Permite que Google encuentre la página |
| `_headers` | Ajustes de seguridad que Cloudflare lee solo |
| `LEEME-PUBLICAR.md` | Esta guía (no afecta a la página) |

## 1. Subir a GitHub (10 minutos)

1. Entra a github.com con tu cuenta y haz clic en **New repository**.
2. Nombre: `portfolio`. Márcalo como **Public** y haz clic en **Create repository**.
3. En la página del repositorio vacío, haz clic en **uploading an existing file**.
4. Abre esta carpeta en Finder, selecciona **todo su contenido** (no la carpeta en sí) y arrástralo a GitHub.
   - `index.html` tiene que quedar en la raíz del repositorio, al lado de la carpeta `img`.
   - Revisa que la carpeta `img` haya subido con todas sus imágenes.
5. Haz clic en **Commit changes**.

## 2. Publicar con Cloudflare Pages (5 minutos)

1. Entra a dash.cloudflare.com, con la misma cuenta que usaste para JC Rides o con una nueva tuya.
2. Ve a **Workers & Pages** → **Create** → pestaña **Pages** → **Connect to Git**.
3. Elige el repositorio `portfolio` y haz clic en **Begin setup**.
4. Configura así:
   - Project name: `mateozurita` (así la dirección queda `mateozurita.pages.dev`)
   - Framework preset: **None**
   - Build command: *(vacío)*
   - Build output directory: `/`
5. Haz clic en **Save and Deploy**. En uno o dos minutos tu portafolio queda en línea.
6. Ábrelo en el celular y revisa que los videos se reproduzcan dentro de la página.

Con eso ya tienes un link profesional y gratis: `https://mateozurita.pages.dev`

## 3. Comprar el dominio (opcional, unos $10 al año)

1. En Cloudflare ve a **Domain Registration** → **Register Domains**.
2. Busca `mateozurita.com`. Si no está disponible, prueba `mateozurita.co` o `mateozurita.me`.
3. Paga con tu tarjeta (eso lo haces tú) y activa **Auto-renew**.
4. Ve a **Workers & Pages** → tu proyecto `mateozurita` → **Custom domains** → **Set up a custom domain**.
5. Escribe `mateozurita.com` y confirma. Repite con `www.mateozurita.com`.
6. Espera unos minutos: el candado HTTPS se activa solo.

### Si compras un dominio distinto a mateozurita.com

En `index.html` hay dos líneas que dicen `https://mateozurita.com`. Son las que hacen que se vea una vista previa con imagen cuando pegas el link en WhatsApp o LinkedIn. Cámbialas por tu dominio:

1. En GitHub abre `index.html` y haz clic en el ícono del lápiz.
2. Busca `mateozurita.com` (Cmd+F) y reemplázalo en las dos líneas.
3. Haz clic en **Commit changes**. Cloudflare publica la nueva versión en un minuto.

## 4. Antes de mandarlo a una empresa

- Pega el link en tu CV, en la línea "Portfolio".
- Pégalo en un chat de WhatsApp contigo mismo para revisar que salga la vista previa con la imagen.
- El cierre de la página dice "Let's make it impossible to ignore", que es el eslogan de The Narrative Club. Para otras aplicaciones, cambia esa frase en `index.html` (busca `impossible`).

## Cómo actualizarlo después

En GitHub abre el archivo → ícono del lápiz → edita → **Commit changes**. Para un arte nuevo, entra a la carpeta `img` → **Add file** → **Upload files**. Cloudflare publica los cambios solo.
