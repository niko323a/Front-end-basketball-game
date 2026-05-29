# Frontend Basket Quiz App

## Om appen

I skal bygge et quizspil til basketkampe — hver gang et hold scorer en kurv, skal de svare på et frontend-spørgsmål for at få pointet. Kan I forklare hvad `display: flex` gør, mens presset er på? Så fortjener I to point.

---

## Spillets regler

- Et hold scorer en kurv → de trækker et spørgsmål
- Svarer de **rigtigt** → holdet får pointet
- Svarer de **forkert** → ingen point,  (men måske lidt skam)
- Første hold til **10 point** vinder
- Hvert spørgsmål må kun bruges **én gang**

---

## App-funktioner

### Startskærm
- Vælg kategori: **CSS**, **HTML**, **JS** eller **Blandet**
- Når valget er truffet, forsvinder startskærmen og spillet går i gang

### Spilleskærm
- Viser begge holds **score**
- Under hvert hold er der en knap: **"Træk spørgsmål"**
- Knappen åbner en **modal** med spørgsmålet

### Modal
- Viser spørgsmålet
- En knap til at **afsløre svaret**
- To knapper: **Rigtig** og **Forkert**
  - Rigtig → holdet får et point → modal lukker
  - Forkert → ingen point → modal lukker

### Sejr
- Første hold til 10 point → sejrsbesked vises
- Mulighed for at **spille igen**

---

## Design

I bestemmer selv over layout og udseende — men husk: det skal ligne noget der hører hjemme på en basketbane. Tænk store tal, stærke farver, energi.

---

## Peer review

Jeres projekt bedømmes af de andre hold på tre punkter:

**Design**
- Er designet fedt nok til basket?

**Kode**
- Virker koden?
- Er den optimeret?
- Kan I forklare hvad den gør?

**Praktisk test**
- Er det sjovt at spille?

---

## Hints — sådan kan du gribe koden an

Det er helt OK at starte simpelt og bygge videre. Tænk over hvilke delproblemer appen består af, og løs dem ét ad gangen.

| Opgave i appen | Begreb / værktøj |
|---|---|
| Gem score for hvert hold | Variabler med `let` — husk at score skal kunne opdateres |
| Hold styr på hvilken kategori der er valgt | En variabel du sætter når brugeren klikker |
| Arbejde med spørgsmålene | De tre arrays i `site.js` — brug array-index til at hente et objekt |
| Blande spørgsmål fra alle kategorier | Spread-syntax til at slå arrays sammen til ét |
| Træk et tilfældigt spørgsmål fra et array | `Math.random()` giver et tilfældigt tal mellem 0 og 1 — kombinér med `Math.floor()` og arrayets længde for at få et gyldigt index |
| Undgå at det samme spørgsmål vises to gange | Hold styr på hvilke index der er brugt |
|Find et HTML-element | `getElementById`, `querySelector` eller `querySelectorAll` |
| Vis spørgsmål og svar i modalen | `innerHTML` eller `innerText` til at skrive indhold ind i et element |
| Åbne og lukke modalen | `classList.toggle` — sammen med en CSS-klasse der skjuler elementet |
| Reagere på knapklik | `addEventListener` med event-typen `'click'` |
| Opdatere scoretavlen på skærmen | Skriv til `innerText` på det element der viser scoren |
| Tjekke om et hold har vundet | En `if`-sætning der sammenligner scoren med 10 |
| Skifte mellem startskærm og spilleskærm | `classList.add` og `classList.remove` — eller `classList.toggle` |

### Anbefalet rækkefølge

1. Byg HTML-strukturen (startskærm, spilleskærm, modal) husk wireframes 
2. Få kategori-valget til at skifte skærm
3. Få "Træk spørgsmål"-knappen til at åbne modalen med et tilfældigt spørgsmål
4. Tilslut Rigtig/Forkert-knapperne så de opdaterer score og lukker modalen
5. Tilføj sejrsbetingelsen
6. Design og polish til sidst

> Tag det ét trin ad gangen. Test efter hvert trin.
