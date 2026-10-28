---
title: Referencia de la API
deprecated: false
hidden: false
metadata:
  robots: index
---
# ¿Qué es una referencia de API? {#what-is-an-api-reference}

Una referencia de API es la guía técnica definitiva sobre tu API, que documenta en detalle cada endpoint, parámetro y código de respuesta. Es tu fuente de verdad definitiva a la que los desarrolladores recurren cuando necesitan saber exactamente cómo interactuar con tu API.

En ReadMe, la referencia de tu API es una experiencia interactiva donde los desarrolladores pueden explorar tu API, realizar llamadas de prueba directamente desde la documentación y ver respuestas reales sin escribir una sola línea de código.

## Por qué es importante la referencia de tu API {#why-your-api-reference-matters}

Una referencia de API bien elaborada puede:

- **Reducir los tickets de soporte** al responder preguntas técnicas antes de que se planteen
- **Acelerar la incorporación de desarrolladores** al ofrecer pautas de implementación claras y precisas
- **Generar confianza en los desarrolladores** al demostrar que tu API está diseñada y mantenida minuciosamente
- **Mostrar todo el potencial de tu API** para que los desarrolladores descubran funcionalidades que de otro modo podrían pasar por alto

## Primeros pasos con la referencia de tu API {#getting-started-with-your-api-reference}

ReadMe ofrece varias formas de crear y mantener la referencia de tu API, ya sea que trabajes con especificaciones OpenAPI (anteriormente Swagger) o prefieras crear tu referencia manualmente.

### En esta sección {#in-this-section}

Aprenderás a:

- **Subir y administrar especificaciones OpenAPI** mediante diversos métodos
- **Trabajar con nuestro API Designer** si no tienes una especificación OpenAPI
- **Personalizar la referencia de tu API** para adaptarla a tu marca y mejorar la usabilidad
- **Crear ejemplos interactivos** que los desarrolladores puedan probar directamente en tu documentación
- **Mantener tu referencia sincronizada** con tu API real a medida que evoluciona

## Subida y administración de OpenAPI {#openapi-upload-and-management}

ReadMe es totalmente compatible con las especificaciones OpenAPI 3.0, OpenAPI 3.1 y Swagger 2.0. Puedes agregar la especificación de tu API a ReadMe de varias formas:

- **Subida de archivos**: arrastra y suelta tu archivo JSON o YAML de OpenAPI/Swagger
- **Importación mediante URL**: indica a ReadMe dónde se encuentra tu especificación en línea
- **Integración con GitHub**: conéctate directamente a tu repositorio de GitHub
- **Línea de comandos (rdme)**: usa nuestra herramienta de CLI para flujos de trabajo automatizados
- **API Sync**: mantén la referencia de tu API sincronizada automáticamente con tu código base

Una vez subida, ReadMe transforma tu especificación en documentación interactiva y con un formato impecable que encantará a los desarrolladores.

## API Designer {#api-designer}

¿No tienes una especificación OpenAPI? ¡No hay problema! El [API Designer](doc:building-apis-from-scratch-with-the-api-designer) de ReadMe te permite crear la referencia de tu API desde cero con una interfaz intuitiva. Documenta tus endpoints, parámetros, cuerpos de solicitud y objetos de respuesta sin necesidad de escribir una sola línea de YAML o JSON.

## Personalización de la referencia de tu API {#customizing-your-api-reference}

Haz que la referencia de tu API sea verdaderamente tuya con opciones de personalización:

- Agrega detalles de autenticación y encabezados personalizados
- Incluye ejemplos de código en múltiples lenguajes de programación
- Organiza los endpoints en grupos lógicos
- Agrega documentación personalizada e información general a cada grupo de endpoints

## Compatibilidad con GraphQL {#graphql-support}

¿Trabajas con GraphQL? ReadMe ofrece una compatibilidad limitada pero creciente con las [APIs de GraphQL](doc:graphql). Puedes documentar tus esquemas, consultas y mutaciones para ayudar a los desarrolladores a explorar tu API de GraphQL.

## Prácticas recomendadas para las referencias de API {#best-practices-for-api-references}

Para crear una referencia de API excepcional:

- **Sé exhaustivo**: documenta cada endpoint, parámetro y respuesta
- **Incluye ejemplos**: muestra pares reales de solicitud/respuesta para casos de uso comunes
- **Explica los errores**: documenta todos los códigos de error y cómo resolverlos
- **Mantenla actualizada**: actualiza la documentación siempre que tu API cambie
- **Pruébala tú mismo**: utiliza periódicamente tu propia documentación para detectar problemas
