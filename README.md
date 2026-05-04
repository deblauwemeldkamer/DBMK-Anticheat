# 🚨 DBMK-Anticheat

![DBMK Anticheat Banner](https://i.imgur.com/NSkBCcG.png)

<p align="center">
  <img src="https://img.shields.io/badge/FiveM-Anticheat-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Price-FREE-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Lua-5.4-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Vite-Frontend-purple?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Active-green?style=for-the-badge">
</p>

<p align="center">
  <b>De Blauwe Meldkamer — dé GRATIS anti-cheat voor FiveM-servers</b><br>
  Gebouwd om betaalde systemen te overtreffen en toegankelijk te maken voor iedereen.
</p>

---

## 📌 Over DBMK

De FiveM-markt zit vol met **dure anti-cheats**.
DBMK breekt dat model volledig.

> 💡 **DBMK is 100% GRATIS en gebouwd om betaalde anti-cheats te overtreffen.**

Geen paywalls. Geen verborgen kosten.
Gewoon een krachtige anti-cheat — voor **iedere roleplay server**.

---

## ⚡ Features

* 🛡️ Real-time anti-cheat detecties
* 🔗 Directe koppeling met webpanel
* ⚙️ Simpele installatie (plug & play)
* 📊 Dashboard & monitoring
* 🧠 Community-driven updates
* 🚀 Actieve development

---

## 🌐 Webpanel

👉 [https://cheat.deblauwemeldkamer.nl](https://cheat.deblauwemeldkamer.nl)

In het panel kun je:

* 🔑 Licentie activeren (gratis)
* 📦 Resources downloaden
* 🔗 Server koppelen
* 🐞 Bugs & features indienen (via top menu)

---

## 📥 Installatie

### 1. Download resources

Ga naar **Mijn Terminal** en download de **2 ZIP bestanden**.

### 2. Upload naar je server

Plaats ze in je `resources` map:

```
resources/[dbmk]/
```

### 3. Voeg toe aan `server.cfg`

⚠️ **Belangrijk:**
Plak **alleen dit blok** in je bestaande `server.cfg`.

# DBMK — alleen dit blok plakken in je bestaande server.cfg.

# (hostname, mysql, sv_licenseKey, ensure-volgorde etc. blijft per server anders.)

setr dbmk_dashboard_url "[https://cheat.deblauwemeldkamer.nl](https://cheat.deblauwemeldkamer.nl)"
setr dbmk_link_token "dbmk_XXXXXXXXXXXX"
setr dbmk_tenant_id "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
setr dbmk_tenant_server_id "usr-XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"

❗ **Gebruik NIET deze demo data**
👉 Gebruik altijd jouw **echte gegevens uit “Mijn Terminal” (linksonder in het panel)**

---

### 4. Start resources

```
ensure dbmk-core
ensure dbmk-client
```

### 5. Restart server

👉 Volledige restart van je FiveM server

---

### 6. In-game gebruik

```
/anticheat
```

---

## 🧠 Community Driven

DBMK wordt actief ontwikkeld op basis van gebruikers.

👉 Gebruik de **🐞 BUG / Feature knop** in het panel om:

* Bugs te melden
* Features aan te vragen
* Ideeën te delen

> 💬 Veel gevraagde features worden direct gebouwd.

---

## 🚀 Visie

In plaats van dure, gesloten systemen:

**Bouw ik een open, gratis anti-cheat die:**

* Voor iedereen beschikbaar is
* Continu verbeterd wordt
* Gebouwd wordt met de community

👉 **DBMK is niet alleen software — het is een nieuwe standaard binnen FiveM.**

---

## 🛠 Support

* 💬 Discord: [https://discord.gg/tyBBudCMsP](https://discord.gg/tyBBudCMsP)
* 🐛 GitHub Issues

---

## 🏷 Tech Stack

* **Lua 5.4** (FiveM resources)
* **Vite** (frontend dashboard)
* **Node.js backend (panel)**
* **REST API koppelingen**

---

## ⚠️ Belangrijk

* Deel je **link token / credentials NOOIT**
* Gebruik alleen data uit jouw eigen panel
* Eén licentie = gekoppeld aan jouw server

---

## 🏁 DBMK

**De Blauwe Meldkamer**

> De eerste stap naar een **gratis en eerlijke FiveM anti-cheat markt.**
