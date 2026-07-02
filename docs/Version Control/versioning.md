---
title: Versiebeheer
excerpt: hallo wereld
deprecated: false
hidden: false
metadata:
  robots: index
---
Het bijhouden van meerdere versies van uw documentatie is essentieel voor veel technische producten. Deze pagina gaat in op de details van hoe versiebeheer werkt in ReadMe, evenals verschillende gebruiksscenario's.

<Callout icon="🚧" theme="warn">
  **Betrokken secties:** Alleen de secties Guides, Recipes en Reference zijn versiegebonden. Inhoud voor de Landingspagina, Discussies en Changelog blijft beschikbaar over alle versies heen.
</Callout>

## Een nieuwe versie aanmaken

Om een nieuwe versie te maken, opent u het menu Versies & Branches door de **versienaam** (bijv. v3.0) te selecteren in de beheernavigatie. Klik vervolgens op de knop **+ Nieuwe versie** in de rechterbovenhoek. Kies van welke versie u wilt vertakken en geef uw nieuwe versie een naam. Dit maakt een kopie van deze versie aan; u kunt de wijzigingen niet terugplaatsen naar de versie waarvan is vertakt.

<Image align="center" border={false} src="https://files.readme.io/c543cc3ff266bd3b210d720cfb7c5e09d7750c78dcb5ccfd60f669eae003ca39-versions.png" />

### Semver(-achtig)

Onze versiebeheer is gebaseerd op <Anchor label="Semver" target="_blank" href="http://semver.org/">Semver</Anchor>, maar is veel flexibeler dan Semver wat betreft de toegestane invoer. Dit betekent dat uw versies zo eenvoudig kunnen zijn als `v1.0`, maar ook zo complex als `v1.0-hello-this-is-a-version`.

***

## Versieopties

<Image align="center" border={false} width="500px" src="https://files.readme.io/159f0425970c8c5849bc6b6e7b684f51fdab23a656f6488139337adaa75e9d60-version_options.png" />

### Standaard

Dit is de versie waarnaar uw domein verwijst. Gebruikers kunnen naar een andere versie overschakelen door op de versie-keuzelijst te klikken.

<Callout icon="🙅‍♂️" theme="default">
  Het is niet mogelijk om twee versies samen te voegen. Als u wijzigingen in beide wilt aanbrengen, moet u dit handmatig doen!
</Callout>

### Openbaar

Dit selecteren maakt de versie beschikbaar in de versie-keuzelijst en voor iedereen die uw documentatie kan bekijken. Als dit niet is geselecteerd, wordt deze versie gemarkeerd als **Verborgen** en is deze alleen zichtbaar voor projectbeheerders.

### Beta

Aangeven dat een versie een beta is, voegt een badge toe naast de versie in de versie-keuzelijst. Dit maakt geen callout op de pagina of andere zichtbare wijzigingen aan.

### Verouderd

Selecteer dit om oudere versies te markeren. Naast een "verouderd"-badge naast de versie in de versie-keuzelijst, zien gebruikers ook een grote rode banner boven de documentatie wanneer ze deze verouderde versie bezoeken. Zo ziet het eruit:

<Image align="center" border={true} width="smart" src="https://files.readme.io/RhO7iWuhSMGsBrHSrFMt_Screen%20Shot%202015-12-16%20at%2012.17.04%20PM.png" className="border" />

***

## Versie-keuzelijst weergeven

<Image align="center" border={false} caption="Admin view: Hidden and Deprecated are not visible to end-users" src="https://files.readme.io/5f0ac4bab3338c5e1cceee0368a02363bb6c2eca6f40324725d6d43593e564ab-version_drop.png" />

Standaard tonen we de eerder genoemde versie-keuzelijst in de subnavigatiebalk. U kunt instellen of u deze wilt weergeven of verbergen via **Instellingen > Koptekst & Voettekst > Subnavigatie**.

<Image align="center" border={false} src="https://files.readme.io/1a975ae96b399662d42cee67ca226a8fd49bfb9188da95ccfd00a2125f0347d7-version_picker.png" />

***

## Herbruikbare inhoud

Elke [Herbruikbare inhoud](doc:reusable-content) die binnen één versie is aangemaakt, kan alleen worden gebruikt binnen de documentatie van die versie; het is niet mogelijk om Herbruikbare inhoudsblokken te definiëren die over versies heen binnen één project kunnen worden gebruikt.

Als een nieuwe versie wordt aangemaakt door te vertakken vanuit een bestaande versie, erft de nieuwe versie alle Herbruikbare inhoudsblokken die in de bestaande versie zijn gedefinieerd. De Herbruikbare inhoudsblokken in de nieuwe versie zijn echter volledig onafhankelijk van de oude versie.

> 📘 Globale herbruikbare inhoud
>
> Projecten met een Enterprise-abonnement hebben de mogelijkheid om **Globale herbruikbare inhoud** te definiëren die _wel_ over projecten en versies heen kan worden gebruikt. Bekijk onze [documentatie over herbruikbare inhoud voor Enterprise-groepen](https://docs.readme.com/ent/docs/reusable-content-enterprise) voor meer informatie!

***

## Gebruiksscenario's

Er zijn veel verschillende situaties waarin documentatieversiebeheer nuttig kan zijn — sommige zijn duidelijker dan andere. Het meest voor de hand liggende gebruiksscenario is wanneer uw documentatieversie moet overeenkomen met de versiebeheer van uw API of ander technisch product, en u kopieën van uw documentatie moet bijhouden voor elke respectieve versie.

Een ander gebruiksscenario is voor grotere inhoudsherstructureringen of migraties, vooral wanneer deze wijzigingen meer omvatten dan het eenvoudigweg bijwerken van een paar pagina's (in welk geval we <Anchor label="Suggested Edits" target="_blank" href="doc:suggested-edits">Voorgestelde bewerkingen</Anchor> aanbevelen). U kunt een nieuwe versie van uw documentatie vertakken, een grote herstructurering uitvoeren (bijv. paginacategorieën reorganiseren, pagina's samenvoegen, verouderde inhoud verwijderen, enz.), en toch uw oude documentatie als publiek zichtbare versie behouden. En wanneer u klaar bent om de overstap te maken, is het zo eenvoudig als het hernoemen van de versies en het aanpassen van een paar versie-instellingen!

***

## Veelgestelde vragen

<Accordion title="Hoeveel versies kan ik aanmaken?" icon="fa-tags">
  Gebruikers van het gratis abonnement kunnen tot 3 versies aanmaken. Upgrade naar het Startup-abonnement of hoger om onbeperkte versies te ontgrendelen.
</Accordion>