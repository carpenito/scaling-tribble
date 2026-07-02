---
title: Ask AI
deprecated: false
hidden: false
metadata:
  robots: index
---
Vos utilisateurs peuvent obtenir des réponses instantanées sur votre produit grâce à Ask AI. L'assistant utilise le modèle que vous avez sélectionné, entraîné sur votre documentation, pour fournir des réponses précises et contextuelles. Il inclut des liens directs vers vos docs, permettant aux utilisateurs d'explorer les sujets plus en détail.

***

## Aperçu pour l'utilisateur final

Lorsque vos utilisateurs interagissent avec Ask AI, l'assistant s'ouvre avec vos exemples de questions personnalisés et fournit des réponses basées sur vos configurations du panneau d'administration. Les réponses ne feront référence qu'aux pages publiques. Pour les groupes Enterprise avec des projets publics et privés, Ask AI fournira des informations en fonction des autorisations de l'utilisateur à consulter un projet.

<Image align="center" border={false} width="750px" src="https://files.readme.io/93bba5b92a2c954d7aa1b5847d3648837ac31668b9861e35479e7a906596b3ab-user_gif.gif" />

## Configurer

Personnalisez le ton de l'assistant IA, la longueur des réponses et les restrictions pour correspondre à votre image de marque. Définissez des exemples de questions pour vos utilisateurs finaux et sélectionnez un modèle disponible qui correspond à vos besoins.

<Image align="center" border={false} src="https://files.readme.io/afc7f66444d7c8186118082c46a34ed5a8af5bbdfdb65cc9af97f8fba3969724-Ask_AI.png" />

### Groupes Enterprise

Toutes les configurations mentionnées ci-dessus sont disponibles pour les projets Enterprise dans votre tableau de bord de groupe. Les personnalisations au niveau du groupe s'appliqueront à tous les projets enfants correspondants.

## Analytique

Analysez les questions, les réponses et les retours des utilisateurs pour comprendre ce que vos utilisateurs recherchent — et dans quelle mesure l'assistant est performant. Vous pouvez consulter toutes les analytiques dans le **tableau de bord Ask AI** sous **Paramètres**. Pour partager des informations avec votre équipe, exportez les données au format CSV avec des plages de dates personnalisées. Le processus d'exportation peut prendre un certain temps selon le volume de données, mais une fois prêt, le téléchargement démarrera immédiatement dans votre navigateur.

<Image align="center" border={false} width="650px" src="https://files.readme.io/27af66805d9c4eb18c468750023284c9682c2734dd2422bb650d7408b98a4787-analytics.png" />

<br />

## FAQ

<Accordion title="Que se passe-t-il avec mes données ?" icon="fa-chart-simple">
  Ask AI est alimenté par les API d'OpenAI, et le contenu Markdown ainsi que les définitions d'API leur sont envoyés pour générer des réponses aux questions des utilisateurs.
  Bien qu'OpenAI conserve les journaux de ces requêtes API pendant 30 jours, aucune donnée n'est utilisée pour entraîner leurs modèles d'IA.
</Accordion>

<Accordion title="Ask AI fait-il référence aux pages masquées ?" icon="fa-user-ninja">
  Non, les pages masquées ne sont jamais indexées par Ask AI.
  Pour les groupes Enterprise, seul le contenu du projet auquel l'utilisateur a accès est utilisé pour répondre aux questions.
</Accordion>

<Accordion title="À quelle vitesse les modifications sont-elles ajoutées aux modèles d'Ask AI ?" icon="fa-swap">
  Actuellement, le nouveau contenu est mis à jour toutes les 2 heures, bien que cela puisse changer au fur et à mesure que nous continuons à développer Ask AI.
</Accordion>

<Accordion title="Quels outils sont proposés pour surveiller les réponses ?" icon="fa-monitor-waveform">
  Les journaux de chaque question et réponse sont disponibles dans le tableau de bord d'administration. Voir [Analytique](https://docs.readme.com/maindocs/ask-ai#analytics) ci-dessus.
</Accordion>

<Accordion title="Comment puis-je essayer Ask AI ?" icon="fa-sparkles">
  Vous pouvez tester Ask AI sur la documentation de ReadMe ou sur votre propre documentation à titre d'essai.
</Accordion>

<Accordion title="J'utilise l'ancienne expérience Ask AI. Où puis-je trouver ces paramètres ?" icon="fa-robot">
  Vous pouvez passer à la nouvelle expérience depuis le panneau de configuration dans le panneau Ask AI. La mise à niveau est permanente et ne peut pas être annulée.
</Accordion>