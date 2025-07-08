
# uupdump-iso-creator-config
uupdump-iso-creator-config
=======
﻿# uupdump-iso-creator-config

Ez a repository támogatja az [uupdump.net](https://uupdump.net) használatát Windows ISO képfájlok automatikus létrehozásához részletes konfigurációk és scriptek segítségével.

---

## Mi az uupdump.net?

Az uupdump.net egy nyílt forráskódú webes eszköz, amely a Microsoft Unified Update Platform (UUP) frissítési csomagjaiból képes Windows ISO telepítő képfájlokat létrehozni. Az oldal segítségével egyedi, friss és testreszabott Windows telepítőket készíthetünk.

Az eszköz főbb jellemzői:

- Kiválasztható Windows verzió, kiadás, nyelv és architektúra  
- Legfrissebb frissítések beépítése  
- Egyszerű és automatizálható ISO készítés

---

## Fontos dokumentáció és GYIK

Az uupdump hivatalos GYIK-je (FAQ-ja) megtalálható [itt](https://git.uupdump.net/uup-dump/misc/src/branch/master/FAQ.md), amely részletesen választ ad a leggyakoribb kérdésekre, működési elvekre és problémákra.

---

## A repóról

Ez a repó konfigurációkat és scripteket tartalmaz, amelyek megkönnyítik az uupdump.net segítségével történő ISO képfájlok letöltését és összeállítását automatizált módon.

---

## Következő lépések

A repó folyamatosan bővül a részletes konfigurációkkal és használati útmutatókkal. Kérlek, kövesd nyomon a fejlesztést!

---

Ha bármilyen kérdésed van, vagy segítségre van szükséged, nyugodtan írj!

# uupdump-iso-creator-config

Ez a repository egy automatizált konfigurációs és script csomag az [uupdump.net](https://uupdump.net) használatához, amely lehetővé teszi Windows ISO telepítő képfájlok gyors, egyszerű és megbízható létrehozását.

---

## Mi az az uupdump.net?

Az [uupdump.net](https://uupdump.net) egy nyílt forráskódú webes eszköz, amely a Microsoft Unified Update Platform (UUP) frissítési csomagjaiból képes Windows ISO telepítő képfájlokat létrehozni. Így testreszabott, a legfrissebb frissítéseket tartalmazó Windows telepítőket készíthetünk.

### Az uupdump.net főbb jellemzői:
- Több Windows verzió, kiadás, nyelv és architektúra közül választhatunk  
- A legfrissebb frissítések beépítése  
- Könnyen automatizálható és testreszabható folyamat

---

## Hasznos dokumentáció és GYIK

Az uupdump hivatalos GYIK-je (Frequently Asked Questions) részletes választ ad a leggyakoribb kérdésekre, működési elvekre és hibakezelésre.  
Megtalálod itt:  
[uupdump FAQ (angol nyelven)](https://git.uupdump.net/uup-dump/misc/src/branch/master/FAQ.md)

---

## A repository tartalma

- `configs/` — Kész konfigurációs fájlok, melyek meghatározzák a letöltendő Windows verziót, nyelvet, kiadást stb.  
- `scripts/` — PowerShell vagy más script fájlok az automatikus letöltéshez, telepítéshez és ISO összeállításhoz  
- `README.md` — Ez a részletes dokumentáció  
- `LICENSE` — A projekt licencfeltételei

---

## Használati útmutató

1. Klónozd vagy töltsd le a repót:

   ```bash
   git clone https://github.com/gabywap/uupdump-iso-creator-config.git


---

## 🧪 Példa: Windows 11 Insider Preview 26200.5670 (x64) ISO létrehozása

Ez a részletes példa bemutatja, hogyan készíthetsz Windows 11 ISO-t az uupdump.net segítségével manuálisan, tesztelési céllal.

### 🌐 Letöltési oldal

1. Látogass el az alábbi linkre:
   [https://uupdump.net/known.php?q=category:w11-25h2-dev](https://uupdump.net/known.php?q=category:w11-25h2-dev)

2. Keresd ki az alábbi buildet:
   **Windows 11 Insider Preview 10.0.26200.5670 (ge_release_upr) amd64 - x64**  
   Dátum: *2025-06-27 19:00 UTC*

3. Kattints rá, vagy közvetlenül erre a nyelvválasztós linkre:
   [https://uupdump.net/selectlang.php?id=adf22284-b67d-4ffe-b3c3-cc0209447019](https://uupdump.net/selectlang.php?id=adf22284-b67d-4ffe-b3c3-cc0209447019)

---

### 🏳️ Nyelv kiválasztása

- A megnyíló oldalon a legördülő menüből válaszd ki: `Hungarian (Magyar)`
- Kattints a **Next** gombra

---

### 💻 Kiadás kiválasztása

- A következő oldalon CSAK a **Windows Pro** legyen bepipálva
  - `Windows Home` jelölést vedd ki
- Kattints ismét a **Next** gombra

---

### 💿 ISO készítési beállítások

- A "Download method" résznél hagyd kiválasztva az alapértelmezett opciót:  
  ✅ **Download and convert to ISO**

- A "Conversion options" alatt jelöld be az alábbi három opciót:

  - ☑️ Include updates (Windows converter only)  
  - ☑️ Run component cleanup (Windows converter only)  
  - ☑️ Integrate .NET Framework 3.5 (Windows converter only)

- Kattints a **Create download package** gombra

---

### 📦 Letöltés és ISO összeállítása

- A gomb megnyomása után letöltődik egy `.zip` fájl, például:

  ```text
  26200.5670_amd64_hu-hu_professional_adf22284_convert.zip


Csomagold ki a zip fájlt egy külön mappába

Futtasd a megfelelő szkriptet rendszergazdaként:

Windows-on: uup_download_windows.cmd

Linux/macOS-en: uup_download_linux.sh vagy .mac.sh

A letöltés és konvertálás automatikusan elindul és idővel elkészül a *.iso fájl

 Tartalom: configs/26200.5670_amd64_hu-hu_professional_adf22284.json
Ez lehet egy metaadat fájl, hogy a repóban egyértelmű legyen, milyen buildhez tartozik:

{
  "build": "26200.5670",
  "arch": "amd64",
  "lang": "hu-HU",
  "edition": "Professional",
  "uup_id": "adf22284-b67d-4ffe-b3c3-cc0209447019",
  "filename": "26200.5670_amd64_hu-hu_professional_adf22284_convert.zip",
  "download_url": "https://uupdump.net/selectlang.php?id=adf22284-b67d-4ffe-b3c3-cc0209447019",
  "created": "2025-06-27T19:00:30Z"
}


Tartalom: scripts/run-download.cmd
Ez a ZIP-ből kicsomagolt uup_download_windows.cmd másolata is lehet (vagy hivatkozás rá), de saját néven, hogy a repó egységes legyen. Például:

@echo off
REM Windows 11 Insider Preview ISO letöltése és konvertálása
REM Build: 26200.5670 | Arch: amd64 | Nyelv: hu-HU | Kiadás: Pro

set SCRIPT_DIR=%~dp0
cd /d "%SCRIPT_DIR%..\build\26200.5670_adf22284"

call uup_download_windows.cmd


---

## 📦 Elérhető konfigurációk

| Build             | Arch   | Nyelv | Kiadás       | Letöltés                             |
|------------------|--------|-------|--------------|--------------------------------------|
| 26200.5670        | amd64 | hu-HU | Professional | [`configs/26200.5670_amd64_hu-hu_professional_adf22284.json`](configs/26200.5670_amd64_hu-hu_professional_adf22284.json)


📝 ConvertConfig_minta_magyarul.ini – magyar magyarázatos minta

[convert-UUP]
; 🔁 Automatikus konvertálás induljon a script elindításakor
AutoStart    =1

; ⬇️ Frissítések letöltése és integrálása a telepítőbe
AddUpdates   =1

; 🧹 Komponens-takarítás a rendszerképben (DISM Cleanup)
Cleanup      =1

; 🧼 Alapverzió visszaállítása (nem ajánlott, adatvesztést okozhat)
ResetBase    =0

; 🧱 .NET Framework 3.5 integrálása
NetFx3       =1

; 💻 Virtuális gépen történő konvertálás engedélyezése (nem szükséges)
StartVirtual =0

; 💾 WIM → ESD átalakítás (kisebb ISO, de veszteséges tömörítés)
wim2esd      =0

; 🧩 WIM → SWM feldarabolás több fájlra (FAT32 USB-hez, ha >4GB)
wim2swm      =0

; 📦 Ne hozzon létre ISO-t (ha csak mappát szeretnél)
SkipISO      =0

; 🛠 WinRE (helyreállító környezet) kihagyása
SkipWinRE    =0

; 🩹 WinRE-hez külön frissítés integrálása (speciális)
LCUwinre     =0

; 📁 MSU fájlok kibontása a frissítésekhez (haladó)
LCUmsuExpand =0

; 🥾 Bootfájlok frissítése (általában nem szükséges)
UpdtBootFiles=0

; 🔧 DISM kényszerített használata (hibák megoldására)
ForceDism    =0

; 📦 Referencia ESD használata (haladó)
RefESD       =0

; 🛑 LCU (legutóbbi kumulatív frissítés) kihagyása
SkipLCUmsu   =0

; ❌ Microsoft Edge eltávolítása
SkipEdge     =1

; 🏁 Script automatikus bezárása a végén
AutoExit     =0

; 🚫 Ne frissítse az upgrade-telepítéseket
DisableUpdatingUpgrade=0

; 🧰 Illesztőprogramok integrálása (ha van Drivers mappa)
AddDrivers   =0

; 📁 Illesztőprogram mappa elérési útja
Drv_Source   =\Drivers


[Store_Apps]
; 🛍️ Microsoft Store appok kihagyása (0 = engedélyezve)
SkipApps     =0

; 📱 Appok szintje (0 = teljes, 1 = minimal, 2 = csak kritikus)
AppsLevel    =0

; 📦 Stub alkalmazások teljes verzióinak telepítése
StubAppsFull =0

; 📜 Egyedi Store App lista használata (pl. CustomAppsList.txt)
CustomList   =1


[create_virtual_editions]
; 🧪 DISM használata virtuális kiadások létrehozásához
vUseDism     =1

; 🔁 Virtuális kiadások automatikus generálása
vAutoStart   =1

; 🧹 Forrás fájlok törlése a végén
vDeleteSource=0

; 🧷 Eredeti fájlok megtartása
vPreserve    =0

; 💾 WIM → ESD átalakítás a virtuális verzióknál
vwim2esd     =0

; 💾 WIM → SWM szétvágás a virtuális verzióknál
vwim2swm     =0

; 📦 ISO kihagyása a virtuális kiadásoknál
vSkipISO     =0

; ➕ Kiadások automatikus hozzáadása (pl. Education, Enterprise)
vAutoEditions=

### 🧩 ConvertConfig_minta_magyarul.ini

Ez egy teljes, részletes magyar magyarázattal ellátott konfigurációs fájlminta, amit a `UUP → ISO` konverzió során használhatsz.

📁 Elérési út: `configs/ConvertConfig_minta_magyarul.ini`  
💡 Segítséget nyújt a saját `ConvertConfig.ini` fájlod kialakításához.

👉 Tipp: A fájl soronként elmagyarázza, mit csinál az adott kapcsoló, így könnyen testre szabhatod.



📄 Tartalom: CustomAppsList_minta_magyarul.md

# CustomAppsList – magyar magyarázatos minta

Ez a fájl testreszabja, hogy a Windows ISO-ba milyen Microsoft Store alkalmazások kerüljenek bele az UUP → ISO konverzió során.

**FONTOS:** csak a Windows 22563 buildtől felfelé működik.  
A használatához a `ConvertConfig.ini` fájlban legyen:

```ini
CustomList = 1

🔧 Hogyan működik?
A sorok elején a # jel kikapcsolja az adott app telepítését.

Amit meghagysz # nélkül, az bekerül az ISO-ba.

📋 Alkalmazások magyarázattal

Microsoft.WindowsStore_8wekyb3d8bbwe
### Microsoft Store – szükséges, ha más appokat is telepíteni szeretnél

Microsoft.StorePurchaseApp_8wekyb3d8bbwe
### Vásárláskezelő – Store vásárlásokhoz szükséges

Microsoft.SecHealthUI_8wekyb3d8bbwe
### Windows Security (Védelem) felhasználói felület

Microsoft.DesktopAppInstaller_8wekyb3d8bbwe
### Winget, AppInstaller – Store-on kívüli telepítésekhez

Microsoft.Windows.Photos_8wekyb3d8bbwe
### Képek megtekintése és szerkesztése (modern alkalmazás)

Microsoft.WindowsCamera_8wekyb3d8bbwe
### Kamera alkalmazás – webkamera kezelése

Microsoft.WindowsNotepad_8wekyb3d8bbwe
### Modern Jegyzettömb (Notepad) alkalmazás

Microsoft.Paint_8wekyb3d8bbwe
### Modern Paint – képszerkesztő

Microsoft.WindowsTerminal_8wekyb3d8bbwe
### Windows Terminál – modern parancssor, PowerShell

MicrosoftWindows.Client.WebExperience_cw5n1h2txyewy
### Web Experience Pack – időjárás, hír widgetek, keresősáv

Microsoft.WindowsAlarms_8wekyb3d8bbwe
### Ébresztőóra és időzítő

Microsoft.WindowsCalculator_8wekyb3d8bbwe
### Számológép

# Microsoft.WindowsMaps_8wekyb3d8bbwe
### Térkép alkalmazás – ritkán használt, online térképek

Microsoft.MicrosoftStickyNotes_8wekyb3d8bbwe
### Jegyzetek – ragadós cetlik az asztalon

Microsoft.ScreenSketch_8wekyb3d8bbwe
### Képernyőkép készítő és jegyzetelő (Snip & Sketch)

# microsoft.windowscommunicationsapps_8wekyb3d8bbwe
### Mail és Naptár (összevont app)

# Microsoft.People_8wekyb3d8bbwe
### Kapcsolatok – személyes névjegyalapú app

# Microsoft.BingNews_8wekyb3d8bbwe
### Bing Hírek – online hírportál alkalmazás

# Microsoft.BingWeather_8wekyb3d8bbwe
### Bing Időjárás

# Microsoft.MicrosoftSolitaireCollection_8wekyb3d8bbwe
### Pasziánsz játék

# Microsoft.MicrosoftOfficeHub_8wekyb3d8bbwe
### Office hub – Office appok telepítése/linkje

# Microsoft.WindowsFeedbackHub_8wekyb3d8bbwe
### Visszajelzés küldése a Microsoftnak

Microsoft.GetHelp_8wekyb3d8bbwe
### Súgó – Microsoft online támogatás

# Microsoft.Getstarted_8wekyb3d8bbwe
### Első lépések (bemutató app)

# Microsoft.Todos_8wekyb3d8bbwe
### Microsoft To Do – feladatlista alkalmazás

# Microsoft.XboxSpeechToTextOverlay_8wekyb3d8bbwe
### Xbox diktálás/játék segéd

# Microsoft.XboxGameOverlay_8wekyb3d8bbwe
### Xbox játék HUD

# Microsoft.XboxIdentityProvider_8wekyb3d8bbwe
### Xbox-fiók kezelés

# Microsoft.PowerAutomateDesktop_8wekyb3d8bbwe
### Automatizálási eszköz (fejlett felhasználóknak)

# Microsoft.549981C3F5F10_8wekyb3d8bbwe
### WebView2 runtime (webtartalom megjelenítés)

MicrosoftCorporationII.QuickAssist_8wekyb3d8bbwe
### Távoli segítségkérés (Quick Assist)

# MicrosoftCorporationII.MicrosoftFamily_8wekyb3d8bbwe
### Microsoft Családi beállítások

# Clipchamp.Clipchamp_yxz26nhyzhsrt
### Videószerkesztő (webes alapú)

# Microsoft.OutlookForWindows_8wekyb3d8bbwe
### Új Outlook app (előzetes verzió)

MicrosoftTeams_8wekyb3d8bbwe
### Microsoft Teams (alapverzió)

# Microsoft.Windows.DevHome_8wekyb3d8bbwe
### Fejlesztői központ app (Dev Home)

# Microsoft.BingSearch_8wekyb3d8bbwe
### Bing kereső app

Microsoft.ApplicationCompatibilityEnhancements_8wekyb3d8bbwe
### Kompatibilitási fejlesztések

MicrosoftWindows.CrossDevice_cw5n1h2txyewy
### Többeszközös élmények (pl. telefon-PC integráció)

MSTeams_8wekyb3d8bbwe
### Teams újabb verzió vagy külön példány

Microsoft.MicrosoftPCManager_8wekyb3d8bbwe
### PC Manager – optimalizáló eszköz (preview)

# Microsoft.StartExperiencesApp_8wekyb3d8bbwe
### Start menü élmények bővítése

### Média alkalmazások (nem-N kiadások esetén)

Microsoft.ZuneMusic_8wekyb3d8bbwe
### Zenelejátszó (Groove Music néven is ismert)

Microsoft.ZuneVideo_8wekyb3d8bbwe
### Videólejátszó

Microsoft.YourPhone_8wekyb3d8bbwe
### Telefon app – mobil és PC integráció

Microsoft.WindowsSoundRecorder_8wekyb3d8bbwe
### Hangrögzítő

Microsoft.GamingApp_8wekyb3d8bbwe
### Xbox App – játékkezelő felület

Microsoft.XboxGamingOverlay_8wekyb3d8bbwe
### Xbox HUD játék közben

Microsoft.Xbox.TCUI_8wekyb3d8bbwe
### Xbox kontextusmenü/fiókkezelő

### Média kodekek (nem-N kiadásokhoz, Surface Team kiadás)

Microsoft.WebMediaExtensions_8wekyb3d8bbwe
### Webes média támogatás

Microsoft.RawImageExtension_8wekyb3d8bbwe
### RAW formátum támogatás (fényképezőgépek)

Microsoft.HEIFImageExtension_8wekyb3d8bbwe
### HEIF (nagy hatékonyságú képformátum) támogatás

Microsoft.HEVCVideoExtension_8wekyb3d8bbwe
### HEVC (H.265) videók támogatása

Microsoft.VP9VideoExtensions_8wekyb3d8bbwe
### VP9 videóformátum támogatás (YouTube)

Microsoft.WebpImageExtension_8wekyb3d8bbwe
### WebP képformátum támogatás

Microsoft.DolbyAudioExtensions_8wekyb3d8bbwe
### Dolby Audio dekóder

Microsoft.AVCEncoderVideoExtension_8wekyb3d8bbwe
### AVC/H.264 videókódolás támogatás

Microsoft.MPEG2VideoExtension_8wekyb3d8bbwe
### MPEG-2 dekódoló

Microsoft.AV1VideoExtension_8wekyb3d8bbwe
### AV1 videóformátum támogatás

### Surface Hub appok (általában csak Team kiadáshoz)

# Microsoft.Whiteboard_8wekyb3d8bbwe
### Microsoft Whiteboard – rajz és ötlet app

# microsoft.microsoftskydrive_8wekyb3d8bbwe
### Régi OneDrive kliens

# Microsoft.MicrosoftTeamsforSurfaceHub_8wekyb3d8bbwe
### Teams Surface Hubhoz

# MicrosoftCorporationII.MailforSurfaceHub_8wekyb3d8bbwe
### Mail Surface Hubhoz

# Microsoft.MicrosoftPowerBIForWindows_8wekyb3d8bbwe
### Power BI alkalmazás

# Microsoft.SkypeApp_kzf8qxf38zg5c
### Skype (UWP) alkalmazás

# Microsoft.Office.Excel_8wekyb3d8bbwe
### Office Excel (Store-os változat)

# Microsoft.Office.PowerPoint_8wekyb3d8bbwe
### PowerPoint (Store)

# Microsoft.Office.Word_8wekyb3d8bbwe
### Word (Store)


configs/
└── 26200.5670/
    └── CustomAppsList_minta_magyarul.md


A letöltött ZIP csomag kibontása és az ISO elkészítése
Győződj meg róla, hogy elegendő szabad hely van a meghajtódon, mert a letöltött ZIP fájl és az ISO elkészítése jelentős tárhelyet igényelhet.

Csomagold ki a letöltött ZIP fájlt, amely tartalmazza a konfigurációs fájlokat, például:

CustomAppsList.txt

ConvertConfig.ini

Ezeket a konfigurációs fájlokat igény szerint szerkesztheted, vagy felülírhatod a korábban elkészített, személyre szabott változatokkal.

Futtasd rendszergazdaként a uup_download_windows.cmd fájlt a mappában.

Ha a parancssor kér valamit, írj be R betűt és nyomj Entert a folytatáshoz.

Az ISO elkészítése a géped teljesítményétől függően akár több órát is igénybe vehet.

A kész ISO fájl neve hasonló lesz az alábbihoz:
26200.5670.250619-1641.GE_PRERELEASE_IM_CLIENTPRO_OEMRET_X64FRE_HU-HU.ISO

