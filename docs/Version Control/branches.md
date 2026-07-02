---
title: Branches
deprecated: false
hidden: false
metadata:
  robots: index
---
Avec les branches, vous pouvez continuer à éditer comme vous en avez l'habitude ! Les branches sont un flux de travail optionnel qui offre de la flexibilité dans votre processus de rédaction. Les rédacteurs utilisent les branches pour :

* Apporter des modifications et les examiner dans un environnement de prévisualisation avant leur mise en ligne.
* Envoyer des modifications à des coéquipiers pour révision.
* Apporter des modifications sur plusieurs pages.

<PlanTable currentPlan="Business" />

<Callout icon="💼" theme="default">
  **Remarque :** Des options de révision supplémentaires sont uniquement disponibles avec les plans Enterprise.
</Callout>

***

## Créer une branche

Il existe trois façons de créer une branche :

1. Accédez au menu des versions et des branches. Une fois là, vous pouvez créer de nouvelles branches à partir d'une version.
2. Lors de l'édition d'une version, au lieu d'enregistrer, vous pouvez enregistrer dans une nouvelle branche.
3. Si vous [synchronisez avec GitHub](https://docs.readme.com/main/docs/bi-directional-sync), les branches créées dans GitHub apparaîtront dans ReadMe. Et les branches créées dans l'interface ReadMe apparaîtront automatiquement dans GitHub !

Une fois votre branche créée, vous pouvez commencer à écrire ! Les modifications ne seront pas en ligne tant que vous n'aurez pas fusionné votre branche dans une version publique.

<Image align="center" border={false} src="https://files.readme.io/65abcb59c51a4be0b668815cf0046ee818e93228057a6bff5ddbe4d3a4b9b97e-Getting_Started_with_Owlberts_Journeys-20250512-1502362x.webp" />

Il n'y a pas de limite de temps ni d'expiration sur les branches. Tout administrateur de votre équipe peut afficher, modifier, fusionner et supprimer n'importe quelle branche.

***

## Réviser les modifications

<Image align="center" alt="Review tab showing the diff between two pages line-by-line" border={false} src="https://files.readme.io/95ab92ffd9eec49ad16b279f1e4a66de1f54cc95eb121f43c381258fb1d7915e-Review-20251104-1847122x.webp" />

Lors de l'édition d'une branche, vous pouvez accéder à l'onglet Révision pour comparer les modifications apportées dans votre branche.

<Callout icon="☝️" theme="default">
  Lors de la réorganisation des fichiers, ils sont représentés comme des modifications du fichier `_order` dans votre documentation. Chaque élément du fichier `_order` représente une page de votre documentation et correspond au slug de chaque page.
</Callout>

Les clients disposant de la fonctionnalité Révision peuvent également marquer les branches comme prêtes pour la révision, ce qui ajoute un badge dans le menu des versions et des branches, et lance le [Linter IA](https://docs.readme.com/main/docs/linter). Les utilisateurs peuvent contourner les exigences de fusion en cochant la case « Fusionner sans les exigences requises » pour activer le bouton **Fusionner**.

***

## Fusionner les modifications

Une fois que vous êtes prêt à mettre les modifications en ligne, vous pouvez fusionner depuis le menu des branches :

<Image align="center" border={false} width="300px" src="https://files.readme.io/0c4c2909e376be33b974e008b8b9b9f14860b13c3eff12b5be8a377395fd68e4-Getting_Started_with_Owlberts_Journeys-20250528-1418472x.png" />

Lors de la fusion, une vérification sera effectuée pour s'assurer qu'il n'y a pas de conflits de fusion. S'il existe des conflits à résoudre, nous recommandons de [résoudre les conflits depuis GitHub](https://docs.readme.com/main/docs/branches#/handling-conflicts). Si votre projet ne se synchronise pas avec GitHub, vous pouvez ignorer le conflit et forcer la fusion des modifications — en donnant la priorité aux modifications de la branche.

Une fois fusionnées, vos branches ne sont pas supprimées afin que vous puissiez examiner les modifications avant de les supprimer.

<Callout icon="💁‍♂️" theme="default">
  Les utilisateurs GitHub peuvent également fusionner une branche dans une version — y compris via des Pull Requests.
</Callout>

### Restreindre la fusion aux administrateurs

Les clients Enterprise peuvent restreindre l'accès à la fusion par projet à [Uniquement les administrateurs ou les administrateurs et éditeurs](https://docs.readme.com/ent/docs/user-roles/). Les paramètres se trouvent sur la page Projet du tableau de bord Enterprise. Ouvrez **Paramètres** > **Nom de l'entreprise** (en bas) > **Projets**

***

## Synchronisation avec GitHub

Vous n'êtes pas obligé de vous synchroniser avec GitHub pour utiliser les branches.

Lors de la création de branches depuis GitHub, leur nom doit être formaté pour inclure leur version : `{version}_{branch}`. Exemples :

```
v2.0_rewrite-getting-started
v2.0_add-new-feature
v2.0_fix-typo
```

### Accès et permissions

Les permissions ReadMe et GitHub sont indépendantes. Les utilisateurs ayant accès aux branches de votre projet GitHub auront accès à toutes les modifications de contenu. Pour que les utilisateurs puissent consulter les modifications de contenu effectuées dans les branches via GitHub, ils auront besoin d'un compte ReadMe avec accès à la branche de votre projet.

### Gestion des conflits

Lors d'une fusion depuis GitHub, l'utilisateur peut résoudre les conflits via l'éditeur GitHub ou l'outil de fusion de son choix en local avant de pousser les modifications.

Lors d'une fusion depuis ReadMe, les modifications que vous voyez lors de la prévisualisation correspondront toujours à ce qui sera mis en ligne lors de la fusion. Les modifications conflictuelles provenant de GitHub n'apparaîtront pas.

***

## FAQ

<Accordion title="Qui peut consulter une branche ?" icon="fa-help-circle">
  Seuls les coéquipiers ayant accès à votre projet peuvent consulter vos branches — y compris les rôles Éditeur et Lecteur de l'équipe.
</Accordion>