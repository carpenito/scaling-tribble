---
title: Bi-directionele synchronisatie
deprecated: false
hidden: false
metadata:
  robots: index
---
Bi-directionele synchronisatie maakt een tweerichtingsverbinding tussen uw ReadMe-project en een GitHub- of GitLab-repository. Deze optionele workflow houdt inhoud consistent op beide platforms:

* Schrijf in uw favoriete omgeving, of dat nu ReadMe is of uw lokale ontwikkelomgeving.
* Ontwikkelaars, engineers en technische schrijvers kunnen samenwerken met de tools die zij verkiezen.
* Wijzigingen worden automatisch gesynchroniseerd tussen ReadMe en Git, waardoor één enkele bron van waarheid ontstaat.

<PlanTable currentPlan="Startup" />

***

## Bi-directionele synchronisatie instellen

ReadMe ondersteunt bi-directionele synchronisatie met zowel <Anchor label="GitHub" target="_blank" href="https://docs.readme.com/main/docs/sync-with-github">GitHub</Anchor> als <Anchor label="GitLab" target="_blank" href="https://docs.readme.com/main/docs/sync-with-gitlab">GitLab</Anchor>.

Voor synchronisatie met GitHub kunt u verbinding maken met GitHub Cloud. Als u het Enterprise-abonnement heeft, ondersteunt ReadMe bi-directionele synchronisatie met <Anchor label="GitHub Enterprise Server" target="_blank" href="https://docs.readme.com/ent/docs/connecting-github-enterprise-server">GitHub Enterprise Server</Anchor>.

<Image align="center" border={true} src="https://files.readme.io/6335bcb6aa344d9d1f23d11b3cf420cbe94493872630760fb04d2cce9df10189-Screenshot_2025-10-27_at_12.29.28_PM.png" className="border" />

<Callout icon="❗️" theme="error">
  De repository waarmee u synchroniseert moet leeg zijn — geen commits of bestanden (bijv. README.md) — voordat u verbinding maakt met ReadMe. U kunt bestanden toevoegen of verwijderen na de installatie.
</Callout>

***

## Documentatieversies

Als uw ReadMe-project meerdere [Versies](doc:versions) gebruikt, wordt alleen de Hoofdversie aanvankelijk gesynchroniseerd wanneer u Bi-directionele synchronisatie voor het eerst inschakelt. Nadat u Bi-directionele synchronisatie succesvol heeft ingeschakeld, worden wijzigingen in de andere versies gesynchroniseerd naar uw Git-repository.

***

## Uw documentatie bewerken

Zodra uw Git-verbinding is ingesteld, worden alle wijzigingen in de ReadMe-editor automatisch gesynchroniseerd naar uw Git-repository, en vice versa. Bij het bewerken van documentatie in Git kunt u uw favoriete code-editor of Git-tools gebruiken.

Volg deze structuurrichtlijnen om succesvolle synchronisatie van _Git naar ReadMe_ te garanderen:

**Markdown-bestanden:**

* Bestanden moeten verplichte frontmatter bevatten: `title` en `summary`
* Inhoud moet worden geschreven in standaard Markdown-formaat
* Bestandsnamen moeten overeenkomen met de beoogde URL-slug voor correcte routering

**Navigatie:**

* Paginavolgorde wordt gedefinieerd met behulp van `_order.yaml`-bestanden
* Elke categoriemap kan zijn eigen `order.yaml` hebben
* [Navigatiestructuur](https://docs.readme.com/main/docs/documentation-structure#/) in Git weerspiegelt de hiërarchie van uw ReadMe-project

**[Branches](https://docs.readme.com/main/docs/branches#/)**

* De initiële commit vanuit ReadMe is bedoeld om branchsynchronisatie met GitHub tot stand te brengen
* Branchnamen moeten exact overeenkomen met de versienamen die in ReadMe zijn gedefinieerd
* Niet-overeenkomende versies en namen zullen bestaan in GitHub en worden niet gesynchroniseerd met ReadMe.

<HTMLBlock>{`
<div class="migrating-column">
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-hexagon-exclamation"></i> Niet gesynchroniseerd
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2-new-branch
		</pre>
  </section>
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-circle-check"></i> Gesynchroniseerd
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

### Conflicten afhandelen

Wanneer een conflict wordt gedetecteerd tijdens het opslaan in ReadMe, vraagt het systeem u onmiddellijk om de Git-wijzigingen te Overschrijven of het opslaan te Annuleren en door te gaan met bewerken. Wijzigingen die in ReadMe worden opgeslagen, komen altijd overeen met wat live gaat.

Bij het samenvoegen vanuit GitHub kan de gebruiker conflicten oplossen via de GitHub-editor of de samenvoegingstool naar keuze, lokaal, voordat ze worden gepusht.

***

## Veelgestelde vragen

<Accordion title="Hoe integreert ReadMe met GitHub en welke machtigingen zijn vereist?" icon="fa-question-circle">
  ReadMe gebruikt een GitHub App met toegang op repository-niveau: alleen-lezen voor metadata (vereist) en lezen/schrijven voor het synchroniseren van inhoud. Webhooks verwerken synchronisaties, wijzigingsdetectie en conflictoplossing.
</Accordion>

<Accordion title="Why aren't my branches showing up in GitHub or GitLab?" icon="fa-question-circle">
  Nieuwe branches die u aanmaakt nadat u bi-directionele synchronisatie heeft ingeschakeld, maken automatisch een overeenkomstige branch aan in Git-tools, maar bestaande branches maken pas een overeenkomstige branch aan in Git-tools nadat u een wijziging in die branch in ReadMe heeft opgeslagen.
</Accordion>

<Accordion title="Welke machtigingen zijn vereist bij synchronisatie met GitLab?" icon="fa-question-circle">
  ReadMe vraagt toegang tot:

  * `read_api` voor het weergeven van projecten
  * `read_user` en `read_profile` om gebruikersinformatie weer te geven
  * `read_repository` om inhoud in GitLab te synchroniseren naar ReadMe
  * `write_repository` om inhoud in ReadMe te synchroniseren naar GitLab
</Accordion>