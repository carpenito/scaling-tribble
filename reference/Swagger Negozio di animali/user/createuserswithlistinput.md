---
title: Crea lista di utenti con array di input fornito
excerpt: >-
  Endpoint API per creare una lista di utenti utilizzando un array di dati di
  input fornito
api:
  file: petstore.json
  operationId: createUsersWithListInput
hidden: false
link:
  new_tab: false
---
Questo endpoint API consente di creare più utenti contemporaneamente fornendo un array di oggetti utente. È particolarmente utile per operazioni di importazione in blocco o per la creazione di più account utente in una singola richiesta.

## Panoramica

Utilizzare questo endpoint per creare più utenti in una sola chiamata API, fornendo un array di oggetti utente nell'input.

### Parametri della Richiesta

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|-------------|-------------|
| `users` | Array | Sì | Array di oggetti utente da creare |

### Struttura dell'Oggetto Utente

Ogni oggetto utente nell'array deve contenere i seguenti campi:

```json
{
  "username": "string",
  "email": "string", 
  "password": "string",
  "firstName": "string",
  "lastName": "string",
  "phone": "string",
  "userStatus": "integer"
}
```

| Campo | Tipo | Obbligatorio | Descrizione |
|-------|------|-------------|-------------|
| `username` | String | Sì | Nome utente univoco |
| `email` | String | Sì | Indirizzo email valido |
| `password` | String | Sì | Password dell'utente |
| `firstName` | String | No | Nome dell'utente |
| `lastName` | String | No | Cognome dell'utente |
| `phone` | String | No | Numero di telefono |
| `userStatus` | Integer | No | Stato dell'utente (0 = inattivo, 1 = attivo) |

## Esempio di Richiesta

```json
POST /user/createWithList
Content-Type: application/json

[
  {
    "username": "mario_rossi",
    "email": "mario.rossi@example.com",
    "password": "password123",
    "firstName": "Mario",
    "lastName": "Rossi",
    "phone": "+39 123 456 7890",
    "userStatus": 1
  },
  {
    "username": "lucia_verdi",
    "email": "lucia.verdi@example.com", 
    "password": "password456",
    "firstName": "Lucia",
    "lastName": "Verdi",
    "phone": "+39 098 765 4321",
    "userStatus": 1
  }
]
```

## Risposte

### Successo (200 OK)

Quando tutti gli utenti sono stati creati con successo:

```json
{
  "message": "Utenti creati con successo",
  "created_users": [
    {
      "id": 1001,
      "username": "mario_rossi",
      "email": "mario.rossi@example.com"
    },
    {
      "id": 1002,
      "username": "lucia_verdi", 
      "email": "lucia.verdi@example.com"
    }
  ]
}
```

### Errore di Validazione (400 Bad Request)

Quando i dati di input non sono validi:

```json
{
  "error": "VALIDATION_ERROR",
  "message": "Dati di input non validi",
  "details": [
    {
      "field": "email",
      "message": "Formato email non valido",
      "user_index": 0
    }
  ]
}
```

### Errore di Conflitto (409 Conflict)

Quando un utente esiste già:

```json
{
  "error": "USER_EXISTS",
  "message": "Uno o più utenti esistono già",
  "existing_users": [
    {
      "username": "mario_rossi",
      "email": "mario.rossi@example.com"
    }
  ]
}
```

## Note Importanti

<Accordion title="Limitazioni" icon="exclamation-triangle">
- Massimo 100 utenti per richiesta
- Ogni nome utente deve essere univoco nel sistema
- Gli indirizzi email devono essere validi e univoci
- Le password devono rispettare i criteri di sicurezza minimi
</Accordion>

<Accordion title="Gestione degli Errori" icon="bug">
- Se uno qualsiasi degli utenti nell'array non supera la validazione, l'intera operazione fallisce
- Utilizzare l'endpoint di validazione per verificare i dati prima della creazione
- In caso di errore parziale, nessun utente verrà creato
</Accordion>

<Accordion title="Best Practices" icon="lightbulb">
- Validare tutti i dati lato client prima dell'invio
- Implementare una gestione appropriata degli errori nell'applicazione
- Considerare l'utilizzo di operazioni batch per grandi quantità di utenti
- Monitorare i limiti di rate limiting per evitare blocchi temporanei
</Accordion>

## Codici di Stato

| Codice | Descrizione |
|--------|-------------|
| 200 | Tutti gli utenti sono stati creati con successo |
| 400 | Richiesta non valida - errore di validazione dei dati |
| 401 | Non autorizzato - token API non valido o mancante |
| 409 | Conflitto - uno o più utenti esistono già |
| 422 | Entità non processabile - formato dei dati non corretto |
| 429 | Troppe richieste - limite di rate limiting raggiunto |
| 500 | Errore interno del server |

## Esempio di Implementazione

```javascript
// Esempio con JavaScript/Node.js
const createUsersWithList = async (users) => {
  try {
    const response = await fetch('/user/createWithList', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': 'Bearer YOUR_API_TOKEN'
      },
      body: JSON.stringify(users)
    });
    
    if (!response.ok) {
      throw new Error(`Errore HTTP: ${response.status}`);
    }
    
    const result = await response.json();
    console.log('Utenti creati:', result.created_users);
    return result;
  } catch (error) {
    console.error('Errore nella creazione degli utenti:', error);
    throw error;
  }
};

// Utilizzo
const nuoviUtenti = [
  {
    username: "utente1",
    email: "utente1@example.com",
    password: "password123",
    firstName: "Nome",
    lastName: "Cognome",
    userStatus: 1
  }
];

createUsersWithList(nuoviUtenti);
```