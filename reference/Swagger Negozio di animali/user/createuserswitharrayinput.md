---
title: Crea una lista di utenti con array di input dato
excerpt: >-
  Crea più utenti contemporaneamente utilizzando un array di oggetti utente come
  input
api:
  file: petstore.json
  operationId: createUsersWithArrayInput
hidden: false
link:
  new_tab: false
---
# Crea una lista di utenti con array di input dato

Questo endpoint consente di creare più utenti contemporaneamente utilizzando un array di oggetti utente come input.

## Endpoint

`POST /user/createWithArray`

## Descrizione

Questo endpoint accetta un array di oggetti utente e crea tutti gli utenti specificati nell'array in una singola operazione. È utile per operazioni di importazione in blocco o quando è necessario creare più utenti contemporaneamente.

## Parametri

### Body della richiesta

Il body della richiesta deve contenere un array JSON di oggetti utente. Ogni oggetto utente nell'array deve avere la seguente struttura:

```json
[
  {
    "id": 1,
    "username": "nomeutente1",
    "firstName": "Mario",
    "lastName": "Rossi",
    "email": "mario.rossi@example.com",
    "password": "password123",
    "phone": "+39123456789",
    "userStatus": 1
  },
  {
    "id": 2,
    "username": "nomeutente2", 
    "firstName": "Anna",
    "lastName": "Verdi",
    "email": "anna.verdi@example.com",
    "password": "password456",
    "phone": "+39987654321",
    "userStatus": 1
  }
]
```

### Campi obbligatori

- `username` (stringa): Nome utente univoco
- `email` (stringa): Indirizzo email dell'utente
- `password` (stringa): Password dell'utente

### Campi opzionali

- `id` (numero): ID univoco dell'utente
- `firstName` (stringa): Nome dell'utente
- `lastName` (stringa): Cognome dell'utente  
- `phone` (stringa): Numero di telefono dell'utente
- `userStatus` (numero): Stato dell'utente (0 = inattivo, 1 = attivo)

## Esempio di richiesta

```bash
curl -X POST "https://api.example.com/user/createWithArray" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_TOKEN" \
  -d '[
    {
      "username": "testuser1",
      "firstName": "Test",
      "lastName": "User",
      "email": "test1@example.com",
      "password": "test123",
      "userStatus": 1
    },
    {
      "username": "testuser2", 
      "firstName": "Another",
      "lastName": "User",
      "email": "test2@example.com",
      "password": "test456",
      "userStatus": 1
    }
  ]'
```

## Risposta

### Successo (200)

```json
{
  "success": true,
  "message": "Utenti creati con successo",
  "data": {
    "created_users": 2,
    "user_ids": [1, 2]
  }
}
```

### Errore (400 - Richiesta non valida)

```json
{
  "success": false,
  "message": "Dati di input non validi",
  "errors": [
    {
      "field": "username",
      "message": "Il nome utente è obbligatorio"
    },
    {
      "field": "email", 
      "message": "L'email deve avere un formato valido"
    }
  ]
}
```

### Errore (409 - Conflitto)

```json
{
  "success": false,
  "message": "Alcuni utenti esistono già",
  "conflicts": [
    {
      "username": "testuser1",
      "message": "Nome utente già esistente"
    }
  ]
}
```

## Note importanti

<Accordion title="Limitazioni" icon="exclamation-triangle">
- L'array può contenere un massimo di 100 oggetti utente per richiesta
- Tutti i nomi utente devono essere univoci all'interno dell'array
- Gli indirizzi email devono essere unici all'interno dell'array
</Accordion>

<Accordion title="Validazione" icon="check-circle">
- Tutti i campi vengono validati prima della creazione
- Se un utente nell'array non è valido, l'intera operazione viene annullata
- I nomi utente e le email vengono controllati per duplicati esistenti nel sistema
</Accordion>

<Accordion title="Sicurezza" icon="shield-alt">
- Questo endpoint richiede autenticazione
- Le password vengono automaticamente crittografate prima del salvataggio
- È consigliabile utilizzare HTTPS per tutte le richieste
</Accordion>

## Codici di stato HTTP

| Codice | Descrizione |
|--------|-------------|
| 200 | Tutti gli utenti sono stati creati con successo |
| 400 | Richiesta non valida - errori di validazione |
| 401 | Non autorizzato - token di accesso mancante o non valido |
| 403 | Proibito - permessi insufficienti |
| 409 | Conflitto - utenti duplicati |
| 500 | Errore interno del server |

## Esempi di implementazione

<Tabs>
  <Tab title="JavaScript">
    ```javascript
    const users = [
      {
        username: "utente1",
        firstName: "Mario",
        lastName: "Rossi", 
        email: "mario@example.com",
        password: "password123"
      },
      {
        username: "utente2",
        firstName: "Anna",
        lastName: "Verdi",
        email: "anna@example.com", 
        password: "password456"
      }
    ];

    const response = await fetch('/user/createWithArray', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': 'Bearer ' + token
      },
      body: JSON.stringify(users)
    });

    const result = await response.json();
    console.log('Utenti creati:', result);
    ```
  </Tab>
  
  <Tab title="Python">
    ```python
    import requests
    import json

    users = [
        {
            "username": "utente1",
            "firstName": "Mario", 
            "lastName": "Rossi",
            "email": "mario@example.com",
            "password": "password123"
        },
        {
            "username": "utente2",
            "firstName": "Anna",
            "lastName": "Verdi", 
            "email": "anna@example.com",
            "password": "password456"
        }
    ]

    headers = {
        'Content-Type': 'application/json',
        'Authorization': 'Bearer ' + token
    }

    response = requests.post(
        'https://api.example.com/user/createWithArray',
        headers=headers,
        data=json.dumps(users)
    )

    result = response.json()
    print('Utenti creati:', result)
    ```
  </Tab>

  <Tab title="PHP">
    ```php
    <?php
    $users = [
        [
            'username' => 'utente1',
            'firstName' => 'Mario',
            'lastName' => 'Rossi',
            'email' => 'mario@example.com', 
            'password' => 'password123'
        ],
        [
            'username' => 'utente2',
            'firstName' => 'Anna',
            'lastName' => 'Verdi',
            'email' => 'anna@example.com',
            'password' => 'password456'
        ]
    ];

    $curl = curl_init();
    curl_setopt_array($curl, [
        CURLOPT_URL => 'https://api.example.com/user/createWithArray',
        CURLOPT_RETURNTRANSFER => true,
        CURLOPT_POST => true,
        CURLOPT_POSTFIELDS => json_encode($users),
        CURLOPT_HTTPHEADER => [
            'Content-Type: application/json',
            'Authorization: Bearer ' . $token
        ]
    ]);

    $response = curl_exec($curl);
    $result = json_decode($response, true);
    
    echo 'Utenti creati: ' . print_r($result, true);
    ?>
    ```
  </Tab>
</Tabs>