---
title: CSS & JavaScript personnalisés
deprecated: false
hidden: false
metadata:
  robots: index
---
Dans cette section, vous pouvez ajouter du CSS et du Javascript pour personnaliser davantage l'apparence de votre site de documentation.

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

> 🚧 Sélecteurs
>
> Utilisez des sélecteurs préfixés `.rm-`. Les sélecteurs hachés changent constamment et **ne doivent pas** être utilisés comme sélecteurs (ex. `Header-bottom2eLKOFXMEmh5`).

## Feuille de style personnalisée

<Callout icon="📘" theme="info">
  Vous devriez limiter vos modifications à des ajustements mineurs. De plus, les feuilles de style ne sont pas versionnées ; toutes les versions utilisent la même feuille de style.
</Callout>

## Javascript personnalisé

Votre Javascript sera inclus en bas de la page.

<details>
  <summary><b>Variables globales</b></summary>

  ReadMe expose certaines variables globales pour vous aider à personnaliser l'expérience utilisateur de votre hub :

  * **`RM_ReferenceSidebarScrollTopOffset`**\
    Décalage en pixels pour la logique de défilement vers l'élément actif dans la barre latérale des sections <Glossary>Référence</Glossary> continues.
</details>

## Balises d'inclusion personnalisées

**HTML d'en-tête**

Tout HTML ici sera inclus dans la balise head, ce qui est utile pour des éléments tels que les balises meta et le chargement de CSS ou JS externes.

**HTML de pied de page**  
​  
Ceci sera placé juste avant la balise `</body>`. Utile pour des éléments tels que les analyses et le suivi.

## Activer/désactiver le Javascript et le CSS personnalisés

Ajoutez le paramètre de requête `?disableCustomCss=true&disableCustomJs=true` à la fin de n'importe quelle URL.