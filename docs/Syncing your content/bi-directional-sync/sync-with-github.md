---
title: Synchroniseren met GitHub
deprecated: false
hidden: false
metadata:
  robots: index
---
## Bi-directionele synchronisatie instellen met GitHub

### Vereisten

* Je hebt een GitHub-account nodig.
* Wanneer je synchroniseert met een repository in een organisatie, heb je toestemming nodig om een **lege repository** aan te maken.

### Instellen

1. Ga naar **Instellingen** > **Git-verbinding**.
2. Selecteer GitHub.
3. Als je dat nog niet hebt gedaan, maak dan een lege repository aan in [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)—zorg ervoor dat je de optie om een README aan te maken uitvinkt.
4. **Synchroniseer** met je provider en verifieer jezelf. Verleen toegang tot de repository waarmee je wilt synchroniseren en bevestig je repository op het volgende scherm.

***

## Van repository wisselen

1. Verbreek binnen ReadMe de verbinding met het project via het prullenbakpictogram.
2. Maak binnen GitHub je nieuwe repository aan (moet leeg zijn).
3. Ga naar **Applicaties > Geïnstalleerde GitHub Apps**.
4. Zoek **ReadMe Sync** en klik op **Configureren**.
5. Selecteer onder _Toegang tot repository_ de nieuwe repository waarmee je wilt synchroniseren.
6. Ga terug naar ReadMe en maak verbinding met je nieuwe repository.

***

## Je documentatie bewerken

**[Branches](https://docs.readme.com/main/docs/branches#/)**

* De eerste commit vanuit ReadMe is bedoeld om branchsynchronisatie met GitHub tot stand te brengen
* Branchnamen moeten exact overeenkomen met de versienamen die in ReadMe zijn gedefinieerd
* Versies en namen die niet overeenkomen, bestaan wel in GitHub maar worden niet gesynchroniseerd met ReadMe.

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

***

### GitHub Enterprise Server

Als je een zelfgehoste **[GitHub Enterprise Server (GHES)](https://docs.readme.com/ent/docs/connecting-github-enterprise-server)** gebruikt, kun je synchronisatie instellen vanuit je groepsdashboard onder **Git-verbinding**. Synchronisatie vereist een nieuwe, lege repository en elk onderliggend project kan slechts met één repository synchroniseren.

<Image align="center" border={false} src="https://files.readme.io/bd2640dae70270e20b0a71ae98adf56bd4e3a59b275b1609e86bbc4fc8ad81cd-GHES.png" />

Als GHES niet beschikbaar is voor jouw project, neem dan contact op met je Customer Success Manager.

### GitHub-branchbeveiliging

Als je GitHub-repository gebruikmaakt van branchbeveiligingsregels, moet je deze configureren zodat de ReadMe Sync-app wijzigingen kan pushen. Hier lees je hoe je dit instelt op basis van je GitHub-configuratie:

#### Voor GitHub Rulesets (nieuwe versie)

1. Ga naar de branchbeveiligingsinstellingen van je repository.
2. Klik onder de sectie _Bypass-lijst_ op **+ Bypass toevoegen**.
3. Zoek naar _ReadMe Sync_ (App • readmeio) en stel de toestemming in op **Altijd toestaan**.

<Image align="center" alt="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." border={false} caption="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." src="https://files.readme.io/0e52415eb4dede062a4d9df4a2d3f06dda62500c26caae7f000e4ecd50f4521d-Screenshot_2024-11-22_at_11.12.14_AM.png" width="600px" />

#### Voor verouderde branchbeveiliging

1. Ga naar de branchbeveiligingsregels van je repository.
2. Zoek de sectie _Bepaalde actoren toestaan vereiste pull requests te omzeilen_.
3. Voeg _readme-sync_ (ReadMe Sync) toe aan de lijst met toegestane actoren.

<Image align="center" alt="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." border={false} caption="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." src="https://files.readme.io/8f3765d6ebbe96f5a93e4c6f915e52392ad6ba1512d0af4d4113ca8ff6ef8077-Screenshot_2024-11-22_at_11.12.07_AM.png" />

Deze configuratie zorgt ervoor dat wijzigingen die in de editor van ReadMe worden aangebracht, kunnen worden gesynchroniseerd naar beveiligde branches in je GitHub-repository.

***

<br />

## Veelgestelde vragen

<Accordion title="Hoe integreert ReadMe met GitHub en welke machtigingen zijn vereist?" icon="fa-question-circle">
  ReadMe gebruikt een GitHub App met toegang op repositoryniveau: alleen-lezen voor metadata (vereist) en lezen/schrijven voor het synchroniseren van inhoud. Webhooks verwerken synchronisaties, wijzigingsdetectie en conflictoplossing.
</Accordion>

<Accordion title="Why don't my branches show on GitHub?" icon="fa-question-circle">
  Nieuwe branches die je aanmaakt nadat je bi-directionele synchronisatie hebt ingeschakeld, krijgen automatisch een overeenkomstige branch op GitHub. Bestaande branches krijgen echter pas een overeenkomstige branch op GitHub als je een wijziging (hoe klein ook) opslaat in die branch aan de ReadMe-kant.
</Accordion>