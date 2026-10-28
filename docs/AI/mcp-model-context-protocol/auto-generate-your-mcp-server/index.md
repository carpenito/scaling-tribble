---
title: Genera automáticamente tu servidor MCP
deprecated: false
hidden: false
metadata:
  robots: index
---
Con ReadMe, cada proyecto incluye automáticamente un servidor MCP totalmente configurado. Simplemente activa MCP para conectar la documentación de tu API con herramientas de IA.

## Cómo generar tu propio servidor MCP {#how-to-generate-your-own-mcp-server}

En el modo de edición, en la esquina superior derecha, haz clic en **:sparkles:AI** para abrir el panel lateral. Selecciona **MCP** y activa MCP Server para poner en funcionamiento tu servidor MCP. Tu URL de MCP será: `https://your-project.readme.com/mcp`. Puedes compartir tu URL de MCP con tus desarrolladores para que conecten sus asistentes y herramientas de IA directamente a tu API. Los endpoints a los que no quieras permitir el acceso en tu servidor MCP se pueden deshabilitar en Enabled MCP Routes.

La IA ahora debería tener acceso a los datos y a la documentación de tu cuenta de ReadMe a través del servidor MCP.

<Image align="center" border={false} width="35% " src="https://files.readme.io/f4981199e6757d7c7a64ff259c4c592ab97b8b91f91255804a6a5a8d696fbd9b-mcp_advanced.png" />

### Herramientas personalizadas {#custom-tools}

<br />

## Cómo probar tu configuración de MCP {#testing-your-mcp-setup}

Una vez configurado, puedes probar la conexión de tu servidor MCP:

1. Abre tu editor de IA (Cursor, VS Code, etc.)
2. Inicia un nuevo chat con el asistente de IA
3. Pregunta sobre tu API y documentación. Prueba estas preguntas:
   - "¿Cómo hago \[caso de uso común]?"
   - "Muéstrame un ejemplo de \[funcionalidad de la API]"
   - "Crea un \[tipo de integración] usando \[tu API]

## Cómo generar instrucciones de acceso para tus usuarios {#how-to-generate-access-instructions-for-your-users}

Una vez que hayas activado tu servidor MCP, puedes generar automáticamente instrucciones de acceso para tus usuarios finales haciendo clic en el botón "Generate MCP Template". Esto crea un nuevo documento sin publicar llamado "MCP" en tus Guías que muestra cómo conectarse a tu servidor MCP en herramientas como Cursor y Claude Desktop. Puedes encontrar el documento en la parte inferior de tus Guías o Referencia de API en una nueva categoría llamada "MCP SERVER".
