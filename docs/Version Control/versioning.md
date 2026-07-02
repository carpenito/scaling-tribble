---
title: Versionnage
excerpt: bonjour le monde
deprecated: false
hidden: false
metadata:
  robots: index
---
La gestion de plusieurs versions de votre documentation est essentielle pour de nombreux produits techniques. Cette page détaille le fonctionnement du versionnage dans ReadMe, ainsi que plusieurs cas d'utilisation.

<Callout icon="🚧" theme="warn">
  **Sections concernées :** Seules les sections Guides, Recettes et Référence sont versionnées. Le contenu de la Page d'accueil, des Discussions et du Journal des modifications persistera d'une version à l'autre.
</Callout>

## Créer une nouvelle version

Pour créer une nouvelle version, ouvrez le menu Versions & Branches en sélectionnant le **nom de la version** (par exemple v3.0) dans la navigation d'administration. Cliquez ensuite sur le bouton **+ Nouvelle version** dans le coin supérieur droit. Choisissez la version à partir de laquelle effectuer le fork et nommez votre nouvelle version. Cela créera une copie de cette version ; il ne sera pas possible de reporter les modifications sur la version qui a été forkée.

<Image align="center" border={false} src="https://files.readme.io/c543cc3ff266bd3b210d720cfb7c5e09d7750c78dcb5ccfd60f669eae003ca39-versions.png" />

### Semver(-ish)

Notre versionnage est basé sur <Anchor label="Semver" target="_blank" href="http://semver.org/">Semver</Anchor>, mais est bien plus flexible que Semver en termes d'entrées acceptables. Cela signifie que vos versions peuvent être aussi simples que `v1.0`, mais aussi complexes que `v1.0-hello-this-is-a-version`.

***

## Options de version

<Image align="center" border={false} width="500px" src="https://files.readme.io/159f0425970c8c5849bc6b6e7b684f51fdab23a656f6488139337adaa75e9d60-version_options.png" />

### Par défaut

Il s'agit de la version vers laquelle votre domaine redirigera. Les utilisateurs peuvent passer à une autre version en cliquant sur le sélecteur de version dans le menu déroulant.

<Callout icon="🙅‍♂️" theme="default">
  Il n'est pas possible de fusionner deux versions. Si vous souhaitez apporter des modifications aux deux, vous devrez le faire manuellement !
</Callout>

### Publique

Sélectionner cette option rendra la version disponible dans le sélecteur de version et accessible à toute personne pouvant consulter votre documentation. Si elle n'est pas sélectionnée, cette version sera marquée comme **Masquée** et ne sera visible que par les administrateurs du projet.

### Bêta

Indiquer qu'une version est en bêta ajoutera un badge à côté de la version dans le sélecteur de version. Cela ne crée pas d'encadré sur la page ni aucune autre modification visible.

### Dépréciée

Sélectionnez cette option pour marquer les anciennes versions. En plus d'afficher un badge « déprécié » à côté de la version dans le sélecteur de version, les utilisateurs verront également une grande bannière rouge en haut de la documentation lorsqu'ils consultent cette version dépréciée. Voici à quoi cela ressemble :

<Image align="center" border={true} width="smart" src="https://files.readme.io/RhO7iWuhSMGsBrHSrFMt_Screen%20Shot%202015-12-16%20at%2012.17.04%20PM.png" className="border" />

***

## Affichage du sélecteur de version

<Image align="center" border={false} caption="Admin view: Hidden and Deprecated are not visible to end-users" src="https://files.readme.io/5f0ac4bab3338c5e1cceee0368a02363bb6c2eca6f40324725d6d43593e564ab-version_drop.png" />

Par défaut, nous affichons le sélecteur de version mentionné ci-dessus dans la barre de sous-navigation. Vous pouvez activer ou désactiver son affichage dans **Paramètres > En-tête & Pied de page > Sous-navigation**.

<Image align="center" border={false} src="https://files.readme.io/1a975ae96b399662d42cee67ca226a8fd49bfb9188da95ccfd00a2125f0347d7-version_picker.png" />

***

## Contenu réutilisable

Tout [Contenu réutilisable](doc:reusable-content) créé dans une version ne peut être utilisé que dans la documentation de cette version ; il n'est pas possible de définir des blocs de contenu réutilisable utilisables entre différentes versions au sein d'un même projet.

Si une nouvelle version est créée par fork d'une version existante, la nouvelle version hérite de tous les blocs de contenu réutilisable définis dans la version existante. Cependant, les blocs de contenu réutilisable de la nouvelle version sont totalement indépendants de l'ancienne version.

> 📘 Contenu réutilisable global
>
> Les projets disposant d'un plan Enterprise ont la possibilité de définir du **Contenu réutilisable global** qui _peut_ être utilisé entre différents projets et versions. Consultez notre [documentation sur le contenu réutilisable pour les groupes Enterprise](https://docs.readme.com/ent/docs/reusable-content-enterprise) pour plus d'informations !

***

## Cas d'utilisation

Il existe de nombreux scénarios dans lesquels le versionnage de la documentation peut être utile — certains sont plus évidents que d'autres. Le cas d'utilisation le plus évident est celui où la version de votre documentation doit correspondre au versionnage de votre API ou d'un autre produit technique, et où vous devez conserver des copies de votre documentation pour chaque version respective.

Un autre cas d'utilisation concerne les restructurations ou migrations importantes de contenu, notamment lorsque ces changements sont plus complexes que la simple mise à jour de quelques pages (auquel cas nous recommanderions <Anchor label="Suggested Edits" target="_blank" href="doc:suggested-edits">les Suggestions de modifications</Anchor>). Vous pouvez forker une nouvelle version de votre documentation, effectuer une restructuration majeure (par exemple, réorganiser les catégories de pages, fusionner des pages, supprimer du contenu obsolète, etc.), tout en conservant votre ancienne documentation comme version publique. Et lorsque vous êtes prêt à basculer, il suffit de renommer les versions et d'ajuster quelques paramètres de version !

***

## FAQ

<Accordion title="Combien de versions puis-je créer ?" icon="fa-tags">
  Les utilisateurs du plan Gratuit peuvent créer jusqu'à 3 versions. Passez au plan Startup ou supérieur pour bénéficier de versions illimitées.
</Accordion>