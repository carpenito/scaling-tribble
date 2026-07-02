---
title: Liens vers les pages
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
## Liens internes

Pour créer un lien entre des pages, commencez par taper `[` et un menu déroulant des pages disponibles à lier apparaîtra. Au fur et à mesure que vous continuez à saisir des caractères, des options de liens internes pertinentes s'afficheront.

<Image align="center" border={true} src="https://files.readme.io/cff6bf4-link_to_pages.gif" className="border" />

Le Markdown résultant ressemblera à ceci :

<Image align="center" border={true} src="https://files.readme.io/9b34336-CleanShot_2022-10-18_at_11.19.16.gif" className="border" />

Et apparaîtra comme le lien ci-dessus pour les utilisateurs !

> 📘 Les liens internes ne fonctionnent qu'au sein d'un seul projet.
>
> Si vous créez un lien entre plusieurs projets, vous devez utiliser des hyperliens standard.

 

## Liens d'ancrage

Tous les en-têtes de section incluent un lien d'ancrage. Le format est `#header-name`. Ainsi, par exemple, ce [lien](doc:linking-to-pages#anchor-links) vous ramènera à cette section :

```
[link](doc:linking-to-pages#anchor-links)
```

 

## Liens externes

### Liens en ligne

Pour créer un lien en ligne, saisissez le texte que vous souhaitez lier entre crochets, `[x]`, suivi directement de l'URL du lien entre parenthèses, `(y)`.

Les liens ressemblent à ceci dans l'éditeur Markdown :

```
[ReadMe](readme.com)
```

Et donnent un lien qui ressemble à ceci : [ReadMe](https://readme.com/)

 

### Liens par référence

Les liens par référence vous permettent d'attribuer un numéro ou un « nom » à un lien et d'y faire référence plusieurs fois.

Par exemple, si vous saisissez ce qui suit dans votre tableau de bord :

```
When I first research something I look at [Wikipedia][1] then at [Google][2] then [Wookiepedia][3].

[1]: https://wikipedia.org            "Wikipedia"
[2]: https://google.com               "Google"
[3]: https://starwars.fandom.com      "Wookiepedia"
```

...les liens ressembleront à ceci dans votre Hub :

Lorsque je recherche quelque chose pour la première fois, je consulte [Wikipedia][1] puis [Google][2] puis [Wookiepedia][3].

[1]: https://wikipedia.org "Wikipedia"

[2]: https://google.com "Google"

[3]: https://starwars.fandom.com "Wookiepedia"

 

## Ouvrir les liens dans un nouvel onglet

Markdown et [RDMD](https://docs.readme.com/rdmd/docs/) ne disposent actuellement d'aucun moyen de définir la cible d'un lien. Il faudra plutôt utiliser du HTML standard pour ouvrir des liens dans un nouvel onglet.

La syntaxe HTML est `target="_blank"`, qui s'utilise comme suit dans la balise `<a>` :

```html
<a href="https://readme.com/" target="_blank">ReadMe</a>
```

Cela peut être combiné avec notre syntaxe `doc:page` pour ouvrir des [liens vers des pages au sein du même projet](doc:linking-to-pages#internal-links) comme suit :

```html
<a href="doc:intro-to-readme" target="_blank">Introduction</a>
```

 

## Validation des liens

ReadMe prend en charge plusieurs outils tiers pour détecter automatiquement les liens brisés dans un projet de documentation. L'un des services que nous recommandons est le [Validateur W3C](https://validator.w3.org/checklink). Aucune connexion requise. Dans le champ **URL**, saisissez le domaine personnalisé de votre documentation. Sélectionnez **Masquer les redirections** et **Vérifier les documents liés de manière récursive**. Laissez la profondeur de récursion vide.

Les résultats n'afficheront que les liens brisés, et non **sur quelles** pages ces liens apparaissent, ni combien de fois les liens brisés se produisent.

 

## Étape suivante

Vous pouvez utiliser la section **Étape suivante** en bas de la page pour créer des liens vers des pages pertinentes au sein de votre projet et/ou des liens externes pertinents. Vous pouvez également ajouter une description pour fournir plus de contexte.

<Image align="center" border={true} src="https://files.readme.io/1ae72b6-New_Whats_Next.gif" className="border" />