# Notas de seguridad y cumplimiento

Son notas internas. No se enlazan desde el sitio. Última revisión: 29 de septiembre de 2026.

Las "tres páginas" de este repositorio son:

- `index.html`
- `demos/ferreteria/index.html`
- `demos/gimnasio/index.html`

Santiago_Clothes está en otro repositorio y no entra en esta revisión.

## Datos personales

- **Las tres páginas no recogen ni envían datos personales.** No usan `fetch`, `XMLHttpRequest`, `sendBeacon` ni WebSocket. No tienen formularios con `action`. No usan cookies, `localStorage` ni `sessionStorage`. No tienen analítica ni píxeles.
- Por eso **no llevan política de tratamiento de datos ni aviso de cookies**.
- El formulario de clase de prueba del gimnasio pide nombre y celular. Solo arma el mensaje y lo muestra en pantalla para que el visitante lo copie. Los datos no salen del navegador.
- El cotizador de la ferretería funciona igual.
- El botón de WhatsApp de la portada abre `wa.me` con un saludo fijo. No manda ningún dato del visitante. Si el visitante escribe algo, lo hace él mismo dentro de WhatsApp.
- Los únicos datos personales publicados a propósito son **mi número de WhatsApp y mi correo de trabajo**, en el bloque `CONFIG` de `index.html`.

## Terceros

- El único tercero es **Google Fonts**: `fonts.googleapis.com` sirve el CSS y `fonts.gstatic.com` sirve los archivos de fuente. Recibe la IP y el user-agent del visitante.
- **Pendiente:** alojar las tipografías en el mismo sitio (archivos `.woff2` en el repo y `@font-face` propio) para quitar ese tercero.

## Hosting y HTTPS

- GitHub Pages está publicado desde `main`, en la raíz `/`.
- **Enforce HTTPS: activo.** La API devuelve `https_enforced: true` y `http://` redirige a `https://` con un 301.
- **GitHub Pages no permite cabeceras HTTP propias** (CSP, `Permissions-Policy`, `Referrer-Policy`, etc.).
- Para sitios de clientes, usar **Netlify** o **Cloudflare Pages** con un archivo `_headers`.
- Todo lo que está en este repositorio público se puede ver en GitHub, y GitHub Pages sirve también los `.md`. Este archivo, por ejemplo, se abre en `/SECURITY-NOTAS.md` aunque no esté enlazado. **No escribir aquí nada privado.**

## Si algún día se conecta un formulario a un servidor

Antes de publicarlo hay que agregar:

1. Una política de tratamiento de datos personales.
2. Un aviso de privacidad.
3. La autorización expresa del titular, con casilla sin marcar por defecto, antes de enviar.

Además, revisar si el servicio que recibe los datos es un tercero y mencionarlo en la política.

## Revisión antes de cada push

- Buscar en todo el historial (`git log --all -p`) tokens, claves de API, llaves privadas y contraseñas. En la revisión del 29 de septiembre de 2026 no se encontró nada.
- Confirmar que el remoto no tenga un token incrustado en la URL.
- Confirmar que los commits usen el correo noreply de GitHub.
