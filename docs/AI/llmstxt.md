---
title: LLMs.txt
deprecated: false
hidden: false
metadata:
  robots: index
---
## Aperçu

Grâce à notre nouvelle fonctionnalité [LLMs.txt](https://llmstxt.org/), vous pouvez apprendre aux modèles d'IA à comprendre et à représenter correctement la documentation de votre API. Cela vous permet de fournir le contexte dont les assistants IA comme ChatGPT ou Claude ont besoin pour répondre avec précision aux questions sur votre API sans halluciner (inventer des informations). La configuration ne prend littéralement que quelques secondes – il suffit d'activer un bouton et nous générerons automatiquement le fichier de configuration. En coulisses, nous créons des métadonnées qui aident les systèmes d'IA à comprendre la structure, la terminologie et les informations les plus récentes de votre documentation. LLMs.txt est disponible sur tous les plans.

Le résultat ? Les développeurs obtiennent des réponses précises sur votre API, même lorsqu'ils utilisent des outils d'IA plutôt que de lire directement votre documentation. C'est une documentation qui fonctionne partout où vos développeurs travaillent !

## Avantages

* **Précision** : Aide les modèles d'IA à représenter correctement votre documentation
* **Cohérence** : Garantit une terminologie et des informations de version appropriées
* **Pertinence** : Guide les modèles d'IA vers les informations les plus récentes
* **Zéro maintenance** : Générée automatiquement à partir de votre documentation existante

## Fonctionnement

LLMs.txt fonctionne comme un fichier de configuration à la racine de votre site de documentation, accessible et interprétable par les modèles de langage IA. Ce fichier sert de guide technique qui indique aux systèmes d'IA comment lire et référencer correctement votre contenu.

Lorsqu'il est activé, ReadMe génère automatiquement ce fichier de configuration en se basant sur la structure de votre documentation existante. Le fichier contient des métadonnées sur :

* L'organisation de votre documentation (guides, référence API, recettes, etc.)
* Les informations de version pour s'assurer que les modèles d'IA référencent la documentation la plus récente
* La terminologie importante spécifique à votre API
* La structure hiérarchique de votre contenu

Les modèles d'IA qui prennent en charge LLMs.txt vérifient la présence de ce fichier avant de générer des réponses sur votre API. Lorsqu'ils le trouvent, ils utilisent les instructions pour fournir des informations plus précises, réduisant ainsi les risques de références obsolètes ou de terminologie incorrecte.

Par exemple, si vous avez récemment renommé des endpoints ou modifié des paramètres requis, LLMs.txt aide à s'assurer que les assistants IA ne fournissent pas d'informations obsolètes aux développeurs utilisant votre API.

## Démarrage

Activez LLMs.txt en quelques clics pour aider les modèles d'IA à représenter fidèlement la documentation de votre API.

#### ReadMe Refactored

Pour les projets utilisant l'interface ReadMe Refactored :

1. Accédez au hub de votre projet.
2. Cliquez sur **Paramètres IA (✨ Icône Étincelle)** dans le menu en haut à droite.
3. Activez **Activer LLMs.txt** sur ON.
4. Cliquez sur **Enregistrer**.

#### ReadMe Legacy

1. Accédez à **Configuration** > **Paramètres IA**.
2. Activez **Activer LLMs.txt** sur ON.
3. Cliquez sur **Enregistrer**.