<div align="center">

<img src="public/Arfazrll_light.svg" alt="Project Logo" width="80" height="80" />

# Syahril Arfian Almazril — Portafolio Técnico

### Ingeniería de Sistemas de IA, Software Escalable y Arquitecturas de Datos

[![Next.js](https://img.shields.io/badge/Next.js-16.1.6-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2.4-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Three.js](https://img.shields.io/badge/Three.js-0.170-000000?style=for-the-badge&logo=threedotjs&logoColor=white)](https://threejs.org/)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://vercel.com/)

[![Live Demo](https://img.shields.io/badge/Live_Demo-Visit_Portfolio-6366f1?style=for-the-badge)](https://syahrilarfianalmazril.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-Arfazrll-181717?style=for-the-badge&logo=github)](https://github.com/Arfazrll)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/syahril-arfian-almazril)

---

![GitHub last commit](https://img.shields.io/github/last-commit/Arfazrll/PersonalBlog?style=flat-square&color=6366f1)
![GitHub repo size](https://img.shields.io/github/repo-size/Arfazrll/PersonalBlog?style=flat-square&color=a855f7)
![GitHub stars](https://img.shields.io/github/stars/Arfazrll/PersonalBlog?style=flat-square&color=f59e0b)
![License](https://img.shields.io/badge/license-MIT-22c55e?style=flat-square)

</div>

---

## Resumen Ejecutivo

Una aplicación de portafolio de grado de producción, altamente interactiva, diseñada para exhibir experiencia técnica en Inteligencia Artificial, Ciencia de Datos e Ingeniería de Software Moderna. Más allá de la documentación estática tradicional, esta plataforma ofrece una experiencia inmersiva y de alto rendimiento impulsada por simulaciones físicas WebGL, integraciones de datos en tiempo real y un chatbot asistente autónomo de IA.

---

## Arquitectura del Sistema y Tecnologías

El repositorio está construido sobre una arquitectura moderna y desacoplada, diseñada para maximizar el rendimiento, la escalabilidad y la mantenibilidad.

### Framework Central
- **Next.js 16 (App Router):** Aprovecha la renderización del lado del servidor (SSR), la generación de sitios estáticos (SSG) y mecanismos de caché avanzados para una entrega de contenido óptima.
- **React 19 y TypeScript:** Impone seguridad estricta de tipos y paradigmas reactivos modernos a lo largo de más de 50 componentes de interfaz de usuario personalizados.

### Gráficos 3D y Simulación Física
- **Three.js y React Three Fiber (R3F):** Impulsa el motor de renderizado WebGL principal.
- **Rapier Physics:** Integra simulaciones físicas deterministas en tiempo real (por ejemplo, el modelo 3D interactivo de la Credencial y modelos estructurales).
- **Shaders GLSL Personalizados:** Utilizados para elementos de fondo a medida, incluyendo los efectos "Hyperspeed" y curvatura espacio-temporal.

### Coreografía de UI/UX
- **Framer Motion y GSAP:** Controla las coreografías complejas basadas en líneas de tiempo, microinteracciones y transiciones fluidas de página.
- **Tailwind CSS y Shadcn UI:** Proporciona un sistema de diseño escalable y centrado en utilidades, apoyado en las primitivas de accesibilidad robustas de Radix UI.
- **Lenis:** Implementa dinámicas de desplazamiento suave y premium.

### Integraciones de Sistema y APIs
- **Arquitectura de Chatbot IA de Doble LLM:** Integra Groq (LLaMA 3.1) como proveedor principal con soporte automático hacia Google Gemini (1.5 Flash), utilizando generación aumentada por recuperación (RAG) con contexto mapeado directamente desde `portfolio.ts`.
- **Pipelines GraphQL y REST:** Consume la API GraphQL de GitHub para estadísticas de repositorios y la API de WakaTime para telemetría de código en tiempo real.
- **Next-Intl:** Proporciona una experiencia bilingüe completa (Inglés/Indonesio) dirigida por la detección de cabeceras en el navegador del cliente.

---

## Estructura del Proyecto

Este proyecto sigue una estructura modular dentro del directorio `src/` para mantener la escalabilidad y claridad. A continuación se listan y explican los archivos de cada carpeta:

```text
PersonalBlog/
├── src/
│   ├── app/                          # Puntos de entrada para Next.js App Router
│   │   ├── api/                      # Rutas backend (API routes)
│   │   │   └── (Rutas para manejar peticiones de Chatbot, GitHub y WakaTime)
│   │   ├── projects/                 # Rutas de exhibición de proyectos técnicos
│   │   ├── experience/               # Rutas para el historial laboral interactivo
│   │   ├── skills/                   # Visualizaciones tipo radar de habilidades
│   │   ├── resume/                   # Visor de currículum en PDF usando react-pdf
│   │   ├── blog/                     # Motor de renderizado para entradas en Markdown/MDX
│   │   ├── layout.tsx                # Estructura raíz que incluye proveedores (tema, Lenis, i18n)
│   │   └── page.tsx                  # Página de inicio (Hero) combinada con escenas 3D
│   │
│   ├── components/                   # Arquitectura de UI Reutilizable
│   │   ├── three/                    # Componentes WebGL / Three.js
│   │   │   ├── Lanyard.tsx           # Modelo 3D de la credencial física interactiva
│   │   │   ├── Scene3D.tsx           # Configuración base de la escena y cámaras 3D
│   │   │   └── index.ts              # Exportador principal de la carpeta 3D
│   │   │
│   │   ├── sections/                 # Bloques grandes de página
│   │   │   ├── AboutMeHub.tsx        # Sección central "Sobre mí"
│   │   │   ├── AboutSection.tsx      # Detalles completos de biografía personal
│   │   │   ├── CTASection.tsx        # Botones y llamadas a la acción en el pie
│   │   │   ├── CertificateHeroScroll.tsx # Animación al hacer scroll de los certificados
│   │   │   ├── ExperienceMarquee.tsx # Carrusel infinito del historial laboral
│   │   │   ├── ExperienceStickyScroll.tsx # Sección interactiva que fija los años de experiencia
│   │   │   ├── ExperienceTabsSection.tsx  # Pestañas para navegar por cargos y roles
│   │   │   ├── ExpertiseSection.tsx  # Grid para mostrar principales áreas de conocimiento
│   │   │   ├── HeroVisual.tsx        # Pantalla visual inicial (banner) de alto impacto
│   │   │   ├── IdentitySequence.tsx  # Animaciones secuenciales para presentarse
│   │   │   ├── InnovativeExperienceHero.tsx # Encabezado para la página de experiencia
│   │   │   ├── NavigationShortcuts.tsx # Accesos rápidos de navegación para teclado o UI
│   │   │   ├── ProjectContact.tsx    # Sección de contacto insertada en los proyectos
│   │   │   ├── ProjectStats.tsx      # Muestra de métricas (horas, commits, tecnologías)
│   │   │   ├── SmoothScrollHero.tsx  # Cabecera que interactúa suavemente con Lenis
│   │   │   ├── StatsSection.tsx      # Paneles numéricos estadísticos del portafolio
│   │   │   └── (Carpetas internas: blog/, gallery/, skills/ con secciones específicas)
│   │   │
│   │   ├── effects/                  # Efectos visuales de interfaz y gráficos interactivos
│   │   │   ├── ClickSpark.tsx        # Efecto de chispas o destello al hacer clic
│   │   │   ├── DesignTestimonials.tsx # Carrusel de testimonios dinámicos
│   │   │   ├── ImageTrail.tsx        # Efecto de rastro de imágenes al mover el mouse
│   │   │   ├── InfiniteMenu.tsx      # Menú de navegación que gira en bucle
│   │   │   ├── ScrollReveal.tsx      # Efectos declarativos para hacer aparecer contenido con scroll
│   │   │   └── globe-demo.tsx        # Componente que renderiza el globo terráqueo en 3D
│   │   │
│   │   └── ui/                       # +100 Componentes Shadcn, Magic UI, Aceternity (Base)
│   │       ├── CardNav.tsx, CircularGallery.tsx, 3d-folder.tsx # Navegadores y galerías interactivas
│   │       ├── Hyperspeed.tsx, FlickeringGrid.tsx, Particles.tsx # Fondos y rejillas animadas
│   │       ├── button.tsx, input.tsx, popover.tsx, select.tsx # Primitivas interactivas (Botones, formularios)
│   │       ├── terminal.tsx, pdf-viewer.tsx, wakatime-showcase.tsx # Visores de datos integrados
│   │       └── text-generate-effect.tsx, hover-scramble-text.tsx # Efectos en tipografías
│   │
│   ├── data/                         # Almacenamiento central de datos
│   │   └── portfolio.ts              # Toda la información del portafolio (Proyectos, experiencias, JSON estático)
│   │
│   ├── hooks/                        # Hooks personalizados de React
│   │   ├── usePerformance.ts         # Hook que ajusta gráficos según FPS y dispositivo del cliente
│   │   ├── useScrollAnimation.ts     # Controlador para conectar GSAP con triggers de scroll
│   │   ├── useTypewriter.ts          # Hook para efecto de escritura por teclado automático
│   │   ├── useTextScramble.ts        # Hook para animar texto descifrándose
│   │   ├── useIsMobile.ts / use-mobile.tsx # Hook para reaccionar a vistas de móviles (Responsivo)
│   │   └── useCountUp.ts             # Anima números progresivamente al hacer scroll
│   │
│   ├── i18n/                         # Configuración de Internacionalización (next-intl)
│   │   ├── i18n.ts                   # Inicializador y motor de traducciones EN/ID
│   │   ├── get-strict-context.tsx    # Tipado fuerte para el contexto de idioma
│   │   └── utils.ts                  # Funciones de ayuda para cambiar de idioma
│   │
│   ├── lib/                          # Utilidades generales del código
│   │   └── (Archivos para combinar clases CSS condicionales, etc.)
│   │
│   ├── providers/                    # Proveedores de Contexto global (Context Providers)
│   │   ├── I18nProvider.tsx          # Envuelve la app para distribuir las traducciones
│   │   ├── SmoothScrollProvider.tsx  # Inyecta Lenis para desplazamiento fluido global
│   │   ├── ThemeProvider.tsx         # Gestiona Modo Oscuro / Claro usando next-themes
│   │   └── index.ts                  # Agrupa los proveedores
│   │
│   ├── styles/                       # CSS global
│   │   └── globals.css               # Variables del sistema de diseño, Tailwind y keyframes complejos
│   │
│   └── types/                        # Definiciones de tipo para TypeScript
│       ├── global.d.ts               # Declaraciones de tipos globales del sistema
│       ├── three-types.d.ts          # Declaraciones de extensiones propias para React Three Fiber
│       ├── index.ts                  # Exportación unificada de interfaces TypeScript
│       ├── aos.d.ts                  # Tipado de la librería de animación de scroll (AOS)
│       └── spline-viewer.d.ts        # Declaraciones de módulos para cargar los modelos de Spline
│
├── public/                           # Activos estáticos (Modelos 3D, íconos SVG, el CV en PDF)
├── next.config.ts                    # Archivo de configuración, compilación, y reglas de Next.js
├── tailwind.config.ts                # Diseño, paleta de colores a la medida, y sistema UI para Tailwind
└── package.json                      # Dependencias del proyecto y scripts NPM (dev, build, start)
```

---

## Características Principales

### 1. Entornos 3D Interactivos
Implementa modelos 3D acelerados por hardware usando `@react-three/drei` y `@react-three/fiber`. Las funciones incluyen una tarjeta de identificación simulada físicamente que responde a la velocidad del cursor y a los límites de la ventana en tiempo real.

### 2. Chatbot Autónomo del Portafolio
Un agente conversacional inteligente desplegado vía la ruta `/api/chat`. El sistema construye una ventana de contexto dinámico a partir de la base de datos estática `portfolio.ts` y procesa consultas de lenguaje natural usando una infraestructura redundante de Dos LLMs.

### 3. Telemetría en Tiempo Real
Los paneles de control en toda la plataforma recuperan y muestran métricas de ingeniería en tiempo real, utilizando solicitudes GraphQL autenticadas a GitHub (mapas de calor de actividad, desglose de lenguajes) y WakaTime (horas de programación, preferencias de IDE).

### 4. Visor de Documentos PDF Interactivo
Un motor de renderizado de documentos construido a medida utilizando `react-pdf`, que permite a los usuarios hacer zoom, rotar, buscar y descargar el currículum nativamente dentro de la aplicación del navegador sin depender de complementos externos.

### 5. Diagnósticos de Rendimiento
La aplicación implementa un hook `usePerformance` para evaluar las capacidades de hardware del cliente en tiempo real, desactivando automáticamente los shaders WebGL intensivos y las complejas animaciones GSAP en dispositivos móviles o de baja potencia para preservar la batería y mantener los FPS estables.

---

## Librerías y Tecnologías Instaladas

El proyecto utiliza varias librerías clave para lograr su experiencia interactiva de alto rendimiento:

### Frameworks Centrales
- **[Next.js](https://nextjs.org/)**: El framework de React para SSR, App Router y rutas API.
- **[React 19](https://react.dev/)**: Librería para construir interfaces de usuario.
- **[TypeScript](https://www.typescriptlang.org/)**: Garantiza la seguridad estricta de los tipos en todo el código fuente.

### Renderizado de Gráficos y 3D
- **[Three.js](https://threejs.org/)**: Motor WebGL principal para renderizado 3D.
- **[@react-three/fiber](https://docs.pmnd.rs/react-three-fiber/)**: Renderizador de React para Three.js, construyendo escenas de manera declarativa.
- **[@react-three/drei](https://github.com/pmndrs/drei)**: Ayudantes útiles y abstracciones para React Three Fiber.
- **[@react-three/postprocessing](https://github.com/pmndrs/react-postprocessing)**: Efectos avanzados de post-procesamiento (bloom, desenfoque, aberración cromática).
- **[@react-three/rapier](https://github.com/pmndrs/react-three-rapier)**: Motor de física 3D para interacciones (por ejemplo, el movimiento realista de la cinta de la credencial).
- **[@splinetool/react-spline](https://spline.design/)**: Renderiza escenas 3D de Spline directamente en React.
- **[three-globe](https://github.com/vasturiano/three-globe)**: Librería especializada en renderizar globos terráqueos interactivos en 3D.

### Animación y Micro-Interacciones
- **[Framer Motion](https://www.framer.com/motion/)**: Base de poder para animaciones de interfaz complejas basadas en físicas de resortes (springs).
- **[GSAP](https://gsap.com/)**: Librería de animación de JavaScript de alto rendimiento utilizada para la secuenciación en líneas de tiempo.
- **[Lenis](https://lenis.studiofreight.com/)**: Motor de desplazamiento (scroll) suave de última generación.
- **[AOS (Animate On Scroll)](https://michalsnik.github.io/aos/)**: Animaciones declarativas de elementos disparadas por el scroll.
- **[tsparticles](https://particles.js.org/)**: Crea fondos interactivos ligeros con sistemas de partículas.

### Arquitectura UI y Sistema de Diseño
- **[Tailwind CSS](https://tailwindcss.com/)**: Framework de estilo enfocado en utilidades con tokens de diseño personalizados.
- **[Radix UI](https://www.radix-ui.com/)**: Componentes accesibles sin estilo (`headless`) usados como base para las primitivas personalizadas de Shadcn UI (`@radix-ui/react-*`).
- **[clsx](https://github.com/lukeed/clsx) y [tailwind-merge](https://github.com/dcastil/tailwind-merge)**: Utilidades para combinar dinámicamente clases CSS de Tailwind de forma condicional.
- **[class-variance-authority (cva)](https://cva.style/)**: Define variantes de componentes para un sistema de diseño robusto.
- **[@base-ui/react](https://base-ui.com/) / [@headlessui/react](https://headlessui.com/)**: Componentes accesibles sin estilo para construir sistemas de diseño a la medida.

### Iconografía
- **[lucide-react](https://lucide.dev/)**: Biblioteca de iconos principal para glifos de interfaz limpios y consistentes.
- **[@phosphor-icons/react](https://phosphoricons.com/)**: Familia secundaria de iconos geométricos.
- **[@hugeicons/react](https://hugeicons.com/)**: Iconos de líneas detallados de tipo premium.
- **[react-icons](https://react-icons.github.io/react-icons/)**: Agregador de iconos de propósito general.

### Utilidades de Datos e Integraciones
- **[next-intl](https://next-intl-docs.vercel.app/)**: Gestión robusta del diccionario de traducción y enrutamiento de internacionalización.
- **[react-pdf](https://projects.wojtekmaj.pl/react-pdf/)**: Renderizado nativo de PDF mediante WebAssembly para el visor de currículum.
- **[shiki](https://shiki.style/)**: Resaltado de sintaxis hermoso y preciso para fragmentos de código en proyectos/blogs.
- **[nodemailer](https://nodemailer.com/)**: Cliente SMTP para el manejo de los correos del formulario de "Contáctame".
- **[date-fns](https://date-fns.org/)**: Librería moderna de utilidades de fechas en JavaScript.
- **[react-github-calendar](https://github.com/grubersjoe/react-github-calendar)**: Componente utilizado para renderizar el mapa de calor de contribuciones de GitHub.

---

## Configuración para Desarrollo Local

### Requisitos previos
- Node.js >= 18.0.0
- npm >= 9.0.0

### Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/Arfazrll/PersonalBlog.git
   cd PersonalBlog
   ```

2. **Instalar dependencias:**
   ```bash
   npm install
   ```

3. **Configurar las Variables de Entorno:**
   Crea un archivo `.env.local` en el directorio raíz.

   ```env
   NEXT_PUBLIC_GITHUB_USERNAME=your_username
   GITHUB_TOKEN=your_personal_access_token
   WAKATIME_API_KEY=your_wakatime_key
   GROQ_API_KEY=your_groq_key
   GEMINI_API_KEY=your_gemini_key
   ```

4. **Inicializar el Servidor de Desarrollo:**
   ```bash
   npm run dev
   ```
   Navega a `http://localhost:3000` para interactuar con la aplicación.

### Construcción para Producción
Ejecuta lo siguiente para compilar y servir el paquete optimizado de la aplicación:
```bash
npm run build
npm start
```

---

## Resumen del Showcase de Proyectos

La plataforma documenta actualmente **más de 19 proyectos técnicos** que abarcan múltiples disciplinas de ingeniería:

| Disciplina | Proyectos Destacados | Tecnologías Principales |
|------------|------------------|-------------------|
| **Inteligencia Artificial** | Motor DocsInsight, NeuroVision, Reconocimiento de Gestos Manuales | Python, TensorFlow, OpenCV, LangChain |
| **Ciencia de Datos y Analíticas** | Análisis de Riesgo Crediticio, Análisis de Sentimientos MyTelkomsel, Dashboard de Analista de Datos | Python, LSTM, Pandas, Plotly |
| **Ingeniería de Software** | Donasiaku, SaaS POLABDC, Digilibzx | Laravel, Next.js, Go, PostgreSQL, Prisma |
| **IoT y Sistemas Embebidos** | Plataforma TerraFlow, Detección Inteligente de Movimiento | ESP32, Raspberry Pi, MQTT, C++ |

---

## Licencia

Este proyecto está licenciado bajo la [Licencia MIT](LICENSE).

<div align="center">
  <p>Ingeniería por Syahril Arfian Almazril</p>
</div>
