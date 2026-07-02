---
title: Aangepaste Iconen
deprecated: false
hidden: false
metadata:
  robots: index
---
## Font Awesome

ReadMe laadt Font Awesome 6's [Regular](https://fontawesome.com/search?s=regular\&f=classic\&o=r) en [Duotone](https://fontawesome.com/search?s=solid\&f=duotone\&o=r) bibliotheken, en je kunt ze gebruiken in je documentatie!

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

### Toegankelijkheid

Als een icoon decoratief wordt gebruikt, kun je het markeren als verborgen. Bijvoorbeeld door het naast een passend tekstlabel te plaatsen:

```html
<button>
  <i aria-hidden="true" class="fa-duotone fa-solid fa-computer-classic"></i>
  Download to Floppy
</button>
```

Als je icoon semantisch geïnterpreteerd moet worden, gebruik dan het `aria-label` attribuut:

```html
<i aria-label="Download to Floppy" class="fa-duotone fa-solid fa-computer-classic"></i>
```

Je kunt de [documentatie over toegankelijkheid](https://docs.fontawesome.com/web/dig-deeper/accessibility) van Font Awesome raadplegen voor meer informatie.