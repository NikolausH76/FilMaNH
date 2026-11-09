<p align="center">
  <img src="handbuch/bilder/logo.png" width="104" alt="FilMaNH logo">
</p>

<h1 align="center">FilMaNH</h1>

<p align="center">
  <b>Filament and spool manager for Bambu Lab printers</b><br>
  What's in the AMS, how much is left on the spool, what did the print cost?<br>
  Runs locally on your computer, no cloud, no printer settings to change.
</p>

<p align="center">
  🌐 <b>English · Deutsch · Español · Français · Italiano · Nederlands · Polski</b><br>
  <sub>App, phone apps and built-in help in 7 languages</sub>
</p>

<p align="center">
  <a href="https://github.com/NikolausH76/FilMaNH/releases/latest"><img src="https://img.shields.io/github/v/release/NikolausH76/FilMaNH?label=Version&color=2A59D6" alt="Latest version"></a>
</p>

<p align="center"><a href="README.md">Deutsch</a> · <b>English</b></p>

<p align="center">
  <img src="handbook/images/05-spulen.png" width="900" alt="FilMaNH: all spools with remaining amount">
</p>

<p align="center">
  <a href="https://github.com/NikolausH76/FilMaNH/releases/latest"><img src="https://img.shields.io/badge/macOS-Download-2A59D6?style=for-the-badge" alt="Download for macOS"></a>
  <a href="https://github.com/NikolausH76/FilMaNH/releases/latest"><img src="https://img.shields.io/badge/Windows-Download-2A59D6?style=for-the-badge" alt="Download for Windows"></a>
  <a href="https://github.com/NikolausH76/FilMaNH/releases/latest/download/FilMaNH-Android.apk"><img src="https://img.shields.io/badge/Android-Download-2A59D6?style=for-the-badge" alt="Download for Android"></a>
  <img src="https://img.shields.io/badge/iPhone-soon_on_the_App_Store-555?style=for-the-badge" alt="iPhone: soon on the App Store">
</p>

## What it's for

With several spools and an AMS it's easy to lose track: What's loaded where? How much is left? Is it enough for the
next print? FilMaNH follows your printers on your home network and, after every print, books the usage off the right
spool – from the print file, including the purge when changing colours. Your stock stays right without entering
anything after each print.

## How it works

1. **Add spools** – from the catalog with more than 7,000 filaments, by EAN scan or with the link to the product page.
   FilMaNH recognises Bambu spools with RFID by itself when you load them.
2. **Print a label and load the spool** – every spool gets a number and a label with a QR code. When it's in the AMS,
   FilMaNH asks once which spool it is.
3. **Print** – at the end of every print, FilMaNH books the usage per spool. If the computer was off, it catches up on
   the next start.
4. **Keep track** – printers and AMS as they look, with live view, remaining amounts, cost per print, notices for the
   wrong material or filament left open too long, statistics and a shopping list.

> [!NOTE]
> FilMaNH only reads from the printers. It never sends them commands and needs neither LAN-only mode nor developer mode.

## Features

<table>
<tr>
<td width="50%" valign="top">

<img src="handbook/images/01-uebersicht.png" alt="Overview">

### Overview and notices

- All printers with the current print, time left and print hours – with their AMS as a picture, spools in their colour
- **Live view** of the printer camera on click
- Notices with the matching action: wrong material or different colour in a slot (assign right away or add a new
  spool), unassigned spool, filament open too long, spools almost empty, maintenance due
- Recent prints, with cost

</td>
<td width="50%" valign="top">

<img src="handbook/images/11-drucker-ams.png" alt="Printer with AMS">

### Printers and AMS

- Find printers on the network, take the access code from Bambu Studio
- AMS, AMS 2 Pro and AMS HT as a picture: spools in their real colour, material, humidity, temperature, drying with time
  left
- Live view: video on H2, X1 and P2S, continuous still images on P1 and A1
- Humidity history of the last 7 days, total print hours per printer
- H2C and H2D with two nozzles: AMS and external spools per nozzle
- At print start: wrong material, different colour, spool won't last, abrasive filament on a soft nozzle
- Maintenance plan per printer by print hours or time

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="handbook/images/06-spule.png" alt="Spool">

### Spools

- Remaining amount, price, shop, location, rating and history for every spool
- Weighing makes the stock exact – FilMaNH learns the deviation per filament from it
- Notice when filament has been open too long (PETG after 30 days, TPU after 14, PA and PC after 7)
- Filter by state, material, brand and location; sort by fill level, name, brand and more
- Catalog with the newest Bambu Studio profiles and your own filament presets from Bambu Studio
- More than 80 filament colours to choose from, also multicolour and gradient

</td>
<td width="50%" valign="top">

<img src="handbook/images/15-druck.png" alt="Print with cost">

### Prints and cost

- Usage per slot from the print file, with purge waste (prime tower included); for a cancelled print only up to the
  layer reached
- Cost per print, net and gross: material, electricity and machine time (from purchase price and service life);
  12 currencies, VAT preset per country
- Projects: group prints per job, with a selling price from costs, labour and markup
- History with image, 3D view, timelapse and your own photos – also per project
- Keep the print file and open it in Bambu Studio; models with all prints, cost and success rate

</td>
</tr>
<tr>
<td width="50%" valign="top">

<img src="handbook/images/09-etiketten.png" alt="Labels">

### Labels

- Number, colour, brand, date opened and QR code; optionally print temperature, location, purchase date, price
- Brother QL via USB directly, no driver needed (Mac); any system printer for rolls and A4/Letter sheets
- **Missing labels** prints exactly the new spools

</td>
<td width="50%" valign="top">

<img src="handbook/images/19-auswertung.png" alt="Statistics">

### Statistics and shopping

- Cost per month (a click shows the days), where the money goes, comparison with the previous period
- Purge waste, colours, when you print, utilisation per printer, waste and cancellation reasons
- Humidity and failed prints, slicer estimate vs. reality, stock value and shelf warmers
- **Check print file:** Is there enough filament, what will the print cost?
- Minimum stock per filament: shopping list with shop and last price
- Reach based on usage: what will run out in the coming weeks

</td>
</tr>
</table>

## On your phone

<p align="center">
  <img src="handbook/images/android-drucker.png" width="220" alt="Phone: printers with AMS">
  <img src="handbook/images/android-spule.png" width="220" alt="Phone: spool">
  <img src="handbook/images/android-bearbeiten.png" width="220" alt="Phone: edit spool">
</p>

Scan spools, put them in slots, weigh, photograph and edit them, printers and AMS as pictures – together with FilMaNH
on your computer, on your home network and encrypted, plus a widget with the running prints. The **Android** app is available for download below; the **iPhone** app is coming soon to the
App Store. Guides: [Android](handbook/android.md) · [iPhone](handbook/iphone.md)

## Download

| System | Download |
|---|---|
| **macOS** · Apple Silicon and Intel, notarized by Apple | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_universal.dmg` |
| **Windows** · 10 and 11, 64-bit | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_x64-setup.exe` |
| **Android** · Android 9 or later | **[FilMaNH-Android.apk](https://github.com/NikolausH76/FilMaNH/releases/latest/download/FilMaNH-Android.apk)** · [How to install](handbook/android.md#1-installing) |
| **iPhone** | coming soon to the App Store |

<img src="handbook/images/android-download.png" width="140" alt="QR code: download the Android app"><br>
<sub>Android app: scan with your phone</sub>

The program on your computer announces new versions itself and installs them with one click.

**Languages:** Deutsch, English, Español, Français, Italiano, Nederlands, Polski – on the computer and on the phone.

**Requirements:** Bambu Lab printers on the same network as the computer (tested with A1 mini, P2S and H2C). FilMaNH
takes the access code from Bambu Studio; otherwise you find it on the printer under **Settings › WLAN**.

## User guide

**[User guide with screenshots](handbook/README.md)** – installation, setup and all features. Also right inside the
app under **Settings › Help** (F1), in all 7 languages.
For the phones: [Android](handbook/android.md) · [iPhone](handbook/iphone.md)

## Privacy

All data stays on your computer – no account, no ads, no analytics. FilMaNH only goes online for updates and the
filament catalog (both on GitHub), for a shop link you paste or scan with your phone and for importing from Spoolman. More:
[privacy statement](DATENSCHUTZ.md)

## Built in, but not yet tested

These features are already in the program but haven't been tried on real hardware yet – the matching device is
missing or the situation hasn't come up. If you use them, a short [report](https://github.com/NikolausH76/FilMaNH/issues)
helps.

- **AMS HT** as a unit of its own
- **Live view on X1, P1 and P2S** (tested with H2C and A1 mini)
- **Labels on Windows** printed directly to a system printer
- **Android app widget** on a real phone (checked in the emulator)
- **Spool ran out:** if a spool runs out during a print, one click sets its remaining amount to 0
- **Drying in the AMS 2 Pro and AMS HT:** the loaded spools count as dried afterwards – not if drying was stopped
  before half the time
- **Spool change during a print:** AMS backup spool or swapped by hand – usage is split between both spools at that
  layer
- **Print without a print file** (e.g. H2 without a USB drive): enter the usage per spool, with a suggestion from the
  RFID reading

## Questions and bugs

Please open an [issue](https://github.com/NikolausH76/FilMaNH/issues).

---

© 2026 N. Hass. Kostenlos nutzbar, alle Rechte vorbehalten; der Quellcode ist nicht öffentlich.
*Free to use, all rights reserved; the source code is not public.* ([Lizenz / License](LICENSE.txt))

FilMaNH ist ein unabhängiges Projekt und nicht mit Bambu Lab verbunden. Es nutzt das inoffizielle lokale Protokoll
der Drucker und greift nur lesend zu. *FilMaNH is an independent project and not affiliated with Bambu Lab. It uses
the printers’ unofficial local protocol and only reads from them.*
