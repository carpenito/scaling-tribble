---
title: Trova pet per ID
excerpt: Restituisce un singolo pet
api:
  file: petstore.json
  operationId: getPetById
hidden: false
link:
  new_tab: false
---
```json
{
  "/pet": {
    "get": {
      "summary": "Trova pet per Nome",
      "description": "Restituisce un singolo pet",
      "operationId": "getPetByName",
      "parameters": [
        {
          "name": "petName",
          "in": "body",
          "description": "Nome del pet da restituire",
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

Per la maggior parte delle API, i moduli sulle pagine di riferimento API sono il modo più intuitivo per inserire i parametri del corpo per le richieste API. Nell'esempio [petstore](https://petstore.swagger.io/) qui sotto, i seguenti dati del modulo:

<Image align="center" src="https://files.readme.io/f071cd2-CleanShot_2023-11-27_at_17.15.532x.png" />

...produrranno JSON che assomiglia a questo:

```json
{ "complete": false, "id": 123 }
```

Ogni metodo verrebbe raggruppato insieme sotto una pagina con il titolo di `/pet`.

# Sottopagine

Una nuova sottopagina viene creata per ciascuno degli endpoint nel tuo documento OpenAPI.

Se presente, utilizziamo il `summary` dell'[oggetto Path Item](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#fixed-fields-7) come titolo della pagina. Se non hai un summary ma stai usando tags, allora utilizziamo l'URL. Come fallback utilizziamo il metodo se nient'altro è disponibile.

Prendiamo il percorso `/pet`, rimuoviamo tutti i caratteri non alfanumerici, lo convertiamo in minuscolo e lo concateniamo alla fine del metodo. Quindi l'esempio sopra diventerebbe `post_pet`.

> ❗️
>
> **Ti consigliamo di fornire sempre un `operationId` per ciascuno dei tuoi endpoint per ridurre il rischio di perdita di dati associato alla creazione di un ID univoco da parte nostra.**