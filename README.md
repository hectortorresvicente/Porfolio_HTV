# Portfolio profesional · Hèctor Torres Vicente

Sitio web personal **estático**, preparado para publicar con **GitHub Pages**. No necesita Node.js, compilación ni instalar dependencias.

## Estructura

```text
index.html                 ← página principal (obligatoria para GitHub Pages)
.nojekyll                  ← evita procesamiento de Jekyll
.gitignore
assets/
  css/styles.css           ← diseño visual y responsive
  js/navigation.js         ← menú, enlaces a secciones y navegación
  js/chatbot.js            ← asistente local + IA generativa opcional
  img/favicon.svg          ← icono HT
README.md
```

## Publicar en GitHub Pages (desde el navegador)

1. Inicia sesión en [GitHub](https://github.com/) y crea un repositorio (por ejemplo, `portfolio-hector-torres`). Si usas GitHub Free, mantenlo **público** para publicar con Pages.
2. **Descomprime el archivo ZIP**. No subas el ZIP como si fuera la web: sube los archivos y carpetas **de su interior** a la raíz del repositorio. Debe verse `index.html` en la raíz, no dentro de otra carpeta.
3. En el repositorio, entra en **Settings → Pages** (en la barra lateral, sección **Code and automation**).
4. En **Build and deployment**, selecciona **Source: Deploy from a branch**.
5. Selecciona **Branch: main** y carpeta **/ (root)**. Pulsa **Save**.
6. Cuando finalice la publicación, GitHub mostrará la dirección del sitio. Su formato habitual es:
   `https://TU-USUARIO.github.io/portfolio-hector-torres/`

En GitHub Pages, el nombre real del repositorio reemplaza `portfolio-hector-torres`. Los cambios que hagas en la rama publicada se reflejarán después de cada despliegue.

**Guía oficial de GitHub:**
- [Configurar la fuente de publicación](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Crear un sitio con GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

## Probar antes de publicar

- Para ver el diseño y utilizar el **chat local**, abre `index.html` con un navegador.
- Para probar todas las funciones en condiciones similares a la web publicada, inicia un servidor local en la carpeta del proyecto:

  ```bash
  python -m http.server 8000
  ```

  Y abre `http://localhost:8000/`. En Windows también puedes usar `py -m http.server 8000` si Python está instalado.

## Chatbot: qué funciona y qué requiere terceros

- **Respuestas locales**: funcionan sin API, conexión ni registro, a partir de la información publicada en la propia web. No son un modelo de IA generativa.
- **IA generativa**: botón `Activar IA generativa`. Solicita consentimiento al visitante; luego carga **Puter.js** desde `https://js.puter.com/v2/` y puede requerir autenticación o créditos/tarifas según Puter. Este modo necesita conexión a internet y que la web se abra por HTTP(S). No se almacena ninguna clave de API en el repositorio.
- Las preguntas y la información pública del portfolio se envían a Puter **solo al activar el modo online**. Revisa las condiciones y la política de privacidad del proveedor antes de hacer pública la web.
- No se garantiza disponibilidad continua del proveedor externo ni respuestas correctas al 100 %. Cuando falla el modo online, el chatbot vuelve al modo local.

Documentación externa: [Puter.js - IA de chat](https://docs.puter.com/AI/chat/).

## Actualizar el portfolio

- **Textos, experiencia, competencias, idiomas y contacto:** edita `index.html`.
- **Estilo y colores:** edita `assets/css/styles.css`.
- **Menú y scroll:** edita `assets/js/navigation.js`.
- **Respuestas del chatbot y servicio de IA:** edita `assets/js/chatbot.js`.

## Nota de privacidad

El repositorio y la web serán públicos si publicas con GitHub Pages. Antes de hacerlo, comprueba que quieres mostrar los datos de contacto y el contenido profesional incluidos en la web. No se ha incluido ninguna fotografía ni el CV PDF en este repositorio.
