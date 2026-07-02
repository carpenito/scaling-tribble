---
title: Docs aanpassen met CSS-variabelen
deprecated: false
hidden: false
metadata:
  robots: index
---
## Aanpassingsopties

Er zijn twee manieren om je documentatie aan te passen. We raden aan om CSS-variabelen te gebruiken; dit is de eenvoudigste en veiligste manier om aanpassingen toe te voegen aan je docs.

Als je de achtergrond van je header wilt wijzigen, kun je de CSS-variabele als volgt instellen:

```css
.App {
  --Header-background: #fff;
}
```

De andere optie is om aangepaste CSS te schrijven. We stellen globale klassenamen beschikbaar die je als selectors kunt gebruiken (voorafgegaan door `rm`):

```css
.rm-Header {
  background: #fff;
}
```

> 📘 :root vs body
>
> Onze CSS-variabelen zijn gericht op de `:root`-selector en worden na die van jou geladen, dus gebruik de `body`-selector om ervoor te zorgen dat jouw variabelen prioriteit krijgen!

***

## Je Lettertype Wijzigen

Je kunt het lettertype in je gehele documentatie wijzigen via de `--font-family`-variabele.

```css Custom CSS
.App {
  --font-family: 'Your Typeface';
}

```

Als je een dienst zoals Google Fonts gebruikt, moet je de `<link />`-elementen opnemen in je aangepaste HTML.

***

## Header

Sommige variabelen variëren afhankelijk van de primaire kleur van de achtergrond van je header (ingesteld op de Weergavepagina, of deze donker of licht is). Je kunt je CSS-variabele-overschrijvingen baseren op licht of donker door het volgende te doen:

```cs
.ThemeContext_dark {
  --Header-button-color: #fff;
}
```

### CSS-variabelen

| Naam                         | Standaardwaarde                  | Beschrijving                                                                                      |
| :--------------------------- | :----------------------------- | :----------------------------------------------------------------------------------------------- |
| `--Header-background`        | `var(--color-primary)`         | `--color-primary` is de achtergrond van je header op de Weergavepagina van het dashboard.                |
| `--Header-border-color`      | `rgba(0, 0, 0, 0.1)`           |                                                                                                  |
| `--Header-border-width`      | `1px`                          |                                                                                                  |
| `--Header-button-color`      |                                | Kleur van de knoptekst in de header.                                                              |
| `--Header-button-hover`      |                                | Kleur van de knoptekst wanneer er overheen wordt gehoverd.                                                 |
| `--Header-button-active`     |                                | Kleur van de knoptekst wanneer deze geselecteerd is.                                                 |
| `--Header-button-focus`      |                                |                                                                                                  |
| `--Header-jumpTo-background` | `var(--color-primary-inverse)` |                                                                                                  |
| `--Header-jumpTo-color`      | `var(--color-primary)`         |                                                                                                  |
| `--Header-tab-padding`       | `5px 2px`                      | Hoeveelheid opvulling binnen elk navigatietabblad (beschikbaar met de Lijn-headeroptie).            |
| `--Header-tab-underline`     | `var(--color-primary)`         | Kleur van de tabonderstreping bij gebruik van tabbladnavigatie (beschikbaar met de Lijn-headeroptie). |

### Globale klassen

<Image border={false} src="https://files.readme.io/fd2d896-An_Introduction_to_ReadMe-20220323-115038.png" />

1. `.rm-Header`
2. `.rm-Logo`
3. `.rm-Header-top-link`
4. `.rm-Header-bottom-link`
5. `.rm-SearchToggle`
6. `.rm-Header-top-link_login`

Niet afgebeeld:

* `.rm-JumpTo`
* `.rm-Logo-img`

***

## Zijbalk

### Globale klassen

<Image border={false} src="https://files.readme.io/861a758-Safari_-_An_Introduction_to_ReadMe_-_2021-10-27_at_09.55_AM.png" title="Safari - An Introduction to ReadMe - 2021-10-27 at 09.55 AM.png" />

1. `.rm-Sidebar`
2. `.rm-Sidebar-link `
3. `.rm-Sidebar-wrapper` (omhult zowel de kop als de lijst)
4. `.rm-Sidebar-heading` (alleen de kop)
5. `.rm-Sidebar-list` (alleen de lijst)

### CSS-variabelen

| Naam                       | Standaardwaarde        | Beschrijving                                  |
| :------------------------- | :------------------- | :------------------------------------------- |
| `--Sidebar-border-color`   | `rgba(0, 0, 0, 0.1)` |                                              |
| `--Sidebar-indent`         | `15px`               | Inspringing van subpagina's                |
| `--Sidebar-link-padding-y` | `5px`                | Verticale opvulling van elk item in de zijbalk |

***

## Artikel

### Globale klassen

<Image border={false} src="https://files.readme.io/93ce267-Safari_-_Get_changelogs_-_2021-05-25_at_01.42_PM.png" title="Safari - Get changelogs - 2021-05-25 at 01.42 PM.png" />

1. `.rm-APISectionHeader` (deze selector wordt ook gebruikt in de Playground en heeft daar ook invloed op)
2. `.rm-APILogInfo`
3. `.rm-APILogsTable`
4. `.rm-ParamContainer `
5. `.rm-ParamInput` of `.rm-ParamSelect`
6. `.rm-APIResponseSchemaPicker`

Niet afgebeeld:

* `.rm-Pagination` (de wrapper voor de navigatieknoppen Vorige / Volgende pagina onderaan de pagina)

## Playground

### CSS-variabelen

| Naam                          | Standaardwaarde                                          | Beschrijving                                                                                                              |
| :---------------------------- | :----------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| `--tryit-background`          | `var(--color-primary, #118cfd)`                        | Achtergrondkleur van de Try It-knop. `--color-primary` is de achtergrond van je header op de Weergavepagina van het dashboard. |
| `--tryit-background-hover`    | `var(--color-primary-darken-10, #0272d9)`              |                                                                                                                          |
| `--tryit-background-active`   | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-background-focus`    | `var(--color-primary-alpha-25, rgba(17,140,253,0.25))` |                                                                                                                          |
| `--tryit-background-disabled` | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-border-radius`       | `var(--border-radius-lg)`                              | `--border-radius-lg` is standaard 7,5px.                                                                                  |
| `--tryit-color`               | `var(--color-primary-inverse)`                         |                                                                                                                          |
| `--tryit-spinner-color`       | `var(--color-primary-inverse)`                         |                                                                                                                          |

### Globale klassen

<Image border={false} src="https://files.readme.io/561e588-Safari_-_Get_metadata_-_2021-05-25_at_01.15_PM.png" title="Safari - Get metadata - 2021-05-25 at 01.15 PM.png" />

Taalkiezer:

1. `.rm-LanguageButton`
2. `.rm-LanguageButton-more`
3. `.rm-APISectionHeader` (deze selector wordt ook gebruikt in het Artikel en heeft daar ook invloed op)
4. `.rm-PlaygroundRequest`
5. `.rm-TryIt`
6. `.rm-PlaygroundResponse`

***

## Globale variabelen

| Naam                      | Standaardwaarde                                                                                                                       |
| :------------------------ | :---------------------------------------------------------------------------------------------------------------------------------- |
| `--border-radius`         | `5px`                                                                                                                               |
| `--border-radius-lg`      | `calc(var(--border-radius) * 1.5)`                                                                                                  |
| `--box-shadow-menu-light` | `0 5px 10px rgba(0,0,0,.05), 0 2px 6px rgba(0,0,0,.025), 0 1px 3px rgba(0,0,0,.025)`                                                |
| `--box-shadow-pill`       | `inset 0 1px 1px 0 rgba(255,255,255,.2), inset 0 -1px 2px 0 rgba(0,0,0,.2), 0 1px 2px 0 rgba(0,0,0,0.05)`                           |
| `--box-shadow-tooltip`    | `0 1px 2px rgba(0,0,0,.05), inset 0 -1px 2px rgba(0,0,0,.2), inset 0 1px 1px rgba(255,255,255,.2)`                                  |
| `--font-family`           | `-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif` |
| `--font-family-mono`      | `"SF Mono", SFMono-Regular, ui-monospace, "DejaVu Sans Mono", Menlo, Consolas, monospace`                                           |
| `--font-weight`           | `500`                                                                                                                               |
| `--font-weight-bold`      | `600`                                                                                                                               |
| `--transition-fast`       | `.15s`                                                                                                                              |
| `--transition-slow`       | `.3s`                                                                                                                               |
| `--transition-timing`     | `cubic-bezier(.16,1,.3,1)`                                                                                                          |

## ReadMe Markdown

We hebben ook verschillende variabelen die specifiek zijn voor [ReadMe Markdown (RDMD)](https://rdmd.readme.io), de Markdown-engine die alle Markdown-inhoud van ReadMe rendert. Je kunt meer lezen over deze variabelen en andere tips voor het [aanpassen van RDMD](https://rdmd.readme.io/docs/custom-css).