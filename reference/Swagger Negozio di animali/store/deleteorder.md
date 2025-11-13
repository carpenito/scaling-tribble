---
title: Elimina ordine di acquisto per ID
excerpt: >-
  Per una risposta valida utilizza ID interi con valori interi positivi. Valori
  negativi o non interi genereranno errori API
api:
  file: petstore.json
  operationId: deleteOrder
hidden: false
link:
  new_tab: false
---
# Elimina ordine di acquisto per ID

Elimina un ordine di acquisto specificando il suo ID univoco.

## Panoramica

Questo endpoint consente di eliminare un ordine di acquisto esistente utilizzando il suo identificatore univoco. L'operazione è irreversibile e rimuoverà permanentemente l'ordine di acquisto dal sistema.

## Parametri

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|-------------|-------------|
| `id` | integer | Sì | L'ID univoco dell'ordine di acquisto da eliminare |

## Risposte

### 204 - Nessun Contenuto
L'ordine di acquisto è stato eliminato con successo.

### 400 - Richiesta Non Valida
La richiesta contiene parametri non validi.

### 401 - Non Autorizzato
Credenziali di autenticazione mancanti o non valide.

### 404 - Non Trovato
L'ordine di acquisto con l'ID specificato non è stato trovato.

## Esempi

### Richiesta di esempio
```http
DELETE /purchase-orders/123
Authorization: Bearer your-api-token
```

### Risposta di successo
```http
HTTP/1.1 204 No Content
```

### Risposta di errore (ID non trovato)
```http
HTTP/1.1 404 Not Found
Content-Type: application/json

{
  "error": "PURCHASE_ORDER_NOT_FOUND",
  "message": "L'ordine di acquisto con l'ID specificato non esiste",
  "suggestion": "Verifica che l'ID dell'ordine di acquisto sia corretto"
}
```

## Note Importanti

> ⚠️ **Attenzione**: Questa operazione è irreversibile. Una volta eliminato, l'ordine di acquisto non può essere recuperato.

> 📝 **Suggerimento**: Per una risposta valida, utilizza ID interi con valori interi positivi. Valori negativi o non interi genereranno errori API.

## Codici di Errore

| Codice | Descrizione |
|--------|-------------|
| `INVALID_ID` | L'ID fornito non è un numero intero valido |
| `PURCHASE_ORDER_NOT_FOUND` | L'ordine di acquisto con l'ID specificato non esiste |
| `UNAUTHORIZED` | Token di autenticazione mancante o non valido |
| `FORBIDDEN` | Autorizzazioni insufficienti per eliminare questo ordine |

## Casi d'Uso Comuni

- Annullamento di ordini di acquisto errati
- Pulizia di ordini di test durante lo sviluppo
- Rimozione di ordini duplicati
- Gestione del ciclo di vita degli ordini

## Sicurezza

Assicurati di:
- Utilizzare sempre HTTPS per le richieste API
- Mantenere sicuro il tuo token di autenticazione
- Verificare l'ID dell'ordine prima dell'eliminazione
- Implementare controlli di autorizzazione appropriati