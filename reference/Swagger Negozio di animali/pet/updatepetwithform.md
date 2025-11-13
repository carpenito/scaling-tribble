---
title: Aggiorna un animale domestico nel negozio con dati del modulo
excerpt: >-
  Aggiorna un animale domestico nel negozio utilizzando i dati del modulo
  tramite l'API
api:
  file: petstore.json
  operationId: updatePetWithForm
hidden: false
link:
  new_tab: false
---
Per la maggior parte delle API, i moduli nelle pagine di riferimento API rappresentano il modo più intuitivo per inserire i parametri del corpo per le richieste API. Nell'esempio del [petstore](https://petstore.swagger.io/) qui sotto, i seguenti dati del modulo:

<Image align="center" src="https://files.readme.io/f071cd2-CleanShot_2023-11-27_at_17.15.532x.png" />

...produrranno JSON che appare così:

```json
{ "complete": false, "id": 123 }
```

## Tag JSON

```json
{
  "/pet": {
    "post": {
      "tags": [
        "pet"
      ],
      "summary": "Aggiungi un nuovo animale domestico al negozio",
      "operationId": "addPet"
    }
  }
}
```

Prendiamo il percorso `/pet`, rimuoviamo tutti i caratteri non alfanumerici, lo convertiamo in minuscolo e lo concateniamo alla fine del metodo. Quindi quello sopra diventerebbe `post_pet`.

> ❗️
>
> **Ti consigliamo di fornire sempre un `operationId` per ciascuno dei tuoi endpoint per ridurre il rischio di perdita di dati associata alla nostra creazione di un ID univoco per te.**

```json
{
  "/pet": {
    "get": {
      "summary": "Trova animale domestico per Nome",
      "description": "Restituisce un singolo animale domestico",
      "operationId": "getPetByName",
      "parameters": [
        {
          "name": "petName",
          "in": "body",
          "description": "Nome dell'animale domestico da restituire",
          "required": false,
          "schema": {
            "type": "string",
            "default": "Buster",
            "example": "Apollo"
          }
        }
      ]
    }
  }
}
```

## Formato File

Le pagine di documentazione utilizzano Markdown con metadati front matter:

```markdown
---
title: Elenca tutti i gufi
api:
  file: hoot.json
  operationId: get_owls
hidden: false
metadata:
  title: Il mio titolo SEO
  description: Una breve descrizione per SEO
  keywords:
    - parola_chiave1
    - parola_chiave2
---

# Contenuto Principale

Il contenuto della tua documentazione va qui...
```

* Una volta completato il flusso di configurazione nella pagina Primi Passi, la pagina mostrerà il widget Primi Passi in 3 passaggi a sinistra e il widget Attività Recenti a destra, con la possibilità di aggiungere Markdown qui sotto

Una volta completato il flusso di Configurazione, la pagina di Autenticazione rifletterà come apparirà nell'hub. Non puoi modificare il contenuto della Tabella Chiave API, Autenticazione e widget Esempio Codice, tuttavia gli ingranaggi in ogni widget sono cliccabili, permettendoti di cambiare l'URL del Server del Webhook Docs Personalizzati o cambiare l'endpoint selezionato. Puoi anche aggiungere più dettagli qui sotto utilizzando il nuovo editor Markdown:

* **Copia Markdown**: Permette agli utenti di copiare facilmente il contenuto dalla tua documentazione in formato markdown, rendendo semplice incollarlo in altri strumenti AI, IDE o documenti preservando la formattazione.

* **Visualizza come Markdown**: Consente agli utenti di vedere la struttura markdown sottostante delle pagine della tua documentazione, che è particolarmente utile per gli sviluppatori che vogliono capire come strutturare contenuti simili o fare riferimento al tuo stile di documentazione.