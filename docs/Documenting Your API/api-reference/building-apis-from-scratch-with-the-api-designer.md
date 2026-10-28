---
title: Creación de APIs desde cero con API Designer
deprecated: false
hidden: false
metadata:
  robots: index
---
# Descripción general {#overview}

¿No tienes una especificación OpenAPI? ¡No hay problema! El Diseñador de API de ReadMe te permite crear tu referencia de API directamente en la plataforma con una interfaz visual intuitiva – sin necesidad de YAML ni JSON.

En esta guía, veremos cómo crear una API de redes sociales con endpoints para listar y crear publicaciones. Verás lo fácil que es documentar tu API incluso si comienzas desde cero.

## Creación de tu definición de API {#creating-your-api-definition}

Empecemos configurando la estructura básica para tu API:

1. Ve a **Referencia de API** en tu proyecto de ReadMe
2. Haz clic en el botón **+ Agregar**
3. Selecciona **Comenzar a crear** debajo de "Crear una definición de API desde cero"

<Image align="center" border={false} src="https://files.readme.io/f9e241f98e3e8ad91e999561f4e3b4dfe260a8e6a18662e23da840887977b6c7-CleanShot_2025-03-11_at_11.18.13.gif" />

4. Introduce los detalles de tu definición de API:
   - **Título de la API**: introduce un nombre descriptivo (p. ej., "API de redes sociales")
   - **URL del host de destino**: la URL base de tu API (p. ej., "[http://api.example.com](http://api.example.com)")
   - **Tipo de autenticación**: selecciona tu método de autenticación (Ninguno, API Key, Basic o Bearer)

<Image align="center" border={false} src="https://files.readme.io/7a81519f9faf96f4af361d26c405792fe78488558a9c8e972d084d102dda098e-CleanShot_2025-03-11_at_11.21.07.gif" />

5. Haz clic en **Guardar** para crear tu definición de API

Tu nueva definición de API aparecerá en el panel de navegación izquierdo, lista para que agregues endpoints.

## Creación de tu primer endpoint (Listar publicaciones de redes sociales) {#creating-your-first-endpoint-list-social-media-posts}

Vamos a crear un endpoint para recuperar una lista de publicaciones de redes sociales:

1. En el panel de navegación izquierdo, verás un endpoint predeterminado con la etiqueta `/new-endpoint`
2. Cambia su nombre para que refleje mejor la estructura de tu API; llamémoslo "Posts"
3. Ahora verás esta categoría en tu panel de navegación izquierdo

<Image align="center" border={false} src="https://files.readme.io/fc908c66586d12aa0327f1bc17d60a045a23e550e82161ae4818a37eb91b3931-CleanShot_2025-03-11_at_11.29.12.gif" />

4. Crea tu endpoint GET para listar publicaciones:
   - Haz clic en el endpoint para editarlo
   - Cambia el título a "Listar publicaciones de redes sociales"
   - Selecciona el método **GET** en el menú desplegable
   - Establece la ruta en `/posts`
   - Añade una descripción que explique qué hace el endpoint (p. ej., "Devuelve una lista paginada de publicaciones de redes sociales")

<Image align="center" border={false} src="https://files.readme.io/72e65717ef6534caa7b0d2a187deb7125b1466bc72a95a8fdcd7459267ae8b35-CleanShot_2025-03-11_at_11.31.27.gif" />

### Adición de parámetros de consulta {#adding-query-parameters}

La mayoría de los endpoints de tipo lista admiten paginación o filtrado. Vamos a añadir algunos parámetros de consulta:

1. Ubica la sección **Parámetros de consulta** y haz clic en el botón **+**
2. Añade parámetros para la paginación:
   - Añade un parámetro `page` de tipo `integer`
   - Añade un parámetro `limit` de tipo `integer`
   - Añade cualquier otro parámetro de filtrado (p. ej., `category` como `string`)
3. Para cada parámetro:
   - Añade una descripción
   - Indica si es obligatorio
   - Proporciona un valor predeterminado si corresponde

<Image align="center" border={false} src="https://files.readme.io/c596d7f09014adbfb1166f81b10936c0427f6b0e4a4c1cc9f2983a51c55aaa55-CleanShot_2025-03-11_at_11.35.30.gif" />

<br />

## Creación de tu segundo endpoint (Crear una publicación en redes sociales) {#creating-your-second-endpoint-create-a-social-media-post}

Ahora vamos a añadir un endpoint para crear nuevas publicaciones:

1. En el panel de navegación izquierdo, haz clic en el botón **+ Nueva categoría** si necesitas una nueva categoría, o usa tu categoría existente "Posts"
2. Haz clic en el icono + para añadir un nuevo endpoint
3. Configura tu endpoint POST:
   - Título: "Crear nueva publicación"
   - Método: selecciona **POST** en el menú desplegable
   - Ruta: `/posts`
   - Descripción: "Permite a los usuarios autenticados crear nuevas publicaciones"

<Image align="center" border={false} src="https://files.readme.io/fa7c7a03010f8fdbc0bee4ff32db7a11e34f723f3640ed6e3f311234e93dd2bd-CleanShot_2025-03-11_at_11.52.25.gif" />

### Adición de parámetros del cuerpo de la solicitud {#adding-request-body-parameters}

Para un endpoint POST, deberás definir el cuerpo de la solicitud:

1. Ubica la sección **Cuerpo de la solicitud** y haz clic para expandirla
2. Establece el tipo de contenido en `object`
3. Añade los campos obligatorios:
   - Añade un campo `content` de tipo `string` y márcalo como obligatorio
   - Añade cualquier campo adicional que acepte tu API (p. ej., `image_url`, `tags`)
4. Para cada campo:
   - Añade una descripción clara
   - Marca si es obligatorio
   - Proporciona cualquier restricción (longitud mínima/máxima, patrón, etc.)

<Image align="center" border={false} src="https://files.readme.io/2a114a0bb8cfab72df455ea87638aa51d75a1ea3b931987fc18d1450f94cb08d-CleanShot_2025-03-11_at_11.57.21.gif" />

### Adición de ejemplos de código de solicitud {#adding-request-code-samples}

Una de las funciones más potentes de ReadMe es la generación automática de ejemplos de código:

1. Busca la sección **Código de la solicitud** a la derecha
2. ReadMe genera automáticamente ejemplos de código en múltiples lenguajes
3. También puedes hacer clic en "Escribe tus propios ejemplos estáticos" para añadir ejemplos personalizados

<Image align="center" border={false} src="https://files.readme.io/646ce4e3467087d3d7b8396632e29af646bf02be9113054d0c63e69c14561a6c-CleanShot_2025-03-11_at_12.03.35.gif" />

<br />

## Prueba de la documentación de tu API {#testing-your-api-documentation}

Después de crear tus endpoints:

1. Guarda los cambios
2. Cambia al modo "Ver" para comprobar cómo ven la documentación los desarrolladores
3. Prueba las funciones interactivas para asegurarte de que tus ejemplos funcionen correctamente

## Consejos para una excelente documentación de API {#tips-for-great-api-documentation}

- **Sé minucioso con las descripciones**: explica con claridad qué hace cada endpoint y por qué
- **Proporciona ejemplos realistas**: utiliza datos de ejemplo que reflejen un uso en el mundo real
- **Documenta los estados de error**: incluye ejemplos de respuestas de error y cómo gestionarlas
- **Usa una nomenclatura coherente**: mantén un estilo uniforme en todos los endpoints y parámetros
- **Añade "¿Qué sigue?"**: usa la sección "¿Qué sigue?" para orientar a los usuarios sobre endpoints relacionados que puedan necesitar

Siguiendo esta guía, has creado desde cero una referencia de API bien documentada mediante el Diseñador de API de ReadMe. Tus desarrolladores ahora cuentan con documentación clara e interactiva que les ayuda a integrarse con tu API de forma rápida y sencilla.

Recuerda que siempre puedes volver al Diseñador de API para añadir endpoints, actualizar parámetros o mejorar tu documentación a medida que tu API evolucione.

<br />

## Funciones de OpenAPI no admitidas actualmente en el Diseñador de API {#currently-unsupported-openapi-features-in-the-api-designer}

Actualmente no admitimos todas las funciones de OpenAPI en nuestro Diseñador de API. Si utilizas alguna de estas funciones en un endpoint, no podrás editarla en nuestra interfaz de usuario. Sin embargo, estos endpoints se seguirán mostrando correctamente en la documentación y se podrán seguir actualizando editando el archivo OpenAPI directamente.

<br />

| Función de OpenAPI no admitida | Explicación                                                                                                                                                                                                                    | Documentación de OpenAPI                                                                                                              |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| Propiedades adicionales        | La palabra clave additionalProperties se utiliza dentro de un esquema para definir si se permiten en los objetos propiedades que no están definidas explícitamente en el esquema y, de ser así, cuáles deberían ser sus tipos. | [Diccionarios, mapas hash y matrices asociativas](https://swagger.io/docs/specification/v3_0/data-models/dictionaries/)               |
| Callbacks/Webhooks             | OpenAPI tiene una función para definir endpoints que realizarán una llamada a la API una vez que se haya completado un evento.                                                                                                 | [Callbacks](https://swagger.io/docs/specification/v3_0/callbacks/)                                                                    |
| Referencias                    | Cualquier endpoint que defina un objeto usando un $ref.                                                                                                                                                                        | [Uso de Ref](https://swagger.io/docs/specification/v3_0/using-ref/)                                                                   |
| Parámetros comunes             | Endpoints donde los parámetros se definen a nivel de ruta en lugar del método, de modo que los parámetros se comparten entre todos los métodos para esa URL.                                                                   | [Descripción de parámetros](https://swagger.io/docs/specification/v3_0/describing-parameters/#common-parameters)                      |
| Enlaces                        | Los enlaces son una función de OpenAPI que describe cómo las respuestas de un endpoint pueden usarse como entrada para otras operaciones.                                                                                      | [Enlaces](https://swagger.io/docs/specification/v3_0/links/)                                                                          |
| Polimorfismo                   | El polimorfismo te permite definir un esquema que puede representar múltiples tipos o modelos.                                                                                                                                 | [Herencia y polimorfismo](https://swagger.io/docs/specification/v3_0/data-models/inheritance-and-polymorphism/?sbsearch=Polymorphism) |
| Variables de servidor          | Se pueden definir variables en la ruta base que pueden tener una lista preestablecida de valores entre los que el usuario puede elegir.                                                                                        | [Servidor de API y ruta base](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/?sbsearch=server%20variables)         |
| Estilo                         | La palabra clave Style permite configurar cómo deben pasarse múltiples valores a un parámetro.                                                                                                                                 | [Serialización de parámetros](https://swagger.io/docs/specification/v3_0/serialization/?sbsearch=Styles)                              |
| XML                            | Endpoints que aceptan o responden con datos XML.                                                                                                                                                                               | [Representación de XML](https://swagger.io/docs/specification/v3_0/data-models/representing-xml/?sbsearch=xml)                        |
