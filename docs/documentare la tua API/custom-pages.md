---
title: Pagine Personalizzate
excerpt: >-
  Le Pagine Personalizzate permettono di mantenere la navigazione superiore del
  progetto ReadMe con un aspetto personalizzato sotto la barra di ricerca.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
<br />

<Callout icon="👍" theme="okay">
  Visualizza questo articolo come [una Pagina Personalizzata](https://docs.readme.com/page/custom-page)
</Callout>

Le Pagine Personalizzate sono ideali quando vuoi mantenere la navigazione superiore del tuo progetto ReadMe, ma desideri anche un aspetto personalizzato sotto la barra di ricerca.

# Cosa cambia?

1. Nessuna barra di navigazione laterale sinistra
2. Nessun sommario a destra, anche quando vengono utilizzati i titoli
3. Percorso URL diverso (la sottocartella è /page invece di /docs)
4. Nessuna Modifica Suggerita
5. Nessun voto della pagina
6. Nessun "aggiornato x giorni fa"

<Callout icon="🚧" theme="warn">
  Le Pagine Personalizzate non sono influenzate dal controllo delle versioni e sono condivise. Se elimini una Pagina Personalizzata, verrà rimossa ovunque.
</Callout>

# Cosa rimane uguale?

Con un [layout di sottotestata a discesa](/main/docs/subheader-layout), il Titolo della Pagina appare nella navigazione breadcrumb.

<Image align="center" border={true} width="smart" src="https://files.readme.io/14c46d5-Screen_Shot_2021-05-19_at_3.28.30_PM.png" className="border" />

> 📘 Nota
>
> Il Titolo della Pagina Personalizzata occupa lo spazio di una Sezione nella navigazione breadcrumb ma **non** crea una Sezione permanente nel menu a discesa.

## Modalità

Le Pagine Personalizzate hanno due modalità:

1. **Markdown:** La modalità standard utilizzata nella sezione Documentazione

<Image border={true} src="https://files.readme.io/5300f08-CleanShot_2022-10-15_at_08.56.122x.png" className="border" />

2. **HTML:** Il codice viene [sanificato](https://en.wikipedia.org/wiki/HTML_sanitization). Se vuoi includere CSS o JavaScript, fallo in Aspetto > Javascript/Foglio di stile personalizzato.