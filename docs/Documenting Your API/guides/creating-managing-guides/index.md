---
title: Creación y gestión de guías
deprecated: false
hidden: false
metadata:
  robots: index
---
# Descripción general {#overview}

Profundicemos en los aspectos prácticos de la organización de tu documentación en ReadMe. Desde la creación de nuevas guías hasta la gestión del contenido a lo largo del tiempo, esta guía te mostrará cómo crear y mantener una base de conocimiento bien estructurada que ayude a los desarrolladores a encontrar exactamente lo que necesitan, cuando lo necesitan.

### Por qué son importantes las guías {#why-guides-matter}

Las guías son la columna vertebral de tu documentación para desarrolladores. Mientras que tu referencia de API les muestra lo que es posible, las guías les enseñan cómo tener éxito. Las buenas guías:

- Guían a los desarrolladores de principiante a experto
- Aportan un contexto que las referencias de API no pueden capturar
- Responden al "por qué" junto con el "cómo"
- Resuelven problemas del mundo real con los que se encuentran los desarrolladores

## Creación de tu primera guía {#creating-your-first-guide}

### Creación de categorías 📂 {#creating-categories-}

Las categorías te ayudan a organizar tu documentación en secciones lógicas, funcionando como capítulos en la historia de tu API. Cada categoría crea una pausa natural en la narrativa de tu documentación, facilitando que los desarrolladores la sigan.

1. Dirígete a tu hub de documentación y cambia al **Modo de edición**.
2. Haz clic en el botón **+ NUEVA CATEGORÍA** en la navegación de la barra lateral.
3. Introduce un nombre para tu categoría (por ejemplo, "Primeros pasos" o "Temas avanzados")
4. Pulsa **Enter** para guardar.

<Callout icon="📘" theme="info">
  ### Experiencia de usuario {#user-experience}

  Piensa en el recorrido de los desarrolladores al nombrar las categorías. ¿Qué tendría más sentido para alguien que explora tu API por primera vez? Considera organizar las categorías por nivel de habilidad (de principiante a avanzado) o por caso de uso.
</Callout>

### Creación de una página de guía 📝 {#creating-a-guide-page-}

Ahora que ya tienes configuradas tus categorías, añadamos algunas páginas:

1. En el modo de **Edición**, pasa el cursor sobre una categoría y haz clic en el botón **+**
2. Completa los datos esenciales:
   - **Título**: hazlo claro y descriptivo
   - **Slug**: esta será la ruta de la URL (se genera automáticamente, pero puedes personalizarla)
   - **Oculto**: activa esta opción si quieres trabajar en la guía antes de hacerla pública
3. Haz clic en **Guardar** para crear tu nueva guía

### Uso de la interfaz de usuario del editor ✏️ {#using-the-editor-ui-️}

<Image align="left" border={false} width="50% " src="https://files.readme.io/53c229bb50f36b2a6398894e5de72e9909397911c2deba6c77e629733e714a99-Editing_UI_-_view_to_edit_toggle.gif" />

<br />

<br />

<br />

<br />

<br />

<br />

Con la interfaz de edición de ReadMe, crearás y editarás contenido directamente en tu hub. Esto significa que lo que ves es exactamente lo que verán tus desarrolladores.

1. Después de crear tu página, entrarás automáticamente en el editor
2. Usa la barra de herramientas de formato para aplicar estilos de texto básicos
3. Escribe `/` para acceder al menú de comandos e insertar:
   - Bloques de código
   - Cuadros de aviso
   - Imágenes
   - ¡Y más!
4. Alterna entre los modos de **Edición** y **Vista** para ver exactamente cómo verán tu contenido los desarrolladores

<Image align="center" border={false} src="https://files.readme.io/a106664539184b9eebb366fd2c51ed5ba10ca5c1224c0ce52a209dd8c08ac143-CleanShot_2024-11-08_at_20.24.59.gif" />

<Callout icon="📘" theme="info">
  ### Control total de tu Markdown {#complete-control-of-your-markdown}

  El Modo Raw de ReadMe te permite añadir contenido nuevo y editar el contenido existente directamente en Markdown. Solo tienes que abrir el menú de tres puntos situado junto a la configuración de visibilidad y elegir **Modo Raw**.
</Callout>

## Estructuración de guías eficaces {#structuring-effective-guides}

### La anatomía de una gran guía {#the-anatomy-of-a-great-guide}

Las guías exitosas siguen una estructura coherente que ayuda a los desarrolladores a comprender y aplicar la información rápidamente:

1. **Introducción clara**: ¿qué problema resuelve esta guía?
2. **Requisitos previos**: ¿qué deben saber o tener los desarrolladores antes de comenzar?
3. **Instrucciones paso a paso**: divide los procesos complejos en pasos manejables
4. **Ejemplos de código**: muestra, no te limites a explicar
5. **Resolución de problemas**: aborda los problemas habituales y sus soluciones
6. **Siguientes pasos**: ¿a dónde deberían dirigirse los desarrolladores después de completar esta guía?

### Redacción para desarrolladores {#writing-for-developers}

Al redactar guías, recuerda que los desarrolladores quieren resolver problemas con rapidez:

- **Sé conciso**: ve al grano y evita explicaciones innecesarias
- **Usa ejemplos de código con frecuencia**: los desarrolladores suelen entender el código más rápido que el texto explicativo
- **Destaca la información importante**: usa cuadros de aviso para advertencias, consejos y notas importantes
- **Divide el texto**: usa encabezados, listas y párrafos cortos para mejorar la legibilidad
- **Usa ejemplos del mundo real**: muestra código que resuelva problemas reales

<Callout icon="📘" theme="info">
  ### Hazlo realista {#keep-it-real}

  Usa ejemplos de código auténticos que demuestren implementaciones realistas. Si estás mostrando la autenticación, utiliza un ejemplo completo con gestión de errores. Si estás demostrando la recuperación de datos, muestra cómo procesar y utilizar esos datos de forma práctica. Los ejemplos del mundo real ayudan a los desarrolladores a acortar la distancia entre la documentación y la implementación.
</Callout>

```javascript
// Good example - with meaningful comments and clear variable names
const apiKey = 'your_api_key_here';

// Initialize the client with your API key
const client = new ReadMeAPI(apiKey);

// Fetch user data and handle potential errors
try {
  const userData = await client.getUser(userId);
  console.log(`Found user: ${userData.name}`);
} catch (error) {
  console.error(`Error fetching user: ${error.message}`);
}
```

## Mejora de las guías con MDX {#enhancing-guides-with-mdx}

ReadMe ahora es compatible con MDX (Markdown + JSX), lo que te brinda la posibilidad de crear documentación interactiva con componentes reutilizables.

### Componentes básicos de MDX {#basic-mdx-components}

A continuación tienes un ejemplo de nuestros componentes integrados de pestañas MDX que puedes utilizar para mejorar tus guías:

<Tabs>
  <Tab title="Node.js">
    ```javascript
    const client = new ReadMeAPI(apiKey);
    ```
  </Tab>

  <Tab title="Python">
    ```python
    client = ReadMeAPI(api_key)
    ```
  </Tab>

  <Tab title="Ruby">
    ```ruby
    client = ReadMeAPI.new(api_key)
    ```
  </Tab>
</Tabs>

### Creación de contenido reutilizable {#creating-reusable-content}

Para el contenido que utilizarás en varias guías, [crea bloques de contenido reutilizables](doc:reusable-content)

1. Dirígete a **Configuración de contenido** en la interfaz de edición
2. Selecciona **Contenido reutilizable**
3. Crea bloques para elementos comunes como:
   - Pasos de autenticación de la API
   - Instrucciones de configuración del entorno
   - Patrones de código estándar
4. Insértalos en cualquier guía con el comando `/`

## Organización de tu documentación {#organizing-your-documentation}

### Creación de una estrategia de documentación {#creating-a-documentation-strategy}

Antes de profundizar en guías individuales, considera la estructura general de tu documentación:

1. **Traza el recorrido del desarrollador**: ¿qué camino siguen los desarrolladores desde el primer registro hasta el uso avanzado?
2. **Identifica las lagunas de conocimiento**: ¿dónde suelen atascarse los desarrolladores?
3. **Crea rutas de aprendizaje progresivas**: ¿cómo puede basarse cada guía en los conocimientos previos?

### Tipos de guías a considerar {#guide-types-to-consider}

Diferentes guías tienen diferentes propósitos:

- **Primeros pasos**: incorporación de nuevos desarrolladores
- **Tutoriales**: instrucciones paso a paso para tareas específicas
- **Guías conceptuales**: explicación de ideas complejas o arquitectura
- **Guías prácticas**: instrucciones detalladas para funciones específicas
- **Resolución de problemas**: soluciones a problemas comunes

## Mantenimiento de las guías a lo largo del tiempo {#maintaining-guides-over-time}

### Mantener el contenido actualizado {#keeping-content-fresh}

La documentación requiere un mantenimiento periódico:

1. Programa ciclos de revisión periódicos (los trimestrales funcionan bien)
2. Actualiza las guías y tu registro de cambios cuando las funciones cambien
3. Presta atención a los comentarios de los usuarios que indiquen confusión
4. Monitorea las analíticas para ver qué guías necesitan mejoras

### Consideraciones sobre el control de versiones {#versioning-considerations}

Si tu API tiene varias versiones:

1. Usa la función de control de versiones de ReadMe para mantener conjuntos de documentación independientes
2. Indica claramente la información específica de cada versión
3. Considera el uso de cuadros de aviso para destacar las diferencias entre versiones

## Colaboración con la integración de Git {#collaborating-with-git-integration}

Con la [sincronización bidireccional con Git](doc:bi-directional-sync) de ReadMe, ahora puedes colaborar en la documentación utilizando los flujos de trabajo habituales de Git:

1. Conecta tu proyecto de ReadMe a GitHub/GitLab
2. Edita los archivos de documentación directamente en tu repositorio
3. Los cambios se sincronizan automáticamente con tu proyecto de ReadMe
4. Usa pull requests y revisiones para los cambios en la documentación

## Medición del éxito {#measuring-success}

### Uso de las analíticas {#using-analytics}

ReadMe proporciona información sobre cómo los desarrolladores utilizan tu documentación:

1. Monitorea las visitas a las páginas para identificar las guías más populares
2. Rastrea las consultas de búsqueda para encontrar información faltante
3. Utiliza estos datos para priorizar las mejoras en la documentación

### Recopilación de comentarios {#gathering-feedback}

Crea ciclos de retroalimentación para mejorar continuamente:

1. Habilita los debates en las guías
2. Revisa con regularidad las preguntas y los comentarios
3. Actualiza las guías en función de las preguntas frecuentes

## Siguientes pasos {#next-steps}

Ahora que ya sabes cómo crear y gestionar guías en ReadMe, prueba a:

- Crear tu primera categoría y guía
- Experimentar con componentes MDX
- Configurar un proceso de revisión de la documentación
- Conectar tu documentación a GitHub para la edición colaborativa

¿Necesitas más ayuda? Consulta nuestros otros recursos:

- [Documentación de MDX](doc:mdx)
- [Configuración de la sincronización bidireccional](doc:bi-directional-sync)
