# hetweeskind.nl: bouwplan

Klein familieproject van Liam: de site van 't Weeskind (zijn moeder Nelleke; voormalige winkel in Culemborg,
cadeaux/brocante/antiek, sinds 2016 alleen nog op markten). Houd het klein.

## Stand
Deze map is een kopie van de live site (hetweeskind.nl, gehost bij Yourhosting/SoHosted), op 23-9 van de live
server gehaald. Nog geen git-repo. Oude template: Bootstrap 2 + jQuery 1.8, 8 pagina's, foto's in
`images/weeskindfotos/` (1-11.jpg, Image000-009.png, assort000-005.png, banner.png).

## Nieuwe versie in `nieuw/`
Eén pagina (`nieuw/index.html` + `nieuw/style.css`, foto's verkleind in `nieuw/img/`). Getest op 375 en desktop:
geen horizontaal scrollen, alle beelden laden, verlopen markten verdwijnen vanzelf (`data-tot`), zonder markten
verschijnt "Nieuwe data volgen". Lokaal bekijken: `python3 -m http.server 4455 --directory nieuw` en dan
http://127.0.0.1:4455. Bij publiceren wordt `nieuw/` de root van de GitHub Pages-repo; de oude bestanden hier zijn
alleen nog bron.
Tekst: uit de oude site (home, afscheidsbericht 29-1-2016, Culemborg, Media), licht ingekort; niets verzonnen.
Open: de twee markten staan erin zoals vorig jaar ("datum volgt"), nog bevestigen voor 2026.

## Wat er moet komen
Eén statische, mobielvriendelijke pagina (plain HTML/CSS, geen framework), op GitHub Pages met eigen domein:
1. **Intro**: wie ze is, in 2 zinnen (winkel gesloten na 8,5 jaar, nu op markten).
2. **Waar staan we**: de komende markten (datum, plaats, wat ze meeneemt). Moet met één regel per markt te
   onderhouden zijn. Verlopen data niet laten staan.
3. **Fotostrook**: de beste bestaande foto's, later aan te vullen met foto's van recente markten.
4. **Contact**: info@hetweeskind.nl, telefoon 06 20059114, Facebook https://www.facebook.com/Hetweeskind.
5. Optioneel kort onderaan: de Culemborg/weeshuis-tekst (`culemborg.html`) en persvermeldingen (`media.html`).

De lege pagina's (assortiment, fotogalerij, shop) vervallen. Sfeer houden: mint #97d0c9, bloemenachtergrond,
naam "'t Weeskind, Cadeaux & Curiosa". Geen em-dash in zichtbare tekst.

## Nog nodig van Liam
- Marktdata voor dit najaar/de kerst (Liam vraagt het aan zijn moeder, 23-9).
- Eventueel nieuwe foto's.

## Hosting en DNS: let op
- De mail (`info@hetweeskind.nl`) draait nu op het Yourhosting-hostingpakket (MX `mx.sohosted.*`). Die gaat naar
  TransIP. **De site en mail moeten werken vóór de Yourhosting-hosting afloopt (24-05-2027).**
- Het domein wordt naar TransIP **verhuisd** (verhuiscode), niet opgezegd bij Yourhosting.
- DNS bij TransIP straks: GitHub Pages A-records + `www` CNAME, MX + SPF van TransIP-mail. Oude mail via IMAP
  overzetten, en de nieuwe instellingen op het apparaat van Liams moeder zetten.
- Achtergrond en besluiten: `~/Develop/brain/projects/hetweeskind-site/context.md`.
