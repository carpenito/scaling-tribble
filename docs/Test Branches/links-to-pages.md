---
title: Links naar Pagina's
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
## Interne Links

Om een link tussen pagina's te maken, begin je met het typen van `[` en er verschijnt een scrollbaar menu met beschikbare pagina's om naar te linken. Naarmate je meer tekens typt, verschijnen er relevante opties voor interne paginalinks.

<Image align="center" border={true} src="https://files.readme.io/cff6bf4-link_to_pages.gif" className="border" />

De resulterende Markdown ziet er als volgt uit:

<Image align="center" border={true} src="https://files.readme.io/9b34336-CleanShot_2022-10-18_at_11.19.16.gif" className="border" />

En ziet er voor gebruikers uit als de bovenstaande link!

> 📘 Interne links werken alleen binnen één project.
>
> Als je links maakt tussen meerdere projecten, moet je standaard hyperlinks gebruiken.

 

## Ankerlinks

Alle sectiekoppen bevatten een ankerlink. Het formaat is `#header-name`. Zo zal bijvoorbeeld deze [link](doc:linking-to-pages#anchor-links) je terugbrengen naar deze sectie:

```
[link](doc:linking-to-pages#anchor-links)
```

 

## Externe Links

### Inline Linken

Om inline te linken, typ je de tekst die je wilt linken tussen haakjes, `[x]`, gevolgd direct door de link-URL tussen ronde haakjes, `(y)`.

Links zien er als volgt uit in de Markdown-editor:

```
[ReadMe](readme.com)
```

En resulteren in een link die er zo uitziet: [ReadMe](https://readme.com/)

 

### Referentiestijl Linken

Referentiestijl linken stelt je in staat om een link een nummer of "naam" te geven en er meerdere keren naar te verwijzen.

Als je bijvoorbeeld het onderstaande typt in je dashboard:

```
When I first research something I look at [Wikipedia][1] then at [Google][2] then [Wookiepedia][3].

[1]: https://wikipedia.org            "Wikipedia"
[2]: https://google.com               "Google"
[3]: https://starwars.fandom.com      "Wookiepedia"
```

...zien de links er als volgt uit in je Hub:

Als ik iets voor het eerst onderzoek, kijk ik eerst op [Wikipedia][1], dan op [Google][2] en dan op [Wookiepedia][3].

[1]: https://wikipedia.org "Wikipedia"

[2]: https://google.com "Google"

[3]: https://starwars.fandom.com "Wookiepedia"

 

## Links Openen in een Nieuw Tabblad

Markdown en [RDMD](https://docs.readme.com/rdmd/docs/) hebben momenteel geen manier om het doel van een link te definiëren. In plaats daarvan moet standaard HTML worden gebruikt om links in een nieuw tabblad te openen.

De HTML-syntaxis is `target="_blank"`, die als volgt wordt gebruikt binnen de `<a>` tag:

```html
<a href="https://readme.com/" target="_blank">ReadMe</a>
```

Dit kan worden gecombineerd met onze `doc:page` syntaxis om [links naar pagina's binnen hetzelfde project](doc:linking-to-pages#internal-links) als volgt te openen:

```html
<a href="doc:intro-to-readme" target="_blank">Introduction</a>
```

 

## Links Valideren

ReadMe ondersteunt verschillende tools van derden om automatisch verbroken links in een documentatieproject te vinden. Een dienst die wij aanraden is de [W3C Validator](https://validator.w3.org/checklink). Geen login vereist. Voer voor het veld **URL** het aangepaste domein van je documentatie in. Selecteer **Omleidingen verbergen** en selecteer **Gelinkte documenten recursief controleren**. Laat de recursidiepte leeg.

De resultaten tonen alleen links die verbroken zijn, niet op **welke** pagina's die links voorkomen, of hoe vaak de verbroken links voorkomen.

 

## Wat is het Volgende

Je kunt de sectie **Wat is het Volgende** onderaan de pagina gebruiken om te linken naar relevante pagina's binnen je project en/of relevante externe links. Je kunt ook een beschrijving toevoegen om meer context te bieden.

<Image align="center" border={true} src="https://files.readme.io/1ae72b6-New_Whats_Next.gif" className="border" />