---
title: Sincronizzazione con GitLab
excerpt: >-
  Guida completa per configurare la sincronizzazione bidirezionale tra ReadMe e
  GitLab
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
## Come Configurare la Sincronizzazione Bidirezionale con GitLab

### Prerequisiti

* È necessario avere un account GitLab.
* Quando si sincronizza con un repository in un'organizzazione, sarà necessario avere il permesso di creare un **repository vuoto**.

<Image align="center" border={false} src="https://files.readme.io/d2a12db436be321b972fd817432f3754a13d61c0ecb915202862e58fb2252cc1-Screenshot_2025-10-31_at_1.43.41_PM.png" />

### Configurazione

1. Naviga alla pagina **Impostazioni** > **Connessione Git**.
2. Seleziona GitLab.
3. Se non l'hai già fatto, crea un repository vuoto in [GitLab](https://docs.gitlab.com/user/project/)—assicurati di deselezionare l'opzione per creare un README.
4. **Sincronizza** con il tuo provider e autenticati.
5. Crea un token di accesso personale con lo scope `api`. Puoi eliminare questo token dopo aver completato la configurazione. ReadMe utilizza questo token una sola volta durante la configurazione per creare il webhook sul tuo repository e non viene memorizzato.
   1. Per i token di accesso del progetto, avrai bisogno del ruolo Maintainer. Tuttavia, questo non è raccomandato in quanto c'è un limite al numero di token di accesso del progetto creati, a seconda del piano tariffario di GitLab.

<Image border={false} src="https://files.readme.io/b350ddb7403c7d0ffbaa7d4f8e4c5fc6ca0d92308c4c81bde90b2c2b146a1ed3-image.png" />

6. Aggiungi il token di accesso a ReadMe e clicca sull'icona del webhook per creare i webhook necessari per mantenere sincronizzato il tuo contenuto con GitLab.

***

## Cambiare Repository

Se hai bisogno di connettere il tuo progetto ReadMe a un repository diverso, devi disconnettere il repository originale utilizzando l'icona del cestino.

1. All'interno di ReadMe, disconnetti il progetto tramite l'icona del cestino.
2. All'interno di GitLab, crea un nuovo progetto vuoto.
3. Torna a ReadMe e seleziona il progetto con cui desideri sincronizzarti.

***

## Branch Protetti

Tutte le regole dei branch dovrebbero consentire all'utente (che sta sincronizzando da ReadMe a GitLab) di effettuare push.

<Image border={false} src="https://files.readme.io/5ab0dbdd08ca7f9fc31d8a6895ebb9a970819ea4f2c352c92307ab5886b14541-image.png" />

## FAQ

<Accordion title="Quali permessi sono richiesti quando si sincronizza con GitLab?" icon="fa-question-circle">
  ReadMe richiede accesso a:

  * `read_api` per elencare i progetti
  * `read_user` e `read_profile` per visualizzare le informazioni dell'utente
  * `read_repository` per sincronizzare il contenuto da GitLab a ReadMe
  * `write_repository` per sincronizzare il contenuto da ReadMe a GitLab
</Accordion>

<br />