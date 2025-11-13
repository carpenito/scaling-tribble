---
title: Personalizzazione della Documentazione Utilizzando le Variabili CSS
excerpt: >-
  Guida completa per personalizzare la tua documentazione ReadMe utilizzando
  variabili CSS e classi globali per header, sidebar, articoli e playground.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
## Opzioni di Personalizzazione

Ci sono due modi per personalizzare la tua documentazione. Consigliamo di utilizzare le variabili CSS; è il modo più semplice e sicuro per aggiungere personalizzazioni alla tua documentazione.

Se vuoi cambiare lo sfondo dell'header, puoi impostare la variabile CSS così:

```css
.App {
  --Header-background: #fff;
}
```

L'altra opzione è scrivere CSS personalizzato. Esporremo i nomi delle classi globali da utilizzare come selettori (con prefisso `rm`):

```css
.rm-Header {
  background: #fff;
}
```

> 📘 :root vs body
>
> Le nostre variabili CSS sono mirate al selettore `:root` e si caricano dopo le tue, quindi usa il selettore `body` per assicurarti che le tue variabili abbiano la priorità!

***

## Cambiare il Carattere Tipografico

Puoi cambiare il carattere tipografico in tutta la tua documentazione attraverso la variabile `--font-family`.

```css Custom CSS
.App {
  --font-family: 'Your Typeface';
}

```

Se stai utilizzando un servizio come Google Fonts, dovrai includere gli elementi `<link />` nel tuo HTML Personalizzato.

***

## Header

Alcune variabili variano a seconda del colore primario dello sfondo del tuo header (impostato nella pagina Aspetto, se è scuro o chiaro). Puoi basare le tue sostituzioni di variabili CSS su chiaro o scuro facendo:

```cs
.ThemeContext_dark {
  --Header-button-color: #fff;
}
```

### Variabili CSS

| Nome                         | Valore Predefinito             | Descrizione                                                                                      |
| :--------------------------- | :----------------------------- | :----------------------------------------------------------------------------------------------- |
| `--Header-background`        | `var(--color-primary)`         | `--color-primary` è lo sfondo del tuo header dalla pagina Aspetto del dashboard.                |
| `--Header-border-color`      | `rgba(0, 0, 0, 0.1)`           |                                                                                                  |
| `--Header-border-width`      | `1px`                          |                                                                                                  |
| `--Header-button-color`      |                                | Colore del testo del pulsante nell'header.                                                      |
| `--Header-button-hover`      |                                | Colore del testo del pulsante quando viene passato sopra.                                       |
| `--Header-button-active`     |                                | Colore del testo del pulsante quando è selezionato.                                             |
| `--Header-button-focus`      |                                |                                                                                                  |
| `--Header-jumpTo-background` | `var(--color-primary-inverse)` |                                                                                                  |
| `--Header-jumpTo-color`      | `var(--color-primary)`         |                                                                                                  |
| `--Header-tab-padding`       | `5px 2px`                      | Quantità di padding all'interno di ogni scheda di navigazione (disponibile con l'opzione header Line). |
| `--Header-tab-underline`     | `var(--color-primary)`         | Colore della sottolineatura della scheda quando si utilizza la navigazione a schede (disponibile con l'opzione header Line). |

### Classi Globali

<Image border={false} src="https://files.readme.io/fd2d896-An_Introduction_to_ReadMe-20220323-115038.png" />

1. `.rm-Header`
2. `.rm-Logo`
3. `.rm-Header-top-link`
4. `.rm-Header-bottom-link`
5. `.rm-SearchToggle`
6. `.rm-Header-top-link_login`

Non rappresentate:

* `.rm-JumpTo`
* `.rm-Logo-img`

***

## Sidebar

### Classi Globali

<Image border={false} src="https://files.readme.io/861a758-Safari_-_An_Introduction_to_ReadMe_-_2021-10-27_at_09.55_AM.png" title="Safari - An Introduction to ReadMe - 2021-10-27 at 09.55 AM.png" />

1. `.rm-Sidebar`
2. `.rm-Sidebar-link `
3. `.rm-Sidebar-wrapper` (racchiude sia l'intestazione che la lista)
4. `.rm-Sidebar-heading` (solo l'intestazione)
5. `.rm-Sidebar-list` (solo la lista)

### Variabili CSS

| Nome                       | Valore Predefinito   | Descrizione                                    |
| :------------------------- | :------------------- | :--------------------------------------------- |
| `--Sidebar-border-color`   | `rgba(0, 0, 0, 0.1)` |                                                |
| `--Sidebar-indent`         | `15px`               | Spazio di indentazione delle sottopagine      |
| `--Sidebar-link-padding-y` | `5px`                | Padding verticale di ogni elemento nella sidebar |

***

## Articolo

### Classi Globali

<Image border={false} src="https://files.readme.io/93ce267-Safari_-_Get_changelogs_-_2021-05-25_at_01.42_PM.png" title="Safari - Get changelogs - 2021-05-25 at 01.42 PM.png" />

1. `.rm-APISectionHeader` (questo selettore è utilizzato nel Playground e influenzerà anche quello)
2. `.rm-APILogInfo`
3. `.rm-APILogsTable`
4. `.rm-ParamContainer `
5. `.rm-ParamInput` o `.rm-ParamSelect`
6. `.rm-APIResponseSchemaPicker`

Non rappresentate:

* `.rm-Pagination` (il wrapper per i pulsanti di navigazione Pagina Precedente / Pagina Successiva situati in fondo alla pagina)

## Playground

### Variabili CSS

| Nome                          | Valore Predefinito                             | Descrizione                                                                                                              |
| :---------------------------- | :----------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| `--tryit-background`          | `var(--color-primary, #118cfd)`                        | Colore di sfondo del pulsante Try It. `--color-primary` è lo sfondo del tuo header dalla pagina Aspetto del dashboard. |
| `--tryit-background-hover`    | `var(--color-primary-darken-10, #0272d9)`              |                                                                                                                          |
| `--tryit-background-active`   | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-background-focus`    | `var(--color-primary-alpha-25, rgba(17,140,253,0.25))` |                                                                                                                          |
| `--tryit-background-disabled` | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-border-radius`       | `var(--border-radius-lg)`                              | `--border-radius-lg` predefinito a 7.5px.                                                                               |
| `--tryit-color`               | `var(--color-primary-inverse)`                         |                                                                                                                          |
| `--tryit-spinner-color`       | `var(--color-primary-inverse)`                         |                                                                                                                          |

### Classi Globali

<Image border={false} src="https://files.readme.io/561e588-Safari_-_Get_metadata_-_2021-05-25_at_01.15_PM.png" title="Safari - Get metadata - 2021-05-25 at 01.15 PM.png" />

Selettore Linguaggio:

1. `.rm-LanguageButton`
2. `.rm-LanguageButton-more`
3. `.rm-APISectionHeader` (questo selettore è utilizzato nell'Articolo e influenzerà anche quello)
4. `.rm-PlaygroundRequest`
5. `.rm-TryIt`
6. `.rm-PlaygroundResponse`

***

## Variabili Globali

| Nome                      | Valore Predefinito                                                                                                          |
| :------------------------ | :-------------------------------------------------------------------------------------------------------------------------- |
| `--border-radius`         | `5px`                                                                                                                       |
| `--border-radius-lg`      | `calc(var(--border-radius) * 1.5)`                                                                                          |
| `--box-shadow-menu-light` | `0 5px 10px rgba(0,0,0,.05), 0 2px 6px rgba(0,0,0,.025), 0 1px 3px rgba(0,0,0,.025)`                                        |
| `--box-shadow-pill`       | `inset 0 1px 1px 0 rgba(255,255,255,.2), inset 0 -1px 2px 0 rgba(0,0,0,.2), 0 1px 2px 0 rgba(0,0,0,0.05)`                   |
| `--box-shadow-tooltip`    | `0 1px 2px rgba(0,0,0,.05), inset 0 -1px 2px rgba(0,0,0,.2), inset 0 1px 1px rgba(255,255,255,.2)`                          |
| `--font-family`           | `-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif` |
| `--font-family-mono`      | `"SF Mono", SFMono-Regular, ui-monospace, "DejaVu Sans Mono", Menlo, Consolas, monospace`                                   |
| `--font-weight`           | `500`                                                                                                                       |
| `--font-weight-bold`      | `600`                                                                                                                       |
| `--transition-fast`       | `.15s`                                                                                                                      |
| `--transition-slow`       | `.3s`                                                                                                                       |
| `--transition-timing`     | `cubic-bezier(.16,1,.3,1)`                                                                                                  |

## ReadMe Markdown

Abbiamo anche diverse variabili specifiche per [ReadMe Markdown (RDMD)](https://rdmd.readme.io), che è il motore Markdown che renderizza tutto il contenuto Markdown di ReadMe. Puoi leggere di queste variabili e altri suggerimenti per [personalizzare RDMD](https://rdmd.readme.io/docs/custom-css).