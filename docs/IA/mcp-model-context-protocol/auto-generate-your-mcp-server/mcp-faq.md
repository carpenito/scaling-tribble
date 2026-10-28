---
title: Preguntas frecuentes sobre MCP
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

Estas preguntas frecuentes responden a dudas habituales sobre el uso de [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) con proyectos de ReadMe.

## General {#general}

### ¿Qué es el Model Context Protocol (MCP)? {#what-is-the-model-context-protocol-mcp}

El Model Context Protocol (MCP) es un estándar que define cómo los asistentes de IA interactúan con las API. En ReadMe, MCP convierte la documentación de tu API y tu definición de OpenAPI en un recurso estructurado que las herramientas de IA pueden entender, buscar y llamar mediante programación.

### ¿Cómo funciona MCP con mi proyecto de ReadMe? {#how-does-mcp-work-with-my-readme-project}

ReadMe crea un servidor MCP dedicado para tu proyecto. Este servidor se conecta a tu especificación OpenAPI y a tu funcionalidad [Ask AI](/docs/ask-ai), para que los asistentes de IA puedan:

- Leer y comprender tu especificación OpenAPI
- Ejecutar llamadas a la API
- Buscar en tu documentación
- Obtener detalles de endpoints, cuerpos de solicitud, esquemas de respuesta y fragmentos de código de ejemplo

### ¿Qué pueden hacer los asistentes de IA a través del servidor MCP? {#what-can-ai-assistants-do-through-the-mcp-server}

Una vez conectados a tu servidor MCP, los asistentes de IA pueden:

- Explorar y listar los endpoints disponibles de la API
- Inspeccionar esquemas de seguridad y requisitos de autenticación
- Obtener documentación detallada de los endpoints
- Obtener esquemas estructurados de solicitudes y respuestas
- Generar fragmentos de código de ejemplo para llamar a tu API
- Buscar en tu documentación general para obtener contexto y guías

## Habilitar y usar MCP {#enabling--using-mcp}

### ¿Cómo habilito mi servidor MCP en ReadMe? {#how-do-i-enable-my-mcp-server-in-readme}

En Edit Mode, en la esquina superior derecha, haz clic en **:sparkles:AI** para abrir el panel lateral. Selecciona **MCP** y activa **MCP Server** para activar tu servidor MCP. Una vez habilitado, la URL de tu MCP será:

`https://your-project.readme.com/mcp`

Puedes compartir esta URL con tus desarrolladores para que puedan conectar herramientas de IA compatibles (como Cursor) directamente a tu API y documentación.

### ¿Cómo compruebo que mi servidor MCP está funcionando? {#how-do-i-test-that-my-mcp-server-is-working}

Una vez que hayas habilitado MCP:

1. Abre tu editor de IA (Cursor, VS Code, etc.).
2. Inicia un nuevo chat con el asistente de IA.
3. Haz preguntas como:
   - "¿Cómo hago \[caso de uso común]?"
   - "Muéstrame un ejemplo de \[funcionalidad de la API]."
   - "Crea un \[tipo de integración] usando \[tu API]."

Si está configurado correctamente, el asistente debería poder descubrir tus endpoints, leer tu documentación y generar ejemplos funcionales.

### ¿Puedo controlar qué endpoints se exponen a través de MCP? {#can-i-control-which-endpoints-are-exposed-via-mcp}

Sí. Puedes deshabilitar los endpoints a los que no quieras que se pueda acceder desde tu servidor MCP en **Enabled MCP Routes**. Solo las rutas habilitadas estarán disponibles para los asistentes de IA a través de las herramientas de MCP.

## Herramientas y capacidades {#tools--capabilities}

### ¿Qué herramientas de OpenAPI están disponibles a través de MCP? {#what-openapi-tools-are-available-through-mcp}

El servidor MCP expone varias herramientas centradas en OpenAPI, entre ellas:

- `execute-request` – Realiza llamadas a la API directamente desde tu especificación.
- `get-endpoint` – Obtén información detallada del endpoint.
- `get-request-body` – Accede a parámetros de solicitud estructurados.
- `get-response-schema` – Consulta qué devuelve tu API.
- `list-endpoints` – Explora todos los endpoints disponibles de la API.
- `list-security-schemes` – Inspecciona los requisitos de autenticación.
- `search-schema` – Busca en todo tu esquema de OpenAPI.
- `get-code-snippet` – Genera código de ejemplo en tu lenguaje preferido.

### ¿Qué herramientas de documentación están disponibles? {#what-documentation-tools-are-available}

Las herramientas de documentación se centran en tu base de conocimientos más amplia:

- `search` – Busca contenido relevante en todo tu conjunto de documentación.
- `fetch` – Devuelve una página de guías específica.

<Callout icon="📘" theme="info">
  Las herramientas de documentación requieren actualizar tu plan actual con el <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Para los clientes Enterprise, ponte en contacto con tu CSM.

  Para los clientes Startup y Business, actualiza tu plan con el AI Booster Pack desde tu página **Manage Plan** en Settings.
</Callout>

## Configuración y acceso {#configuration--access}

### ¿Cómo funcionan las ramas con MCP? {#how-do-branches-work-with-mcp}

De forma predeterminada, el servidor MCP se conecta a la versión estable más reciente de tu proyecto. Para dirigirte a una rama diferente, añade `?branch=<name>` a la URL de MCP. Al usar un servidor MCP específico de una rama, la funcionalidad `search-documentation` no estará disponible.

### ¿Cómo permito que MCP acceda a proyectos privados? {#how-do-i-allow-mcp-to-access-private-projects}

Para proyectos privados o protegidos, deberás configurar tu cliente MCP para enviar un encabezado `x-readme-auth`:

- **Protegido por contraseña**: `x-readme-auth` debe ser la contraseña del sitio.
- **Solo miembros del equipo e inicio de sesión personalizado**: `x-readme-auth` debe ser una clave de API con el formato `bearer <api_key>`.

### ¿Cómo puedo generar instrucciones de conexión para mis usuarios? {#how-can-i-generate-connection-instructions-for-my-users}

Después de activar tu servidor MCP, haz clic en **Generate MCP Template** en tu proyecto. Esto crea una nueva guía de **MCP** no publicada en Guides o API Reference de tu proyecto, bajo una nueva categoría llamada **MCP SERVER**. La guía incluye instrucciones listas para usar para conectarse a tu servidor MCP desde herramientas como Cursor y Claude Desktop.

## Planes, precios y requisitos {#plans-pricing--requirements}

### ¿Necesito un plan o complemento específico para usar MCP? {#do-i-need-a-specific-plan-or-add-on-to-use-mcp}

Todos los proyectos de ReadMe pueden generar automáticamente un servidor MCP una vez que MCP esté habilitado. Sin embargo, algunas capacidades (como Documentation Tools) requieren el complemento **AI Booster Pack**. Los clientes Enterprise deben ponerse en contacto con su CSM, y los clientes de Startup/Business pueden actualizar su plan desde la página **Manage Plan** en Settings.
