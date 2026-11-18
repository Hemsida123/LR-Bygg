# LR Bygg & Snickerier — webbdesign

46 statiska HTML-sidor: startsida, tjänster, snickeriet, om företaget, kontakt, integritet, 404 samt 26 referensprojekt med bildgallerier. Bilder, typsnitt och skript ligger lokalt. Inga installationssteg behövs för att använda webbplatsen.

## Visa sidan

Öppna `dist/index.html` eller kör en enkel webbserver i `dist`. Den privata designförhandsvisningen ligger på https://lr-bygg-design.carlzzon121.chatgpt.site och kräver rätt ChatGPT-konto.

## GitHub eller webbhotell

Ladda upp **hela innehållet i `dist`**, inklusive `assets`, `styles.css` och `script.js`. Behåll filnamnen. Alla interna länkar är relativa och fungerar även under en GitHub Pages-projektsökväg. Enbart index.html räcker inte.

Förhandsvisningen har `noindex,follow` för att inte konkurrera med företagets nuvarande webbplats. Inför offentlig publicering på företagets slutliga domän:

1. Ändra `ORIGIN` i `build.py` till den slutliga domänen och byt HTML-metataggen `noindex,follow` till `index,follow`. Behåll 404-sidan som `noindex`.
2. Kör `python3 build.py` och `python3 verify.py`. Det uppdaterar canonical, delningsbild, företagsdata och sitemap till rätt domän.
3. Ladda upp hela `dist`, kontrollera HTTPS och lägg vid behov omdirigeringar från företagets äldre `/Web-Content/`-adresser.
4. Skicka sitemap till Google Search Console när webbplatsen är offentlig. Detta är teknisk SEO-grund, ingen garanti för placeringar.

GitHub-paketet levereras som förhandsvisning med samma noindex-inställning. Kontakta oss för slutlig domänanpassning innan offentlig lansering.

## Kontakt

Telefonlänkar ringer Lars eller verkstaden. Kontaktverktyget öppnar besökarens mejlprogram med ett förberett mejl till lars@lrbygg.com. Besökaren skickar själv mejlet. Ingen server, databas eller låtsad skickat-bekräftelse finns.

## Bilder och källor

Företagsinformation och bilder kommer från https://www.lrbygg.com och dess publika tjänste- och referenssidor. Företagets eget bildarkiv innehåller små original, huvudsakligen 227–413 pixlar breda. Bilderna är konverterade till WebP utan uppskalning. Originalbilderna visas nu i mindre bildrutor utan förstoring. Heron använder ett separat högupplöst inspirationsfoto av Craft Kitties från Unsplash, https://unsplash.com/photos/GfYA6q5ESLI, fritt under Unsplash License. Responsiva WebP-filer på 960, 1600 och 2400 pixlar ingår. Bilden framställs inte som LR Byggs eget referensprojekt.

Alla 26 projektgallerier är kvar. Några felkopierade projektrubriker i originalet har ersatts med neutrala, bildstödda rubriker. Arkitekt Katinka Schartau anges vid det arkitektritade bostadshuset. Profilbilden på Lars behåller originalets proportioner.

Inga verifierbara kundrecensioner hittades. Inga betyg, kundcitat, recensioner eller aktuella certifieringar har därför lagts till. Referensprojekten används som förtroendebevis. Inga videor hittades på originalwebbplatsen.

Typsnitt: Cormorant Garamond och DM Sans, lokala WOFF2-filer. Licenser finns i assets.

## Underhåll

HTML genereras med `build.py`; layout i `dist/styles.css`, interaktioner i `dist/script.js`. Projekt- och bildunderlag ligger i `research` och `image-sizes.json`. Ändra generatorn för bestående textändringar. Generering skriver inte över CSS eller JavaScript.

Mobilmeny, tangentbordsvänliga tjänsteflikar, projektfilter, fullbildsgalleri och kontaktval ingår. Reducerad rörelse respekteras. Ingen spårning eller externa typsnitt laddas.
