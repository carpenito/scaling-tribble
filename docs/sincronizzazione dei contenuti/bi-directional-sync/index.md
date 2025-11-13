---
title: Sincronizzazione Bi-direzionale
excerpt: >-
  La sincronizzazione bi-direzionale crea una connessione bidirezionale tra il
  tuo progetto ReadMe e un repository GitHub o GitLab, mantenendo il contenuto
  coerente su entrambe le piattaforme.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
La sincronizzazione bi-direzionale crea una connessione bidirezionale tra il tuo progetto ReadMe e un repository GitHub o GitLab. Questo flusso di lavoro opzionale mantiene il contenuto coerente su entrambe le piattaforme:

* Scrivi nel tuo ambiente preferito, che sia ReadMe o il tuo setup di sviluppo locale.
* Sviluppatori, ingegneri e technical writer possono collaborare utilizzando gli strumenti che preferiscono.
* Le modifiche si sincronizzano automaticamente tra ReadMe e Git creando un'unica fonte di verità.

<PlanTable currentPlan="Startup" />

***

## Configurazione della Sincronizzazione Bi-direzionale

ReadMe supporta la sincronizzazione bi-direzionale sia con <Anchor label="GitHub" target="_blank" href="https://docs.readme.com/main/docs/sync-with-github">GitHub</Anchor> che con <Anchor label="GitLab" target="_blank" href="https://docs.readme.com/main/docs/sync-with-gitlab">GitLab</Anchor>.

Per la sincronizzazione con GitHub, puoi connetterti a GitHub Cloud. Se sei sul piano Enterprise, ReadMe supporta la sincronizzazione bi-direzionale con <Anchor label="GitHub Enterprise Server" target="_blank" href="https://docs.readme.com/ent/docs/connecting-github-enterprise-server">GitHub Enterprise Server</Anchor>.

<Image align="center" border={true} src="https://files.readme.io/6335bcb6aa344d9d1f23d11b3cf420cbe94493872630760fb04d2cce9df10189-Screenshot_2025-10-27_at_12.29.28_PM.png" className="border" />

<Callout icon="❗️" theme="error">
  Il repository con cui stai sincronizzando deve essere vuoto—nessun commit o file (ad esempio, README.md)—prima di connettersi a ReadMe. Puoi aggiungere o rimuovere file dopo la configurazione.
</Callout>

***

## Versionamento della Documentazione

Se il tuo progetto ReadMe utilizza più [Versioni](doc:versions), solo la Versione Principale viene inizialmente sincronizzata quando abiliti per la prima volta la Sincronizzazione Bi-direzionale. Dopo aver abilitato con successo la Sincronizzazione Bi-direzionale, qualsiasi modifica alle altre versioni si sincronizzerà con il tuo repository Git.

***

## Modifica della Documentazione

Una volta configurata la Connessione Git, tutte le modifiche apportate nell'editor ReadMe si sincronizzeranno automaticamente con il tuo repository Git, e viceversa. Quando modifichi la documentazione in Git, puoi utilizzare il tuo editor di codice preferito o gli strumenti Git.

Per garantire una sincronizzazione riuscita da _Git a ReadMe_, segui queste linee guida strutturali:

**File Markdown:**

* I file devono includere il frontmatter richiesto: `title` e `summary`
* Il contenuto dovrebbe essere scritto in formato Markdown standard
* I nomi dei file devono corrispondere allo slug URL previsto per il routing corretto

**Navigazione:**

* L'ordine delle pagine è definito utilizzando file `_order.yaml`
* Ogni cartella di categoria può avere il proprio `order.yaml`
* La [struttura di navigazione](https://docs.readme.com/main/docs/documentation-structure#/) in Git rispecchia la gerarchia del tuo progetto ReadMe

**[Rami](https://docs.readme.com/main/docs/branches#/)**

* Il commit iniziale da ReadMe serve a stabilire la sincronizzazione dei rami con GitHub
* I nomi dei rami devono corrispondere esattamente ai nomi delle versioni definiti in ReadMe
* Qualsiasi versione e nome non corrispondente esisterà in GitHub e non si sincronizzerà con ReadMe.

<HTMLBlock>{`
<div class="migrating-column">
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-hexagon-exclamation"></i> Non sincronizzato
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2-new-branch
		</pre>
  </section>
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-circle-check"></i> Sincronizzato
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

### Gestione dei Conflitti

Quando viene rilevato un conflitto durante il salvataggio in ReadMe, il sistema ti richiederà immediatamente di Sovrascrivere le modifiche Git o Annullare il salvataggio e continuare a modificare. Le modifiche salvate in ReadMe corrisponderanno sempre a ciò che va online.

Durante il merge da GitHub, l'utente può risolvere i conflitti tramite l'editor GitHub o lo strumento di merge di loro scelta localmente prima di fare il push.

***

## FAQ

<Accordion title="Come si integra ReadMe con GitHub e quali permessi sono richiesti?" icon="fa-question-circle">
  ReadMe utilizza una GitHub App con accesso a livello repository: sola lettura per i metadati (richiesto) e lettura/scrittura per sincronizzare il contenuto. I webhook gestiscono sincronizzazioni, rilevamento delle modifiche e risoluzione dei conflitti.
</Accordion>

<Accordion title="Perché i miei rami non appaiono in GitHub o GitLab?" icon="fa-question-circle">
  I nuovi rami che crei dopo aver abilitato la sincronizzazione bi-direzionale creano automaticamente un ramo corrispondente negli strumenti Git, ma i rami esistenti non creeranno un ramo corrispondente negli strumenti Git finché non salvi una modifica a quel ramo in ReadMe.
</Accordion>

<Accordion title="Quali permessi sono richiesti quando si sincronizza con GitLab?" icon="fa-question-circle">
  ReadMe richiede accesso a:

  * `read_api` per elencare i progetti
  * `read_user` e `read_profile` per visualizzare le informazioni utente
  * `read_repository` per sincronizzare il contenuto in GitLab con ReadMe
  * `write_repository` per sincronizzare il contenuto in ReadMe con GitLab
</Accordion>