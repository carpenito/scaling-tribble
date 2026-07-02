---
title: Pages Personnalisées
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

<Callout icon="👍" theme="okay">
  Consultez cet article en tant que [Page Personnalisée](https://docs.readme.com/page/custom-page)
</Callout>

Les Pages Personnalisées sont idéales lorsque vous souhaitez conserver la navigation supérieure de votre projet ReadMe, tout en ayant un aspect personnalisé sous la barre de recherche.

# Qu'est-ce qui est différent ?

1. Pas de navigation dans la barre latérale gauche
2. Pas de table des matières à droite, même lorsque des en-têtes sont utilisés
3. Chemin d'URL différent (le sous-dossier est /page au lieu de /docs)
4. Pas de Suggestions de modifications
5. Pas de vote sur la page
6. Pas de « mis à jour il y a x jours »

<Callout icon="🚧" theme="warn">
  Les Pages Personnalisées ne sont pas affectées par le versionnage et sont partagées. Si vous supprimez une Page Personnalisée, elle sera retirée de partout.
</Callout>

# Qu'est-ce qui est identique ?

Avec une [disposition de sous-en-tête déroulant](/main/docs/subheader-layout), le titre de la page apparaît dans la navigation par fil d'Ariane.

<Image align="center" border={true} width="smart" src="https://files.readme.io/14c46d5-Screen_Shot_2021-05-19_at_3.28.30_PM.png" className="border" />

> 📘 Remarque
>
> Le titre de la Page Personnalisée occupe la place d'une Section dans la navigation par fil d'Ariane, mais il ne **crée pas** de Section permanente dans le menu déroulant.

## Modes

Les Pages Personnalisées disposent de deux modes :

1. **Markdown :** Le mode standard utilisé dans la section Documentation

<Image border={true} src="https://files.readme.io/5300f08-CleanShot_2022-10-15_at_08.56.122x.png" className="border" />

2. **HTML :** Le code est [assaini](https://en.wikipedia.org/wiki/HTML_sanitization). Si vous souhaitez inclure du CSS ou du JavaScript, faites-le dans Apparence > JavaScript/Feuille de style personnalisés.