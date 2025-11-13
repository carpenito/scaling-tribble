---
title: Trova Animali per Tag
excerpt: >-
  È possibile fornire più tag utilizzando stringhe separate da virgole.
  Utilizzare tag1, tag2, tag3 per i test.
api:
  file: petstore.json
  operationId: findPetsByTags
deprecated: true
hidden: false
link:
  new_tab: false
---
# Trova Animali per Tag

Questo endpoint consente di cercare animali domestici utilizzando uno o più tag. È possibile specificare più tag per restringere i risultati di ricerca.

## Parametri

### Tag
- **Tipo**: Stringa
- **Obbligatorio**: Sì
- **Descrizione**: Tag utilizzati per filtrare gli animali domestici. È possibile fornire più tag separati da virgole.

## Esempi di Utilizzo

### Ricerca con un singolo tag
```
tag1
```

### Ricerca con più tag
```
tag1,tag2,tag3
```

## Note per i Test

Per testare questo endpoint, è possibile utilizzare i seguenti tag di esempio:
- `tag1`
- `tag2` 
- `tag3`

Questi tag possono essere combinati utilizzando la virgola come separatore per testare diverse combinazioni di ricerca.

## Formato della Risposta

L'endpoint restituirà una lista di animali domestici che corrispondono ai tag specificati. Gli animali che hanno almeno uno dei tag forniti saranno inclusi nei risultati.

## Esempi di Richiesta

```http
GET /pet/findByTags?tags=tag1,tag2
```

Questa richiesta troverà tutti gli animali domestici che hanno il tag "tag1" o "tag2" o entrambi.