---
title: Linter
deprecated: false
hidden: false
metadata:
  robots: index
---
Le Linter automatise la validation du contenu en vérifiant la documentation par rapport au guide de style de votre entreprise et aux normes de rédaction établies. Il simplifie le processus de révision manuelle que les rédacteurs effectuent généralement avec des outils externes.

Vous pouvez configurer des règles personnalisées pour imposer la mise en forme du code, le choix des mots et le respect du style interne et des bonnes pratiques. Que votre documentation contienne du HTML personnalisé ou de nombreux exemples de code, le Linter garantit la cohérence dans l'ensemble de vos docs.

<PlanTable currentPlan="Startup" />

## Configurer

Vous pouvez ajouter des invites au Linter, classées en guide de style, erreurs ou avertissements.

<Image border={false} src="https://files.readme.io/6844539c6c370fbc5fe87fa2bab007e50aa4fb52673fa629d247d0836534c971-image.png" />

**Guide de style** : Décrivez ce qui fait de bons docs et le Linter évaluera votre contenu. Exemple :

> Soyez concis :
>
> Un texte court est toujours préférable. Les paragraphes courts sont plus faciles à lire. Essayez de limiter les titres à une seule ligne. Les titres sur deux lignes occupent deux fois plus d'espace vertical. Utilisez des mots courts dans les titres ; si un utilisateur emploie des polices plus grandes pour améliorer l'accessibilité, les mots longs risquent de se couper en fin de ligne.

<br />

> Clarté :
>
> Un texte clair et concis pour faciliter la lecture et la navigation. Allez droit au but afin que les utilisateurs trouvent facilement ce dont ils ont besoin. Évitez les mots superflus.

<br />

> Ton naturel et humain :
>
> Utilisez des mots du quotidien, faciles à comprendre. Moins formel, mais plus professionnel qu'une conversation ordinaire. Adoptez occasionnellement un ton enjoué pour les moments de célébration, mais jamais pour un texte informatif. Soyez chaleureux et bienveillant envers les utilisateurs qui lisent la documentation.

<br />

**Erreurs** : Règles pouvant être vérifiées objectivement. Exemple :

> Écrire ReadMe correctement :
>
> Incorrect : Readme
>
> Correct : ReadMe

<br />

> Encadrer les éléments de code avec des backticks (`) :
>
> Incorrect : Run npm install –g my–package
>
> Correct : Run `npm install –g my–package`

<br />

> Signaler les textes de remplacement tels que TODO, FIXME ou Lorem ipsum
>
> Exemple : TODO: Add description and image to this feature

<br />

**Avertissements** : Pour signaler des problèmes pouvant être subjectifs. Exemple :

> Langage hésitant :
>
> Évitez d'utiliser un langage incertain ou excessivement prudent. Cela nuit à la confiance et rend vos instructions moins directes. Optez pour un langage clair et assuré.
>
> Incorrect : Vous pourriez envisager d'installer la dernière version.
>
> Correct : Vous pouvez installer la dernière version pour accéder aux nouvelles fonctionnalités.

<br />

> Rédaction faible :
>
> Évitez les formulations faibles comme « Vous pouvez » ou « Il y a ». Ces tournures noient l'action, rendent la rédaction moins directe et ajoutent souvent des mots inutiles. Une bonne documentation est claire et orientée vers l'action.
>
> Incorrect : Vous pouvez configurer l'API en modifiant le fichier de paramètres.
>
> Correct : Configurez l'API en modifiant le fichier de paramètres.

<br />

> Voix active :
>
> Évitez d'utiliser la voix passive. La voix active est plus claire, plus concise et indique précisément au lecteur qui fait quoi.
>
> Incorrect : Le token est généré lorsque l'utilisateur se connecte.
>
> Correct : Le système génère un token lorsque l'utilisateur se connecte.

<br />

## Exécuter le Linter

Une fois configuré, l'exécution du Linter vérifie votre page par rapport à vos invites. Les problèmes peuvent être corrigés automatiquement à l'aide de l'Agent.

<Image align="center" border={false} width="350px" src="https://files.readme.io/02345a8505f8f89eaa3d97019252e3cfc3c9e16fdaed63ac7ed7b6df97b765f5-linter.png" />

<br />

## FAQ

<Accordion title="Où envoyer mes commentaires ou questions ?" icon="fa-messages-question">
  Envoyez vos commentaires ou questions par e-mail à [beta@readme.io](mailto:beta@readme.io)
</Accordion>

<Accordion title="Quel modèle le Linter utilise-t-il ?" icon="fa-wand-sparkles">
  Pour l'instant, nous utilisons Gemini 2.5 Flash — bien que cela puisse changer au fur et à mesure que nous ajustons l'équilibre entre qualité et rapidité. À l'avenir, les utilisateurs auront la possibilité de choisir le modèle de leur choix.
</Accordion>