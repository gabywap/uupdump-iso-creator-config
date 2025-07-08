<<<<<<< HEAD
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


Magyarázatos változat: ConvertConfig_minta_magyarul.ini

[convert-UUP]
AutoStart    =1        ; Automatikusan elindítja a konvertálási folyamatot a script futtatásakor
AddUpdates   =1        ; Beépíti a letöltött frissítéseket a telepítőbe
Cleanup      =1        ; Komponens-tisztítás (DISM /cleanup-image) a telepítőméret csökkentéséhez
ResetBase    =0        ; Nem reseteli a frissítési alapot (meghagyja a frissítési előzményeket)
NetFx3       =1        ; .NET Framework 3.5 beépítése (gyakori kérés sok szoftverhez)
StartVirtual =0        ; Ne induljon el virtuális kiadások konvertálása automatikusan
wim2esd      =0        ; Nem konvertálja WIM fájlokat tömörített ESD-re (kevésbé tömör, de gyorsabb)
wim2swm      =0        ; Nem darabolja fel a WIM fájlokat (Split-WIM)
SkipISO      =0        ; Nem hagyjuk ki az ISO készítést (ISO fog keletkezni)
SkipWinRE    =0        ; A Windows Recovery Environment (WinRE) ne kerüljön kihagyásra
LCUwinre     =0        ; Nem integrálja az LCU-t a WinRE-be
LCUmsuExpand =0        ; Nem bontja ki manuálisan az MSU-t az LCU-hoz
UpdtBootFiles=0        ; Nem frissíti a boot fájlokat külön (pl. boot.wim, setup boot)
ForceDism    =0        ; Nem kényszeríti a DISM használatát (alapértelmezett eszközhasználat)
RefESD       =0        ; Nem használ meglévő ESD-t referenciaként
SkipLCUmsu   =0        ; Nem hagyjuk ki az LCU MSU használatát
SkipEdge     =1        ; Microsoft Edge eltávolítása az ISO-ból (ha lehetséges)
AutoExit     =0        ; Nem lép ki automatikusan a végén, konzolablak nyitva marad
DisableUpdatingUpgrade=0 ; Frissítési csatorna ne legyen tiltva a telepítőben
AddDrivers   =0        ; Nem integrálunk illesztőprogramokat
Drv_Source   =\Drivers ; (használaton kívül, mivel AddDrivers=0)

[Store_Apps]
SkipApps     =0        ; Nem hagyjuk ki a Store alkalmazásokat
AppsLevel    =0        ; Alap szintű Store app integráció
StubAppsFull =0        ; Ne telepítse a teljes Stub appokat (alapértelmezett viselkedés)
CustomList   =1        ; Egyéni app lista használata engedélyezve

[create_virtual_editions]
vUseDism     =1        ; DISM használata a virtuális kiadások létrehozásához
vAutoStart   =1        ; Automatikus indulás virtuális kiadások létrehozásához
vDeleteSource=0        ; Ne törölje a forrás WIM/ESD fájlokat a konverzió után
vPreserve    =0        ; Ne tartsa meg a köztes fájlokat (tisztább build)
vwim2esd     =0        ; Virtuális kiadásokhoz ne konvertáljon ESD-re
vwim2swm     =0        ; Virtuális kiadásokhoz ne készítsen split WIM-et
vSkipISO     =0        ; Virtuális kiadásokhoz is készüljön ISO
vAutoEditions=         ; (Üres - nincs automatikus kiadáslista megadva)



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






>>>>>>> d6be641 (Initial commit)
