# FilMaNH – Datenschutz

*Stand: 9. November 2026 · English below*

FilMaNH besteht aus einem Programm für Mac und Windows und Apps für iPhone und Android. Sie erheben keine Daten für
den Entwickler oder für Dritte. Es gibt kein Konto, keine Werbung, keine Analyse und kein Tracking.

## Apps für iPhone und Android

- Die App verbindet sich ausschließlich mit FilMaNH auf deinem eigenen Rechner in deinem Heimnetz. Die Verbindung
  ist verschlüsselt und wird einmalig per QR-Code gekoppelt.
- Spulen, Drucke und Fotos liegen auf deinem Rechner. Das Handy speichert die Kopplung, deine Einstellungen
  (z.B. Darstellung) und eine Kopie des letzten Stands samt Spulenfotos, damit die App auch ohne Verbindung etwas zeigt. **Trennen**
  löscht Kopplung und Kopie.
- **Kamera:** zum Scannen von QR-Codes und Strichcodes und für Fotos deiner Spulen. Fotos gehen nur an deinen
  Rechner. Unter Android erkennt ML Kit von Google die Codes direkt auf dem Handy; die App sendet dabei nichts an
  Google (ab Android-App 1.0.1).
- **Lokales Netzwerk:** nur, um den gekoppelten Rechner zu erreichen.
- **Handbuch** und **Fehler melden** öffnen GitHub im Browser; dort gilt die Datenschutzerklärung von GitHub.

## Programm auf dem Rechner

- Es liest deine 3D-Drucker im Heimnetz aus und speichert alle Daten lokal auf deinem Rechner.
- Auf Klick zeigt es das Live-Bild der Druckerkamera. Das Bild geht nur vom Drucker an deinen Rechner und wird nicht
  gespeichert.
- Solange ein Handy gekoppelt ist, nimmt es im Heimnetz verschlüsselte Verbindungen an; Daten bekommen nur gekoppelte
  Handys.
- Es liest auf deinem Rechner Zugangscodes und Filamentprofile aus Bambu Studio. Sie bleiben auf dem Rechner.
- Ins Internet verbindet es sich nur
  - zur Suche nach Updates und für den Filament-Katalog (beides auf GitHub),
  - wenn du einen Shop-Link einfügst oder mit dem Handy scannst: zur Seite dieses Shops (nie zu einer Adresse im
    eigenen Netzwerk),
  - wenn du Spulen aus einem Spoolman-Server übernimmst: zu diesem Server.
- Der Installer für Windows lädt bei Bedarf Microsoft WebView2 nach (die Anzeige-Komponente von Windows), wenn sie auf
  dem Rechner fehlt.

## Kontakt

Fragen zum Datenschutz über [Fehler melden](https://github.com/NikolausH76/FilMaNH/issues/new/choose).

---

# FilMaNH – Privacy

*As of 9 November 2026*

FilMaNH consists of a program for Mac and Windows and apps for iPhone and Android. None of them collects any data for the developer
or for third parties. There is no account, no advertising, no analytics and no tracking.

## Apps for iPhone and Android

- The app connects only to FilMaNH on your own computer on your home network. The connection is encrypted and paired
  once by QR code.
- Spools, prints and photos are stored on your computer. The phone keeps the pairing, your settings (e.g.
  appearance) and a copy of the last state including spool photos, so the app can show something without a connection. **Unpair** deletes
  the pairing and the copy.
- **Camera:** to scan QR codes and barcodes and to take photos of your spools. Photos go only to your computer. On
  Android, Google's ML Kit reads the codes on the phone itself; the app sends nothing to Google (Android app 1.0.1 or
  later).
- **Local network:** only to reach the paired computer.
- **Manual** and **Report a problem** open GitHub in the browser; GitHub's privacy statement applies there.

## Program on the computer

- It reads your 3D printers on your home network and stores all data locally on your computer.
- On click it shows the live image of the printer camera. The image only goes from the printer to your computer and is
  not stored.
- While a phone is paired, it accepts encrypted connections on your home network; only paired phones get data.
- It reads access codes and filament profiles from Bambu Studio on your computer. They stay on your computer.
- It only connects to the internet
  - to check for updates and for the filament catalog (both on GitHub),
  - when you paste a shop link or scan one with your phone: to that shop's page (never to an address on your own
    network),
  - when you import spools from a Spoolman server: to that server.
- The Windows installer downloads Microsoft WebView2 (the Windows display component) if it is missing on the computer.

## Contact

Questions about privacy via [Report a problem](https://github.com/NikolausH76/FilMaNH/issues/new/choose).
