---
title: Aggiorna utente
excerpt: Questo può essere fatto solo dall'utente autenticato.
api:
  file: petstore.json
  operationId: updateUser
hidden: false
link:
  new_tab: false
---
# Aggiorna utente

Questo endpoint consente di aggiornare le informazioni dell'utente attualmente autenticato.

## Autenticazione

Questo endpoint può essere utilizzato solo dall'utente autenticato. È necessario includere un token di autenticazione valido nella richiesta.

## Endpoint

```
PUT /user
```

## Parametri del corpo della richiesta

I seguenti parametri possono essere inclusi nel corpo della richiesta per aggiornare le informazioni dell'utente:

| Parametro | Tipo | Descrizione |
|-----------|------|-------------|
| `name` | string | Nome completo dell'utente |
| `email` | string | Indirizzo email dell'utente |
| `password` | string | Nuova password dell'utente (opzionale) |
| `profile` | object | Informazioni aggiuntive del profilo |

## Esempio di richiesta

```json
{
  "name": "Mario Rossi",
  "email": "mario.rossi@example.com",
  "profile": {
    "bio": "Sviluppatore software con passione per l'innovazione",
    "location": "Milano, Italia"
  }
}
```

## Risposte

### Successo (200)

Restituisce i dati aggiornati dell'utente.

```json
{
  "id": "user123",
  "name": "Mario Rossi", 
  "email": "mario.rossi@example.com",
  "profile": {
    "bio": "Sviluppatore software con passione per l'innovazione",
    "location": "Milano, Italia"
  },
  "updated_at": "2023-11-13T10:30:00Z"
}
```

### Errori

| Codice | Descrizione |
|--------|-------------|
| 400 | Dati della richiesta non validi |
| 401 | Non autenticato - token mancante o non valido |
| 403 | Non autorizzato - non è possibile modificare questo utente |
| 422 | Errore di validazione - controlla i dati forniti |

## Note importanti

- Solo l'utente autenticato può modificare le proprie informazioni
- L'indirizzo email deve essere unico nel sistema
- Se viene fornita una nuova password, deve rispettare i requisiti di sicurezza
- Tutti i campi sono opzionali - verranno aggiornati solo i campi forniti nella richiesta

## Esempio di codice

### JavaScript

```javascript
const updateUser = async (userData) => {
  const response = await fetch('/user', {
    method: 'PUT',
    headers: {
      'Content-Type': 'application/json',
      'Authorization': 'Bearer YOUR_TOKEN_HERE'
    },
    body: JSON.stringify(userData)
  });
  
  return response.json();
};
```

### Python

```python
import requests

def update_user(user_data, token):
    headers = {
        'Content-Type': 'application/json',
        'Authorization': f'Bearer {token}'
    }
    
    response = requests.put('/user', json=user_data, headers=headers)
    return response.json()
```