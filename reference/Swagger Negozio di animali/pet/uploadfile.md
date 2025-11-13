---
title: Carica un'immagine
excerpt: Carica un'immagine al tuo progetto ReadMe tramite l'API.
api:
  file: petstore.json
  operationId: uploadFile
hidden: false
link:
  new_tab: false
---
Carica un'immagine al tuo progetto ReadMe.

## Endpoint

`POST /images`

## Descrizione

Questo endpoint ti permette di caricare un'immagine al tuo progetto ReadMe. Le immagini caricate possono essere utilizzate nella documentazione, nelle pagine personalizzate e in altri contenuti del tuo progetto.

## Parametri della Richiesta

### Body della Richiesta

**Tipo di contenuto:** `multipart/form-data`

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|-------------|-------------|
| `file` | file | Sì | Il file immagine da caricare |

### Parametri della Query

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|-------------|-------------|
| `resize_height` | string | No | Se desideri ridimensionare quest'immagine, fornisci una nuova altezza in pixel. Nota che le GIF sono escluse e non possono essere ridimensionate. |

## Risposta

### 201 - Creato

Restituisce i dettagli dell'immagine caricata con successo.

**Schema della Risposta:**

```json
{
  "data": {
    "name": "string",
    "width": "number",
    "height": "number", 
    "color": "string",
    "links": {
      "original_url": "string"
    },
    "uri": "string",
    "url": "string"
  }
}
```

#### Proprietà della Risposta

| Proprietà | Tipo | Descrizione |
|-----------|------|-------------|
| `name` | string | Il nome del file immagine |
| `width` | number | La larghezza in pixel dell'immagine. Non presente per i file SVG. |
| `height` | number | L'altezza in pixel dell'immagine. Non presente per i file SVG. |
| `color` | string | Il colore primario contenuto nell'immagine. |
| `links.original_url` | string | Se l'immagine è stata ridimensionata durante il caricamento, questo sarà un URL al file originale. |
| `uri` | string | Un URI all'endpoint `getImages` per questa immagine. Se si tratta di un'immagine legacy, questo `uri` sarà `null`. |
| `url` | string | URL pubblico dell'immagine caricata |

## Autenticazione

Questo endpoint richiede l'autenticazione tramite Bearer token:

```
Authorization: Bearer YOUR_API_TOKEN
```

## Esempio di Richiesta

```bash
curl -X POST \
  https://api.readme.com/v2/images \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -F "file=@/path/to/your/image.jpg" \
  -F "resize_height=300"
```

## Note

- I formati di immagine supportati includono JPEG, PNG, GIF, SVG e altri formati comuni
- Le immagini GIF non possono essere ridimensionate
- L'API restituirà automaticamente le dimensioni e il colore primario dell'immagine
- Se specifichi un'altezza di ridimensionamento, l'immagine verrà ridimensionata mantenendo le proporzioni