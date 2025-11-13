---
title: Elimina un animale domestico
excerpt: Elimina un animale domestico dal negozio utilizzando l'API
api:
  file: petstore.json
  operationId: deletePet
hidden: false
link:
  new_tab: false
---
Per la maggior parte delle API, i form nelle pagine di riferimento API sono il modo più intuitivo per inserire i parametri del corpo per le richieste API. Nell'esempio del [petstore](https://petstore.swagger.io/) qui sotto, i seguenti dati del form:

<Image align="center" src="https://files.readme.io/f071cd2-CleanShot_2023-11-27_at_17.15.532x.png" />

...produrranno un JSON che assomiglia a questo:

```json
{ "complete": false, "id": 123 }
```

## Endpoint per Eliminare un Animale Domestico

Questo endpoint ti permette di eliminare un animale domestico dal negozio utilizzando l'ID dell'animale.

### Parametri

Il seguente parametro è richiesto per eliminare un animale domestico:

- **petId** (path parameter): L'ID dell'animale domestico da eliminare
  - Tipo: `integer (int64)`
  - Richiesto: `true`
  - Descrizione: ID dell'animale domestico da eliminare

### Intestazioni Richieste

- **api_key** (header): Chiave API per l'autenticazione
  - Tipo: `string`
  - Richiesto: `false`

### Esempio di Richiesta

```bash
DELETE /pet/{petId}
```

### Risposte

- **200**: Eliminazione riuscita
- **400**: ID animale domestico non valido
- **404**: Animale domestico non trovato

### Codici di Esempio

Ecco come puoi utilizzare questo endpoint in diversi linguaggi di programmazione:

<Tabs>
  <Tab title="JavaScript">
    ```javascript
    const petId = 123;
    const apiKey = 'your-api-key';

    fetch(`https://petstore.swagger.io/v2/pet/${petId}`, {
      method: 'DELETE',
      headers: {
        'api_key': apiKey
      }
    })
    .then(response => {
      if (response.ok) {
        console.log('Animale domestico eliminato con successo');
      } else {
        console.error('Errore durante l\'eliminazione');
      }
    });
    ```
  </Tab>
  <Tab title="Python">
    ```python
    import requests

    pet_id = 123
    api_key = 'your-api-key'
    url = f'https://petstore.swagger.io/v2/pet/{pet_id}'

    headers = {
        'api_key': api_key
    }

    response = requests.delete(url, headers=headers)

    if response.status_code == 200:
        print('Animale domestico eliminato con successo')
    else:
        print('Errore durante l\'eliminazione')
    ```
  </Tab>
  <Tab title="cURL">
    ```bash
    curl -X DELETE \
      'https://petstore.swagger.io/v2/pet/123' \
      -H 'api_key: your-api-key'
    ```
  </Tab>
</Tabs>

### Note Importanti

> ⚠️ **Attenzione**: L'eliminazione di un animale domestico è un'operazione permanente e non può essere annullata. Assicurati di confermare l'ID dell'animale prima di procedere.

### Gestione degli Errori

Quando si utilizza questo endpoint, è importante gestire adeguatamente i possibili errori:

- **Errore 400**: Verifica che l'ID fornito sia un numero intero valido
- **Errore 404**: L'animale domestico con l'ID specificato non esiste nel sistema
- **Errore di autenticazione**: Verifica che la tua chiave API sia valida e abbia i permessi necessari

Se riscontri problemi persistenti, consulta la documentazione completa dell'API o contatta il supporto tecnico.