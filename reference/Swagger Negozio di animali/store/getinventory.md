---
title: Restituisce gli inventari di animali domestici per stato
excerpt: Restituisce una mappa dei codici di stato alle quantità
api:
  file: petstore.json
  operationId: getInventory
hidden: false
link:
  new_tab: false
---
# Ottieni Inventario

Questo endpoint restituisce gli inventari di animali domestici organizzati per stato. La risposta fornisce una mappa che associa i codici di stato alle rispettive quantità.

## Descrizione

L'endpoint `/store/inventory` consente di recuperare un riepilogo completo degli animali domestici disponibili nel negozio, categorizzati per il loro stato attuale. Questo è particolarmente utile per:

- Monitorare i livelli di inventario
- Tracciare la disponibilità degli animali domestici
- Gestire lo stock del negozio
- Analizzare la distribuzione degli stati

## Risposta

La risposta è un oggetto JSON dove:
- Le **chiavi** rappresentano i diversi stati degli animali domestici
- I **valori** rappresentano il numero di animali domestici in quello stato specifico

### Stati Tipici

I possibili stati degli animali domestici includono:

- **disponibile**: Animali domestici pronti per l'adozione
- **venduto**: Animali domestici già venduti
- **in attesa**: Animali domestici in processo di vendita o adozione

## Esempio di Risposta

```json
{
  "disponibile": 15,
  "venduto": 8,
  "in attesa": 3
}
```

## Utilizzo

Questo endpoint è ideale per:

<Cards columns={2}>
  <Card title="Dashboard di Inventario" icon="chart-bar">
    Visualizza rapidamente lo stato complessivo del tuo inventario di animali domestici
  </Card>
  <Card title="Gestione Stock" icon="boxes">
    Monitora i livelli di stock per prendere decisioni informate sui rifornimenti
  </Card>
  <Card title="Report Analitici" icon="analytics">
    Genera report sui trend di vendita e disponibilità
  </Card>
  <Card title="Integrazione Sistema" icon="plug">
    Integra con sistemi di gestione inventario esistenti
  </Card>
</Cards>

## Note Importanti

<Accordion title="Autenticazione" icon="key">
Questo endpoint potrebbe richiedere autenticazione a seconda della configurazione del server. Verifica i requisiti di autenticazione nella documentazione dell'API.
</Accordion>

<Accordion title="Limiti di Frequenza" icon="clock">
Potrebbero essere applicati limiti di frequenza per le richieste. Controlla gli header di risposta per informazioni sui limiti rimanenti.
</Accordion>

<Accordion title="Caching" icon="database">
I dati di inventario potrebbero essere memorizzati in cache. Per ottenere informazioni in tempo reale, considera l'utilizzo di parametri di query appropriati.
</Accordion>