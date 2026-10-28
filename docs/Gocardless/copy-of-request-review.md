---
title: Copia de solicitud de revisión
deprecated: false
hidden: true
icon: fad fa-rocket-launch
metadata:
  robots: index
---
<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Plataforma ReadMe — Desglose de criterios</title>
<style>
  :root {
    --bg: #f9f8f6;
    --bg-card: #ffffff;
    --text-primary: #1a1a18;
    --text-secondary: #5c5c57;
    --text-tertiary: #9c9a92;
    --border: rgba(0,0,0,0.1);
    --border-strong: rgba(0,0,0,0.18);
    --green-bg: #eaf3de;
    --green-text: #3b6d11;
    --amber-bg: #faeeda;
    --amber-text: #854f0b;
    --red-bg: #fcebeb;
    --red-text: #a32d2d;
    --radius-md: 8px;
    --radius-lg: 12px;
  }
  @media (prefers-color-scheme: dark) {
    :root {
      --bg: #1c1c1a;
      --bg-card: #252523;
      --text-primary: #e8e6de;
      --text-secondary: #b0ae a6;
      --text-tertiary: #6e6c65;
      --border: rgba(255,255,255,0.08);
      --border-strong: rgba(255,255,255,0.14);
      --green-bg: #173404;
      --green-text: #97c459;
      --amber-bg: #412402;
      --amber-text: #ef9f27;
      --red-bg: #501313;
      --red-text: #f09595;
    }
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'DM Sans', 'Helvetica Neue', Arial, sans-serif;
    background: var(--bg);
    color: var(--text-primary);
    padding: 2.5rem 2rem;
    max-width: 960px;
    margin: 0 auto;
    line-height: 1.6;
  }
  header { margin-bottom: 2rem; }
  h1 { font-size: 22px; font-weight: 600; margin-bottom: 4px; }
  .subtitle { font-size: 14px; color: var(--text-secondary); }
  .legend {
    display: flex; gap: 20px; margin-bottom: 1.5rem; flex-wrap: wrap;
    font-size: 12px; color: var(--text-secondary);
  }
  .legend span { display: flex; align-items: center; gap: 6px; }
  .legend-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }
  .section-label {
    font-size: 11px; font-weight: 600; color: var(--text-tertiary);
    text-transform: uppercase; letter-spacing: 0.07em;
    margin: 2rem 0 0.75rem;
  }
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 12px;
  }
  .card {
    background: var(--bg-card);
    border: 0.5px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 1rem 1.25rem;
  }
  .card-header {
    display: flex; align-items: flex-start;
    justify-content: space-between; gap: 10px; margin-bottom: 8px;
  }
  .card-title { font-size: 13px; font-weight: 600; color: var(--text-primary); }
  .badge {
    font-size: 11px; font-weight: 600; padding: 3px 9px;
    border-radius: 20px; white-space: nowrap; flex-shrink: 0;
  }
  .badge-yes  { background: var(--green-bg); color: var(--green-text); }
  .badge-partial { background: var(--amber-bg); color: var(--amber-text); }
  .badge-no   { background: var(--red-bg); color: var(--red-text); }
  .card-body  { font-size: 12px; color: var(--text-secondary); line-height: 1.65; }
  .card-detail {
    font-size: 11px; color: var(--text-tertiary);
    margin-top: 8px; padding-top: 8px;
    border-top: 0.5px solid var(--border);
    font-style: italic;
  }
  footer {
    margin-top: 2.5rem;
    font-size: 11px;
    color: var(--text-tertiary);
    border-top: 0.5px solid var(--border);
    padding-top: 1rem;
  }
</style>
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&display=swap" rel="stylesheet">
</head>
<body>

<header>
  <h1>ReadMe — Desglose de criterios de la plataforma</h1>
  <p class="subtitle">Evaluación de ReadMe frente a los requisitos de la plataforma de documentación</p>
</header>

<div class="legend">
  <span><span class="legend-dot" style="background:#3b6d11"></span>Nativo / encaje óptimo</span>
  <span><span class="legend-dot" style="background:#854f0b"></span>Parcial / con configuración</span>
  <span><span class="legend-dot" style="background:#a32d2d"></span>Carencia / requiere solución alternativa</span>
</div>

<!-- Core platform -->
<div class="section-label">Plataforma de documentación principal</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Referencia de API como código</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Especificación OpenAPI como única fuente de verdad: ReadMe genera la referencia de la API directamente a partir de su especificación y se actualiza automáticamente ante cambios en el esquema. Se puede subir manualmente, mediante API o a través de una canalización de CI/CD.</div>
    <div class="card-detail">Compatible con OAS 3.x. Utilice la CLI rdme para la sincronización de especificaciones en GitHub Actions.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Muestras de código en varios lenguajes</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Muestras de código generadas automáticamente a partir de la especificación OpenAPI en más de 10 lenguajes. Se pueden agregar muestras personalizadas por endpoint. Selector de lenguaje integrado en la interfaz de usuario de referencia.</div>
    <div class="card-detail">No requiere mantenimiento manual si proviene de extensiones de especificación (x-readme).</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Try-it / sandbox interactivo</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Explorador de API "Try It!" integrado en cada endpoint. Admite autenticación previa con claves de API específicas de cada usuario para integradores mediante la integración JWT/OAuth de ReadMe.</div>
    <div class="card-detail">Enterprise: variables personalizadas que se completan a partir del contexto de inicio de sesión del usuario.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Registro de cambios como contenido</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Sección de registro de cambios de primer nivel con control de versiones y suscripción RSS. Permite vincular entradas del registro de cambios desde las páginas de referencia de la API. Se puede redactar en Markdown o mediante la API.</div>
    <div class="card-detail">La vinculación automática desde la referencia requiere enlaces cruzados manuales; no es totalmente automática.</div>
  </div>
</div>

<!-- Search -->
<div class="section-label">Búsqueda &amp; detectabilidad</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Búsqueda mejorada</span>
      <span class="badge badge-partial">Parcial</span>
    </div>
    <div class="card-body">ReadMe cuenta con búsqueda de texto completo integrada. La búsqueda semántica y el seguimiento de vacíos sin resultados no son nativos; el seguimiento de vacíos está disponible mediante el informe de análisis Search Queries, pero no se marca automáticamente.</div>
    <div class="card-detail">Las analíticas de búsqueda muestran lo que los usuarios buscaron sin obtener resultados. La clasificación semántica no es configurable actualmente.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Arquitectura de información detectable</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Navegación jerárquica con categorías, subcategorías y orden personalizado. Admite múltiples versiones de documentación y navegación según la audiencia. La arquitectura de información se gestiona en el panel de control o mediante la API de Guides.</div>
    <div class="card-detail">La navegación personalizada por tipo de integración requiere JS personalizado o bloques de contenido dinámico.</div>
  </div>
</div>

<!-- AI -->
<div class="section-label">IA &amp; herramientas modernas</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Nativo para IA / legible por LLM</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Pila completa nativa para IA: LLMs.txt generado automáticamente con un solo interruptor (todos los planes, sin mantenimiento). Dos servidores MCP nativos: uno para que los autores de la documentación la gestionen mediante IA y otro para que los usuarios de la API brinden a sus herramientas de IA acceso en vivo a su especificación y documentos. Las páginas de ReadMe generan HTML limpio y exponen un sitemap público rastreable por LLM. llms.txt nativo es compatible y genera automáticamente un archivo de configuración en la raíz de su sitio de documentación según la estructura existente de sus documentos.</div>
    <div class="card-detail">LLMs.txt está disponible en todos los planes. Los servidores MCP están integrados de forma nativa, no como una integración personalizada.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Personalización</span>
      <span class="badge badge-partial">Parcial</span>
    </div>
    <div class="card-body">ReadMe admite variables de usuario (p. ej., claves de API precompletadas, nombre de la empresa) mediante JWT SSO. La ramificación de contenido según esquema, país o método de integración no es nativa; requiere lógica personalizada o versiones independientes de la documentación.</div>
    <div class="card-detail">La inyección de variables en el plan Enterprise es potente para el contexto de autenticación; los bloques de contenido condicional son limitados.</div>
  </div>
</div>

<!-- Performance -->
<div class="section-label">Rendimiento &amp; gobernanza</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">SSR / carga rápida de página</span>
      <span class="badge badge-partial">Parcial</span>
    </div>
    <div class="card-body">La plataforma alojada de ReadMe utiliza SSR. El TTFB y las Core Web Vitals son generalmente buenos en el tema predeterminado, pero usted no controla la infraestructura directamente; los SLA de TTFB inferiores a 100 ms no están garantizados ni disponibles por contrato.</div>
    <div class="card-detail">Se admiten dominios personalizados y CDN. La optimización del rendimiento es limitada en comparación con las soluciones autohospedadas.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Gobernanza del contenido</span>
      <span class="badge badge-partial">Parcial</span>
    </div>
    <div class="card-body">La sincronización bidireccional con GitHub permite a los equipos usar PR para revisiones de documentación. La comprobación de enlaces rotos y el linting no son nativos; necesitaría un paso de CI en el sitio en vivo o sobre el contenido exportado.</div>
    <div class="card-detail">GitHub Sync está disponible en los planes Business y Enterprise. Las herramientas de control de calidad (quality gates) son una carencia.</div>
  </div>
</div>

<!-- Analytics -->
<div class="section-label">Analítica &amp; feedback</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Ciclos de retroalimentación de desarrolladores</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Las valoraciones por página (pulgar arriba/abajo) están integradas. El CSAT de desarrolladores se muestra en el panel de Metrics. Se pueden habilitar comentarios por página para recibir retroalimentación directa.</div>
    <div class="card-detail">Las valoraciones se consolidan en el panel de analíticas, con filtros por página, versión y rango de tiempo.</div>
  </div>
  <div class="card">
    <div class="card-header">
      <span class="card-title">Analítica de contenido</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">ReadMe Metrics realiza un seguimiento de las visitas a páginas, el tiempo en página, las consultas de búsqueda y las tasas de salida. Las analíticas de llamadas a la API también están disponibles al utilizar el registro de API de ReadMe.</div>
    <div class="card-detail">Dispone de un análisis completo de vacíos de búsqueda. El envío de datos a herramientas externas requiere la API de Metrics o un webhook.</div>
  </div>
</div>

<!-- Workflow -->
<div class="section-label">Flujo de trabajo &amp; edición</div>
<div class="grid">
  <div class="card">
    <div class="card-header">
      <span class="card-title">Fácil de actualizar</span>
      <span class="badge badge-yes">Nativo</span>
    </div>
    <div class="card-body">Editor WYSIWYG para perfiles no técnicos, Markdown/MDX para ingenieros, además de GitHub Sync para equipos orientados al código. Barrera de entrada baja para ambos públicos: no se requiere ningún paso de compilación para ediciones exclusivas de contenido.</div>
    <div class="card-detail">Los ingenieros también pueden utilizar la API de Guides o la CLI para actualizaciones masivas y automatización.</div>
  </div>
</div>

<footer>Generado a partir de la evaluación de la plataforma ReadMe · readme_criteria_breakdown</footer>

</body>
</html>
`}</HTMLBlock>

Así es como se puede analizar el panorama completo:

Aspectos en los que ReadMe encaja a la perfección:

- El núcleo de lo que busca es exactamente para lo que se diseñó ReadMe. La referencia sincronizada con OpenAPI, los ejemplos de código en múltiples lenguajes, el sandbox Try It, el registro de cambios, las valoraciones de páginas y la analítica de contenido son funciones de primer nivel. La combinación de WYSIWYG + GitHub Sync responde directamente al requisito de "fácil de actualizar para ingenieros y perfiles no técnicos".
- Indexación nativa para IA / MCP: ReadMe cubre ambas facetas del ecosistema MCP:
  El servidor MCP para autores permite a su equipo consultar, leer y actualizar la documentación a través de herramientas de IA, lo que resulta útil para los flujos de trabajo de contenido, las ediciones masivas y la redacción asistida por IA directamente sobre sus documentos publicados.
  El servidor MCP orientado al usuario es el más relevante estratégicamente para esta evaluación: proporciona a las herramientas de IA de los usuarios de su API (Cursor, Claude, Windsurf, etc.) acceso en vivo a su especificación y documentación como contexto mientras programan. Eso es exactamente lo que exigía el criterio "indexado por MCP" en los requisitos originales.
  De hecho, esto hace que la propuesta nativa para IA de ReadMe sea más sólida de lo que evalué inicialmente, y más fuerte que la ofrecida por muchos competidores. El único matiz restante en esa ficha sería si llms.txt se genera de forma nativa, pero la parte de MCP está claramente cubierta. Vale la pena actualizar el artefacto si lo va a compartir.

Aspectos en los que es parcial y qué hacer al respecto:

- Búsqueda semántica: la búsqueda actual se basa en palabras clave. El seguimiento de consultas sin resultados está disponible en las analíticas (puede ver qué búsquedas no arrojaron resultados), pero no se presenta automáticamente como una lista de tareas pendientes para la creación de contenido. Si la búsqueda semántica es un criterio imprescindible, esta es la mayor carencia frente a alternativas como Mintlify o una integración personalizada con Algolia.
- Garantía de TTFB inferior a 100 ms: el rendimiento de SSR en ReadMe suele ser sólido, pero depende de su infraestructura y no es posible exigir un SLA de TTFB por contrato. Si este es un requisito estricto, las soluciones autohospedadas (Mintlify, Docusaurus + Vercel) ofrecen un mayor control.
- Gobernanza del contenido / controles de calidad (quality gates): GitHub Sync gestiona adecuadamente la parte de revisión mediante PR, pero la verificación de enlaces rotos y el linting deben añadirse en CI (p. ej., broken-link-checker contra la URL de staging en cada PR). ReadMe no aplica esto de forma nativa.
- Personalización por esquema/país/método de integración: la inyección de variables de usuario (claves de API, nombre de la empresa) es excelente. La ramificación condicional real del contenido según el tipo de integración no es nativa y requeriría árboles de documentación versionados independientes o bloques de JS personalizados.
- En cuanto al dilema de desarrollar vs. comprar vs. código abierto: ReadMe se sitúa de lleno en la columna de "comprar", con una sólida propuesta de plataforma gestionada. Si los SLA estrictos de rendimiento, las capacidades nativas avanzadas de IA/MCP o el contenido condicional complejo son requisitos imprescindibles, vale la pena comparar directamente con Mintlify (propuesta nativa de IA más sólida, mayor flexibilidad de configuración) y Docusaurus + Vercel (control total, mayor esfuerzo de ingeniería). Con gusto realizaré una comparación directa con cualquiera de ellos si resulta de utilidad.
