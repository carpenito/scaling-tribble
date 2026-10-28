---
title: Preguntar a la IA
deprecated: false
hidden: false
metadata:
  robots: index
---
Tus usuarios pueden obtener respuestas instantáneas sobre tu producto con Ask AI. El asistente utiliza el modelo seleccionado, entrenado con tu documentación, para ofrecer respuestas precisas y adaptadas al contexto. Incluye enlaces directos a tu documentación, lo que permite a los usuarios explorar los temas con más detalle.

***

## Vista previa del usuario final {#end-user-preview}

Cuando tus usuarios interactúan con Ask AI, se abrirá el Asistente con tus preguntas de ejemplo personalizadas y recibirán respuestas basadas en tus configuraciones del panel de administración. Las respuestas solo harán referencia a páginas públicas. Para los grupos Enterprise con proyectos públicos y privados, Ask AI proporcionará información según los permisos de los usuarios para ver un proyecto.

<Image align="center" border={false} width="750px" src="https://files.readme.io/93bba5b92a2c954d7aa1b5847d3648837ac31668b9861e35479e7a906596b3ab-user_gif.gif" />

## Configurar {#configure}

Personaliza el tono del asistente de IA, la longitud de las respuestas y los temas prohibidos para que se adapten a tu marca. Define preguntas de ejemplo para que las vean tus usuarios finales y selecciona un modelo disponible que se ajuste a tus necesidades.

<Image align="center" border={false} src="https://files.readme.io/afc7f66444d7c8186118082c46a34ed5a8af5bbdfdb65cc9af97f8fba3969724-Ask_AI.png" />

### Grupos Enterprise {#enterprise-groups}

Todas las configuraciones mencionadas anteriormente están disponibles para los proyectos Enterprise en tu Panel de grupo. Las personalizaciones a nivel de grupo se aplicarán en todos los proyectos secundarios correspondientes.

## Analítica {#analytics}

Profundiza en las preguntas, respuestas y comentarios de los usuarios para comprender qué buscan—y con qué eficacia funciona el asistente. Puedes ver todas las analíticas en el **panel de Ask AI** dentro de **Configuración**. Para compartir información con tu equipo, exporta los datos como CSV con rangos de fechas personalizados. El proceso de exportación puede tardar algún tiempo según el volumen de datos, pero cuando esté listo, la descarga comenzará inmediatamente en tu navegador.

<Image align="center" border={false} width="650px" src="https://files.readme.io/27af66805d9c4eb18c468750023284c9682c2734dd2422bb650d7408b98a4787-analytics.png" />

<br />

## Preguntas frecuentes {#faq}

<Accordion title="¿Qué ocurre con mis datos?" icon="fa-chart-simple">
  Ask AI funciona con las API de OpenAI, y el contenido en Markdown junto con las definiciones de la API se les envían para generar respuestas a las preguntas de los usuarios.
  Aunque OpenAI conserva los registros de estas solicitudes de API durante 30 días, no se utiliza ningún dato para entrenar sus modelos de IA.
</Accordion>

<Accordion title="¿Ask AI hace referencia a páginas ocultas?" icon="fa-user-ninja">
  No, Ask AI nunca indexa las páginas ocultas.
  Para los grupos Enterprise, solo se utiliza el contenido del proyecto al que el usuario tiene acceso para responder preguntas.
</Accordion>

<Accordion title="¿Con qué rapidez se incorporan los cambios a los modelos de Ask AI?" icon="fa-swap">
  Actualmente, el contenido nuevo se actualiza cada 2 horas, aunque esto podría cambiar a medida que continuamos desarrollando Ask AI.
</Accordion>

<Accordion title="¿Qué herramientas se ofrecen para supervisar las respuestas?" icon="fa-monitor-waveform">
  Los registros de cada pregunta y respuesta están disponibles en el panel de administración. Consulta [Analítica](https://docs.readme.com/maindocs/ask-ai#analytics) más arriba.
</Accordion>

<Accordion title="¿Cómo puedo probar Ask AI?" icon="fa-sparkles">
  Puedes probar Ask AI en la documentación de ReadMe o en tu propia documentación como prueba.
</Accordion>

<Accordion title="Estoy usando la experiencia anterior de Ask AI. ¿Dónde puedo encontrar estos ajustes?" icon="fa-robot">
  Puedes actualizar a la nueva experiencia desde el panel de configuración en el panel de Ask AI. La actualización es permanente y no se puede deshacer.
</Accordion>
