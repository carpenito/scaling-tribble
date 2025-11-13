---
title: Riferimento API
excerpt: >-
  Guida completa su come creare e gestire un riferimento API in ReadMe, con
  OpenAPI, API Designer e personalizzazioni per una documentazione interattiva.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
# Cos'è un Riferimento API?

Un riferimento API è la guida tecnica definitiva alla tua API, che documenta ogni endpoint, parametro e codice di risposta nel dettaglio. È la tua fonte assoluta di verità a cui gli sviluppatori si rivolgono quando hanno bisogno di sapere esattamente come interagire con la tua API.

In ReadMe, il tuo riferimento API è un'esperienza interattiva dove gli sviluppatori possono esplorare la tua API, effettuare chiamate di test direttamente dalla documentazione e vedere risposte reali senza scrivere una singola riga di codice.

## Perché il Tuo Riferimento API è Importante

Un riferimento API ben realizzato può:

* **Ridurre i ticket di supporto** rispondendo alle domande tecniche prima che vengano poste
* **Accelerare l'onboarding degli sviluppatori** fornendo una guida di implementazione chiara e accurata
* **Costruire fiducia negli sviluppatori** dimostrando che la tua API è progettata e mantenuta con attenzione
* **Mostrare le piene capacità della tua API** in modo che gli sviluppatori scoprano funzionalità che altrimenti potrebbero perdere

## Come Iniziare con il Tuo Riferimento API

ReadMe offre diversi modi per creare e mantenere il tuo riferimento API, sia che tu stia lavorando con specifiche OpenAPI (precedentemente Swagger) o preferisca costruire il tuo riferimento manualmente.

### In Questa Sezione

Imparerai come:

* **Caricare e gestire le specifiche OpenAPI** attraverso diversi metodi
* **Lavorare con il nostro API Designer** se non hai una specifica OpenAPI
* **Personalizzare il tuo riferimento API** per adattarlo al tuo brand e migliorare l'usabilità
* **Creare esempi interattivi** che gli sviluppatori possono provare direttamente nella tua documentazione
* **Mantenere il tuo riferimento sincronizzato** con la tua API reale mentre evolve

## Caricamento e Gestione OpenAPI

ReadMe supporta completamente le specifiche OpenAPI 3.0, OpenAPI 3.1 e Swagger 2.0. Puoi aggiungere la tua specifica API a ReadMe in diversi modi:

* **Caricamento file**: Trascina e rilascia il tuo file OpenAPI/Swagger JSON o YAML
* **Importazione URL**: Indica a ReadMe dove si trova online la tua specifica
* **Integrazione GitHub**: Connettiti direttamente al tuo repository GitHub
* **Riga di comando (rdme)**: Usa il nostro strumento CLI per flussi di lavoro automatizzati
* **API Sync**: Mantieni il tuo riferimento API automaticamente sincronizzato con il tuo codice

Una volta caricata, ReadMe trasforma la tua specifica in documentazione interattiva splendidamente formattata che gli sviluppatori ameranno.

## API Designer

Non hai una specifica OpenAPI? Nessun problema! L'[API Designer](doc:building-apis-from-scratch-with-the-api-designer) di ReadMe ti permette di costruire il tuo riferimento API da zero con un'interfaccia intuitiva. Documenta i tuoi endpoint, parametri, corpi delle richieste e oggetti di risposta senza dover scrivere una singola riga di YAML o JSON.

## Personalizzazione del Tuo Riferimento API

Rendi il tuo riferimento API veramente tuo con le opzioni di personalizzazione:

* Aggiungi dettagli di autenticazione e header personalizzati
* Includi esempi di codice in diversi linguaggi di programmazione
* Organizza gli endpoint in gruppi logici
* Aggiungi documentazione personalizzata e panoramiche a ogni gruppo di endpoint

## Supporto GraphQL

Lavori con GraphQL? ReadMe offre supporto limitato ma in crescita per le [API GraphQL](doc:graphql). Puoi documentare i tuoi schemi, query e mutazioni per aiutare gli sviluppatori a navigare nella tua API GraphQL.

## Best Practice per i Riferimenti API

Per creare un riferimento API eccezionale:

* **Sii completo**: Documenta ogni endpoint, parametro e risposta
* **Includi esempi**: Mostra coppie di richiesta/risposta reali per casi d'uso comuni
* **Spiega gli errori**: Documenta tutti i codici di errore e come risolverli
* **Mantienilo aggiornato**: Aggiorna la documentazione ogni volta che la tua API cambia
* **Testalo tu stesso**: Usa regolarmente la tua stessa documentazione per individuare i problemi