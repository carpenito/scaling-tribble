---
title: Aangepaste Pagina's
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

<Callout icon="👍" theme="okay">
  Bekijk dit artikel als [een Aangepaste Pagina](https://docs.readme.com/page/custom-page)
</Callout>

Aangepaste Pagina's zijn ideaal wanneer je de bovenste navigatie van je ReadMe-project wilt behouden, maar ook een aangepaste weergave onder de zoekbalk wilt.

# Wat is er anders?

1. Geen linker zijbalknavigatie
2. Geen inhoudsopgave aan de rechterkant, ook niet wanneer koppen worden gebruikt
3. Ander URL-pad (submap is /page in plaats van /docs)
4. Geen Voorgestelde Bewerkingen
5. Geen paginastemming
6. Geen "x dagen geleden bijgewerkt"

<Callout icon="🚧" theme="warn">
  Aangepaste Pagina's worden niet beïnvloed door versiebeheer en worden gedeeld. Als je een Aangepaste Pagina verwijdert, wordt deze overal verwijderd.
</Callout>

# Wat is hetzelfde?

Met een [dropdown-subkopindeling](/main/docs/subheader-layout) verschijnt de Paginatitel in de broodkruimelnavigatie.

<Image align="center" border={true} width="smart" src="https://files.readme.io/14c46d5-Screen_Shot_2021-05-19_at_3.28.30_PM.png" className="border" />

> 📘 Opmerking
>
> De Aangepaste Paginatitel neemt de ruimte in van een Sectie in de broodkruimelnavigatie, maar maakt **geen** permanente Sectie aan in het vervolgkeuzemenu.

## Modi

Aangepaste Pagina's hebben twee modi:

1. **Markdown:** De standaardmodus die wordt gebruikt in de Documentatiesectie

<Image border={true} src="https://files.readme.io/5300f08-CleanShot_2022-10-15_at_08.56.122x.png" className="border" />

2. **HTML:** De code wordt [gesaneerd](https://en.wikipedia.org/wiki/HTML_sanitization). Als je CSS of JavaScript wilt opnemen, doe dit dan via Weergave > Aangepaste Javascript/Stylesheet.