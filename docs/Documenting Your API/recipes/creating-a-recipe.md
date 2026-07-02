---
title: Een Recipe aanmaken
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overzicht

Klaar om je codevoorbeelden om te zetten in ontwikkelaarsvriendelijke leerervaringen? Deze gids leidt je stap voor stap door het maken van je eerste Recipe. Je leert hoe je complexe code opsplitst in begrijpelijke stappen, nuttige annotaties toevoegt en de visuele weergave aanpast aan je huisstijl.

<br />

<Image align="center" border={false} src="https://files.readme.io/05e72a5519ad6e9421775f6688bbee366623e93528abf9df93dd5ae1973b81dd-Screenshot_2025-05-22_at_2.16.36_PM.png" />

<br />

## Voordat je begint

* Zorg dat je codevoorbeeld klaar is (of weet welk API-endpoint je als startpunt wilt gebruiken)
* Controleer of de sectie Recipes toegankelijk is in je ReadMe-project
* Bedenk welke programmeertalen je ontwikkelaars het meest gebruiken
* Denk na over de belangrijkste leerdoelen voor deze specifieke code-walkthrough

## Een Recipe aanmaken

<Image border={false} src="https://files.readme.io/4482047-Screen_Shot_2020-12-01_at_3.42.35_PM.png" />

### 1. Open de Recipe Editor

Navigeer naar je ReadMe-project en klik op **Bewerken** om de bewerkingsinterface te openen. Selecteer in de hoofdnavigatie **Recipes** om naar het Recipe-beheergebied te gaan. Klik op de knop **Nieuw Recipe aanmaken** om de Recipe-builder te starten.

<Image align="center" border={false} src="https://files.readme.io/139f1a2224d1add344a0071284be7614929b7cac5be5babf7cb0860b16b9f81e-Screenshot_2025-05-22_at_12.47.08_PM.png" />

### 2. Configureer je codevoorbeeld

1. Selecteer in het paneel rechtsboven je programmeertaal uit het dropdownmenu.
2. Voeg je codevoorbeeld toe en zorg ervoor dat het correct is opgemaakt met syntaxismarkering. Dit vormt de basis waarnaar je stapsgewijze annotaties zullen verwijzen.

<Image align="center" border={false} src="https://files.readme.io/91f78f372bffaf5521f48ba6972275b5d3fa1b74cf4b4f917a5d7284a6d51c11-Screenshot_2025-05-22_at_2.09.51_PM.png" />

**Opmerking:** Elke Recipe kan meerdere programmeertalen ondersteunen, zodat je na het instellen van de eerste taal extra taalversies kunt toevoegen.

### 3. Bouw je stapsgewijze annotaties

Maak in de linker zijbalk je gemarkeerde stappen aan die ontwikkelaars door je code begeleiden. Voor elke stap:

* Schrijf een duidelijke, beschrijvende titel die uitlegt wat dit deel van de code doet
* Voeg gedetailleerde uitleg toe die ontwikkelaars helpt het "waarom" achter elke sectie te begrijpen
* Geef de regelnummers op die voor deze stap gemarkeerd moeten worden
* Gebruik toegankelijke taal die complexe concepten begrijpelijk maakt

Elke stap moet zich richten op een specifiek concept of een specifieke actie binnen je codevoorbeeld, zodat het begrip geleidelijk wordt opgebouwd.

<Image border={false} src="https://files.readme.io/cece453-Screen_Shot_2020-12-01_at_3.49.54_PM.png" />

### **4. Voeg responsvoorbeelden toe**

Neem in het paneel rechtsonder de verwachte API-respons op wanneer je code succesvol wordt uitgevoerd. Dit laat ontwikkelaars precies zien hoe succes eruitziet en helpt hen hun implementatie te verifiëren.

Als je code geen respons genereert (of als het tonen ervan niet relevant is), kun je deze sectie leeg laten — deze wordt automatisch verborgen in de definitieve Recipe.

**Opmerking:** Gebruikersdatavariabelen werken ook in Recipes! Als je gepersonaliseerde docs hebt ingesteld, kun je dynamische inhoud in je responsen opnemen.

> 👍 Gebruikersdatavariabelen werken in Recipes!
>
> Als je [variabelen](doc:personalized-docs) in je documentatie hebt, bijvoorbeeld doorgegeven via de Personalized Docs Webhook, werken ze ook in Recipes!

### 5. Pas de visuele weergave aan

Schakel over naar het tabblad **Weergave** om je Recipe een eigen stijl te geven:

* **Selecteer een emoji**: Klik op het emoji-pictogram om een keuze te maken uit het dropdownmenu
* **Stel de achtergrondkleur in**: Gebruik de kleurkiezer om een achtergrond te selecteren die bij je huisstijl past (ondersteunt RGB-, HSL- of HEX-waarden)
* **Schrijf een beschrijving**: Voeg een gedetailleerde beschrijving toe die verschijnt op de grotere Recipe-kaart in je Recipes-sectie

De kleur van de knop _Recipe openen_ wordt automatisch overgenomen van de linkkleurinstellingen van je project.

<Image border={false} src="https://files.readme.io/ea6500f-Screen_Shot_2020-10-19_at_12.41.19_PM.png" />

### **6. Kies insluitlocaties**

Bepaal waar je Recipe in je documentatie moet verschijnen:

* **API Reference-insluiting**: Selecteer specifieke endpoints waar deze Recipe relevante context biedt
* **Recipes-sectie**: Je Recipe verschijnt automatisch in het hoofdgedeelte Recipes zodra het is gepubliceerd
* **Gids-insluiting**: Je kunt de Recipe later handmatig insluiten in gidspagina's via de Recipe-widget

Selecteer de selectievakjes naast relevante endpoints om je Recipe precies daar toegankelijk te maken waar ontwikkelaars het het meest nodig hebben.

De Recipe verschijnt als een klikbare kaart, zoals weergegeven in het voorbeeldgebied van de stap Weergave.

<Image border={false} src="https://files.readme.io/20cf1e2-Screen_Shot_2020-12-03_at_5.14.16_PM.png" />

<br />

<Image border={false} src="https://files.readme.io/e4619b5-Screen_Shot_2020-12-01_at_2.59.43_PM.png" />

<br />

<Callout icon="🚧" theme="warn">
  Insluitingen verschijnen niet in de Reference-sectie [totdat de Recipes-sectie is ingeschakeld](#enable-recipes-section).
</Callout>

<br />

### 7. Stel de publicatiestatus in

Kies het zichtbaarheidsniveau van je Recipe:

* **Niet gepubliceerd**: Alleen zichtbaar voor projectbeheerders (standaard voor nieuwe Recipes)
* **Gepubliceerd**: Zichtbaar voor alle gebruikers in je Recipe-collectie
* **Uitgelicht**: Prominent weergegeven bovenaan je Recipes-sectie (slechts één Recipe kan tegelijk worden uitgelicht)

Begin met "Gepubliceerd" om je Recipe beschikbaar te maken voor ontwikkelaars, of houd het op "Niet gepubliceerd" terwijl je de inhoud nog verfijnt.

|                      |                                                                                                                                                                                          |
| :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Uitgelicht**       | Dit is de uitgelichte Recipe bovenaan de Recipes-sectie. Eén Recipe moet worden uitgelicht als je Recipes-pagina openbaar is, en deze moet de status Gepubliceerd hebben. |
| **Gepubliceerd**     | Zichtbaar voor gebruikers in het kaartraster onder de uitgelichte Recipe                                                                                                                 |
| **Niet gepubliceerd**| Niet zichtbaar voor klanten. Nieuwe Recipes zijn standaard niet gepubliceerd.                                                                                                            |

<Image border={false} src="https://files.readme.io/445d0c8-Screen_Shot_2020-12-16_at_3.54.22_PM.png" />

<br />

## Veelgestelde vragen & probleemoplossing

**Kan ik het Recipe-pictogram in de navigatiebalk verwijderen?**

Deze sectie is alleen zichtbaar voor projectbeheerders. Je klanten zien deze sectie niet tenzij je [deze inschakelt](#enabling-your-recipes-page) om hem voor hen zichtbaar te maken.

Naarmate we meer bewerkingsmogelijkheden naar de frontend van je docs hub verplaatsen, zullen we duidelijker maken wat projectbeheerders zien versus wat je klanten zien.

**Hoe verander ik de kleur van de blauwe knop "Recipe openen"?**

De kleur van deze knop wordt overgenomen van de Linkkleur die je hebt ingesteld in de [Thema-editor](/main/docs/design-themes) in je projectinstellingen. Om deze te wijzigen, moet je de Linkkleur voor je gehele ReadMe-hub aanpassen.

**Kan ik de naam van de Recipes-sectie wijzigen, net als de andere secties?**

Nog niet, maar we werken eraan!

**Mijn codemarkering werkt niet correct?** Controleer of je regelnummers kloppen en of je de juiste programmeertaal hebt geselecteerd. Onthoud dat regelnummers beginnen bij 1, niet bij 0.

**De Recipe-widget verschijnt niet in mijn gidsen?** Zorg ervoor dat de Recipes-sectie is ingeschakeld in de navigatie-instellingen van je site. De widget is pas beschikbaar als Recipes zijn geactiveerd voor je project.

**Mijn ingesloten Recipe verschijnt niet op API Reference-pagina's?** Ingesloten Recipes verschijnen pas zodra de Recipes-sectie openbaar is ingeschakeld. Controleer je sitenavigatie-instellingen en zorg ervoor dat er minimaal één Recipe is gepubliceerd.

**De responssectie is verdwenen?** Als je de standaard responsinhoud volledig verwijdert, wordt het responspaneel automatisch verborgen. Voeg inhoud toe om het weer zichtbaar te maken.