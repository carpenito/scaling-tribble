---
title: Disconnette la sessione dell'utente attualmente autenticato
excerpt: >-
  Guida per disconnettere la sessione dell'utente attualmente autenticato dalla
  documentazione
api:
  file: petstore.json
  operationId: logoutUser
hidden: false
link:
  new_tab: false
---
# Disconnessione dell'Utente

Questa funzionalità consente di disconnettere un utente dalla sua sessione attualmente attiva nella documentazione.

## Come Funziona la Disconnessione

Quando un utente è autenticato nella tua documentazione, la sua sessione viene mantenuta tramite cookie del browser. La disconnessione termina questa sessione attiva e rimuove l'autenticazione dell'utente.

## Processo di Disconnessione

1. **L'utente richiede la disconnessione** - L'utente clicca sul pulsante di logout o accede all'endpoint di disconnessione
2. **Terminazione della sessione** - Il sistema invalida la sessione corrente dell'utente
3. **Rimozione dei cookie** - I cookie di autenticazione vengono rimossi dal browser
4. **Reindirizzamento** - L'utente viene reindirizzato alla pagina di login o alla homepage

## Scadenza Automatica della Sessione

<Accordion title="Configurazione della Scadenza del Login" icon="clock">
L'autenticazione persiste tramite cookie del browser. Puoi impostare un periodo di scadenza personalizzato nelle "opzioni avanzate" in **Navigazione Sito** > **Login Personalizzato** per richiedere agli utenti di effettuare nuovamente il login dopo un determinato periodo di tempo.

La configurazione predefinita include:
- **Durata sessione**: Tempo prima della scadenza automatica
- **Avviso di scadenza**: Notifica all'utente prima della disconnessione
- **Reindirizzamento automatico**: Pagina di destinazione dopo la disconnessione
</Accordion>

## Sicurezza della Sessione

<Cards columns="2">
  <Card title="Protezione della Sessione" icon="shield-alt">
    Mantieni sicuro il tuo hub per sviluppatori con timeout di autenticazione configurati correttamente. La disconnessione garantisce che le sessioni non rimangano attive indefinitamente.
  </Card>
  <Card title="Gestione Cookie" icon="cookie">
    I cookie di autenticazione vengono gestiti automaticamente durante il processo di disconnessione per garantire una pulizia completa della sessione.
  </Card>
</Cards>

## Considerazioni Importanti

- **Salvataggio automatico**: Assicurati che eventuali modifiche non salvate vengano gestite prima della disconnessione
- **Sessioni multiple**: Se l'utente ha sessioni attive su più dispositivi, questa azione disconnette solo la sessione corrente
- **Reindirizzamento**: Configura appropriatamente la pagina di destinazione post-disconnessione per una migliore esperienza utente

## Risoluzione dei Problemi

Se riscontri problemi con la disconnessione degli utenti:

<Tabs>
  <Tab title="Cookie non rimossi">
    Verifica che i cookie di dominio siano configurati correttamente e che il processo di logout li stia effettivamente cancellando.
  </Tab>
  <Tab title="Sessione persiste">
    Controlla le impostazioni di scadenza del login e assicurati che la logica di invalidazione della sessione funzioni correttamente.
  </Tab>
  <Tab title="Errori di reindirizzamento">
    Verifica che l'URL di reindirizzamento post-logout sia valido e accessibile all'utente.
  </Tab>
</Tabs>

---

> **Nota**: La disconnessione è un'operazione irreversibile per la sessione corrente. L'utente dovrà effettuare nuovamente il login per accedere ai contenuti personalizzati della documentazione.