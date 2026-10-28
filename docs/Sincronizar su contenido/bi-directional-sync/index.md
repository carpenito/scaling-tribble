---
title: Sincronización bidireccional
deprecated: false
hidden: false
metadata:
  robots: index
---
La sincronización bidireccional crea una conexión bidireccional entre tu proyecto de ReadMe y un repositorio de GitHub o GitLab. Este flujo de trabajo opcional mantiene el contenido uniforme en ambas plataformas:

- Escribe en tu entorno preferido, ya sea ReadMe o tu configuración de desarrollo local.
- Los desarrolladores, ingenieros y redactores técnicos pueden colaborar utilizando las herramientas que prefieran.
- Los cambios se sincronizan automáticamente entre ReadMe y Git, creando una única fuente de verdad.

<PlanTable currentPlan="Startup" />

***

## Configurar la sincronización bidireccional {#setting-up-bi-directional-sync}

ReadMe admite la sincronización bidireccional tanto con <Anchor label="GitHub" target="_blank" href="https://docs.readme.com/main/docs/sync-with-github">GitHub</Anchor> como con <Anchor label="GitLab" target="_blank" href="https://docs.readme.com/main/docs/sync-with-gitlab">GitLab</Anchor>.

Para sincronizar con GitHub, puedes conectarte a GitHub Cloud. Si estás en el plan Enterprise, ReadMe admite la sincronización bidireccional con <Anchor label="GitHub Enterprise Server" target="_blank" href="https://docs.readme.com/ent/docs/connecting-github-enterprise-server">GitHub Enterprise Server</Anchor>.

<Image align="center" border={true} src="https://files.readme.io/6335bcb6aa344d9d1f23d11b3cf420cbe94493872630760fb04d2cce9df10189-Screenshot_2025-10-27_at_12.29.28_PM.png" className="border" />

<Callout icon="❗️" theme="error">
  El repositorio con el que te sincronices debe estar vacío (sin confirmaciones ni archivos, por ejemplo, README.md) antes de conectarlo a ReadMe. Puedes agregar o eliminar archivos después de la configuración.
</Callout>

***

## Control de versiones de la documentación {#documentation-versioning}

Si tu proyecto de ReadMe utiliza varias [Versiones](doc:versions), solo la versión principal se sincroniza inicialmente cuando activas la sincronización bidireccional por primera vez. Después de activar con éxito la sincronización bidireccional, cualquier cambio en las demás versiones se sincronizará con tu repositorio de Git.

***

## Editar tu documentación {#editing-your-docs}

Una vez configurada tu conexión de Git, todos los cambios realizados en el editor de ReadMe se sincronizarán automáticamente con tu repositorio de Git, y viceversa. Al editar la documentación en Git, puedes usar tu editor de código o herramientas de Git preferidos

Para garantizar una sincronización correcta de _Git a ReadMe_, sigue estas pautas de estructura:

**Archivos Markdown:**

- Los archivos deben incluir el frontmatter obligatorio: `title` y `summary`
- El contenido debe estar escrito en formato Markdown estándar
- Los nombres de los archivos deben coincidir con el slug de URL previsto para un enrutamiento adecuado

**Navegación:**

- El orden de las páginas se define mediante archivos `_order.yaml`
- Cada carpeta de categoría puede tener su propio `order.yaml`
- La [estructura de navegación](https://docs.readme.com/main/docs/documentation-structure#/) en Git refleja la jerarquía de tu proyecto de ReadMe

**[Ramas](https://docs.readme.com/main/docs/branches#/)**

- El commit inicial desde ReadMe sirve para establecer la sincronización de ramas con GitHub
- Los nombres de las ramas deben coincidir exactamente con los nombres de las versiones definidos en ReadMe
- Cualquier versión y nombre que no coincida existirá en GitHub y no se sincronizará con ReadMe.

<HTMLBlock>{`
<div class="migrating-column">
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-hexagon-exclamation"></i> No sincronizado
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2-new-branch
		</pre>
  </section>
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-circle-check"></i> Sincronizado
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2.0_new-branch
		</pre>
  </section>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<!-- style guide CSS -->
<style>
  .migrating-column {
    border: 1px solid var(--color-border-default);
    border-radius: var(--border-radius);
    display: flex;
    justify-content: center;
    
    + .migrating-column {
      margin-top: 1em;
    }
    
    section {
      flex: 1 1 50%;
      overflow: hidden;
      
      + section {
        border-left: 1px solid var(--color-border-default);
      }
    }
    
    pre {
      background: transparent;
      border: 0;
      border-radius: 0;
      font-size: 0.8em;
      margin: 0;
      overflow: auto;
      padding: 15px;
      
      + pre {
        border-top: 1px solid var(--color-border-default);
      }
    }
    
    header {
      align-items: center;
      border-bottom: 1px solid var(--color-border-default);
      display: flex;
      font-size: 15px;
      font-weight: var(--font-weight-bold);
      gap: 0.5em;
      padding: 1em;
    }

    .fa-circle-check {
      color: var(--green);
    }

    .fa-hexagon-exclamation {
      color: var(--red);
    }
  }
</style>
`}</HTMLBlock>

### Gestión de conflictos {#handling-conflicts}

Cuando se detecte un conflicto al guardar en ReadMe, el sistema te preguntará inmediatamente si deseas sobrescribir los cambios de Git o cancelar el guardado y continuar editando. Los cambios guardados en ReadMe siempre coincidirán con lo que se publique.

Al fusionar desde GitHub, el usuario puede resolver los conflictos a través del editor de GitHub o con la herramienta de fusión de su elección localmente antes de hacer push.

***

## Preguntas frecuentes {#faq}

<Accordion title="¿Cómo se integra ReadMe con GitHub y qué permisos se requieren?" icon="fa-question-circle">
  ReadMe utiliza una GitHub App con acceso a nivel de repositorio: solo lectura para metadatos (obligatorio) y lectura/escritura para sincronizar contenido. Los webhooks gestionan las sincronizaciones, la detección de cambios y la resolución de conflictos.
</Accordion>

<Accordion title="¿Por qué no aparecen mis ramas en GitHub o GitLab?" icon="fa-question-circle">
  Las ramas nuevas que crees después de activar la sincronización bidireccional crearán automáticamente una rama correspondiente en las herramientas de Git, pero las ramas existentes no crearán una rama correspondiente en las herramientas de Git hasta que guardes un cambio en esa rama en ReadMe.
</Accordion>

<Accordion title="¿Qué permisos se requieren para sincronizar con GitLab?" icon="fa-question-circle">
  ReadMe solicita acceso a:

  - `read_api` para listar proyectos
  - `read_user` y `read_profile` para mostrar la información del usuario
  - `read_repository` para sincronizar el contenido de GitLab con ReadMe
  - `write_repository` para sincronizar el contenido de ReadMe con GitLab
</Accordion>
