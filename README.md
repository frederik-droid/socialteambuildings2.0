# socialteambuildings.com

Statische site van Give a Day voor sociale teambuildings. Eén bestand (`index.html`), geen build-stap.

## Structuur
- `index.html`: alle tekst, structuur en stijl. Elke sectie start met een duidelijk commentaarblok.
- `images/`: foto's en logo's.
- `fonts/`: F37 Judge (koppen) en Primed (script). DM Sans (broodtekst) komt van Google Fonts.
- `handleiding-sociale-teambuilding.pdf`: de downloadbare handleiding.
- `CNAME`: het domein voor GitHub Pages.

## Live zetten op GitHub Pages
1. Maak een repo aan (bv. `give-a-day/socialteambuildings`) en push deze map naar de branch `main`.
2. Settings > Pages > Source: "Deploy from a branch", branch `main`, map `/ (root)`.
3. Bij je domeinregistrar: zet de DNS van `www.socialteambuildings.com` op een CNAME naar `<gebruikersnaam>.github.io`
   en voor de kale domeinnaam vier A-records naar 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
4. In GitHub Pages: vink "Enforce HTTPS" aan zodra het certificaat er is (kan tot een dag duren).
5. Zet pas daarna de Wix-site uit, anders is er downtime.

## Contactformulier (Formspree)
1. Maak een gratis account op formspree.io en een nieuw formulier met als ontvanger info@giveaday.eu.
2. Kopieer de form-ID (bv. `xabc1234`) en vervang `JOUW_FORM_ID` in `index.html`.
3. Test één keer: de eerste inzending moet je bevestigen via de mail van Formspree.
4. Na verzenden landt de bezoeker op `bedankt.html?src=teambuilding`. Zet daar je conversietracking (GA4-event, LinkedIn Insight, Meta Pixel).
5. Elke inzending bevat automatisch: bron, pagina, utm_source, utm_medium, utm_campaign en referrer. Gebruik dus UTM-links in campagnes.

## Aanpassen
- Tekst: zoek de sectie in `index.html` en pas de tekst aan.
- Thema toevoegen in "Kies je impact": kopieer een `<div class="tile ...">` regel.
- Partnerlogo's: zet de bestanden in `images/` en vervang de tekst in de `<li>` van "Een aantal van onze trotse partners" door `<img src="images/naam.png" alt="Naam">`.
