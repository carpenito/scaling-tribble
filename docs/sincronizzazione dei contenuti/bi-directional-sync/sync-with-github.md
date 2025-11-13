---
title: Sincronizzazione con GitHub
excerpt: >-
  Scopri come configurare la sincronizzazione bidirezionale tra ReadMe e GitHub,
  gestire i repository e modificare la documentazione.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
## Come Configurare la Sincronizzazione Bidirezionale con GitHub

### Prerequisiti

* Avrai bisogno di un account GitHub.
* Quando sincronizzi con un repository in un'organizzazione, avrai bisogno del permesso per creare un **repository vuoto**.

### Configurazione

1. Naviga alla pagina **Impostazioni** > **Connessione Git**.
2. Seleziona GitHub.
3. Se non l'hai già fatto, crea un repository vuoto in [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)—assicurati di deselezionare l'opzione per creare un README.
4. **Sincronizza** con il tuo provider e autenticati. Concedi l'accesso al repository con cui vuoi sincronizzarti e conferma il tuo repository nella schermata successiva.

***

## Cambiare Repository

1. All'interno di ReadMe, disconnetti il progetto tramite l'icona del cestino.
2. All'interno di GitHub, crea il tuo nuovo repository (deve essere vuoto).
3. Naviga a **Applicazioni > App GitHub Installate**.
4. Trova **ReadMe Sync** e clicca **Configura**.
5. Sotto _Accesso al repository_, seleziona il nuovo repository con cui vuoi sincronizzarti.
6. Torna a ReadMe e connettiti al tuo nuovo repository.

***

## Modificare la Tua Documentazione

**[Branch](https://docs.readme.com/main/docs/branches#/)**

* Il commit iniziale da ReadMe serve a stabilire la sincronizzazione dei branch con GitHub
* I nomi dei branch devono corrispondere esattamente ai nomi delle versioni definite in ReadMe
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

***

### GitHub Enterprise Server

Se stai utilizzando un **[GitHub Enterprise Server (GHES)](https://docs.readme.com/ent/docs/connecting-github-enterprise-server)** auto-ospitato, puoi configurare la sincronizzazione dalla tua dashboard di Gruppo sotto **Connessione Git**. La sincronizzazione richiede un repository nuovo e vuoto, e ogni progetto figlio può sincronizzarsi solo con un repository.

<Image align="center" border={false} src="https://files.readme.io/bd2640dae70270e20b0a71ae98adf56bd4e3a59b275b1609e86bbc4fc8ad81cd-GHES.png" />

Se GHES non è disponibile per il tuo progetto, contatta il tuo Customer Success Manager.

### Protezione Branch GitHub

Se il tuo repository GitHub utilizza regole di protezione dei branch, dovrai configurarle per permettere all'app ReadMe Sync di inviare modifiche. Ecco come configurarla in base alla tua configurazione GitHub:

#### Per GitHub Rulesets (Nuova Versione)

1. Naviga alle impostazioni di protezione dei branch del tuo repository.
2. Nella sezione _Elenco bypass_, **+ Aggiungi bypass**.
3. Cerca _ReadMe Sync_ (App • readmeio) e imposta il permesso su **Consenti sempre**.

<Image align="center" alt="Aggiungere ReadMe Sync all'elenco bypass di GitHub Rulesets per l'accesso push diretto." border={false} caption="Aggiungere ReadMe Sync all'elenco bypass di GitHub Rulesets per l'accesso push diretto." src="https://files.readme.io/0e52415eb4dede062a4d9df4a2d3f06dda62500c26caae7f000e4ecd50f4521d-Screenshot_2024-11-22_at_11.12.14_AM.png" width="600px" />

#### Per Protezione Branch Legacy

1. Vai alle regole di protezione dei branch del tuo repository.
2. Trova la sezione _Consenti agli attori specificati di bypassare le pull request obbligatorie_.
3. Aggiungi _readme-sync_ (ReadMe Sync) all'elenco degli attori consentiti.

<Image align="center" alt="Configurare ReadMe Sync nelle impostazioni di protezione branch legacy per bypassare i requisiti delle pull request." border={false} caption="Configurare ReadMe Sync nelle impostazioni di protezione branch legacy per bypassare i requisiti delle pull request." src="https://files.readme.io/8f3765d6ebbe96f5a93e4c6f915e52392ad6ba1512d0af4d4113ca8ff6ef8077-Screenshot_2024-11-22_at_11.12.07_AM.png" />

Questa configurazione assicura che le modifiche apportate nell'editor di ReadMe possano essere sincronizzate con i branch protetti nel tuo repository GitHub.

***

<br />

## FAQ

<Accordion title="Come si integra ReadMe con GitHub e quali permessi sono richiesti?" icon="fa-question-circle">
  ReadMe utilizza una GitHub App con accesso a livello di repository: sola lettura per i metadati (richiesto) e lettura/scrittura per sincronizzare il contenuto. I webhook gestiscono le sincronizzazioni, il rilevamento delle modifiche e la risoluzione dei conflitti.
</Accordion>

<Accordion title="Perché i miei branch non appaiono su GitHub?" icon="fa-question-circle">
  I nuovi branch che crei dopo aver abilitato la sincronizzazione bidirezionale creano automaticamente un branch corrispondente su Github, ma i branch esistenti non creeranno un branch corrispondente su GitHub finché non salvi una modifica (anche piccola) a quel branch sul lato ReadMe.
</Accordion>