---
title: Accesso utente al sistema
excerpt: Guida per effettuare l'accesso degli utenti al sistema di documentazione
api:
  file: petstore.json
  operationId: loginUser
hidden: false
link:
  new_tab: false
---
1. L'utente clicca sul link di Login in ReadMe e viene indirizzato a una pagina di Login sul tuo sito.
2. L'utente effettua l'accesso (o è già autenticato).
3. Il tuo sito crea un URL di redirect JWT con le informazioni dell'utente.
4. L'utente viene reindirizzato alla tua documentazione e accede a ReadMe!

Dietro le quinte, il processo di login è guidato da un URL di redirect che contiene un [JSON Web Token (JWT)](https://jwt.io/) speciale per quell'utente. Il token codificato dovrebbe includere alcuni dati di base sull'utente, come nome e indirizzo email. Puoi leggere di più su Custom Login e JWT nella [pagina della documentazione dedicata](https://docs.readme.com/docs/custom-login-page).

Nella sezione **Settings > Custom Login** della dashboard del tuo progetto, puoi aggiungere un URL a cui gli utenti verranno indirizzati tramite il pulsante di login nella tua documentazione. (Per un esempio di una pagina di login personalizzata, dai un'occhiata al nostro [progetto demo Node.js](https://github.com/readmeio/readme-custom-login-demo/blob/master/views/index.jade).)

<Image title="custom-login.png" alt="redirect login personalizzato" align="center" src="https://files.readme.io/76aac10-custom-login.png">
  redirect login personalizzato
</Image>

Affinché un utente possa avere un'esperienza di documentazione personalizzata, dobbiamo prima sapere... chi è quell'utente! Quindi il primo passo è far accedere i tuoi utenti al tuo hub di sviluppatori. Sono disponibili diversi tipi di opzioni di login:

## Opzione 1: Login Basato su ReadMe 🦉

Questo è il metodo di login *fantastico-di-default* per i tuoi utenti quando configuri un hub di sviluppatori con noi. Prendi come esempio un'azienda, come [l'Acme Corporation](https://en.wikipedia.org/wiki/Acme_Corporation). Questo è come apparirebbe la pagina di login per l'hub di sviluppatori di Acme alimentato da ReadMe, senza alcuna configurazione: