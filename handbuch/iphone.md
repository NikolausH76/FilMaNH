# FilMaNH für iPhone – Handbuch

*Deutsch · [English](../handbook/iphone.md) · [Handbuch für den Rechner](README.md)*

Die iPhone-App arbeitet mit FilMaNH auf deinem Rechner zusammen: Spulen scannen, in Slots legen, wiegen,
fotografieren und bearbeiten. Die Daten bleiben auf dem Rechner. Das iPhone verbindet sich nur im Heimnetz mit ihm,
verschlüsselt. Die App erscheint demnächst im App Store.

1. [Voraussetzungen](#1-voraussetzungen)
2. [Koppeln](#2-koppeln)
3. [Drucker](#3-drucker)
4. [Spulen](#4-spulen)
5. [Neue Spule](#5-neue-spule)
6. [Scannen](#6-scannen)
7. [Einstellungen](#7-einstellungen)
8. [Widget](#8-widget)
9. [Häufige Fragen](#9-häufige-fragen)

---

## 1. Voraussetzungen

- FilMaNH ab Version 0.5 läuft auf dem Rechner (Mac oder Windows). Das Fenster darf geschlossen sein.
- Am Rechner ist **Einstellungen › iPhone** eingeschaltet (ab Werk aus).
- iPhone mit iOS 17 oder neuer im selben WLAN wie der Rechner.

## 2. Koppeln

<p>
  <img src="bilder/iphone-start.png" width="240" alt="Start">
  <img src="bilder/iphone-koppeln.png" width="240" alt="Koppeln">
</p>

1. Am Rechner in FilMaNH: **Einstellungen › iPhone › QR-Code zeigen**.
2. Auf dem iPhone **Mit Rechner koppeln** antippen, den Code scannen und **Koppeln** bestätigen.
3. Beim ersten Mal fragt iOS nach dem **lokalen Netzwerk**: erlauben. Ohne diese Erlaubnis findet das iPhone den
   Rechner nicht.

**Beispieldaten ansehen** zeigt die App ohne Rechner mit erfundenen Spulen; Änderungen werden nicht gespeichert.

## 3. Drucker

<p>
  <img src="bilder/iphone-drucker.png" width="240" alt="Drucker">
  <img src="bilder/iphone-slot.png" width="240" alt="Slot">
  <img src="bilder/iphone-hinweis.png" width="240" alt="Hinweis">
</p>

Alle Drucker mit Zustand, laufendem Druck und Restzeit. Darunter jedes AMS mit den Slots 1–4 und der Feuchte (beim
Trocknen die Restzeit), dann die externe Spule (an H2D und H2C mit links/rechts).

Ein Slot öffnet die Auswahl: **Im Slot** zeigt die Spule, **Slot leeren** nimmt sie heraus. Unter **Spule
einlegen** stehen passende Spulen oben (gleiches Material wie im Slot gemeldet, dann noch nirgends eingelegte), oder
**Etikett scannen** und die Spule über ihren QR-Code wählen.

Passt ein Slot nicht zur Meldung des Druckers, steht ein Hinweis auf der Karte des Druckers – wie am Rechner (siehe
[Abgleich mit dem Drucker](README.md#abgleich-mit-dem-drucker)): **Ja**, **Andere …**, **Zuordnen**,
**Andere Spule …**, **Stimmt so**, **Ja, entnommen** oder **Steckt noch**.

## 4. Spulen

<p>
  <img src="bilder/iphone-spulen.png" width="240" alt="Spulen">
  <img src="bilder/iphone-spule.png" width="240" alt="Spule">
  <img src="bilder/iphone-spule-aktionen.png" width="240" alt="Spule: Aktionen">
</p>

Suche nach Nummer, Hersteller und Farbe; Filter **Im Bestand**, **Fast leer** und **Archiv**. Die Pfeile oben links
sortieren nach Nummer, Rest oder Hersteller.

Eine Spule zeigt Rest, Füllung, leere Spule, Ort, Preis, Händler und Kaufdatum und den **Verlauf** aller Buchungen.
Die Sterne bewerten das Filament; derselbe Stern noch einmal löscht die Bewertung. Darunter:

- **In Slot legen** – Drucker und Slot wählen.
- **Wiegen** – siehe unten.
- **Foto aufnehmen** – das Foto gilt für alle Spulen dieses Filaments.
- **Heute getrocknet** – setzt die Feuchte-Zeit zurück.
- **Weitere Spule wie diese** – neue Spule desselben Filaments.
- **EAN scannen** – Strichcode der Spule merken.
- **Archivieren** – leere Spule ablegen.
- **Löschen …** – versehentlich angelegte Spule entfernen; geht nur ohne gebuchte Drucke (ab FilMaNH 0.7).

### Wiegen

<img src="bilder/iphone-wiegen.png" width="240" alt="Wiegen">

Spule samt Rolle wiegen und das Gewicht eintippen. FilMaNH zieht das Leergewicht ab und zeigt den Rest gleich an.

### Bearbeiten

<img src="bilder/iphone-bearbeiten.png" width="240" alt="Bearbeiten">

**Bearbeiten** oben rechts. Hersteller, Bezeichnung, Material, Farbname und Farbe gelten für das Filament, also für
alle Spulen dieser Sorte. Die Farbe kommt aus der Farbbibliothek (Standard, Matt, Seide, Galaxy, Transparent,
Mehrfarbig) oder wird selbst eingestellt; **+** fügt Farben für Verlaufs- und mehrfarbiges Filament hinzu. Dazu Rest, leere Spule, Lagerort, Mindestbestand, Preis (brutto oder netto), MwSt.,
Händler, Kaufdatum, **Geöffnet am**, Charge und Notiz.

## 5. Neue Spule

<p>
  <img src="bilder/iphone-neue-spule.png" width="240" alt="Neue Spule">
  <img src="bilder/iphone-farbe.png" width="240" alt="Farbe">
</p>

**+** in der Spulenliste. Die Suche geht über den Katalog des Rechners (Hersteller, Bezeichnung, Farbe). **Eigenes
Filament** zum selbst Eintragen (Farbe wie beim Bearbeiten), darunter die **Vorhandenen Filamente**. Danach Füllung, Kauf, Lagerort und Anzahl,
dann **Anlegen**.

Das Etikett druckt der Rechner: Dort steht in der Spulenliste **Fehlende Etiketten** mit allen neuen Spulen (ab
FilMaNH 0.6).

## 6. Scannen

Der Tab **Scannen** erkennt:

- **FilMaNH-Etikett** (QR-Code) – öffnet die Spule.
- **EAN** (Strichcode auf Spule oder Karton) – zeigt die Spulen mit dieser EAN. Dazu **Neue Spule anlegen** bzw.
  **Weitere Spule anlegen**, **Vorhandener Spule zuordnen** oder **Am Rechner weitermachen**: Dort öffnet sich
  **Neue Spule** mit der EAN.
- **Link** (z.B. Produktseite) – **An den Rechner schicken** öffnet dort **Neue Spule**, und FilMaNH liest Name,
  Preis und Shop von der Seite.

## 7. Einstellungen

<img src="bilder/iphone-einstellungen.png" width="240" alt="Einstellungen">

Zahnrad oben rechts.

- **Darstellung:** System, Hell oder Dunkel. **Hintergrundbild** ein oder aus.
- **Sprache:** Deutsch, English, Español, Français, Italiano, Nederlands, Polski – wie das iPhone, sonst Englisch; ein Tipp öffnet die Einstellungen von iOS für
  FilMaNH.
- **Rechner:** Name, Status und Adresse. **Neu koppeln** ersetzt die Kopplung, **Trennen** hebt sie auf. Am Rechner
  unter **Einstellungen › iPhone** lässt sich ein iPhone ebenfalls **Entfernen**.
- **Handbuch** und **Fehler melden**.

## 8. Widget

Das Widget **Drucke** (ab App-Version 1.2) gibt es klein und mittel für den Home-Bildschirm und für den
Sperrbildschirm. Es zeigt die laufenden Drucke mit Drucker, Fortschritt, dem voraussichtlichen Ende („fertig um
17:54“) und einem Punkt in der Farbe der Spule, aus der gerade gedruckt wird – klein einen Druck oder bis zu drei
knapp, mittel bis zu drei. Hinzufügen: lange auf den Home-Bildschirm tippen › **Bearbeiten** › **Widget hinzufügen**
› **FilMaNH**. Ein Tipp aufs Widget öffnet die App.

Das Widget holt den Stand selbst vom Rechner, nur im Heimnetz. Wie oft, entscheidet iOS; die App aktualisiert es
sofort, wenn sie neue Daten hat. Ohne Verbindung steht der letzte Stand mit Uhrzeit da.

## 9. Häufige Fragen

**„Rechner nicht erreichbar“?** FilMaNH muss am Rechner laufen, **Einstellungen › iPhone** muss an sein, und das
iPhone muss im selben WLAN sein. In den iOS-Einstellungen unter FilMaNH muss **Lokales Netzwerk** erlaubt sein.

Läuft FilMaNH auf einem **Windows-PC**, blockiert oft die Windows-Firewall: am Rechner unter **Einstellungen › iPhone**
bei **Windows-Firewall** auf **Freigeben** klicken und die Rückfrage von Windows bestätigen.

**Geht das auch unterwegs?** Nein. Die App spricht nur im Heimnetz mit dem Rechner; ins Internet geht dabei nichts.

**Mehrere iPhones?** Ja, jedes wird einzeln gekoppelt.
