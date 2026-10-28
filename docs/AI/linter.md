---
title: Linter
deprecated: false
hidden: false
metadata:
  robots: index
---
El Linter automatiza la validación de contenido al contrastar la documentación con la guía de estilo y los estándares de redacción establecidos de tu empresa. Optimiza el proceso de revisión manual que los redactores suelen realizar con herramientas externas.

Puedes configurar reglas personalizadas para exigir el formato del código, la elección de palabras y el cumplimiento del estilo interno y las prácticas recomendadas. Ya sea que tu documentación incluya HTML personalizado o extensos ejemplos de código, el Linter garantiza la coherencia en todos tus documentos.

<PlanTable currentPlan="Startup" />

## Configurar {#configure}

Puedes agregar prompts al Linter clasificados como guía de estilo, errores o advertencias.

<Image border={false} src="https://files.readme.io/6844539c6c370fbc5fe87fa2bab007e50aa4fb52673fa629d247d0836534c971-image.png" />

**Guía de estilo**: describe qué hace que una documentación sea excelente y el Linter calificará tu contenido. Ejemplo:

> Mantenlo breve:
>
> El texto breve siempre es mejor. Los párrafos cortos son más fáciles de leer. Intenta mantener los encabezados en una sola línea. Los encabezados de dos líneas ocupan el doble de espacio vertical. Usa palabras cortas en los encabezados; si un cliente usa fuentes más grandes para mejorar la accesibilidad, las palabras largas pueden dividirse entre líneas.

<br />

> Claridad:
>
> Texto claro y conciso para facilitar el escaneo visual y la legibilidad. Ve al grano para que los usuarios puedan encontrar fácilmente lo que necesitan. No uses palabras innecesarias.

<br />

> Tono natural y humano:
>
> Usa palabras cotidianas que sean fáciles de entender. Menos formal pero más profesional que una conversación diaria. Ocasionalmente, usa un tono divertido para momentos de celebración, pero nunca para texto informativo. Sé cálido y servicial con los usuarios que leen la documentación.

<br />

**Errores**: reglas que se pueden comprobar de forma objetiva. Ejemplo:

> Escribe ReadMe con las mayúsculas correctas:
>
> Incorrecto: Readme
>
> Correcto: ReadMe

<br />

> Envuelve los elementos de código entre comillas invertidas (\`):
>
> Incorrecto: Ejecuta npm install –g my–package
>
> Correcto: Ejecuta `npm install –g my–package`

<br />

> Marca el texto provisional como TODO, FIXME o Lorem ipsum
>
> Ejemplo: TODO: Agregar descripción e imagen a esta función

<br />

**Advertencias**: para señalar problemas que pueden ser subjetivos. Ejemplo:

> Lenguaje dubitativo:
>
> Evita usar un lenguaje dudoso o excesivamente cauteloso. Resta confianza y hace que tus instrucciones sean menos directas. Opta por un lenguaje claro y seguro.
>
> Incorrecto: Podrías considerar instalar la versión más reciente.
>
> Correcto: Puedes instalar la versión más reciente para acceder a nuevas funciones.

<br />

> Redacción débil:
>
> Evita la redacción débil como ‘Puedes’ o ‘Hay’. Estas frases ocultan la acción, hacen que la redacción sea menos directa y a menudo añaden palabras innecesarias. Una buena documentación es clara y está orientada a la acción.
>
> Incorrecto: Puedes configurar la API editando el archivo de configuración.
>
> Correcto: Configura la API editando el archivo de configuración.

<br />

> Voz activa:
>
> Evita usar la voz pasiva. La voz activa es más clara, más breve y le dice al lector exactamente quién está haciendo qué.
>
> Incorrecto: El token es generado cuando el usuario inicia sesión.
>
> Correcto: El sistema genera un token cuando el usuario inicia sesión.

<br />

## Ejecutar el Linter {#running-the-linter}

Una vez configurado, al ejecutar el Linter se revisa tu página en función de tus prompts. Los problemas se pueden corregir automáticamente con el Agent.

<Image align="center" border={false} width="350px" src="https://files.readme.io/02345a8505f8f89eaa3d97019252e3cfc3c9e16fdaed63ac7ed7b6df97b765f5-linter.png" />

<br />

## Preguntas frecuentes {#faq}

<Accordion title="¿Dónde debo enviar comentarios o preguntas?" icon="fa-messages-question">
  Envía comentarios o preguntas por correo electrónico a [beta@readme.io](mailto:beta@readme.io)
</Accordion>

<Accordion title="¿Qué modelo utiliza el Linter?" icon="fa-wand-sparkles">
  En este momento usamos Gemini 2.5 Flash, aunque eso podría cambiar a medida que realizamos ajustes para equilibrar la calidad y la velocidad. En el futuro, los usuarios tendrán la opción de seleccionar los modelos que prefieran.
</Accordion>
