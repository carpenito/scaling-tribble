---
title: Trova ordine di acquisto per ID
excerpt: >-
  Per una risposta valida, prova ID interi con valore >= 1 e <= 10. Altri valori
  genereranno eccezioni
api:
  file: petstore.json
  operationId: getOrderById
hidden: false
link:
  new_tab: false
---
# Trova ordine di acquisto per ID

Questo endpoint permette di recuperare un ordine di acquisto specifico utilizzando il suo identificativo univoco.

## Parametri

| Nome | Tipo | Descrizione |
|------|------|-------------|
| `orderId` | integer | L'ID dell'ordine di acquisto da recuperare |

## Risposta di successo

Restituisce i dettagli dell'ordine di acquisto richiesto.

## Note importanti

> **⚠️ Valori di test validi**
> 
> Per una risposta valida, utilizzare ID interi con valore compreso tra 1 e 10 (inclusi).
> 
> Altri valori genereranno delle eccezioni.

## Esempi

### Richiesta di esempio

```http
GET /store/order/{orderId}
```

### Parametri di esempio

- `orderId`: 5 (valore valido per il test)

## Gestione degli errori

L'API restituirà un errore se:
- L'ID fornito non è compreso nell'intervallo 1-10
- L'ID non è un numero intero valido
- L'ordine non esiste

## Codici di risposta

| Codice | Descrizione |
|--------|-------------|
| 200 | Ordine trovato con successo |
| 400 | ID ordine non valido |
| 404 | Ordine non trovato |