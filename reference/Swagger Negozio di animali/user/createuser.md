---
title: Crea utente
excerpt: Questo può essere fatto solo dall'utente loggato.
api:
  file: petstore.json
  operationId: createUser
hidden: false
link:
  new_tab: false
---
# Crea utente

Crea un nuovo utente nel sistema. Questa operazione può essere eseguita solo dall'utente autenticato.

## Endpoint

```
POST /user
```

## Autenticazione

Questo endpoint richiede l'autenticazione. È necessario essere loggati per creare un nuovo utente.

## Parametri della richiesta

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| username | string | Sì | Nome utente per il nuovo account |
| email | string | Sì | Indirizzo email dell'utente |
| firstName | string | No | Nome dell'utente |
| lastName | string | No | Cognome dell'utente |
| password | string | Sì | Password per il nuovo account |

## Esempio di richiesta

```json
{
  "username": "nuovoutente",
  "email": "utente@example.com",
  "firstName": "Mario",
  "lastName": "Rossi",
  "password": "passwordsicura123"
}
```

## Risposta

### Successo (201 Created)

```json
{
  "id": 12345,
  "username": "nuovoutente",
  "email": "utente@example.com",
  "firstName": "Mario",
  "lastName": "Rossi",
  "createdAt": "2023-11-13T10:30:00Z",
  "status": "active"
}
```

### Errori

#### 400 Bad Request
Richiesta non valida - parametri mancanti o non validi

```json
{
  "error": "Bad Request",
  "message": "I campi username, email e password sono obbligatori"
}
```

#### 401 Unauthorized
Utente non autenticato

```json
{
  "error": "Unauthorized",
  "message": "È richiesta l'autenticazione per accedere a questa risorsa"
}
```

#### 409 Conflict
Utente già esistente

```json
{
  "error": "Conflict",
  "message": "Un utente con questo username o email esiste già"
}
```

## Note

- L'username deve essere univoco nel sistema
- L'indirizzo email deve essere valido e univoco
- La password deve rispettare i requisiti minimi di sicurezza
- Dopo la creazione, l'utente riceverà una email di conferma