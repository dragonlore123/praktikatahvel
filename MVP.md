# PraktikaTahvel – MVP plaan

Board: [GitHub Projects – PraktikaTahvel (Kanban)](https://github.com/users/dragonlore123/projects/1) · Protsess: [docs/protsess.md](docs/protsess.md)

## 1. Probleem ja kasutaja

**Kasutaja:** TTK tarkvaraarenduse õpilane, kes otsib praktikakohta või on praktika juba läbinud.

**Probleem:** info praktikakohtade kohta on laiali kursusekaaslaste vestlustes, vanades meilides ja kuulujuttudes. Õpilane ei tea, millised firmad praktikante võtavad, milliste tehnoloogiatega seal töötatakse ja kuidas eelmistel praktikantidel läks. Seetõttu kulub praktikakoha otsimisele palju aega ja otsus tehakse vähese info põhjal.

## 2. MVP ja hilisemad funktsioonid

MVP on kõige väiksem versioon, mis juba lahendab põhiprobleemi: õpilane näeb ühest kohast ettevõtteid ja loeb, mida teised praktikandid nende kohta kirjutasid.

### MVP-s kindlasti olemas (P0)

| Funktsioon | Miks MVP-s |
|---|---|
| Projekti skelett (Node.js + Express + MySQL) | Ilma selleta ei saa midagi muud ehitada |
| Andmebaasi skeem: ettevõtted, arvustused, kasutajad | Kõik põhifunktsioonid salvestavad nendesse tabelitesse |
| Ettevõtete nimekiri | Põhiprobleem: info ühes kohas |
| Ettevõtte detailvaade | Õpilane peab nägema ettevõtte tehnoloogiaid ja linna |
| Registreerumine ja sisselogimine | Arvustusi saavad lisada ainult kooli õpilased, mitte anonüümsed |
| Praktikakogemuse arvustuse lisamine | Ilma arvustusteta on see lihtsalt firmade nimekiri |

### Hiljem (P1 ja P2)

| Funktsioon | Prioriteet | Miks jääb hilisemaks |
|---|---|---|
| Keskmine hinne ja teiste arvustused | P1 | Esimestel nädalatel on arvustusi vähe, keskmine ei ütle veel palju |
| Uue ettevõtte lisamine | P1 | Alguses lisan ettevõtted ise seemneandmetena |
| Filtreerimine tehnoloogia ja linna järgi | P1 | Väikese nimekirja puhul saab ka ilma filtriteta hakkama |
| Mobiilivaade | P1 | Põhiline kasutus on arvutis, aga oluline enne avalikku kasutust |
| Deploy (avalikult üles) | P1 | Arendus ja demo saab teha lokaalselt, deploy enne lõpuülevaadet |
| Otsing nime järgi | P2 | Filtrid katavad suurema osa vajadusest |
| Oma arvustuse muutmine ja kustutamine | P2 | Mugavus, mitte põhiprobleem |
| Administraatori modereerimine | P2 | Väike kasutajaskond, alguses saan sisu käsitsi andmebaasist eemaldada |
| Automaattestid | P2 | Vajalikud, aga MVP kontrollin vastuvõtukriteeriumide järgi käsitsi |

## 3. Kasutajalood

MVP lood (on ka boardil Backlog veerus):

1. **#1** Arendajana tahan Node.js + Express + MySQL projekti skeletti, et saaksin funktsioone lisama hakata.
2. **#2** Arendajana tahan andmebaasi skeemi ettevõtete, arvustuste ja kasutajatega, et andmeid saaks salvestada.
3. **#3** Õpilasena tahan näha ettevõtete nimekirja, et teaksin, kuhu praktikale kandideerida.
4. **#4** Õpilasena tahan avada ettevõtte detailvaate, et näha selle linna ja tehnoloogiaid.
5. **#5** Õpilasena tahan registreeruda ja sisse logida, et saaksin arvustusi lisada.
6. **#6** Õpilasena tahan lisada oma praktikakohale arvustuse (hinne 1–5 ja kirjeldus), et teised saaksid minu kogemusest teada.

Hilisemad lood: #7–#15 (vt tabel ülal ja boardi).

## 4. Hinnangud

Hinnangud on story point'ides Fibonacci skaalal (1, 2, 3, 5, 8), boardil väli *Estimate*.

| Lugu | Story point'id |
|---|---|
| #1 Projekti seadistus | 2 |
| #2 Andmebaasi skeem | 3 |
| #3 Ettevõtete nimekiri | 3 |
| #4 Ettevõtte detailvaade | 2 |
| #5 Registreerumine ja sisselogimine | 5 |
| #6 Arvustuse lisamine | 5 |
| **MVP kokku** | **20** |

Hilisemad lood kokku: 24 punkti (P1: 13, P2: 11).

## 5. Kes mida teeb

Töötan üksi, seega on kõik rollid minu peal. Kanbani teenusrollid on kirjeldatud [docs/protsess.md](docs/protsess.md).

| Liige | Roll | Vastutusala |
|---|---|---|
| Georg Volov | Service Request Manager | Backlog, lugude järjekord ja vastuvõtukriteeriumid |
| Georg Volov | Service Delivery Manager | Töövoog, WIP-limiidid, standupid ja retrod |
| Georg Volov | Arendaja | Frontend, backend, andmebaas, testimine, deploy |
| TTK kursusekaaslased | Kasutajad | Proovivad rakendust ülevaatusel ja annavad tagasisidet |

## 6. Esimene voog

Kanbanis ei ole sprinte, töö liigub pideva voona. Esimesel nädalal (23.–29.11) võtan Ready veergu (WIP-limiit 3):

1. #1 Projekti seadistus – esimesena, sest kõik teised lood sõltuvad sellest
2. #2 Andmebaasi skeem
3. #3 Ettevõtete nimekiri

In progress veerus on korraga kuni 2 lugu. Kui #1 on valmis, tõmban järgmisena #2 ja Ready veergu lisan #4. Teisel nädalal (30.11–6.12) tulevad #5 ja #6, nii et MVP on valmis nädala 2 lõpuks.

## 7. Valmis-definitsioon (Definition of Done)

Lugu on valmis, kui:

- kood on `main` harus
- kõik vastuvõtukriteeriumid on läbi kontrollitud
- rakendus käivitub ilma vigadeta
- issue on suletud ja viitab commit'idele
