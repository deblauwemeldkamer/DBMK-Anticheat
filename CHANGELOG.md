## DBMK Anticheat — Patch Notes (bundle `2026.05.06.05`)

### ✅ Added
- **Anti‑Evasion backend**
  - `POST /api/fivem/evasion/check` (VPN/HWID/Alt scoring + opslag)
  - `POST /api/fivem/evasion/allowlist` (license/fingerprint/ip allowlist)
- **IP/VPN detectie (API‑ready)**
  - TTL cache + optionele IPQualityScore integratie via `IPQUALITYSCORE_API_KEY`
  - Zonder key blijft het “simulated” (range-based)
- **Alt link detection uitgebreid**
  - Matchtypes: **HWID**, **IP**, **Steam-link**, **Discord-link**
  - “Linked accounts” payload terug naar resource/tablet
- **Dashboard runtime configuratie (Event Policies)**
  - Nieuwe **Anti‑Evasion (VPN/HWID/Alt)** sectie: enable/disable, action (warn/kick/ban), threshold, vpn/hwid/alt scores, ban duration
- **Ingame Tablet**
  - Anti‑Evasion tab: **Linked accounts lijst** (HWID/IP/Steam/Discord); click = selecteer online speler, anders kopieer license
  - Server tab (incident tools): **Lockdown**, **Mass strip (non‑staff)**, **Mass evidence (top risk)**

### 🔁 Changed
- **HWID fingerprinting**
  - Fingerprint gebruikt stabiele identifiers (excl. `license:`) + tenant‑salt voor betere cross‑account matches
- **Smart behavior**
  - Risk (low/medium/high) schaalt met jouw threshold (geen hardcoded 80/40)
- **Discord webhook routing**
  - “Anti‑Evasion/VPN/Proxy” mapt nu correct naar module key `evasionGuard` (module toggles werken)

### 🛠 Fixed
- **Staff bypass / whitelist flow**
  - Staff wordt niet meer onterecht gekickt/geflagged door o.a. **Vehicle spawn policy**
  - Bypass werkt nu robuust via:
    - ESX group `superadmin/admin/mod/staff`
    - óf ACE `dbmk.bypass`
    - óf ACE `group.superadmin/admin/mod/staff`
  - Fallback group resolving (getGroup → xPlayer.group → xPlayer.get('group')) voor forks/timing issues
- **Staff toast spam**
  - Identieke enforcement toasts worden gededuped (20s) om spam te voorkomen

### 🔒 Database / Security
- Nieuwe tabellen:
  - `evasion_fingerprints`, `evasion_allowlist`, `evasion_events`
- **RLS policies toegevoegd** (tenant isolation via `dbmk_user_accessible_tenant_ids()`)

### ⚙️ Config / Install Notes
- **CORE update vereist**
  - Deploy nieuwe CORE ZIP/build en restart `dbmk-anticheat` (+ guard/resources indien gebruikt)
- **Optioneel: echte VPN reputatie**
  - Zet `IPQUALITYSCORE_API_KEY` op je API host
- **Aanbevolen: staff bypass via ACE (server.cfg)**
  ```cfg
  add_ace group.superadmin dbmk.bypass allow
  add_ace group.admin      dbmk.bypass allow
  add_ace group.mod        dbmk.bypass allow
  add_ace group.staff      dbmk.bypass allow

  # Voorbeeld extra groepen (pas aan naar jouw server):
  add_ace group.moderator       dbmk.bypass allow
  add_ace group.anticheat_staff dbmk.bypass allow
