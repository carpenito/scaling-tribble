---
title: MCP (Model Context Protocol)
deprecated: false
hidden: false
metadata:
  robots: index
---
[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) es una estandarización de cómo los asistentes de IA interactúan con las API, y ReadMe lleva esta capacidad a tu centro de desarrolladores. Con los servidores MCP, puedes convertir la documentación de tu API en un recurso estructurado que los asistentes de IA puedan entender y con el que puedan interactuar mediante programación.

## Características principales {#key-features}

- **Herramientas personalizadas**: define combinaciones personalizadas de flujos de trabajo y endpoints. <Badge label="Nuevo" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
- **Rutas habilitadas**: deshabilita los endpoints a los que no quieras permitir el acceso en tu servidor MCP <Badge label="Nuevo" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
- **Integración con OpenAPI**: genera un servidor MCP a partir de tu especificación OpenAPI existente.
- **Los asistentes de IA pueden conectarse a tu servidor MCP para**:
  - Leer y comprender tu especificación OpenAPI.
  - Ejecutar llamadas a la API.
  - Buscar en la documentación con [Ask AI](/docs/ask-ai).
- **Herramientas de MCP**:
  - **Herramientas de OpenAPI**:
    - `execute-request` - Realiza llamadas a la API directamente desde tu especificación
    - `get-endpoint` - Obtén información detallada del endpoint bajo demanda
    - `get-request-body` - Accede a parámetros de solicitud estructurados
    - `get-response-schema` - Comprende qué devuelve tu API
    - `list-endpoints` - Explora todos los endpoints de API disponibles
    - `list-security-schemes` - Accede a los requisitos de autenticación
    - `search-schema` - Encuentra exactamente lo que necesitas en tu especificación de API
    - `get-code-snippet` - Fragmentos de código de ejemplo en tu lenguaje preferido para interactuar con tu endpoint.
  - **Herramientas de documentación**:
    - `search` - Busca información relevante en toda tu base de conocimiento
    - `fetch` - Devuelve una página de guías

<Callout icon="📘" theme="info">
  Las herramientas de documentación requieren actualizar tu plan actual con el <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Para clientes Enterprise, comunícate con tu CSM.

  Para clientes de Startup y Business, actualiza tu plan con el AI Booster Pack desde tu página **Administrar plan** en Configuración.
</Callout>

## Cómo funciona {#how-it-works}

Creamos un servidor MCP dedicado que se conecta a tu especificación OpenAPI y a la funcionalidad [Ask AI](/docs/ask-ai). Esto crea un puente entre la documentación de tu API y los asistentes de IA, haciendo que tu API sea accesible y comprensible al instante para las herramientas de IA.

## Funciones adicionales {#extra-features}

- **Ramas** Por defecto, el servidor MCP está conectado a la versión estable más reciente. Para elegir una rama diferente, añade `?branch=<name>` a la URL del MCP. NOTA: Cuando estés en una rama, `search-documentation` no estará disponible.
- **Proyectos privados** Para acceder a proyectos protegidos, deberás configurar tu cliente MCP para enviar un encabezado `x-readme-auth`
  - Protegido por contraseña: `x-readme-auth` debe ser la contraseña del sitio
  - Solo para miembros del equipo e inicio de sesión personalizado: `x-readme-auth` debe ser una clave de API con el formato `bearer <api_key>`

## Primeros pasos con MCP {#getting-started-with-mcp}

Elige cómo te gustaría empezar a trabajar con MCP:

1. <Anchor label="Genera automáticamente tu propio servidor MCP" target="_blank" href="doc:generate-your-own-mcp-server">Genera automáticamente tu propio servidor MCP</Anchor>: Cada proyecto de ReadMe incluye automáticamente un servidor MCP completamente configurado. Simplemente habilita MCP para conectar la documentación de tu API con las herramientas de IA.
2. <Anchor label="Usa el servidor MCP de ReadMe" target="_blank" href="doc:readmes-mcp-server">Usa el servidor MCP de ReadMe</Anchor>: Con el servidor MCP de ReadMe, puedes hacer todo lo que normalmente harías en ReadMe, como añadir y editar páginas, directamente a través de nuestra API.
