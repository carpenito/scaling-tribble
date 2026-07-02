---
title: Synchronisation bidirectionnelle
deprecated: false
hidden: false
metadata:
  robots: index
---
La synchronisation bidirectionnelle crée une connexion à double sens entre votre projet ReadMe et un dépôt GitHub ou GitLab. Ce flux de travail optionnel maintient la cohérence du contenu sur les deux plateformes :

* Rédigez dans l'environnement de votre choix, que ce soit ReadMe ou votre configuration de développement locale.
* Les développeurs, ingénieurs et rédacteurs techniques peuvent collaborer avec les outils qu'ils préfèrent.
* Les modifications se synchronisent automatiquement entre ReadMe et Git, créant ainsi une source de vérité unique.

<PlanTable currentPlan="Startup" />

***

## Configurer la synchronisation bidirectionnelle

ReadMe prend en charge la synchronisation bidirectionnelle avec <Anchor label="GitHub" target="_blank" href="https://docs.readme.com/main/docs/sync-with-github">GitHub</Anchor> et <Anchor label="GitLab" target="_blank" href="https://docs.readme.com/main/docs/sync-with-gitlab">GitLab</Anchor>.

Pour la synchronisation avec GitHub, vous pouvez vous connecter à GitHub Cloud. Si vous êtes sur le plan Enterprise, ReadMe prend en charge la synchronisation bidirectionnelle avec <Anchor label="GitHub Enterprise Server" target="_blank" href="https://docs.readme.com/ent/docs/connecting-github-enterprise-server">GitHub Enterprise Server</Anchor>.

<Image align="center" border={true} src="https://files.readme.io/6335bcb6aa344d9d1f23d11b3cf420cbe94493872630760fb04d2cce9df10189-Screenshot_2025-10-27_at_12.29.28_PM.png" className="border" />

<Callout icon="❗️" theme="error">
  Le dépôt avec lequel vous effectuez la synchronisation doit être vide — sans commits ni fichiers (par exemple, README.md) — avant de le connecter à ReadMe. Vous pouvez ajouter ou supprimer des fichiers après la configuration.
</Callout>

***

## Gestion des versions de la documentation

Si votre projet ReadMe utilise plusieurs [Versions](doc:versions), seule la version principale est synchronisée lors de la première activation de la synchronisation bidirectionnelle. Une fois celle-ci activée avec succès, toutes les modifications apportées aux autres versions seront synchronisées avec votre dépôt Git.

***

## Modifier votre documentation

Une fois votre connexion Git configurée, toutes les modifications effectuées dans l'éditeur ReadMe se synchronisent automatiquement avec votre dépôt Git, et vice versa. Lors de la modification de la documentation dans Git, vous pouvez utiliser l'éditeur de code ou les outils Git de votre choix.

Pour garantir une synchronisation réussie de _Git vers ReadMe_, suivez ces directives de structure :

**Fichiers Markdown :**

* Les fichiers doivent inclure le frontmatter requis : `title` et `summary`
* Le contenu doit être rédigé en format Markdown standard
* Les noms de fichiers doivent correspondre au slug d'URL prévu pour un routage correct

**Navigation :**

* L'ordre des pages est défini à l'aide des fichiers `_order.yaml`
* Chaque dossier de catégorie peut avoir son propre `order.yaml`
* La [structure de navigation](https://docs.readme.com/main/docs/documentation-structure#/) dans Git reflète la hiérarchie de votre projet ReadMe

**[Branches](https://docs.readme.com/main/docs/branches#/)**

* Le commit initial depuis ReadMe sert à établir la synchronisation des branches avec GitHub
* Les noms de branches doivent correspondre exactement aux noms de versions définis dans ReadMe
* Toute version ou nom non correspondant existera dans GitHub mais ne sera pas synchronisé avec ReadMe.

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

### Gestion des conflits

Lorsqu'un conflit est détecté lors d'une sauvegarde dans ReadMe, le système vous invite immédiatement à Écraser les modifications Git ou à Annuler la sauvegarde et continuer l'édition. Les modifications sauvegardées dans ReadMe correspondront toujours à ce qui est mis en ligne.

Lors d'une fusion depuis GitHub, l'utilisateur peut résoudre les conflits via l'éditeur GitHub ou l'outil de fusion de son choix en local avant de pousser les modifications.

***

## FAQ

<Accordion title="Comment ReadMe s'intègre-t-il à GitHub et quelles autorisations sont requises ?" icon="fa-question-circle">
  ReadMe utilise une application GitHub avec un accès au niveau du dépôt : lecture seule pour les métadonnées (obligatoire) et lecture/écriture pour la synchronisation du contenu. Les webhooks gèrent les synchronisations, la détection des modifications et la résolution des conflits.
</Accordion>

<Accordion title="Why aren't my branches showing up in GitHub or GitLab?" icon="fa-question-circle">
  Les nouvelles branches créées après l'activation de la synchronisation bidirectionnelle génèrent automatiquement une branche correspondante dans les outils Git, mais les branches existantes ne créeront pas de branche correspondante dans les outils Git tant qu'une modification n'aura pas été sauvegardée sur cette branche dans ReadMe.
</Accordion>

<Accordion title="Quelles autorisations sont requises lors de la synchronisation avec GitLab ?" icon="fa-question-circle">
  ReadMe demande l'accès à :

  * `read_api` pour lister les projets
  * `read_user` et `read_profile` pour afficher les informations utilisateur
  * `read_repository` pour synchroniser le contenu de GitLab vers ReadMe
  * `write_repository` pour synchroniser le contenu de ReadMe vers GitLab
</Accordion>