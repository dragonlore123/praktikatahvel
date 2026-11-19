# Projektijuhtimine: Kanban

Projekt: **PraktikaTahvel**, praktikakohtade ja praktikakogemuste veebirakendus TTK õpilastele.
Periood: 19.11.–18.12.2026
Board: https://github.com/users/dragonlore123/projects/1

## 1. Miks Kanban

1. **Töötan üksi.** Scrum on ehitatud tiimile: product owner, scrum master ja arendajad on eraldi vastutused ning sprindi kohustus võetakse tiimina. Kanban ei nõua kindlat tiimi suurust ega uusi rolle. Selle põhimõte „alusta sellest, mis sul praegu on“ sobib ühele inimesele.
2. **Minu ajakasutus on ebaühtlane.** Teen projekti kooli, praktika ja oma ettevõtte kõrvalt, nii et iga nädala töömaht kõigub. Pidevas voos võtan järgmise töö siis, kui eelmine on valmis. Fikseeritud sprindi eesmärki, mis võib halval nädalal läbi kukkuda, ei ole.
3. **WIP-limiit hoiab fookust.** Üksi töötades on suurim oht alustada mitut asja korraga ja mitte midagi lõpetada. Limiit (Töös korraga kuni 2) sunnib asju lõpuni viima.
4. **Edenemine on mõõdetav ka ilma sprintideta.** Board, läbilaskevõime (mitu lugu nädalas valmis) ja tsükliaeg (mitu päeva lugu töös oli) näitavad, kas töö liigub.
5. **Prioriteete saab muuta igal nädalal.** Kui ülevaatel tuleb tagasisidet, saan backlogi järjekorda kohe muuta ilma sprindi lõppu ootamata.

## 2. Rollid

Kanban ei kirjuta rolle ette, aga Kanbani meetodis on kasutusel kaks teenusrolli. Kuna töötan üksi, kannan mõlemat ja olen ka arendaja. Igal kadentsil on selge, millist rolli täidan.

| Roll | Vastutus | Kes |
|---|---|---|
| **Service Request Manager** (SRM) | Backlogi haldus ja järjestus, kasutajalugude ja vastuvõtukriteeriumide kirjutamine, otsus, mis läheb järgmisena tööse (sarnane Scrumi product owneriga) | Georg Volov |
| **Service Delivery Manager** (SDM) | Töövoo jälgimine, WIP-limiitide hoidmine, kadentside läbiviimine, takistuste eemaldamine (sarnane scrum masteriga) | Georg Volov |
| **Arendaja** | Analüüs, kood, testid, deploy | Georg Volov |
| **Kasutaja / huvirühm** | Proovib rakendust ja annab nädalaülevaatel tagasisidet | TTK kursusekaaslased |

## 3. Board ja töövoog

Töövoog GitHub Projectsis:

| Veerg | Tähendus | WIP-limiit |
|---|---|---|
| **Backlog** | Kõik kasutajalood, järjestatud prioriteedi järgi | – |
| **Ready** | Täpsustatud ja hinnatud, järgmisena tööse võetavad | 3 |
| **In progress** | Arenduses | 2 |
| **In review** | Valmis, kontrollin vastuvõtukriteeriume ja testin | 2 |
| **Done** | Vastab valmisoleku definitsioonile | – |

**Tõmbepõhimõte:** uue loo võtan tööse alles siis, kui vasakpoolses veerus on WIP-limiidi all ruumi.

**Definition of Ready:** lugu on vormis „Õpilasena tahan …, et …“, sellel on vastuvõtukriteeriumid ja hinnang.

**Definition of Done:**
- kood on `main` harus
- kõik vastuvõtukriteeriumid on läbi kontrollitud
- issue on suletud ja viitab commit'idele

**Hinnangud:** story point'id Fibonacci skaalal 1, 2, 3, 5, 8 (suhteline keerukus). 1 tähendab paari tunni tööd. 8 on liiga suur ja tuleb tükeldada. Hinnang on boardil väljal *Estimate*, prioriteet väljal *Priority* (P0 kohustuslik MVP, P1 oluline, P2 kui aega jääb).

## 4. Kadentsid

| Kadents | Millal | Sisu | Kuhu kirja |
|---|---|---|---|
| **Igapäevane standup** | iga tööpäev, 5 min | Eile, täna, takistused. Boardi vaatan läbi paremalt vasakule: mis on lõpetamise lähedal? | Kommentaar issue'is „Standup logi“ |
| **Täiendamine** (replenishment) | esmaspäev | Valin backlogist lood Ready veergu, täpsustan ja hindan vajadusel uuesti | Selle dokumendi nädalalogi |
| **Ülevaade** (delivery review) | pühapäev | Mis valmis, demo kursusekaaslasele, mõõdikud | Selle dokumendi nädalalogi |
| **Retrospektiiv** | pühapäev pärast ülevaadet | Mis läks hästi, mis mitte, üks konkreetne muudatus järgmiseks nädalaks | Retro issue + kokkuvõte siin |

## 5. Ajakava

| Nädal | Kuupäevad | Fookus |
|---|---|---|
| 0 | 19.–22.11 | Seadistus: metoodika, board, backlog |
| 1 | 23.–29.11 | Projekti skelett, andmebaas, ettevõtete nimekiri |
| 2 | 30.11–6.12 | Konto, arvustused |
| 3 | 7.–13.12 | Filtrid, mobiilivaade, deploy |
| 4 | 14.–18.12 | Viimased lood, lõpuülevaade ja -retro, esitamine |

## 6. Mõõdikud

| Nädal | Valmis lugusid | Story point'e | Keskmine tsükliaeg (päeva) | WIP ületamisi |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |

## 7. Protsessi muudatused

| Kuupäev | Muudatus | Põhjus |
|---|---|---|
| 19.11.2026 | Protsess loodud: Kanban, WIP-limiidid Ready 3, In progress 2, In review 2 | Algseadistus |

## 8. Nädalalogi

### Nädal 0 (19.–22.11): seadistus

- 19.11: valisin metoodika ja projekti, lõin repo ja GitHub Projectsi boardi (Kanbani mall), kirjutasin backlogi 15 kasutajalooga koos vastuvõtukriteeriumide, hinnangute ja prioriteetidega.

### Nädal 1 (23.–29.11)

**Täiendamine (E 23.11):**
- Ready veergu valitud:
- Põhjendus:

**Ülevaade (P 29.11):**
- Valmis:
- Tagasiside:
- Mõõdikud:

**Retrospektiiv:** (link retro issue'le)
- Hästi:
- Halvasti:
- Muudan:

### Nädal 2 (30.11–6.12)

**Täiendamine (E 30.11):**
- Ready veergu valitud:
- Põhjendus:

**Ülevaade (P 6.12):**
- Valmis:
- Tagasiside:
- Mõõdikud:

**Retrospektiiv:** (link retro issue'le)
- Hästi:
- Halvasti:
- Muudan:
- Eelmise nädala muudatus, kas tegin:

### Nädal 3 (7.–13.12)

**Täiendamine (E 7.12):**
- Ready veergu valitud:
- Põhjendus:

**Ülevaade (P 13.12):**
- Valmis:
- Tagasiside:
- Mõõdikud:

**Retrospektiiv:** (link retro issue'le)
- Hästi:
- Halvasti:
- Muudan:
- Eelmise nädala muudatus, kas tegin:

### Nädal 4 (14.–18.12): lõpetamine

**Täiendamine (E 14.12):**
- Ready veergu valitud:

**Lõpuülevaade:**
- Mis valmis, mis jäi backlogi ja miks:
- Mõõdikud kogu projekti kohta:

**Lõpuretrospektiiv:**
- Mis Kanbanist töötas:
- Mida teeksin järgmisel korral teisiti:
