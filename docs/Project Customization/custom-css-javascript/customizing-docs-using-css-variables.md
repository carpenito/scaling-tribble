---
title: Personnalisation de la documentation avec des variables CSS
deprecated: false
hidden: false
metadata:
  robots: index
---
## Options de personnalisation

Il existe deux façons de personnaliser votre documentation. Nous recommandons d'utiliser les variables CSS ; c'est la méthode la plus simple et la plus sûre pour ajouter des personnalisations à votre documentation.

Si vous souhaitez modifier l'arrière-plan de votre en-tête, vous pouvez définir la variable CSS comme suit :

```css
.App {
  --Header-background: #fff;
}
```

L'autre option consiste à écrire du CSS personnalisé. Nous exposons des noms de classes globaux que vous pouvez utiliser comme sélecteurs (préfixés par `rm`) :

```css
.rm-Header {
  background: #fff;
}
```

> 📘 :root vs body
>
> Nos variables CSS ciblent le sélecteur `:root` et se chargent après les vôtres, donc utilisez le sélecteur `body` pour vous assurer que vos variables ont la priorité !

***

## Changer votre police de caractères

Vous pouvez modifier la police de caractères dans toute votre documentation via la variable `--font-family`.

```css Custom CSS
.App {
  --font-family: 'Your Typeface';
}

```

Si vous utilisez un service comme Google Fonts, vous devrez inclure les éléments `<link />` dans votre HTML personnalisé.

***

## En-tête

Certaines variables varient en fonction de la couleur principale de l'arrière-plan de votre en-tête (définie dans la page Apparence, selon qu'elle est sombre ou claire). Vous pouvez baser vos remplacements de variables CSS sur le mode clair ou sombre en procédant comme suit :

```cs
.ThemeContext_dark {
  --Header-button-color: #fff;
}
```

### Variables CSS

| Nom                          | Valeur par défaut              | Description                                                                                      |
| :--------------------------- | :----------------------------- | :----------------------------------------------------------------------------------------------- |
| `--Header-background`        | `var(--color-primary)`         | `--color-primary` correspond à l'arrière-plan de votre en-tête défini dans la page Apparence du tableau de bord.                |
| `--Header-border-color`      | `rgba(0, 0, 0, 0.1)`           |                                                                                                  |
| `--Header-border-width`      | `1px`                          |                                                                                                  |
| `--Header-button-color`      |                                | Couleur du texte des boutons dans l'en-tête.                                                              |
| `--Header-button-hover`      |                                | Couleur du texte du bouton au survol.                                                 |
| `--Header-button-active`     |                                | Couleur du texte du bouton lorsqu'il est sélectionné.                                                 |
| `--Header-button-focus`      |                                |                                                                                                  |
| `--Header-jumpTo-background` | `var(--color-primary-inverse)` |                                                                                                  |
| `--Header-jumpTo-color`      | `var(--color-primary)`         |                                                                                                  |
| `--Header-tab-padding`       | `5px 2px`                      | Quantité de rembourrage dans chaque onglet de navigation (disponible avec l'option d'en-tête Ligne).            |
| `--Header-tab-underline`     | `var(--color-primary)`         | Couleur du soulignement de l'onglet lors de l'utilisation de la navigation par onglets (disponible avec l'option d'en-tête Ligne). |

### Classes globales

<Image border={false} src="https://files.readme.io/fd2d896-An_Introduction_to_ReadMe-20220323-115038.png" />

1. `.rm-Header`
2. `.rm-Logo`
3. `.rm-Header-top-link`
4. `.rm-Header-bottom-link`
5. `.rm-SearchToggle`
6. `.rm-Header-top-link_login`

Non représentés :

* `.rm-JumpTo`
* `.rm-Logo-img`

***

## Barre latérale

### Classes globales

<Image border={false} src="https://files.readme.io/861a758-Safari_-_An_Introduction_to_ReadMe_-_2021-10-27_at_09.55_AM.png" title="Safari - An Introduction to ReadMe - 2021-10-27 at 09.55 AM.png" />

1. `.rm-Sidebar`
2. `.rm-Sidebar-link `
3. `.rm-Sidebar-wrapper` (englobe à la fois le titre et la liste)
4. `.rm-Sidebar-heading` (uniquement le titre)
5. `.rm-Sidebar-list` (uniquement la liste)

### Variables CSS

| Nom                        | Valeur par défaut    | Description                                  |
| :------------------------- | :------------------- | :------------------------------------------- |
| `--Sidebar-border-color`   | `rgba(0, 0, 0, 0.1)` |                                              |
| `--Sidebar-indent`         | `15px`               | Espace d'indentation des sous-pages                |
| `--Sidebar-link-padding-y` | `5px`                | Rembourrage vertical de chaque élément dans la barre latérale |

***

## Article

### Classes globales

<Image border={false} src="https://files.readme.io/93ce267-Safari_-_Get_changelogs_-_2021-05-25_at_01.42_PM.png" title="Safari - Get changelogs - 2021-05-25 at 01.42 PM.png" />

1. `.rm-APISectionHeader` (ce sélecteur est utilisé dans le Playground et l'affectera également)
2. `.rm-APILogInfo`
3. `.rm-APILogsTable`
4. `.rm-ParamContainer `
5. `.rm-ParamInput` ou `.rm-ParamSelect`
6. `.rm-APIResponseSchemaPicker`

Non représentés :

* `.rm-Pagination` (le conteneur des boutons de navigation Page précédente / Page suivante situés en bas de page)

## Playground

### Variables CSS

| Nom                           | Valeur par défaut                                      | Description                                                                                                              |
| :---------------------------- | :----------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| `--tryit-background`          | `var(--color-primary, #118cfd)`                        | Couleur d'arrière-plan du bouton Essayer. `--color-primary` correspond à l'arrière-plan de votre en-tête défini dans la page Apparence du tableau de bord. |
| `--tryit-background-hover`    | `var(--color-primary-darken-10, #0272d9)`              |                                                                                                                          |
| `--tryit-background-active`   | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-background-focus`    | `var(--color-primary-alpha-25, rgba(17,140,253,0.25))` |                                                                                                                          |
| `--tryit-background-disabled` | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                          |
| `--tryit-border-radius`       | `var(--border-radius-lg)`                              | `--border-radius-lg` est défini par défaut à 7,5px.                                                                                  |
| `--tryit-color`               | `var(--color-primary-inverse)`                         |                                                                                                                          |
| `--tryit-spinner-color`       | `var(--color-primary-inverse)`                         |                                                                                                                          |

### Classes globales

<Image border={false} src="https://files.readme.io/561e588-Safari_-_Get_metadata_-_2021-05-25_at_01.15_PM.png" title="Safari - Get metadata - 2021-05-25 at 01.15 PM.png" />

Sélecteur de langue :

1. `.rm-LanguageButton`
2. `.rm-LanguageButton-more`
3. `.rm-APISectionHeader` (ce sélecteur est utilisé dans l'Article et l'affectera également)
4. `.rm-PlaygroundRequest`
5. `.rm-TryIt`
6. `.rm-PlaygroundResponse`

***

## Variables globales

| Nom                       | Valeur par défaut                                                                                                                   |
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

## Markdown ReadMe

Nous disposons également de plusieurs variables spécifiques au [Markdown ReadMe (RDMD)](https://rdmd.readme.io), qui est le moteur Markdown utilisé pour afficher tout le contenu Markdown de ReadMe. Vous pouvez en savoir plus sur ces variables et d'autres conseils pour [personnaliser RDMD](https://rdmd.readme.io/docs/custom-css).