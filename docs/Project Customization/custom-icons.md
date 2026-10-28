---
title: Iconos personalizados
deprecated: false
hidden: false
metadata:
  robots: index
---
## Font Awesome {#font-awesome}

ReadMe carga las bibliotecas [Regular](https://fontawesome.com/search?s=regular\&f=classic\&o=r) y [Duotone](https://fontawesome.com/search?s=solid\&f=duotone\&o=r) de Font Awesome 6, ¡y puedes usarlas en tu documentación!

<HTMLBlock>{`
<div class="Flex">
  <i class="fa-duotone fa-solid fa-house"></i>
  <i class="fa-duotone fa-solid fa-copyright"></i>
  <i class="fa-duotone fa-solid fa-bomb"></i>
  <i class="fa-duotone fa-solid fa-umbrella"></i>
  <i class="fa-duotone fa-solid fa-paper-plane"></i>
  <i class="fa-duotone fa-solid fa-computer-classic"></i>
  <i class="fa-duotone fa-solid fa-crab"></i>
  <i class="fa-duotone fa-solid fa-bullseye-pointer"></i>
  <i class="fa-duotone fa-solid fa-wheelchair-move"></i>
  <i class="fa-duotone fa-solid fa-table-tennis-paddle-ball"></i>
</div>
`}</HTMLBlock>

```
<i class="fa-duotone fa-solid fa-house"></i>
<i class="fa-duotone fa-solid fa-copyright"></i>
<i class="fa-duotone fa-solid fa-bomb"></i>
<i class="fa-duotone fa-solid fa-umbrella"></i>
<i class="fa-duotone fa-solid fa-paper-plane"></i>
<i class="fa-duotone fa-solid fa-computer-classic"></i>
<i class="fa-duotone fa-solid fa-crab"></i>
<i class="fa-duotone fa-solid fa-bullseye-pointer"></i>
<i class="fa-duotone fa-solid fa-wheelchair-move"></i>
<i class="fa-duotone fa-solid fa-table-tennis-paddle-ball"></i>
```

***

### Accesibilidad {#accessibility}

Si un icono se utiliza de forma decorativa, puedes marcarlo como oculto. Por ejemplo, al usarlo junto a una etiqueta de texto adecuada:

```html
<button>
  <i aria-hidden="true" class="fa-duotone fa-solid fa-computer-classic"></i>
  Download to Floppy
</button>
```

Si tu icono debe interpretarse semánticamente, utiliza el atributo `aria-label`:

```html
<i aria-label="Download to Floppy" class="fa-duotone fa-solid fa-computer-classic"></i>
```

Puedes consultar la [documentación sobre accesibilidad](https://docs.fontawesome.com/web/dig-deeper/accessibility) de Font Awesome para obtener más información.
