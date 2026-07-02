---
title: Thèmes
deprecated: false
hidden: false
metadata:
  robots: index
---
Tous les plans ont accès à la personnalisation dans les paramètres **Thème**. Ouvrez **Paramètres** en haut à gauche de l'interface d'administration, puis sélectionnez **Thème** dans la barre latérale.

* Mise en page
* Image de marque (Logo, Favicon et Couleurs)
* Style d'en-tête

<PlanTable currentPlan="Free" />

<Callout icon="💁‍♂️" theme="default">
  **Remarque :** Des options de personnalisation supplémentaires et des services sont disponibles avec les plans Business et Enterprise.
</Callout>

***

## Mise en page

<Image align="center" border={false} width="400px" src="https://files.readme.io/3d30b1d7f55cd7e37def92bb05c5c4799bc0e1294169209626ff9a24181733cc-Launch_Week-20250628-1026262x.webp" />

Vous pouvez choisir parmi 3 options de mise en page : Classique, Compact et Moderne. Il existe également une option pour étirer la mise en page sur les grands écrans. Vous pourrez prévisualiser la mise en page avant de sauvegarder.

<Callout icon="🚧" theme="warn">
  Une option avec barre latérale uniquement arrive bientôt !
</Callout>

***

## Image de marque

### Logo

Une option pour télécharger un logo blanc est disponible lorsqu'une alternative est nécessaire pour certains thèmes et paramètres de couleur d'en-tête.

**Format**

* Le SVG est préféré pour une meilleure qualité.
* Si votre logo est trop complexe pour un SVG, le WEBP est une bonne alternative — utilisez 2x de la taille souhaitée de votre logo pour une meilleure clarté sur les écrans haute résolution.
* Les GIF ne sont pas pris en charge.

**Dimensions**

* 24px de hauteur par défaut. Dans les thèmes Classique et Moderne, vous pouvez sélectionner une hauteur de logo plus grande de 40px.

**Personnalisation avancée**

* Les clients ayant accès au CSS personnalisé peuvent utiliser nos classes globales et variables CSS pour affiner l'affichage de leur logo :

```css
.rm-Logo-img {
  --Header-logo-height: YOUR_CUSTOM_HEIGHT
}
```

***

## En-tête

<Image align="center" border={false} width="400px" src="https://files.readme.io/9c14d52d69809626037d9cb483cd2fb0619734f6ccc3c3428fd6380936a44b43-Launch_Week-20250628-1043112x.webp" />

Vous pouvez choisir parmi 4 options de mise en page : Ligne, Couleur unie, Dégradé et Superposition.

<Callout icon="💁‍♂️" theme="default">
  L'option d'en-tête Ligne affiche désormais par défaut les liens sous forme d'onglets. Les utilisateurs disposant de l'ancien affichage en boutons peuvent effectuer le changement. Une fois le changement effectué, il ne sera pas possible de revenir en arrière.
</Callout>

**Personnalisation avancée**

* Les clients ayant accès au CSS personnalisé peuvent utiliser nos classes globales et variables CSS pour affiner leur en-tête :

```css
.rm-Header {
  --Header-background: YOUR_CUSTOM_VALUE /* defaults to your brand color */
  --Header-border-color: YOUR_CUSTOM_VALUE /* default: rgba(0, 0, 0, 0.1) */
  --Header-button-padding: YOUR_CUSTOM_VALUE /* default: 10px */

  /* Line theme only */
  --Header-tab-underline: YOUR_CUSTOM_VALUE /* defaults to your brand color */
}
```