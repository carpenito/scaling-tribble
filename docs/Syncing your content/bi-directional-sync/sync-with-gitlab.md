---
title: Synchroniseren met GitLab
deprecated: false
hidden: false
metadata:
  robots: index
---
## Bidirectionele synchronisatie instellen met GitLab

### Vereisten

* Je hebt een GitLab-account nodig.
* Bij het synchroniseren naar een repository in een organisatie heb je toestemming nodig om een **lege repository** aan te maken.

<Image align="center" border={false} src="https://files.readme.io/d2a12db436be321b972fd817432f3754a13d61c0ecb915202862e58fb2252cc1-Screenshot_2025-10-31_at_1.43.41_PM.png" />

### Instellen

1. Ga naar **Instellingen** > **Git-verbinding**.
2. Selecteer GitLab.
3. Als je dat nog niet hebt gedaan, maak dan een lege repository aan in [GitLab](https://docs.gitlab.com/user/project/)—zorg ervoor dat je de optie om een README aan te maken uitvinkt.
4. **Synchroniseer** met je provider en verifieer je identiteit.
5. Maak een persoonlijk toegangstoken aan met het bereik `api`. Je kunt dit token verwijderen nadat de instelling is voltooid. ReadMe gebruikt dit token eenmalig tijdens de instelling om de webhook op je repository aan te maken en slaat het niet op.
   1. Voor projecttoegangstoken heb je de rol Maintainer nodig. Dit wordt echter niet aanbevolen, omdat er een limiet is op het aantal aan te maken projecttoegangstoken, afhankelijk van de GitLab-prijsstelling.

<Image border={false} src="https://files.readme.io/b350ddb7403c7d0ffbaa7d4f8e4c5fc6ca0d92308c4c81bde90b2c2b146a1ed3-image.png" />

6. Voeg het toegangstoken toe aan ReadMe en klik op het webhook-pictogram om de webhooks aan te maken die nodig zijn om je inhoud gesynchroniseerd te houden met GitLab.

***

## Van repository wisselen

Als je je ReadMe-project wilt verbinden met een andere repository, moet je de oorspronkelijke repository loskoppelen via het prullenbakpictogram.

1. Koppel het project los in ReadMe via het prullenbakpictogram.
2. Maak een nieuw leeg project aan in GitLab.
3. Ga terug naar ReadMe en selecteer het project waarmee je wilt synchroniseren.

***

## Beveiligde branches

Alle branchregels moeten de gebruiker (die vanuit ReadMe naar GitLab synchroniseert) toestaan om te pushen.

<Image border={false} src="https://files.readme.io/5ab0dbdd08ca7f9fc31d8a6895ebb9a970819ea4f2c352c92307ab5886b14541-image.png" />

## Veelgestelde vragen

<Accordion title="Welke rechten zijn vereist bij het synchroniseren met GitLab?" icon="fa-question-circle">
  ReadMe vraagt toegang tot:

  * `read_api` voor het weergeven van projecten
  * `read_user` en `read_profile` om gebruikersinformatie weer te geven
  * `read_repository` om inhoud van GitLab naar ReadMe te synchroniseren
  * `write_repository` om inhoud van ReadMe naar GitLab te synchroniseren
</Accordion>

<br />