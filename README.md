# Teleprompter PWA

En professionel, stemmestyret teleprompter-app bygget som en Progressive Web App (PWA), som er designet særligt til iOS (Safari) men også fungerer på andre moderne browsere. Denne app lytter til din oplæsning og scroller automatisk teksten, så du altid ved, hvor du er.

## 🚀 Funktioner

- **Stemmestyret Scrolling:** Appen benytter Web Speech API til at lytte til dig. Den fremhæver det aktive ord, som du læser, og stopper automatisk med at scrolle, hvis du holder pause.
- **Spejlvending (Mirror Mode):** Kan spejlvende teksten, hvilket gør den perfekt til brug i fysiske teleprompter-rigs med et halvtgennemsigtigt spejl.
- **Flersproget Understøttelse:** Understøtter stemmegenkendelse på flere sprog: Dansk (DA), Engelsk (EN), Norsk (NO), Svensk (SV) og Tysk (DE).
- **Tilpasning af Tekst:** Juster nemt tekststørrelsen direkte i appen, så den passer til din læseafstand.
- **Touch & Swipe Controls:** Du kan nemt swipe op eller ned for manuelt at hoppe frem og tilbage i teksten, mens du præsenterer. 
- **Offline Understøttelse:** Da appen er en PWA med en Service Worker (`sw.js`), kan den installeres på din enheds startskærm (Add to Home Screen) og bruges helt uden internetforbindelse efter første indlæsning.
- **Fokus-tilstand:** Clean, mørkt overlay i prompter-tilstanden med en diskret fokus-linje, der gør det let for øjnene.

## 🛠 Teknisk Overblik

Appen er bygget med rene, moderne web-teknologier og er helt uafhængig af tunge frameworks:
- **HTML/CSS/JavaScript (Vanilla):** Alt er skrevet i ét primært HTML-dokument for simpel distribution og lynhurtig indlæsningstid.
- **Web Speech API:** Håndterer the voice recognition ved kontinuerligt at lytte til mikrofonen. 
- **Dice Bigram Similarity:** En avanceret og indbygget "fuzzy matching" algoritme, som sammenligner de talte ord med manuskriptet, hvilket forhindrer appen i at hoppe uforudsigeligt, hvis et ord udtales lidt skævt eller genkendes forkert (især på iOS Safari).

## 📂 Filer i Projektet

- `index.html`: Selve applikationen. Indeholder alt UI (Editor og Prompter), CSS styling og al JavaScript-logikken.
- `manifest.json`: Web app manifest, der gør det muligt at installere appen (PWA) og definerer farver, ikoner og visningstilstand (fullscreen).
- `sw.js`: Service Worker-filen, der tager sig af caching af appen, så den fungerer offline (Network-first for skrifttyper, cache-first for resten).

## 💡 Sådan bruges den

1. Åbn `index.html` i en moderne browser (Safari på iOS 15+ anbefales for optimal stemmegenkendelse).
2. Indsæt dit manuskript i tekstfeltet på startskærmen.
3. Juster evt. tekststørrelse, sprog og spejling.
4. Tryk på **START ▶**.
5. Appen vil bede om adgang til din mikrofon første gang. Tillad dette.
6. Begynd at læse op. Appen vil automatisk fremhæve ordene og scrolle i dit tempo!

---
*Udviklet med fokus på pålidelighed og brugervenlighed under videooptagelser.*
