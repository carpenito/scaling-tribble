---
title: Trova animali per stato
excerpt: È possibile fornire più valori di stato con stringhe separate da virgola
api:
  file: petstore.json
  operationId: findPetsByStatus
hidden: false
link:
  new_tab: false
---
# Trova animali per stato

Questo endpoint consente di recuperare animali domestici in base al loro stato corrente.

## Parametri

### Parametro status

- **Nome**: `status`
- **Tipo**: `string`
- **Richiesto**: Sì
- **Descrizione**: Valori di stato per filtrare i risultati. È possibile fornire più valori separati da virgola.

### Valori di stato disponibili

- `available` - Disponibile
- `pending` - In attesa
- `sold` - Venduto

## Esempi di utilizzo

### Ricerca singolo stato
```
GET /pet/findByStatus?status=available
```

### Ricerca multipli stati
```
GET /pet/findByStatus?status=available,pending
```

## Risposta

L'endpoint restituisce un array di oggetti animale domestico che corrispondono ai criteri di stato specificati.

### Esempio di risposta
```json
[
  {
    "id": 1,
    "name": "Doggie",
    "status": "available",
    "category": {
      "id": 1,
      "name": "Dogs"
    }
  },
  {
    "id": 2,
    "name": "Cat",
    "status": "pending",
    "category": {
      "id": 2,
      "name": "Cats"
    }
  }
]
```

## Codici di stato HTTP

- `200` - Operazione riuscita
- `400` - Valore di stato non valido
- `404` - Nessun animale trovato con i criteri specificati