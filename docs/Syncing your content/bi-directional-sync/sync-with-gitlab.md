---
title: Sincronizar con GitLab
deprecated: false
hidden: false
metadata:
  robots: index
---
## Cómo configurar la sincronización bidireccional con GitLab {#how-to-set-up-bi-directional-sync-with-gitlab}

### Requisitos previos {#prerequisites}

- Necesitarás una cuenta de GitLab.
- Al sincronizar con un repositorio de una organización, necesitarás permisos para crear un **repositorio vacío**.

<Image align="center" border={false} src="https://files.readme.io/d2a12db436be321b972fd817432f3754a13d61c0ecb915202862e58fb2252cc1-Screenshot_2025-10-31_at_1.43.41_PM.png" />

### Configuración {#set-up}

1. Navega a la página **Settings** > **Git Connection**.
2. Selecciona GitLab.
3. Si aún no lo has hecho, crea un repositorio vacío en [GitLab](https://docs.gitlab.com/user/project/)—asegúrate de desmarcar la opción para crear un README.
4. **Sincroniza** con tu proveedor y autentícate.
5. Crea un token de acceso personal con el ámbito `api`. Puedes eliminar este token después de completar la configuración. ReadMe utiliza este token una sola vez durante la configuración para crear el webhook en tu repositorio y no se almacena.
   1. Para los tokens de acceso de proyectos, necesitarás el rol Maintainer. Sin embargo, no se recomienda, ya que existe un límite en la cantidad de tokens de acceso de proyectos que se pueden crear, dependiendo de los precios de GitLab.

<Image border={false} src="https://files.readme.io/b350ddb7403c7d0ffbaa7d4f8e4c5fc6ca0d92308c4c81bde90b2c2b146a1ed3-image.png" />

6. Añade el token de acceso a ReadMe y haz clic en el icono de webhook para crear los webhooks necesarios para mantener tu contenido sincronizado con GitLab.

***

## Cambiar de repositorio {#changing-repositories}

Si necesitas conectar tu proyecto de ReadMe a un repositorio diferente, debes desconectar el repositorio original usando el icono de la papelera.

1. Dentro de ReadMe, desconecta el proyecto mediante el icono de la papelera.
2. Dentro de GitLab, crea un nuevo proyecto vacío.
3. Vuelve a ReadMe y selecciona el proyecto con el que te gustaría sincronizar.

***

## Ramas protegidas {#protected-branches}

Todas las reglas de ramas deben permitir hacer push al usuario (que está sincronizando con GitLab desde ReadMe).

<Image border={false} src="https://files.readme.io/5ab0dbdd08ca7f9fc31d8a6895ebb9a970819ea4f2c352c92307ab5886b14541-image.png" />

## Preguntas frecuentes {#faq}

<Accordion title="¿Qué permisos se requieren al sincronizar con GitLab?" icon="fa-question-circle">
  ReadMe solicita acceso a:

  - `read_api` para listar proyectos
  - `read_user` y `read_profile` para mostrar información del usuario
  - `read_repository` para sincronizar el contenido de GitLab con ReadMe
  - `write_repository` para sincronizar el contenido de ReadMe con GitLab
</Accordion>

<br />
