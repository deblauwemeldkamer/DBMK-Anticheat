# DBMK-Anticheat

**De Blauwe Meldkamer — anti-cheat voor FiveM-servers**

> **GitHub “About” (korte beschrijving voor je repo):**  
> *DBMK FiveM anti-cheat: welke bestanden je op je game-server zet en hoe je je licentie koppelt — De Blauwe Meldkamer.*

> *English:*  
> *DBMK FiveM anti-cheat: what to install on your game server and how to link your license — De Blauwe Meldkamer.*

---

## Voor wie is deze README?

Deze pagina gaat **alleen** over wat **jij als servereigenaar** op **jouw FiveM-hosting** zet en welke stappen je in het **webpanel** doet om je licentie te koppelen.

**Hoe en waar het beheersysteem technisch draait, hoort bij de aanbieder en gaat verder gebruikers niet aan.** Hier staat dus geen uitleg over servers, databases of hosting van het panel — enkel jouw kant: bestanden, `server.cfg` en herstart.

---

## Webpanel (inloggen & downloads)

**Officieel panel:** [https://cheat.deblauwemeldkamer.nl](https://cheat.deblauwemeldkamer.nl)

Daar log je in (zoals bij DBMK gebruikelijk), regel je je **licentie**, haal je de **twee ZIP-downloads** op onder **Mijn Terminal**, en zie je de **regels voor je `server.cfg`**.

![DBMK Anti-cheat — voorbeeld van het panel](https://i.imgur.com/jN2kwqF.png)

---

## Wat je uploadt op je FiveM-server

Uit **Mijn Terminal** download je **twee ZIP-bestanden**. Dat zijn de **resource-pakketten** van DBMK die op **jouw** machine moeten draaien:

- Je **zet ze uit** in je resources-structuur (of volgt de mapnamen zoals in de ZIP), net zoals je andere FiveM-resources installeert.
- Samen vormen ze de **anti-cheat op de game-server**: verbinding met je licentie, detecties, en het gedrag dat DBMK op de server uitvoert.

Exacte mapnamen en volgorde volg je zoals in de pakketten / korte instructies in het panel aangegeven; het gaat hier om: **deze bestanden = wat er op jouw FiveM-host draait**, niet om de omgeving van het panel zelf.

---

## Stappenplan (van licentie tot `/anticheat`)

1. **Licentie (eenmalig gratis proberen)**  
   In het panel: **Licentie winkel** → pak de **Free 24H Pass** (gratis, om te testen).  
   Wil je daarna door: dan **betaal** je volgens het gekozen product — tot die tijd geldt je proef of betaalde looptijd zoals gekocht.

2. **Downloads**  
   Ga naar **Mijn Terminal** en download **beide** ZIP’s.

3. **Upload op jouw hosting**  
   **Upload** de inhoud naar **jouw** FiveM-server (txAdmin, FTP, of hoe jij resources uitrolt). Niets hiervan “host” de gebruiker voor het panel — dit staat **alleen** op jouw game-server.

4. **`server.cfg` op je game-server**  
   Ga in het panel terug naar **Mijn Terminal** (of het scherm waar je **server- / cfg-regels** ziet). **Kopieer de regels die bij jouw licentie horen** en plak ze in de **`server.cfg`** van **jouw** FiveM-server. Daarmee koppelt DBMK jouw server aan **jouw** licentie in het panel.

5. **Volledige restart**  
   Herstart je **hele** FiveM-server na wijzigingen aan resources en `server.cfg`.

6. **In-game**  
   Na het joinen van de server: typ **`/anticheat`** om het DBMK-commando / menu in-game te openen.

---

## Hulp en meldingen

- **Discord:** [Support-server](https://discord.gg/tyBBudCMsP)  
- **Fouten of verbeteringen:** open een **GitHub Issue** in deze repository.

---

## Merk

**De Blauwe Meldkamer / DBMK** — gebruik van software en merk volgens je overeenkomst met de aanbieder. Deze README is geen juridisch contract; zie je licentievoorwaarden in het panel waar van toepassing.
