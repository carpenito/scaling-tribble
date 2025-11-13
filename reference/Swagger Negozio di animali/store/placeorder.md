---
title: Effettua un ordine per un animale domestico
excerpt: API per effettuare un ordine per un animale domestico nel negozio
api:
  file: petstore.json
  operationId: placeOrder
hidden: false
link:
  new_tab: false
---
# Effettua un ordine per un animale domestico

Questo endpoint ti permette di effettuare un ordine per un animale domestico dal negozio.

## Parametri della richiesta

Per la maggior parte delle API, i moduli nelle pagine di riferimento API sono il modo più intuitivo per inserire i parametri del corpo per le richieste API.

### Esempio di dati del modulo

I dati del modulo inseriti genereranno un JSON simile a questo:

```json
{
  "complete": false,
  "id": 123,
  "petId": 456,
  "quantity": 1,
  "shipDate": "2023-11-27T10:30:00.000Z",
  "status": "placed"
}
```

## Risposta

Una volta effettuato con successo l'ordine, riceverai una conferma con i dettagli dell'ordine, incluso:

- ID dell'ordine
- Stato dell'ordine
- Data di spedizione stimata
- Dettagli dell'animale domestico ordinato

## Note importanti

- Assicurati che l'animale domestico sia disponibile prima di effettuare l'ordine
- Gli ordini vengono elaborati nell'ordine in cui vengono ricevuti
- Riceverai una notifica quando l'ordine cambia stato