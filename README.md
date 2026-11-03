# FilMaNH

**Deutsch** · [English](#english)

Filament- und Spulenverwaltung für Bambu-Lab-Drucker. Läuft lokal auf deinem Rechner (macOS und Windows),
ohne Cloud und ohne Einstellungen am Drucker zu ändern. Dazu gibt es Apps für Android und iPhone. Alles auf Deutsch
und Englisch.

## Download

| System | Download |
|---|---|
| **macOS** · Apple Silicon und Intel, von Apple geprüft | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_universal.dmg` |
| **Windows** · 64 Bit | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_x64-setup.exe` |
| **Android** · ab Android 9 | **[FilMaNH-Android.apk](https://github.com/NikolausH76/FilMaNH/releases/latest/download/FilMaNH-Android.apk)** · [Installieren](handbuch/android.md#1-installieren) |
| **iPhone** | demnächst im App Store |

<img src="handbuch/bilder/android-download.png" width="140" alt="QR-Code: Android-App laden"><br>
<sub>Android-App: mit dem Handy scannen</sub>

Neue Versionen meldet das Programm auf dem Rechner selbst und installiert sie auf Klick. Die Apps für Android und
iPhone arbeiten mit FilMaNH auf dem Rechner zusammen.

## Handbuch

**[Benutzerhandbuch mit Screenshots](handbuch/README.md)** – Installation, Einrichtung und alle Funktionen.

## Was FilMaNH kann

- Spulen anlegen mit Katalog (über 7.000 Filamente), per EAN-Scan oder Shop-Link; wiegen, bewerten, Etiketten drucken
- Drucker im Netz finden, AMS live, Bambu-Spulen mit RFID automatisch erkennen – mit Farbnamen aus Bambu Studio
- H2C und H2D mit zwei Düsen: AMS und externe Spulen je Düse (links, rechts)
- Verbrauch jedes Drucks automatisch abbuchen – auch wenn der Rechner während des Drucks aus war
- Kosten je Druck, netto und brutto, mit Strom und Maschinenzeit
- Druckverlauf mit Bild und 3D-Ansicht, „Reicht die Spule?“, Feuchte, Einkaufsliste, Auswertung

## Apps für Android und iPhone

Spulen scannen, in Slots legen, wiegen, fotografieren und bearbeiten – am Handy, zusammen mit FilMaNH auf deinem
Rechner, im Heimnetz und ohne Cloud. Laden unter [Download](#download). Anleitungen: [Android](handbuch/android.md) ·
[iPhone](handbuch/iphone.md)

<p>
  <img src="handbuch/bilder/android-drucker.png" width="220" alt="Android: Drucker mit AMS">
  <img src="handbuch/bilder/android-spule.png" width="220" alt="Android: Spule">
  <img src="handbuch/bilder/android-bearbeiten.png" width="220" alt="Android: Spule bearbeiten">
</p>
<p>
  <img src="handbuch/bilder/iphone-drucker.png" width="220" alt="iPhone: Drucker mit AMS">
  <img src="handbuch/bilder/iphone-spule.png" width="220" alt="iPhone: Spule">
  <img src="handbuch/bilder/iphone-bearbeiten.png" width="220" alt="iPhone: Spule bearbeiten">
</p>

## Demnächst

In Arbeit – schon in der App angelegt, aber noch nicht an echten Druckern geprüft:

- **AMS HT** als eigene Einheit
- **Spule leer gelaufen:** Läuft eine Spule im Druck leer, setzt ein Klick ihren Rest auf 0
- **Trocknen im AMS 2 Pro und AMS HT:** Die eingelegten Spulen gelten danach als getrocknet – nicht, wenn die
  Trocknung vor der Hälfte der Zeit abgebrochen wurde
- **Spulenwechsel im Druck:** Ersatzspule im AMS oder von Hand getauscht – der Verbrauch wird an dieser Schicht auf
  beide Spulen aufgeteilt
- **Druck ohne Druckdatei** (z.B. H2 ohne USB-Stick): Verbrauch je Spule eintragen, mit Vorschlag aus der RFID-Anzeige

## Fragen und Fehler

Bitte als [Issue](https://github.com/NikolausH76/FilMaNH/issues) melden.

---

## English

Filament and spool manager for Bambu Lab printers. Runs locally on your computer (macOS and Windows), no cloud,
no printer settings to change. Apps for Android and iPhone come with it. Everything in English and German.

### Download

| System | Download |
|---|---|
| **macOS** · Apple Silicon and Intel, notarized by Apple | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_universal.dmg` |
| **Windows** · 64-bit | [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest) → `FilMaNH_…_x64-setup.exe` |
| **Android** · Android 9 or later | **[FilMaNH-Android.apk](https://github.com/NikolausH76/FilMaNH/releases/latest/download/FilMaNH-Android.apk)** · [How to install](handbook/android.md#1-installing) |
| **iPhone** | coming soon to the App Store |

<img src="handbook/images/android-download.png" width="140" alt="QR code: download the Android app"><br>
<sub>Android app: scan with your phone</sub>

The program on your computer announces new versions itself and installs them with one click. The Android and iPhone
apps work together with FilMaNH on your computer.

### User guide

**[User guide with screenshots](handbook/README.md)** – installation, setup and every feature.

### Features

- Add spools from a catalog (more than 7,000 filaments), by EAN scan or shop link; weigh, rate, print labels
- Find printers on the network, live AMS view, Bambu spools with RFID recognised automatically – with colour names
  from Bambu Studio
- H2C and H2D with two nozzles: AMS units and external spools per nozzle (left, right)
- Deducts what every print uses, automatically – even if the computer was off during the print
- Cost per print, net and gross, including electricity and machine time
- Print history with image and 3D view, “Will the spool last?”, moisture, shopping list, statistics

### Apps for Android and iPhone

Scan spools, put them in slots, weigh, photograph and edit them – on your phone, together with FilMaNH on your
computer, on your home network and without a cloud. Get them under [Download](#download-1). Guides:
[Android](handbook/android.md) · [iPhone](handbook/iphone.md)

<p>
  <img src="handbook/images/android-drucker.png" width="220" alt="Android: printers with AMS">
  <img src="handbook/images/android-spule.png" width="220" alt="Android: spool">
  <img src="handbook/images/android-bearbeiten.png" width="220" alt="Android: edit spool">
</p>
<p>
  <img src="handbook/images/iphone-drucker.png" width="220" alt="iPhone: printers with AMS">
  <img src="handbook/images/iphone-spule.png" width="220" alt="iPhone: spool">
  <img src="handbook/images/iphone-bearbeiten.png" width="220" alt="iPhone: edit spool">
</p>

### Coming soon

In progress – already in the app, but not yet tested on real printers:

- **AMS HT** as a unit of its own
- **Spool ran out:** if a spool runs out during a print, one click sets its remaining amount to 0
- **Drying in the AMS 2 Pro and AMS HT:** the loaded spools count as dried afterwards – not if drying was stopped
  before half the time
- **Spool change during a print:** AMS backup spool or swapped by hand – usage is split between both spools at that
  layer
- **Print without a print file** (e.g. H2 without a USB drive): enter the usage per spool, with a suggestion from the
  RFID reading

### Questions and bugs

Please open an [issue](https://github.com/NikolausH76/FilMaNH/issues).

---

© 2026 N. Hass. Kostenlos nutzbar, alle Rechte vorbehalten; der Quellcode ist nicht öffentlich.
*Free to use, all rights reserved; the source code is not public.* ([Lizenz / License](LICENSE.txt))

FilMaNH ist ein unabhängiges Projekt und nicht mit Bambu Lab verbunden. Es nutzt das inoffizielle lokale Protokoll
der Drucker und greift nur lesend zu. *FilMaNH is an independent project and not affiliated with Bambu Lab. It uses
the printers’ unofficial local protocol and only reads from them.*
