---
title: Ramas
deprecated: false
hidden: false
metadata:
  robots: index
---
¡Con las ramas, puedes seguir editando como siempre lo has hecho! Las ramas son un flujo de trabajo opcional que ofrece flexibilidad en tu proceso de redacción. Los redactores usan las ramas para:

- Realizar cambios y revisarlos en un entorno de vista previa antes de que se publiquen.
- Enviar cambios a compañeros de equipo para su revisión.
- Realizar cambios en múltiples páginas.

<PlanTable currentPlan="Business" />

<Callout icon="💼" theme="default">
  **Nota:** Las opciones de revisión adicionales solo están disponibles en los planes Enterprise.
</Callout>

***

## Crear una rama {#creating-a-branch}

Hay tres formas de crear una rama:

1. Ve al menú de versiones y ramas. Una vez allí, puedes crear nuevas ramas a partir de una versión.
2. Al editar una versión, en lugar de guardar, puedes guardar en una nueva rama.
3. Si te estás [sincronizando con GitHub](https://docs.readme.com/main/docs/bi-directional-sync), las ramas creadas en GitHub aparecerán en ReadMe. ¡Y las ramas creadas en la interfaz de usuario de ReadMe aparecerán automáticamente en GitHub!

Una vez creada la rama, ¡puedes empezar a escribir! Los cambios no se publicarán hasta que fusiones tu rama con una versión pública.

<Image align="center" border={false} src="https://files.readme.io/65abcb59c51a4be0b668815cf0046ee818e93228057a6bff5ddbe4d3a4b9b97e-Getting_Started_with_Owlberts_Journeys-20250512-1502362x.webp" />

No hay límite de tiempo ni caducidad en las ramas. Cualquier administrador de tu equipo puede ver, editar, fusionar y eliminar cualquier rama.

***

## Revisar cambios {#reviewing-changes}

<Image align="center" alt="Pestaña de revisión que muestra la diferencia entre dos páginas línea por línea" border={false} src="https://files.readme.io/95ab92ffd9eec49ad16b279f1e4a66de1f54cc95eb121f43c381258fb1d7915e-Review-20251104-1847122x.webp" />

Al editar una rama, puedes acceder a la pestaña de revisión para comparar los cambios realizados en tu rama.

<Callout icon="☝️" theme="default">
  Al reordenar archivos, se representan como cambios en el archivo `_order` de tu documentación. Cada elemento en el archivo `_order` representa una página en tu documentación y coincide con el slug de cada página
</Callout>

Los clientes con la función de revisión también pueden marcar ramas como listas para revisión, lo que añade una insignia en el menú de versiones y ramas e inicia el [AI Linter](https://docs.readme.com/main/docs/linter). Los usuarios pueden omitir los requisitos de fusión marcando la casilla "Fusionar sin cumplir los requisitos" para habilitar el botón **Fusionar**.

***

## Fusionar cambios {#merging-changes}

Una vez que tengas todo listo para que los cambios se publiquen, puedes fusionar desde el menú de la rama:

<Image align="center" border={false} width="300px" src="https://files.readme.io/0c4c2909e376be33b974e008b8b9b9f14860b13c3eff12b5be8a377395fd68e4-Getting_Started_with_Owlberts_Journeys-20250528-1418472x.png" />

Al fusionar, se ejecutará una verificación para garantizar que no haya conflictos de fusión. Si hay conflictos que deban resolverse, recomendamos [resolver los conflictos desde GitHub](https://docs.readme.com/main/docs/branches#/handling-conflicts). Si tu proyecto no se sincroniza con GitHub, puedes ignorar el conflicto y forzar la fusión de los cambios, dando preferencia a los cambios de la rama.

Una vez fusionadas, tus ramas no se eliminan para que puedas revisar los cambios antes de eliminarlas.

<Callout icon="💁‍♂️" theme="default">
  Los usuarios de GitHub también pueden fusionar una rama en una versión, incluso a través de Pull Requests.
</Callout>

### Restringir la fusión a administradores {#restricting-merge-to-admins}

Los clientes de Enterprise pueden restringir el acceso de fusión por proyecto a [Solo administradores o Administradores y editores](https://docs.readme.com/ent/docs/user-roles/). La configuración se encuentra en la página de proyectos del panel de Enterprise. Abre **Configuración** > **Nombre de Enterprise** (en la parte inferior) > **Proyectos**

***

## Sincronización con GitHub {#syncing-with-github}

No es necesario sincronizar con GitHub para usar ramas.

Al crear ramas desde GitHub, su nombre debe tener el formato adecuado para incluir su versión: `{version}_{branch}`. Ejemplos:

```
v2.0_rewrite-getting-started
v2.0_add-new-feature
v2.0_fix-typo
```

### Acceso y permisos {#access--permissions}

Los permisos de ReadMe y GitHub son independientes. Los usuarios con acceso a las ramas de tu proyecto de GitHub tendrán acceso a cualquier cambio de contenido. Para que los usuarios puedan ver los cambios de contenido realizados en las ramas a través de GitHub, necesitarán una cuenta de ReadMe con acceso a la rama de tu proyecto.

### Gestión de conflictos {#handling-conflicts}

Al fusionar desde GitHub, el usuario puede resolver conflictos a través del editor de GitHub o con la herramienta de fusión de su elección localmente antes de hacer push.

Al fusionar desde ReadMe, los cambios que ves en la vista previa siempre coincidirán con lo que se publica al fusionar. Los cambios en conflicto de GitHub no aparecerán.

***

## Preguntas frecuentes {#faq}

<Accordion title="¿Quién puede ver una rama?" icon="fa-help-circle">
  Solo los compañeros de equipo con acceso a tu proyecto pueden ver tus ramas, incluidos los roles de editor y visualizador del equipo.
</Accordion>
