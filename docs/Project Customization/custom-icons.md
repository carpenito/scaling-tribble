---
title: Icônes personnalisées
deprecated: false
hidden: false
metadata:
  robots: index
---
## Font Awesome

ReadMe charge les bibliothèques [Regular](https://fontawesome.com/search?s=regular\&f=classic\&o=r) et [Duotone](https://fontawesome.com/search?s=solid\&f=duotone\&o=r) de Font Awesome 6, et vous pouvez les utiliser dans votre documentation !

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

### Accessibilité

Si une icône est utilisée à titre décoratif, vous pouvez la marquer comme masquée. Par exemple, en l'utilisant à côté d'un libellé textuel approprié :

```html
<button>
  <i aria-hidden="true" class="fa-duotone fa-solid fa-computer-classic"></i>
  Download to Floppy
</button>
```

Si votre icône doit être interprétée de manière sémantique, utilisez l'attribut `aria-label` :

```html
<i aria-label="Download to Floppy" class="fa-duotone fa-solid fa-computer-classic"></i>
```

Vous pouvez consulter la [documentation sur l'accessibilité](https://docs.fontawesome.com/web/dig-deeper/accessibility) de Font Awesome pour plus d'informations.