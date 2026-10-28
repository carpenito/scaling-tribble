---
title: Agente
deprecated: false
hidden: false
metadata:
  robots: index
---
El Agente es un potente asistente de documentación que te ayuda a crear, editar y mejorar contenido en Guías, Referencias de API y Páginas personalizadas con capacidades avanzadas de investigación y análisis.

## Qué puede hacer {#what-it-can-do}

El Agente ofrece asistencia integral para la documentación:

- **Creación y edición de contenido**: Escribe, reescribe, traduce y corrige la gramática con el formato markdown adecuado
- **Investigación y análisis**: Busca en la web, analiza URL y recupera información de tu documentación
- **Componentes inteligentes**: Sugiere e implementa los componentes MDX integrados de ReadMe
- **Flujos de trabajo de varios pasos**: Combina investigación, análisis y creación de contenido en una sola solicitud
- **Corrección de errores del linter**: Resuelve errores de sintaxis y advertencias según tu guía de estilo configurada

## Uso {#usage}

El Agente destaca en tareas de documentación complejas y de varios pasos. Puedes realizar solicitudes como:

- “Investiga las últimas tendencias de diseño de API y crea una guía”
- “Analiza esta URL y añade los puntos clave a nuestra documentación”
- “Busca información de autenticación en nuestra documentación y amplía esta sección”

Cada sesión de chat mantiene el contexto completo de tu página actual y de los archivos de especificación OpenAPI. Todas las conversaciones son privadas para tu cuenta. Utiliza nuestro modelo seleccionado automáticamente o elige tu propio modelo de la lista preconfigurada.

<Image align="center" border={false} src="https://files.readme.io/f678000604c17fb27accb05314a554ec94cf776d81f91701f4ed479db7e6b551-agent_mini.png" />

### Preguntar sobre ReadMe {#ask-about-readme}

Haz preguntas relacionadas con ReadMe al Agente para navegar rápidamente por nuestra plataforma mientras trabajas en tu documentación. Se basa en nuestra base de conocimientos para responder a tus preguntas y guiarte a través de funciones, herramientas y mejores prácticas.

## Configurar {#configure}

Ayuda al Agente a funcionar mejor para ti:

- Si ciertos modelos no son compatibles con tu documentación, desactívalos en la configuración de AI Chat (<i class="fa-regular fa-solid fa-gear" color="var(--gray80"></i>).
- Para mejorar las respuestas del Agente, indexa tu base de código para proporcionar contexto adicional o añade contenido personalizado.

<Image align="center" border={false} width="350px" src="https://files.readme.io/5525b67a2ebb59fdfefbdc82f8c8b88f86f6cf3ba9b03c6c5b927d5acb8a499d-agent_settings_2.png" />

<br />

## Preguntas frecuentes {#faq}

<Accordion title="¿Qué LLM impulsa al agente?" icon="fa-robot">
  El Agente funciona con modelos de lenguaje avanzados, incluidos Google Gemini Pro 2.5, Claude y modelos de OpenAI, lo que proporciona capacidades avanzadas de razonamiento e investigación.
</Accordion>

<Accordion title="¿Se comparten mis datos con el LLM?" icon="fa-shield-alt">
  Solo cuando utilizas la función del Agente. Si no la utilizas, no se comparte ningún dato. Cuando se activa, la página actual que estás viendo y la documentación relevante se incluyen en el prompt enviado al modelo de lenguaje para generar una respuesta.
</Accordion>

<Accordion title="¿Puede acceder a sitios web externos?" icon="fa-globe">
  ¡Sí! El Agente puede buscar en la web y analizar URL para mejorar tu documentación.
</Accordion>

<Accordion title="¿Cómo accede a mi documentación existente?" icon="fa-search">
  Puede buscar en la documentación de tu proyecto y en las fuentes de conocimiento para encontrar e incorporar información relevante.
</Accordion>
