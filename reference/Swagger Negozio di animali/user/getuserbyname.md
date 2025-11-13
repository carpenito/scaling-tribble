---
title: Ottieni utente per nome utente
excerpt: >-
  Ottieni indirizzi email unici di utenti con il maggior numero di
  visualizzazioni per un progetto, ordinati per visualizzazioni totali per
  utente.
api:
  file: petstore.json
  operationId: getUserByName
hidden: false
link:
  new_tab: false
---
Grazie alle [pagine Introduzione e Autenticazione](https://docs.readme.com/main/docs/reference-core-pages#/) nel tuo Riferimento API, è molto più facile per i nuovi utenti iniziare con la tua API. Hanno le loro [chiavi API in primo piano](https://docs.readme.com/main/docs/personalized-docs#/), possono fare richieste autenticate dalla tua documentazione, copiare e incollare frammenti di codice, e vedere le risposte in tempo reale.

<Image alt="Un endpoint di riferimento API in ReadMe. Nota il menu a discesa sul lato destro. Contiene l'elenco delle chiavi API dell'utente connesso, che vengono automaticamente visualizzate in modo che l'utente possa immediatamente iniziare a fare richieste API autenticate 🚀" align="center" src="https://files.readme.io/533cec7-Screen_Shot_2022-09-28_at_12.59.14_PM.png">

Un endpoint di riferimento API in ReadMe. Nota il menu a discesa sul lato destro. Contiene l'elenco delle chiavi API dell'utente connesso, che vengono automaticamente visualizzate in modo che l'utente possa immediatamente iniziare a fare richieste API autenticate 🚀
</Image>

Le pagine **Introduzione** e **Autenticazione** nella sezione Riferimento API ti aiutano proprio a fare questo — e a creare un'esperienza molto più interattiva e personalizzata per i tuoi sviluppatori. Una volta configurate, queste pagine ti permettono di mostrare facilmente le chiavi API ai tuoi utenti connessi, così non devono consultare una pagina separata delle impostazioni sul tuo sito web prima di iniziare.

## Parametri

| Parametro | Descrizione |
|-----------|-------------|
| `rangeLength` | Lunghezza dell'intervallo di date (numero, predefinito: 30, minimo: 1, massimo: 720) |
| `resolution` | Intervallo temporale relativo dei gruppi di dati (stringa, predefinito: "day", valori: "hour", "day", "week", "month", "year") |
| `rangeStart` | Data di inizio (stringa, formato: date, esempio: "2021-01-01") |
| `rangeEnd` | Data di fine (stringa, formato: date, esempio: "2021-01-01") |
| `x-timezone` | Fuso orario locale in formato IANA (stringa, predefinito: "UTC") |
| `limit` | Il numero di risultati da recuperare (numero, predefinito: 30, massimo: 500, minimo: 1) |
| `page` | La pagina corrente dell'elenco dei risultati (numero, predefinito: 0) |
| `pageSize` | Numero di elementi per pagina (numero, predefinito: 30, massimo: 100, minimo: 1) |

## Risposte

### 200 - Successo

Utenti principali per numero di pagine visualizzate e conteggi associati.

**Schema della risposta:**
```json
{
  "users": {
    "additionalProperties": [
      {
        "email": "string",
        "count": "number"
      }
    ]
  }
}
```

## Sicurezza

Questo endpoint richiede l'autenticazione tramite chiave API utilizzando lo schema HTTP Basic.

## Esempio di Utilizzo

Questo endpoint è utile per ottenere informazioni sugli utenti che stanno visualizzando maggiormente le pagine della tua documentazione. Puoi utilizzare questi dati per:

- Identificare gli utenti più attivi
- Analizzare i pattern di utilizzo
- Personalizzare l'esperienza utente basata sul coinvolgimento

### 3. Recuperare l'Utente e Rispondere con JSON

Una volta verificato che la richiesta provenga da ReadMe, il passo successivo è recuperare i dati necessari per l'utente che ha effettuato l'accesso. Questo passaggio varierà a seconda di come appare la tua API e di come sono memorizzati i tuoi dati. ReadMe invierà l'indirizzo email dell'utente connesso nel corpo `POST`, che può essere utilizzato per recuperare le informazioni dell'utente dal database (o dovunque sia memorizzata la sua chiave API e altre informazioni necessarie).

ReadMe ha diversi strumenti disponibili per aiutarti a personalizzare l'esperienza di documentazione dei tuoi utenti per ogni fase del loro percorso. Ci sono due passaggi chiave per raggiungere questo obiettivo: fare **accedere** i tuoi utenti al tuo hub, e poi **mostrare dati utente personalizzati** come chiavi API o variabili server a ogni utente. Ti guideremo attraverso entrambi qui sotto.

# Come Far Accedere i Tuoi Utenti 🔐