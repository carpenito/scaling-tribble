---
title: Synchronisation avec GitLab
deprecated: false
hidden: false
metadata:
  robots: index
---
## Comment configurer la synchronisation bidirectionnelle avec GitLab

### Prérequis

* Vous aurez besoin d'un compte GitLab.
* Lors de la synchronisation avec un dépôt dans une organisation, vous devrez avoir la permission de créer un **dépôt vide**.

<Image align="center" border={false} src="https://files.readme.io/d2a12db436be321b972fd817432f3754a13d61c0ecb915202862e58fb2252cc1-Screenshot_2025-10-31_at_1.43.41_PM.png" />

### Configuration

1. Accédez à la page **Paramètres** > **Connexion Git**.
2. Sélectionnez GitLab.
3. Si ce n'est pas déjà fait, créez un dépôt vide dans [GitLab](https://docs.gitlab.com/user/project/)—assurez-vous de décocher l'option de création d'un README.
4. **Synchronisez** avec votre fournisseur et authentifiez-vous.
5. Créez un jeton d'accès personnel avec la portée `api`. Vous pouvez supprimer ce jeton après avoir terminé la configuration. ReadMe utilise ce jeton une seule fois lors de la configuration pour créer le webhook sur votre dépôt et il n'est pas stocké.
   1. Pour les jetons d'accès de projet, vous aurez besoin du rôle Mainteneur. Cependant, cela n'est pas recommandé car il existe une limite au nombre de jetons d'accès de projet créés, selon le tarif GitLab.

<Image border={false} src="https://files.readme.io/b350ddb7403c7d0ffbaa7d4f8e4c5fc6ca0d92308c4c81bde90b2c2b146a1ed3-image.png" />

6. Ajoutez le jeton d'accès à ReadMe et cliquez sur l'icône webhook pour créer les webhooks nécessaires afin de maintenir votre contenu synchronisé avec GitLab.

***

## Changer de dépôt

Si vous devez connecter votre projet ReadMe à un dépôt différent, vous devez déconnecter le dépôt d'origine en utilisant l'icône de corbeille.

1. Dans ReadMe, déconnectez le projet via l'icône de corbeille.
2. Dans GitLab, créez un nouveau projet vide.
3. Retournez dans ReadMe et sélectionnez le projet avec lequel vous souhaitez vous synchroniser.

***

## Branches protégées

Toutes les règles de branche doivent permettre à l'utilisateur (qui synchronise vers GitLab depuis ReadMe) d'effectuer des push.

<Image border={false} src="https://files.readme.io/5ab0dbdd08ca7f9fc31d8a6895ebb9a970819ea4f2c352c92307ab5886b14541-image.png" />

## FAQ

<Accordion title="Quelles permissions sont requises lors de la synchronisation avec GitLab ?" icon="fa-question-circle">
  ReadMe demande l'accès à :

  * `read_api` pour lister les projets
  * `read_user` et `read_profile` pour afficher les informations de l'utilisateur
  * `read_repository` pour synchroniser le contenu de GitLab vers ReadMe
  * `write_repository` pour synchroniser le contenu de ReadMe vers GitLab
</Accordion>

<br />