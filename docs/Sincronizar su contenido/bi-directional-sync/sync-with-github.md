---
title: Sincronizar con GitHub
deprecated: false
hidden: false
metadata:
  robots: index
---
## Cómo configurar la sincronización bidireccional con GitHub {#how-to-set-up-bi-directional-sync-with-github}

### Requisitos previos {#prerequisites}

- Necesitarás una cuenta de GitHub.
- Al sincronizar con un repositorio de una organización, necesitarás permisos para crear un **repositorio vacío**.

### Configuración {#set-up}

1. Ve a la página **Settings** > **Git Connection**.
2. Selecciona GitHub.
3. Si aún no lo has hecho, crea un repositorio vacío en [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)—asegúrate de desmarcar la opción de crear un README.
4. **Sincroniza** con tu proveedor y autentícate. Concede acceso al repositorio con el que te gustaría sincronizar y confirma tu repositorio en la siguiente pantalla.

***

## Cambiar de repositorio {#changing-repositories}

1. En ReadMe, desconecta el proyecto mediante el icono de la papelera.
2. En GitHub, crea tu nuevo repositorio (debe estar vacío).
3. Ve a **Applications > Installed GitHub Apps**.
4. Busca **ReadMe Sync** y haz clic en **Configure**.
5. En _Repository access_, selecciona el nuevo repositorio con el que te gustaría sincronizar.
6. Vuelve a ReadMe y conéctate a tu nuevo repositorio.

***

## Editar tu documentación {#editing-your-docs}

**[Ramas](https://docs.readme.com/main/docs/branches#/)**

- El commit inicial de ReadMe sirve para establecer la sincronización de ramas con GitHub
- Los nombres de las ramas deben coincidir exactamente con los nombres de versión definidos en ReadMe
- Cualquier versión y nombre que no coincidan existirán en GitHub y no se sincronizarán con ReadMe.

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

***

### GitHub Enterprise Server {#github-enterprise-server}

Si utilizas un **[GitHub Enterprise Server (GHES)](https://docs.readme.com/ent/docs/connecting-github-enterprise-server)** autohospedado, puedes configurar la sincronización desde el panel de control de tu grupo en **Git Connection**. La sincronización requiere un repositorio nuevo y vacío, y cada proyecto secundario solo se puede sincronizar con un repositorio.

<Image align="center" border={false} src="https://files.readme.io/bd2640dae70270e20b0a71ae98adf56bd4e3a59b275b1609e86bbc4fc8ad81cd-GHES.png" />

Si GHES no está disponible para tu proyecto, contacta con tu Customer Success Manager.

### Protección de ramas de GitHub {#github-branch-protection}

Si tu repositorio de GitHub utiliza reglas de protección de ramas, deberás configurarlas para permitir que la aplicación ReadMe Sync envíe cambios mediante push. A continuación te explicamos cómo configurarlo según tu configuración de GitHub:

#### Para GitHub Rulesets (nueva versión) {#for-github-rulesets-new-version}

1. Ve a la configuración de protección de ramas de tu repositorio.
2. En la sección _Bypass list_, haz clic en **+ Add bypass**.
3. Busca _ReadMe Sync_ (App • readmeio) y establece el permiso en **Always allow**.

<Image align="center" alt="Adición de ReadMe Sync a la lista de omisión de GitHub Rulesets para acceso de push directo." border={false} caption="Adición de ReadMe Sync a la lista de omisión de GitHub Rulesets para acceso de push directo." src="https://files.readme.io/0e52415eb4dede062a4d9df4a2d3f06dda62500c26caae7f000e4ecd50f4521d-Screenshot_2024-11-22_at_11.12.14_AM.png" width="600px" />

#### Para la protección de ramas heredada {#for-legacy-branch-protection}

1. Ve a las reglas de protección de ramas de tu repositorio.
2. Busca la sección _Allow specified actors to bypass required pull requests_.
3. Añade _readme-sync_ (ReadMe Sync) a la lista de actores permitidos.

<Image align="center" alt="Configuración de ReadMe Sync en las opciones heredadas de protección de ramas para omitir los requisitos de pull request." border={false} caption="Configuración de ReadMe Sync en las opciones heredadas de protección de ramas para omitir los requisitos de pull request." src="https://files.readme.io/8f3765d6ebbe96f5a93e4c6f915e52392ad6ba1512d0af4d4113ca8ff6ef8077-Screenshot_2024-11-22_at_11.12.07_AM.png" />

Esta configuración garantiza que los cambios realizados en el editor de ReadMe se puedan sincronizar con las ramas protegidas de tu repositorio de GitHub.

***

<br />

## Preguntas frecuentes {#faq}

<Accordion title="¿Cómo se integra ReadMe con GitHub y qué permisos se requieren?" icon="fa-question-circle">
  ReadMe utiliza una GitHub App con acceso a nivel de repositorio: solo lectura para metadatos (obligatorio) y lectura/escritura para sincronizar contenido. Los webhooks gestionan las sincronizaciones, la detección de cambios y la resolución de conflictos.
</Accordion>

<Accordion title="¿Por qué no aparecen mis ramas en GitHub?" icon="fa-question-circle">
  Las nuevas ramas que crees tras habilitar la sincronización bidireccional crearán automáticamente una rama correspondiente en GitHub, pero las ramas existentes no crearán una rama correspondiente en GitHub hasta que guardes un cambio (por pequeño que sea) en esa rama desde ReadMe.
</Accordion>
