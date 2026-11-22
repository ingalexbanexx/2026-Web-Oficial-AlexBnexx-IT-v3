# Alexbanexx IT | Sitio Web Oficial — v3

![Estado](https://img.shields.io/badge/estado-en%20desarrollo-00d8f5)
![HTML5](https://img.shields.io/badge/HTML5-sem%C3%A1ntico-E34F26?logo=html5&logoColor=white)
![SCSS](https://img.shields.io/badge/SCSS-Sass-CC6699?logo=sass&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-7952B3?logo=bootstrap&logoColor=white)
![Licencia](https://img.shields.io/badge/licencia-por%20definir-lightgrey)

Sitio web institucional y portafolio profesional del **Ing. Marcelo Alejandro Banega (Alexbanexx IT)**, orientado a la presentación de servicios de consultoría tecnológica, trayectoria, competencias y proyectos de ingeniería en sistemas.

> **Repositorio:** [2026-Web-Oficial-AlexBnexx-IT-v3](https://github.com/ingalexbanexx/2026-Web-Oficial-AlexBnexx-IT-v3) · **Rama principal:** `main`

## Índice

1. [Objetivo](#objetivo)
2. [Secciones](#secciones)
3. [Tecnologías](#tecnologías)
4. [Estructura del proyecto](#estructura-del-proyecto)
5. [Instalación y ejecución local](#instalación-y-ejecución-local)
6. [Compilación de estilos SCSS](#compilación-de-estilos-scss)
7. [Diseño y experiencia de usuario](#diseño-y-experiencia-de-usuario)
8. [Despliegue](#despliegue)
9. [Estado y próximos pasos](#estado-y-próximos-pasos)
10. [Autor y contacto](#autor-y-contacto)

## Objetivo

Desarrollar un sitio web estático, profesional y adaptable a distintos dispositivos, que permita:

- Presentar el perfil técnico, académico y profesional.
- Difundir áreas de especialización y servicios de ingeniería IT.
- Exhibir proyectos, implementaciones y casos de aplicación.
- Facilitar el contacto con potenciales clientes, instituciones y reclutadores.
- Consolidar la identidad visual de **Alexbanexx IT**.

El sitio está organizado en **cinco páginas HTML** y utiliza una arquitectura de estilos **SCSS modular**.

## Secciones

| Página | Archivo | Contenido |
| --- | --- | --- |
| Inicio | `index.html` | Presentación, servicios destacados, especializaciones y contacto |
| Sobre mí | `pages/sobre-mi.html` | Experiencia, formación académica y especializaciones |
| Servicios | `pages/servicios.html` | Gestión IT, redes, bases de datos, desarrollo, seguridad y capacitación |
| Proyectos | `pages/proyectos.html` | Portafolio de soluciones y casos destacados |
| Contacto | `pages/contacto.html` | Canales de comunicación y formulario de consulta |

La sección de proyectos incluye referencias a experiencias como la **Mesa de Ayuda UNJu Virtual**, **SISEXPOA**, portales institucionales y otros desarrollos.

## Tecnologías

| Tecnología | Aplicación |
| --- | --- |
| HTML5 | Estructura y contenido semántico de las páginas |
| CSS3 | Presentación visual y diseño adaptable |
| Sass / SCSS | Organización modular, variables, mixins y estilos reutilizables |
| Bootstrap 5.3.3 | Componentes, grillas y navegación responsive |
| Bootstrap Icons 1.11.3 | Iconografía |
| AOS 2.3.1 | Animaciones durante el desplazamiento |
| JavaScript | Interacciones de interfaz |
| Google Fonts | Orbitron, Plus Jakarta Sans y JetBrains Mono |
| Node.js y npm | Gestión local de la dependencia Sass |

**Arquitectura:** sitio estático multipágina; no necesita backend ni base de datos para servir las páginas actuales. Bootstrap, AOS, iconos y fuentes se obtienen de servicios externos CDN.

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
│   └── ...                 # Otras imágenes y recursos multimedia
├── scss/
│   ├── main.scss
│   ├── utilities/          # Variables, mixins y placeholders
│   ├── base/               # Reset, estilos base y tipografía
│   ├── components/         # Botones, tarjetas, carrusel, formularios, etc.
│   └── layout/             # Header, hero, navegación, secciones, footer, etc.
├── styles/
│   ├── styles.css
│   └── styles.css.map
├── package.json
└── package-lock.json
```

> Nota: `node_modules/` también se encuentra actualmente en el repositorio; se recomienda excluirlo del control de versiones mediante `.gitignore`.

## Instalación y ejecución local

**Requisitos:** Git, Node.js y npm para trabajar con Sass; un navegador moderno y, opcionalmente, Visual Studio Code con la extensión *Live Server*.

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/ingalexbanexx/2026-Web-Oficial-AlexBnexx-IT-v3.git
   cd 2026-Web-Oficial-AlexBnexx-IT-v3
   ```

2. Instalar las dependencias locales:

   ```bash
   npm install
   ```

3. Abrir `index.html` con un servidor estático local. Por ejemplo, desde VS Code: **Open with Live Server**. Como alternativa, si tenés Python instalado:

   ```bash
   python -m http.server 5500
   ```

4. Acceder a [http://localhost:5500](http://localhost:5500) si usás el servidor de Python.

> No se utiliza un framework SPA ni un servidor de aplicación. El archivo `package.json` actual no incluye scripts `dev` o `build`: no ejecutar `npm run dev` o `npm run build` sin configurarlos antes.

## Compilación de estilos SCSS

Los estilos se mantienen en archivos partials agrupados por responsabilidad. El punto de entrada es `scss/main.scss` y el CSS compilado se escribe en `styles/styles.css`.

**Compilación única:**

```bash
npx sass scss/main.scss styles/styles.css
```

**Modo observación (desarrollo):**

```bash
npx sass --watch scss/main.scss:styles/styles.css
```

La arquitectura SCSS utiliza `@use` para organizar las dependencias por capas: utilidades, base, componentes y layout.

## Diseño y experiencia de usuario

- **Enfoque visual:** tecnología, profesionalismo y estética oscura.
- **Paleta principal:** fondo `#080d16`, superficies `#0f172a`, acento cian `#00d8f5` y azul complementario `#2563eb`.
- **Tipografía:** Orbitron para títulos, Plus Jakarta Sans para textos y JetBrains Mono para elementos técnicos.
- **Responsividad:** estilos mobile-first con puntos de quiebre de 576, 768, 992 y 1200 píxeles.
- **Elementos destacados:** cabecera adaptable, tarjetas, carruseles, animaciones y video de presentación en el hero (`assets/video-hero.mp4`).
- **SEO:** cada página tiene su propio título HTML. Se recomienda validar además metadatos, accesibilidad, enlaces e indexación antes de publicar.

## Despliegue

Al tratarse de un sitio estático, puede alojarse en **Netlify, Vercel, GitHub Pages** o un servidor web convencional.

Para desplegar los archivos existentes, conservar la estructura de carpetas y publicar la raíz del repositorio como directorio del sitio. El CSS ya compilado se encuentra en `styles/styles.css`; al modificar SCSS, compilarlo antes de subir los cambios.

En **Netlify** o **Vercel**, si se publica directamente el contenido estático existente, no hace falta un comando de construcción; utilizar la raíz del repositorio como carpeta de publicación según la configuración del proveedor.

> **URL pública:** agregar aquí la dirección definitiva cuando el despliegue esté confirmado.

## Estado y próximos pasos

El repositorio incluye las cinco páginas HTML, recursos multimedia, SCSS y el CSS compilado. Para fortalecer su mantenimiento y publicación se recomienda:

- [ ] Agregar `.gitignore` y dejar de versionar `node_modules/` sin borrar la carpeta local.
- [ ] Verificar el funcionamiento real del formulario de contacto: actualmente declara `action="#"`, por lo que no hay un servicio de recepción configurado en el marcado.
- [ ] Validar navegación, enlaces externos y presentación en móviles.
- [ ] Ejecutar auditorías de accesibilidad, rendimiento y SEO.
- [ ] Configurar un despliegue público y agregar su URL a este documento.
- [ ] Definir una licencia explícita para el código y los recursos.

## Autor y contacto

**Ing. Marcelo Alejandro Banega**  
**Alexbanexx IT — Consultoría, Ingeniería de Sistemas y Soluciones Tecnológicas**  
Jujuy, Argentina

- **GitHub:** [@ingalexbanexx](https://github.com/ingalexbanexx)
- **LinkedIn:** [Ing. Alejandro Banega](https://www.linkedin.com/in/ingalejandrobanega)
- **CV profesional:** [Descargar PDF](assets/cv-ing-marcelo-banega.pdf)
- **Formulario de contacto:** [Contacto](pages/contacto.html)

---

© 2026 Alexbanexx IT. Todos los derechos reservados sobre contenidos de autoría propia, salvo que se indique lo contrario. **La licencia de reutilización del repositorio está pendiente de definición.**
