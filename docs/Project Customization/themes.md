---
title: Thema's
deprecated: false
hidden: false
metadata:
  robots: index
---
Alle abonnementen hebben toegang tot aanpassing via de **Thema**-instellingen. Open **Instellingen** linksboven in de beheerinterface en selecteer vervolgens **Thema** in de zijbalk.

* Indeling
* Huisstijl (Logo, Favicon en Kleuren)
* Headerstijl

<PlanTable currentPlan="Free" />

<Callout icon="💁‍♂️" theme="default">
  **Opmerking:** Aanvullende aanpassingsopties en services zijn beschikbaar op Business- en Enterprise-abonnementen.
</Callout>

***

## Indeling

<Image align="center" border={false} width="400px" src="https://files.readme.io/3d30b1d7f55cd7e37def92bb05c5c4799bc0e1294169209626ff9a24181733cc-Launch_Week-20250628-1026262x.webp" />

Je kunt kiezen uit 3 indelingsopties: Klassiek, Compact en Modern. Er is ook een optie om de indeling uit te rekken voor grotere schermen. Je kunt een voorbeeld van de indeling bekijken voordat je opslaat.

<Callout icon="🚧" theme="warn">
  Een optie met alleen een zijbalk komt binnenkort!
</Callout>

***

## Huisstijl

### Logo

Een optie om een wit logo te uploaden is beschikbaar wanneer een alternatief nodig is voor bepaalde thema's en headerkleurinstellingen.

**Formaat**

* SVG heeft de voorkeur voor de beste kwaliteit.
* Als je logo te complex is voor een SVG, is WEBP een goed alternatief—gebruik 2x van je gewenste logogrootte voor duidelijkheid op hoge-resolutieschermen.
* GIF's worden niet ondersteund.

**Afmetingen**

* Standaard 24px hoogte. In de Klassieke en Moderne thema's kun je een grotere logohoogte van 40px selecteren.

**Verdere aanpassing**

* Klanten met toegang tot Aangepaste CSS kunnen onze globale klassen en CSS-variabelen gebruiken om de weergave van hun logo verder aan te passen:

```css
.rm-Logo-img {
  --Header-logo-height: YOUR_CUSTOM_HEIGHT
}
```

***

## Header

<Image align="center" border={false} width="400px" src="https://files.readme.io/9c14d52d69809626037d9cb483cd2fb0619734f6ccc3c3428fd6380936a44b43-Launch_Week-20250628-1043112x.webp" />

Je kunt kiezen uit 4 indelingsopties: Lijn, Effen kleur, Verloop en Overlay.

<Callout icon="💁‍♂️" theme="default">
  De Lijn-headeroptie gebruikt nu standaard een tabbladweergave voor links. Gebruikers met de oudere knopweergave kunnen overschakelen. Zodra je overschakelt, kun je niet meer terugschakelen.
</Callout>

**Verdere aanpassing**

* Klanten met toegang tot Aangepaste CSS kunnen onze globale klassen en CSS-variabelen gebruiken om hun header verder aan te passen:

```css
.rm-Header {
  --Header-background: YOUR_CUSTOM_VALUE /* defaults to your brand color */
  --Header-border-color: YOUR_CUSTOM_VALUE /* default: rgba(0, 0, 0, 0.1) */
  --Header-button-padding: YOUR_CUSTOM_VALUE /* default: 10px */

  /* Line theme only */
  --Header-tab-underline: YOUR_CUSTOM_VALUE /* defaults to your brand color */
}
```