---
title: Aangepaste CSS & JavaScript
deprecated: false
hidden: false
metadata:
  robots: index
---
In dit gedeelte kunt u CSS en Javascript toevoegen om het uiterlijk van uw documentatiesite verder aan te passen.

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

> 🚧 Selectors
>
> Gebruik `.rm-` vooraf bepaalde selectors. Gehashte selectors veranderen voortdurend en **mogen niet** worden gebruikt als selectors (bijv. `Header-bottom2eLKOFXMEmh5`).

## Aangepast Stylesheet

<Callout icon="📘" theme="info">
  Beperk uw wijzigingen tot kleine aanpassingen. Bovendien zijn stylesheets niet versiegebonden; alle versies gebruiken hetzelfde stylesheet.
</Callout>

## Aangepast Javascript

Uw Javascript wordt onderaan de pagina opgenomen.

<details>
  <summary><b>Globale Variabelen</b></summary>

  ReadMe stelt bepaalde globale variabelen beschikbaar om u te helpen de gebruikerservaring van uw hub aan te passen:

  * **`RM_ReferenceSidebarScrollTopOffset`**\
    Pixeloffset voor de scroll-naar-actief-item zijbalklogica in doorlopende <Glossary>Referentie</Glossary> secties.
</details>

## Aangepaste Include-tags

**Header HTML**

Elke html hier wordt opgenomen in de head-tag, wat handig is voor zaken zoals metatags en het laden van externe CSS of JS.

**Footer HTML**  
​  
Dit wordt direct vóór de `</body>` tag geplaatst. Handig voor zaken zoals analyses en tracking.

## Aangepast Javascript en CSS in- of uitschakelen

Voeg de `?disableCustomCss=true&disableCustomJs=true` queryparameters toe aan het einde van elke URL.