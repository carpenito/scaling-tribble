---
title: Aggiungi un nuovo animale domestico al negozio
excerpt: >-
  Documentazione API per aggiungere un nuovo animale domestico al negozio
  utilizzando l'endpoint POST /pet
api:
  file: petstore.json
  operationId: addPet
hidden: false
link:
  new_tab: false
---
```json tags
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

Per la maggior parte delle API, i moduli sulle pagine di riferimento API sono il modo più intuitivo per inserire i parametri del corpo per le richieste API. Nell'esempio [petstore](https://petstore.swagger.io/) qui sotto, i seguenti dati del modulo:

<Image align="center" src="https://files.readme.io/f071cd2-CleanShot_2023-11-27_at_17.15.532x.png" />

...produrranno JSON che assomiglia a questo:

```json
{ "complete": false, "id": 123 }
```

Ogni percorso che ha un primo tag di `pet` verrebbe raggruppato insieme sotto una pagina padre vuota con il titolo di `pet`.

Ogni metodo verrebbe raggruppato insieme sotto una pagina con il titolo di `/pet`.

# Sottopagine

Una nuova sottopagina viene creata per ciascuno degli endpoint nel tuo documento OpenAPI.

Se presente, utilizziamo il `summary` dell'[oggetto Path Item](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/3.0.2.md#fixed-fields-7) come titolo della pagina. Se non hai un riassunto ma stai utilizzando tag, allora utilizziamo l'URL. Come ultima risorsa utilizziamo il metodo se non è disponibile nient'altro.

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