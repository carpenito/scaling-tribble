---
title: Icone Personalizzate
excerpt: >-
  Come utilizzare le icone Font Awesome nella documentazione ReadMe, inclusi
  esempi di accessibilità e best practices.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
## Font Awesome

ReadMe carica le librerie [Regular](https://fontawesome.com/search?s=regular\&f=classic\&o=r) e [Duotone](https://fontawesome.com/search?s=solid\&f=duotone\&o=r) di Font Awesome 6, e puoi utilizzarle nella tua documentazione!

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

### Accessibilità

Se un'icona viene utilizzata a scopo decorativo, puoi contrassegnarla come nascosta. Ad esempio, utilizzandola accanto a un'etichetta di testo appropriata:

```html
<button>
  <i aria-hidden="true" class="fa-duotone fa-solid fa-computer-classic"></i>
  Scarica su Floppy
</button>
```

Se la tua icona dovrebbe essere interpretata semanticamente, utilizza l'attributo `aria-label`:

```html
<i aria-label="Scarica su Floppy" class="fa-duotone fa-solid fa-computer-classic"></i>
```

Puoi consultare la [documentazione di Font Awesome sull'accessibilità](https://docs.fontawesome.com/web/dig-deeper/accessibility) per ulteriori informazioni.