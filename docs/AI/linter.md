---
title: Linter
deprecated: false
hidden: false
metadata:
  robots: index
---
De Linter automatiseert inhoudsvalidatie door documentatie te controleren aan de hand van de stijlgids en schrijfstandaarden van uw bedrijf. Het stroomlijnt het handmatige beoordelingsproces dat schrijvers doorgaans uitvoeren met externe tools.

U kunt aangepaste regels configureren om codeopmaak, woordkeuze en naleving van interne stijl en best practices af te dwingen. Of uw documentatie nu aangepaste HTML of uitgebreide codevoorbeelden bevat, de Linter zorgt voor consistentie in al uw docs.

<PlanTable currentPlan="Startup" />

## Configureren

U kunt prompts toevoegen aan de Linter die worden gecategoriseerd als stijlgids, fouten of waarschuwingen.

<Image border={false} src="https://files.readme.io/6844539c6c370fbc5fe87fa2bab007e50aa4fb52673fa629d247d0836534c971-image.png" />

**Stijlgids**: Schrijf over wat geweldige docs maakt en de Linter beoordeelt uw inhoud. Voorbeeld:

> Houd het kort:
>
> Korte tekst is altijd beter. Korte alinea's zijn gemakkelijker te lezen. Probeer koppen tot één regel te beperken. Koppen van twee regels nemen twee keer zoveel verticale ruimte in. Gebruik korte woorden in koppen; als een gebruiker grotere lettertypen gebruikt voor toegankelijkheid, kunnen lange woorden over regels breken.

<br />

> Duidelijkheid:
>
> Heldere en beknopte tekst voor eenvoudig scannen en leesbaarheid. Kom ter zake zodat gebruikers gemakkelijk kunnen vinden wat ze nodig hebben. Gebruik geen overbodige woorden.

<br />

> Natuurlijke en menselijke toon:
>
> Gebruik alledaagse woorden die gemakkelijk te begrijpen zijn. Minder formeel maar professioneler dan alledaags gesprek. Gebruik af en toe een speelse toon voor feestelijke momenten, maar nooit voor informatieve tekst. Wees warm en ondersteunend voor gebruikers die de docs lezen.

<br />

**Fouten**: Regels die objectief kunnen worden gecontroleerd. Voorbeeld:

> Schrijf ReadMe correct met hoofdletters:
>
> Fout: Readme
>
> Goed: ReadMe

<br />

> Omsluit code-elementen met backticks (`):
>
> Fout: Run npm install –g my–package
>
> Goed: Run `npm install –g my–package`

<br />

> Markeer tijdelijke aanduidingen zoals TODO, FIXME of Lorem ipsum
>
> Voorbeeld: TODO: Voeg beschrijving en afbeelding toe aan deze functie

<br />

**Waarschuwingen**: Om problemen aan te wijzen die subjectief kunnen zijn. Voorbeeld:

> Aarzelend taalgebruik:
>
> Vermijd onzeker of overdreven voorzichtig taalgebruik. Het ondermijnt het vertrouwen en maakt uw instructies minder direct. Kies voor helder, zelfverzekerd taalgebruik.
>
> Fout: U kunt overwegen de nieuwste versie te installeren.
>
> Goed: U kunt de nieuwste versie installeren om toegang te krijgen tot nieuwe functies.

<br />

> Zwak schrijven:
>
> Vermijd zwak schrijven zoals 'U kunt' of 'Er is'. Deze zinnen begraven de actie, maken schrijven minder direct en voegen vaak onnodige woorden toe. Sterke docs zijn helder en actiegericht.
>
> Fout: U kunt de API configureren door het instellingenbestand te bewerken.
>
> Goed: Configureer de API door het instellingenbestand te bewerken.

<br />

> Actieve stem:
>
> Vermijd het gebruik van passieve stem. Actieve stem is duidelijker, korter en vertelt de lezer precies wie wat doet.
>
> Fout: Het token wordt gegenereerd wanneer de gebruiker inlogt.
>
> Goed: Het systeem genereert een token wanneer de gebruiker inlogt.

<br />

## De Linter uitvoeren

Eenmaal geconfigureerd, controleert het uitvoeren van de Linter uw pagina aan de hand van uw prompts. Problemen kunnen automatisch worden opgelost met behulp van de Agent.

<Image align="center" border={false} width="350px" src="https://files.readme.io/02345a8505f8f89eaa3d97019252e3cfc3c9e16fdaed63ac7ed7b6df97b765f5-linter.png" />

<br />

## Veelgestelde vragen

<Accordion title="Waar kan ik feedback of vragen naartoe sturen?" icon="fa-messages-question">
  Stuur feedback of vragen per e-mail naar [beta@readme.io](mailto:beta@readme.io)
</Accordion>

<Accordion title="Welk model gebruikt de Linter?" icon="fa-wand-sparkles">
  Op dit moment gebruiken we Gemini 2.5 Flash — hoewel dat kan veranderen naarmate we de balans tussen kwaliteit en snelheid aanpassen. In de toekomst kunnen gebruikers zelf modellen naar keuze selecteren.
</Accordion>