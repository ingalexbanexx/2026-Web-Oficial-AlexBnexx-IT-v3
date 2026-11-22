# Alexbanexx IT | Sitio Web Oficial — V3

![HTML5](https://img.shields.io/badge/HTML5-semántico-E34F26?logo=html5&logoColor=white)
![SCSS](https://img.shields.io/badge/SCSS-Sass-CC6699?logo=sass&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-7952B3?logo=bootstrap&logoColor=white)
![Estado](https://img.shields.io/badge/estado-en%20desarrollo-00d8f5)

Sitio web oficial y portafolio profesional del **Ing. Marcelo Alejandro Banega (Alexbanexx IT)**. Presenta servicios de consultoría tecnológica, trayectoria, competencias y proyectos de ingeniería en sistemas.

**Repositorio:** https://github.com/ingalexbanexx/2026-Web-Oficial-AlexBnexx-IT-v3

## Objetivo

Desarrollar un sitio web estático, profesional, responsivo y accesible que permita:

- Presentar el perfil técnico, académico y profesional.
- Difundir servicios de ingeniería y consultoría IT.
- Exhibir proyectos y casos de aplicación.
- Facilitar el contacto con instituciones, clientes y reclutadores.
- Consolidar la identidad visual de Alexbanexx IT.

## Páginas del sitio

| Página | Archivo | Contenido |
| --- | --- | --- |
| Inicio | `index.html` | Presentación, especializaciones y contacto |
| Sobre mí | `pages/sobre-mi.html` | Trayectoria, experiencia y formación |
| Servicios | `pages/servicios.html` | Gestión IT, redes, datos, desarrollo, seguridad y capacitación |
| Proyectos | `pages/proyectos.html` | Portafolio y casos destacados |
| Contacto | `pages/contacto.html` | Canales de comunicación y formulario |

La sección de proyectos incluye experiencias como Mesa de Ayuda UNJu Virtual, SISEXPOA y portales institucionales.

## Tecnologías

- **HTML5:** estructura semántica.
- **CSS3 y Sass/SCSS:** diseño y estilos modulares.
- **Bootstrap 5.3.3:** grillas, navegación y componentes responsivos.
- **Bootstrap Icons 1.11.3:** iconografía.
- **AOS 2.3.1:** animaciones al desplazarse.
- **JavaScript:** interacciones de interfaz.
- **Google Fonts:** Orbitron, Plus Jakarta Sans y JetBrains Mono.
- **Node.js y npm:** gestión de la dependencia de desarrollo Sass.

El sitio es estático: no necesita backend ni base de datos para servir sus páginas actuales. Algunas bibliotecas y fuentes se cargan desde CDN.

## Estructura del proyecto

```text
2026-Web-Oficial-AlexBnexx-IT-v3/
├── index.html
├── pages/
│   ├── sobre-mi.html
│   ├── servicios.html
│   ├── proyectos.html
│   └── contacto.html
├── assets/
│   ├── logo.png
│   ├── perfil.png
│   ├── banner-inicio.jpg
│   ├── video-hero.mp4
│   ├── cv-ing-marcelo-banega.pdf
│   └── ... otros recursos
├── scss/
│   ├── main.scss
│   ├── utilities/
│   ├── base/
│   ├── components/
│   └── layout/
├── styles/
│   ├── styles.css
│   └── styles.css.map
├── package.json
├── package-lock.json
└── README.md
```

## Instalación y ejecución local

**Requisitos:** Git, Node.js, npm, un navegador moderno y opcionalmente Visual Studio Code con Live Server.

1. Clonar el repositorio:

```bash
git clone https://github.com/ingalexbanexx/2026-Web-Oficial-AlexBnexx-IT-v3.git
cd 2026-Web-Oficial-AlexBnexx-IT-v3
```

2. Instalar las dependencias:

```bash
npm install
```

3. Abrir `index.html` con la extensión **Live Server** de VS Code, o ejecutar desde la raíz:

```bash
python -m http.server 5500
```

4. Visitar `http://localhost:5500`.

**Nota:** el `package.json` actual no define scripts `dev` ni `build`. No ejecutar `npm run dev` ni `npm run build` sin configurarlos previamente.

## Compilación SCSS

El punto de entrada es `scss/main.scss` y el archivo CSS generado es `styles/styles.css`.

Compilación única:

```bash
npx sass scss/main.scss styles/styles.css
```

Modo observación:

```bash
npx sass --watch scss/main.scss:styles/styles.css
```

La arquitectura Sass utiliza `@use` y separa utilidades, estilos base, componentes y layout.

## Diseño UI/UX

- **Identidad visual:** estética tecnológica oscura.
- **Colores:** fondo `#080d16`, superficies `#0f172a`, cian `#00d8f5` y azul `#2563eb`.
- **Tipografía:** Orbitron, Plus Jakarta Sans y JetBrains Mono.
- **Responsive:** enfoque mobile-first con breakpoints de 576, 768, 992 y 1200 píxeles.
- **Recursos destacados:** tarjetas, carruseles, animaciones y video en el hero (`assets/video-hero.mp4`).
- **SEO:** títulos HTML individuales por página; revisar metadatos, accesibilidad e indexación antes de producción.

## Despliegue en Vercel

1. Ingresar a https://vercel.com y autenticarse con GitHub.
2. Seleccionar **Add New → Project**.
3. Importar el repositorio `2026-Web-Oficial-AlexBnexx-IT-v3`.
4. Configurar:
   - **Framework Preset:** `Other`
   - **Root Directory:** `./`
   - **Build Command:** vacío (sin compilación)
   - **Output Directory:** raíz del proyecto (`.`)
5. Presionar **Deploy**.
6. Comprobar la página principal, las cuatro páginas internas, imágenes, video y estilos.

El CSS compilado ya está en `styles/styles.css`. Si se modifican archivos SCSS, se debe compilar y subir también el CSS resultante.

**URL pública:** pendiente de completar después del despliegue.

## Estado y mejoras recomendadas

- [ ] Agregar `.gitignore` y dejar de versionar `node_modules/`.
- [ ] Integrar el formulario de contacto con un servicio de recepción: actualmente declara `action="#"`.
- [ ] Revisar navegación, enlaces y experiencia móvil.
- [ ] Auditar accesibilidad, rendimiento y SEO.
- [ ] Publicar el sitio en Vercel y registrar su URL.
- [ ] Definir una licencia explícita para el código y los recursos.

## Autor y contacto

**Ing. Marcelo Alejandro Banega**  
**Alexbanexx IT — Consultoría, Ingeniería de Sistemas y Soluciones Tecnológicas**  
Jujuy, Argentina

- **GitHub:** https://github.com/ingalexbanexx
- **LinkedIn:** https://www.linkedin.com/in/ingalejandrobanega
- **CV profesional:** [Ver PDF](assets/cv-ing-marcelo-banega.pdf)
- **Contacto:** [Formulario](pages/contacto.html)

---

© 2026 Alexbanexx IT. Contenidos de autoría propia. Licencia de reutilización del repositorio pendiente de definición.
