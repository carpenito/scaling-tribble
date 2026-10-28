---
title: LLMs.txt
deprecated: false
hidden: false
metadata:
  robots: index
---
## Descripción general {#overview}

Con nuestra nueva función [LLMs.txt](https://llmstxt.org/), puedes enseñar a los modelos de IA a entender y representar adecuadamente la documentación de tu API. Esto te permite proporcionar el contexto que los asistentes de IA como ChatGPT o Claude necesitan para responder con precisión preguntas sobre tu API sin alucinar (inventar información). Configurarlo lleva literalmente unos segundos: solo tienes que activar un interruptor y generaremos el archivo de configuración automáticamente. En segundo plano, creamos metadatos que ayudan a los sistemas de IA a comprender la estructura de tu documentación, la terminología y la información más actualizada. LLMs.txt está disponible en todos los planes.

¿El resultado? Los desarrolladores obtienen respuestas precisas sobre tu API incluso cuando consultan herramientas de IA en lugar de leer tu documentación directamente. ¡Es documentación que funciona dondequiera que trabajen tus desarrolladores!

## Beneficios {#benefits}

- **Precisión**: ayuda a que los modelos de IA representen tu documentación correctamente
- **Consistencia**: garantiza la terminología y la información de versión adecuadas
- **Relevancia**: guía a los modelos de IA hacia la información más actualizada
- **Cero mantenimiento**: se genera automáticamente a partir de tu documentación existente

## Cómo funciona {#how-it-works}

LLMs.txt funciona como un archivo de configuración en la raíz de tu sitio de documentación al que los modelos de lenguaje de IA pueden acceder e interpretar. Este archivo funciona como una guía técnica que indica a los sistemas de IA cómo leer y hacer referencia adecuadamente a tu contenido.

Cuando está habilitado, ReadMe genera automáticamente este archivo de configuración a partir de la estructura de tu documentación existente. El archivo contiene metadatos sobre:

- La organización de tu documentación (guías, referencia de la API, recetas, etc.)
- Información de versión para garantizar que los modelos de IA consulten la documentación más actualizada
- Terminología importante específica de tu API
- Estructura jerárquica de tu contenido

Los modelos de IA compatibles con LLMs.txt buscarán este archivo antes de generar respuestas sobre tu API. Cuando lo encuentren, utilizarán las instrucciones para ofrecer información más precisa, lo que reduce las probabilidades de referencias desactualizadas o terminología incorrecta.

Por ejemplo, si recientemente has cambiado el nombre de algún endpoint o has modificado los requisitos de los parámetros, LLMs.txt ayuda a garantizar que los asistentes de IA no faciliten información desactualizada a los desarrolladores que utilizan tu API.

## Primeros pasos {#getting-started}

Habilita LLMs.txt en solo unos clics para ayudar a que los modelos de IA representen con precisión la documentación de tu API.

#### ReadMe Refactored {#readme-refactored}

Para proyectos que utilizan la interfaz de ReadMe Refactored:

1. Ve al hub de tu proyecto.
2. Haz clic en **Ajustes de IA (✨ icono de destellos)** en el menú superior derecho.
3. Cambia **Habilitar LLMs.txt** a ACTIVADO.
4. Haz clic en **Guardar**.

#### ReadMe Legacy {#readme-legacy}

1. Ve a **Configuración** > **Ajustes de IA**.
2. Cambia **Habilitar LLMs.txt** a ACTIVADO.
3. Haz clic en **Guardar**.
