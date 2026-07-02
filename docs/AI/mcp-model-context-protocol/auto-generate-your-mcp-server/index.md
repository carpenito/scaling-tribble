---
title: Générez automatiquement votre serveur MCP
deprecated: false
hidden: false
metadata:
  robots: index
---
Avec ReadMe, chaque projet inclut automatiquement un serveur MCP entièrement configuré. Il vous suffit d'activer MCP pour connecter votre documentation API aux outils d'IA.

## Comment générer votre propre serveur MCP

En mode Édition, dans le coin supérieur droit, cliquez sur **:sparkles:AI** pour ouvrir le panneau latéral. Sélectionnez **MCP** et activez le serveur MCP pour démarrer votre serveur MCP. Votre URL MCP sera : `https://your-project.readme.com/mcp`. Vous pouvez partager votre URL MCP avec vos développeurs, qui pourront connecter leurs assistants IA et leurs outils directement à votre API. Les endpoints que vous ne souhaitez pas rendre accessibles dans votre serveur MCP peuvent être désactivés sous Enabled MCP Routes.

L'IA devrait désormais avoir accès aux données de votre compte ReadMe et à votre documentation via le serveur MCP.

<Image align="center" border={false} width="35% " src="https://files.readme.io/f4981199e6757d7c7a64ff259c4c592ab97b8b91f91255804a6a5a8d696fbd9b-mcp_advanced.png" />

### Outils personnalisés

<br />

## Tester votre configuration MCP

Une fois configuré, vous pouvez tester la connexion à votre serveur MCP :

1. Ouvrez votre éditeur IA (Cursor, VS Code, etc.)
2. Démarrez une nouvelle conversation avec l'assistant IA
3. Posez des questions sur votre API et votre documentation. Essayez ces questions :
   * « Comment faire [cas d'utilisation courant] ? »
   * « Montrez-moi un exemple de [fonctionnalité API] »
   * « Créez une [type d'intégration] en utilisant [votre API] »

## Comment générer des instructions d'accès pour vos utilisateurs

Une fois votre serveur MCP activé, vous pouvez générer automatiquement des instructions d'accès pour vos utilisateurs finaux en cliquant sur le bouton « Generate MCP Template ». Cela crée un nouveau document non publié intitulé « MCP » dans vos Guides, expliquant comment se connecter à votre serveur MCP dans des outils tels que Cursor et Claude Desktop. Vous pouvez trouver ce document en bas de vos Guides ou de votre Référence API dans une nouvelle catégorie appelée « MCP SERVER ».