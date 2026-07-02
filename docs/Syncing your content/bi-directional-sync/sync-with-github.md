---
title: Synchronisation avec GitHub
deprecated: false
hidden: false
metadata:
  robots: index
---
## Comment configurer la synchronisation bidirectionnelle avec GitHub

### Prérequis

* Vous aurez besoin d'un compte GitHub.
* Lors de la synchronisation avec un dépôt dans une organisation, vous aurez besoin de l'autorisation de créer un **dépôt vide**.

### Configuration

1. Accédez à la page **Paramètres** > **Connexion Git**.
2. Sélectionnez GitHub.
3. Si ce n'est pas déjà fait, créez un dépôt vide sur [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)—assurez-vous de décocher l'option de création d'un README.
4. **Synchronisez** avec votre fournisseur et authentifiez-vous. Accordez l'accès au dépôt avec lequel vous souhaitez vous synchroniser et confirmez votre dépôt sur l'écran suivant.

***

## Changer de dépôt

1. Dans ReadMe, déconnectez le projet via l'icône de corbeille.
2. Dans GitHub, créez votre nouveau dépôt (doit être vide).
3. Accédez à **Applications > Applications GitHub installées**.
4. Trouvez **ReadMe Sync** et cliquez sur **Configurer**.
5. Sous _Accès au dépôt_, sélectionnez le nouveau dépôt avec lequel vous souhaitez vous synchroniser.
6. Retournez dans ReadMe et connectez-vous à votre nouveau dépôt.

***

## Modifier votre documentation

**[Branches](https://docs.readme.com/main/docs/branches#/)**

* Le commit initial de ReadMe sert à établir la synchronisation des branches avec GitHub
* Les noms de branches doivent correspondre exactement aux noms de versions définis dans ReadMe
* Toute version et tout nom non correspondants existeront dans GitHub et ne se synchroniseront pas avec ReadMe.

<HTMLBlock>{`
<div class="migrating-column">
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-hexagon-exclamation"></i> Non synchronisé
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2-new-branch
		</pre>
  </section>
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-circle-check"></i> Synchronisé
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2.0_new-branch
		</pre>
  </section>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<!-- style guide CSS -->
<style>
  .migrating-column {
    border: 1px solid var(--color-border-default);
    border-radius: var(--border-radius);
    display: flex;
    justify-content: center;
    
    + .migrating-column {
      margin-top: 1em;
    }
    
    section {
      flex: 1 1 50%;
      overflow: hidden;
      
      + section {
        border-left: 1px solid var(--color-border-default);
      }
    }
    
    pre {
      background: transparent;
      border: 0;
      border-radius: 0;
      font-size: 0.8em;
      margin: 0;
      overflow: auto;
      padding: 15px;
      
      + pre {
        border-top: 1px solid var(--color-border-default);
      }
    }
    
    header {
      align-items: center;
      border-bottom: 1px solid var(--color-border-default);
      display: flex;
      font-size: 15px;
      font-weight: var(--font-weight-bold);
      gap: 0.5em;
      padding: 1em;
    }

    .fa-circle-check {
      color: var(--green);
    }

    .fa-hexagon-exclamation {
      color: var(--red);
    }
  }
</style>
`}</HTMLBlock>

***

### GitHub Enterprise Server

Si vous utilisez un **[GitHub Enterprise Server (GHES)](https://docs.readme.com/ent/docs/connecting-github-enterprise-server)** auto-hébergé, vous pouvez configurer la synchronisation depuis le tableau de bord de votre groupe sous **Connexion Git**. La synchronisation nécessite un nouveau dépôt vide, et chaque projet enfant ne peut se synchroniser qu'avec un seul dépôt.

<Image align="center" border={false} src="https://files.readme.io/bd2640dae70270e20b0a71ae98adf56bd4e3a59b275b1609e86bbc4fc8ad81cd-GHES.png" />

Si GHES n'est pas disponible pour votre projet, veuillez contacter votre Customer Success Manager.

### Protection des branches GitHub

Si votre dépôt GitHub utilise des règles de protection de branches, vous devrez les configurer pour permettre à l'application ReadMe Sync de pousser des modifications. Voici comment procéder selon votre configuration GitHub :

#### Pour les ensembles de règles GitHub (nouvelle version)

1. Accédez aux paramètres de protection des branches de votre dépôt.
2. Dans la section _Liste de contournement_, cliquez sur **+ Ajouter un contournement**.
3. Recherchez _ReadMe Sync_ (App • readmeio) et définissez l'autorisation sur **Toujours autoriser**.

<Image align="center" alt="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." border={false} caption="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." src="https://files.readme.io/0e52415eb4dede062a4d9df4a2d3f06dda62500c26caae7f000e4ecd50f4521d-Screenshot_2024-11-22_at_11.12.14_AM.png" width="600px" />

#### Pour la protection de branches héritée

1. Accédez aux règles de protection des branches de votre dépôt.
2. Trouvez la section _Autoriser certains acteurs à contourner les pull requests obligatoires_.
3. Ajoutez _readme-sync_ (ReadMe Sync) à la liste des acteurs autorisés.

<Image align="center" alt="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." border={false} caption="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." src="https://files.readme.io/8f3765d6ebbe96f5a93e4c6f915e52392ad6ba1512d0af4d4113ca8ff6ef8077-Screenshot_2024-11-22_at_11.12.07_AM.png" />

Cette configuration garantit que les modifications effectuées dans l'éditeur de ReadMe peuvent être synchronisées avec les branches protégées de votre dépôt GitHub.

***

<br />

## FAQ

<Accordion title="Comment ReadMe s'intègre-t-il à GitHub et quelles autorisations sont requises ?" icon="fa-question-circle">
  ReadMe utilise une application GitHub avec un accès au niveau du dépôt : lecture seule pour les métadonnées (obligatoire) et lecture/écriture pour la synchronisation du contenu. Les webhooks gèrent les synchronisations, la détection des modifications et la résolution des conflits.
</Accordion>

<Accordion title="Why don't my branches show on GitHub?" icon="fa-question-circle">
  Les nouvelles branches que vous créez après avoir activé la synchronisation bidirectionnelle créent automatiquement une branche correspondante sur GitHub, mais les branches existantes ne créeront pas de branche correspondante sur GitHub tant que vous n'aurez pas enregistré une modification (aussi minime soit-elle) sur cette branche côté ReadMe.
</Accordion>