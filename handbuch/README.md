# FilMaNH – Handbuch

*Deutsch · [English](../handbook/README.md) · [iPhone-App](iphone.md) · [Android-App](android.md)*

FilMaNH verwaltet deine Filamentspulen und bucht den Verbrauch jedes Drucks automatisch ab. Das Programm läuft
lokal auf deinem Rechner und liest die Bambu-Lab-Drucker im Netzwerk nur aus.

1. [Installation](#1-installation)
2. [Ersteinrichtung](#2-ersteinrichtung)
3. [So arbeitet FilMaNH](#3-so-arbeitet-filmanh)
4. [Übersicht](#4-übersicht)
5. [Spulen](#5-spulen)
6. [Drucker](#6-drucker)
7. [Druckdatei prüfen](#7-druckdatei-prüfen)
8. [Verlauf](#8-verlauf)
9. [Modelle](#9-modelle)
10. [Auswertung](#10-auswertung)
11. [Einkauf](#11-einkauf)
12. [Einstellungen](#12-einstellungen)
13. [Im Hintergrund](#13-im-hintergrund)
14. [Tastatur und Scanner](#14-tastatur-und-scanner)
15. [Daten und Datenschutz](#15-daten-und-datenschutz)
16. [Häufige Fragen](#16-häufige-fragen)

---

## 1. Installation

Download unter [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest).

**macOS** (Apple Silicon und Intel): `FilMaNH_…_universal.dmg` öffnen und FilMaNH in den Ordner „Programme“
ziehen. Die App ist von Apple geprüft (notarisiert); beim ersten Öffnen nur bestätigen, dass die aus dem Internet
geladene App geöffnet werden soll.

**Windows 10/11** (64 Bit): `FilMaNH_…_x64-setup.exe` starten. Bei „Der Computer wurde durch Windows geschützt“:
**Weitere Informationen › Trotzdem ausführen**. Administratorrechte sind nicht nötig.

Rechner und Drucker müssen im selben Netzwerk erreichbar sein. Am Drucker muss nichts umgestellt werden. FilMaNH
verbindet sich mit den Ports 8883 (Zustand) und 990 (Druckdateien) des Druckers – liegt eine Firewall dazwischen,
müssen beide offen sein.

## 2. Ersteinrichtung

Beim ersten Start sucht FilMaNH die Drucker im Netzwerk und fragt für jeden einzeln, ob er hinzugefügt werden soll.

![Drucker gefunden](bilder/02-setup-suche.png)

- **Zugangscode:** Ist Bambu Studio auf dem Rechner eingerichtet, übernimmt FilMaNH den Code von dort. Sonst steht
  er am Drucker unter **Einstellungen › WLAN**.
- **Kein Drucker gefunden:** Liegt der Drucker in einem anderen Netz (z.B. einem eigenen Netz für Smart-Home-Geräte),
  das Netz wie `192.168.2` oder die IP-Adresse des Druckers eingeben.

Danach fragt FilMaNH, was mit den Drucken passieren soll, die schon auf der Speicherkarte liegen:

![Drucke auf der Speicherkarte](bilder/03-setup-karte.png)

- **Ab jetzt beginnen:** Alte Drucke bleiben außen vor.
- **Frühere Drucke in den Verlauf übernehmen:** Sie erscheinen im Verlauf und unter Modelle, es wird aber nichts
  von Spulen abgebucht.

Zum Schluss fragt FilMaNH nach dem **Strompreis** je kWh (für die Stromkosten der Drucke) und ob es **mit dem Rechner
starten** soll – empfohlen, so verfolgt FilMaNH jeden Druck.

Die Einrichtung lässt sich mit **Später einrichten** überspringen und unter Einstellungen › Drucker nachholen.

## 3. So arbeitet FilMaNH

- Jede Spule hat eine Nummer (#001, #002 …) und einen Restbestand.
- Steckt eine Spule im AMS oder am externen Halter, ist sie diesem Slot zugeordnet. **Bambu-Spulen mit RFID** legt
  FilMaNH beim Einlegen selbst an. Bei allen anderen fragt es einmal, welche Spule das ist.
- **Am Ende jedes Drucks** liest FilMaNH aus der Druckdatei, wie viel Filament aus welchem Slot verbraucht wurde,
  und bucht es von der Spule ab, das Spülen beim Farbwechsel eingeschlossen. Bei einem Abbruch wird nur bis zur
  erreichten Schicht gebucht.
- **War der Rechner aus**, holt FilMaNH beim nächsten Start nach, was der Drucker in der Zwischenzeit gedruckt hat.
  Was sich nicht sicher klären lässt, erscheint als Hinweis und wird mit einem Klick bestätigt.
- **Wiegen** macht den Bestand genau. Aus den Wiegungen lernt FilMaNH, wie stark der echte Verbrauch je Filament
  von der Berechnung abweicht, und rechnet das künftig ein.
- **„ca.“** vor einem Gewicht heißt: geschätzt, kann etwas abweichen. Wiegen macht den Wert wieder genau.

## 4. Übersicht

![Übersicht](bilder/01-uebersicht.png)

- **Hinweise** oben zeigen, was Aufmerksamkeit braucht: falsches Material im Slot, Druck mit offenem Ende, Spule
  ohne Zuordnung, Feuchte, fast leere Spulen. Die passende Aktion steht jeweils daneben.
- **Drucker** mit Status, laufendem Druck, Restzeit und den Slots samt Restmenge: je AMS die Slots 1–4 (bei mehreren
  AMS mit Überschrift), abgesetzt die externe Spule. Ein Klick öffnet den Drucker.
- **Zuletzt gedruckt** mit Kosten.

## 5. Spulen

![Spulen](bilder/05-spulen.png)

Filter nach Zustand (Voll, Angebrochen, Fast leer, Leer, Archiv), Material, Hersteller und Lagerort; Suche,
Kachel- oder Listenansicht. **Etiketten** druckt Etiketten für alle angezeigten Spulen. **Fehlende Etiketten** steht
da, sobald neue Spulen noch kein Etikett haben (auch am iPhone angelegte), und druckt genau diese.

### Neue Spule

![Neue Spule](bilder/04-neue-spule.png)

Hersteller, Material oder Farbe ins Suchfeld tippen, z.B. „sunlu petg weiß“. Der Katalog kennt über 7.000
Filamente; die Auswahl füllt Farbe, Füllmenge und Leergewicht aus. Dazu optional Preis (brutto oder netto),
Lagerort und **Anzahl**: Bei 3 entstehen drei Spulen mit eigener Nummer. Steht ein Filament nicht im Katalog:
**Ohne Katalog** und selbst eintragen.

Das Suchfeld nimmt auch eine **EAN** (Strichcode auf Spule oder Karton) und einen **Shop-Link**:

- **EAN:** scannen oder eintippen und Enter. Beim ersten Mal das Filament auswählen, FilMaNH merkt sich die EAN.
  Beim nächsten Mal ist das Filament schon gewählt, mit Preis und Händler der letzten Spule.
- **Shop-Link:** den Link zur Produktseite einfügen. FilMaNH liest Name, Preis und Shop von der Seite und schlägt
  passende Filamente aus dem Katalog vor; Preis (in deiner Währung) und Shop werden übernommen. Das klappt nicht bei
  jedem Shop – manche geben diese Daten nicht heraus.

![Shop-Link](bilder/04b-shop-link.png)

Nach dem Anlegen bietet FilMaNH an, gleich das Etikett zu drucken. Bambu-Spulen mit RFID müssen nicht angelegt
werden – einlegen genügt.

### Spule im Detail

![Spule](bilder/06-spule.png)

Restbestand, Ort (Slot oder Lagerort), Material, Preis, Feuchte, **Bewertung** und jede Buchung im Verlauf.
**Mehr** zeigt Charge, Genauigkeit, gelernte Korrektur, Mindestbestand, EAN und Notiz. **Reste aufbrauchen** listet Modelle, die du
schon gedruckt hast und für die der Rest noch reicht.

![Menü einer Spule](bilder/07-spule-mehr.png)

Im Menü **…**: Bearbeiten, Rest korrigieren, Ort ändern, Weitere Spule wie diese, Etikett drucken, Foto hinzufügen
und Archivieren. Ein **Foto** der Spule zeigt die echte Farbe in der Mitte des Rings.

Die **Bewertung** (1–5 Sterne) gilt für das Filament, also für alle Spulen dieser Sorte; derselbe Stern noch einmal
löscht sie. Unter **Bearbeiten** lassen sich EANs von Hand eintragen, mehrere durch Komma getrennt (z.B. mit Spule
und Refill). Dort lassen sich auch **Hersteller**, **Bezeichnung**, **Material** und **Farbe** ändern; das gilt für alle
Spulen dieses Filaments.

### Wiegen

![Wiegen](bilder/08-wiegen.png)

Spule samt Rolle wiegen und das Gewicht eintragen. FilMaNH zieht das Leergewicht ab und übernimmt den Rest.

### Etiketten

![Etiketten](bilder/09-etiketten.png)

Auf dem Etikett: Nummer, Farbe (davor das Material, wenn es nicht schon in der Bezeichnung steht), Hersteller und
Bezeichnung, wann die Spule geöffnet wurde, und ein QR-Code mit der Nummer. Bei ungeöffneten Spulen steht
„Geöffnet“ mit einem Strich zum Eintragen von Hand.

- **Brother QL per USB** (Mac, z.B. QL-570): FilMaNH druckt direkt, ohne Treiber. Unter **Format** stehen alle
  Rollen, die der Drucker kann; die eingelegte ist markiert. Passt das gewählte Format nicht zur eingelegten Rolle,
  sagt FilMaNH das und druckt nicht; nach dem Wechsel **Erneut prüfen**. Das Etikett passt sich dem Format an, die
  Vorschau zeigt genau das Druckbild.
- **Systemdialog:** für andere Etikettendrucker (Brother über den Treiber, Dymo, Niimbot, Phomemo) und A4-Bögen,
  mit Vorlagen für gängige Größen. Unter Windows geht jeder Etikettendruck über den Systemdialog.

**Anzahl je Spule** druckt mehrere gleiche Etiketten. FilMaNH merkt sich, welche Spulen ein Etikett haben.

### Feuchte

PETG, PCTG und PET zeigen nach 30 Tagen offen einen Hinweis, TPU nach 14 Tagen, PA, PC, PVA und BVOH nach 7 Tagen.
**Getrocknet** setzt die Zeit zurück.

## 6. Drucker

![Drucker](bilder/10-drucker.png)

Der laufende Druck in 3D – der schon gedruckte Teil ist grün –, dazu Fortschritt, Schicht, Restzeit und Uhrzeit des
Endes. **angepasst** heißt: Dieser Drucker braucht erfahrungsgemäß länger oder kürzer, als er anzeigt, und FilMaNH
rechnet das ein. Das geschieht erst ab drei Drucken und nur, wenn es nachweislich genauer ist.

Beim Druckstart prüft FilMaNH:

- **Falsches Material oder andere Farbe** als in der Druckdatei vorgesehen. **Ignorieren** blendet den Hinweis für
  diesen Druck überall aus.
- **Spule reicht nicht:** mit Uhrzeit, wann sie leer wird, und ob eine Ersatzspule im AMS steckt.

![AMS](bilder/11-drucker-ams.png)

Weiter unten: das AMS mit Slots, Feuchte und Temperatur, der Feuchteverlauf der letzten 7 Tage und die externe
Spule. H2D und H2C haben zwei externe Halter (links und rechts); ein leerer, nicht zugeordneter wird nicht gezeigt. Eine Spule aus **Spulen im Regal** auf einen Slot ziehen ordnet sie zu. Darunter stehen alle Drucke dieses
Druckers. **Einrichtung** oben rechts führt zu den Druckereinstellungen.

### Spule zuordnen

![Spule zuordnen](bilder/12-zuordnen.png)

Steckt eine Spule ohne RFID im Slot, fragt FilMaNH, welche es ist: oben die passenden, darunter alle weiteren.
Ein Klick auf den Slot öffnet die Auswahl jederzeit wieder, z.B. nach einem Spulenwechsel.

## 7. Druckdatei prüfen

![Druckdatei prüfen](bilder/13-druckdatei.png)

Vor dem Druck klären, ob das Filament reicht: In Bambu Studio die geslicte Platte als `.gcode.3mf` exportieren und
auf das FilMaNH-Fenster ziehen oder über **Druckdatei prüfen** auswählen. FilMaNH zeigt je Filament, welche
Spulen reichen, und schätzt die Kosten (Material, Strom, Maschine). Reicht keine Spule allein, aber zwei gleiche
zusammen, steht **reicht zusammen** mit beiden Nummern.

## 8. Verlauf

![Verlauf](bilder/14-verlauf.png)

Jeder Druck mit Bild, Drucker, Uhrzeit, Dauer, Verbrauch und Kosten; gibt es ein Foto vom fertigen Teil, steht es
statt der Vorschau. Filter nach Zeitraum, Ergebnis und Drucker, Suche, Brutto oder Netto. **CSV** exportiert die
Liste. Unten blättern, wahlweise **10**, **25** oder **50 je Seite**.

**Löschen:** Drucke anhaken (das Kästchen über der Liste wählt alle der Seite), dann **Löschen** und **Wirklich
löschen**. Eintrag, Druckdatei, Foto und Zeitraffer verschwinden; der Verbrauch bleibt auf den Spulen gebucht.
Laufende Drucke lassen sich nicht löschen.

### Druck im Detail

![Druck](bilder/15-druck.png)

- **Foto:** das letzte Bild des Zeitraffers, wenn beim Senden des Drucks „Zeitraffer“ eingeschaltet war. Ohne
  Zeitraffer das letzte Bild der Kameraaufzeichnung, falls der Drucker während des Drucks aufzeichnet (z.B. P2S).
  Gibt es beides nicht, kannst du ein eigenes Foto hinzufügen. **3D** und **Bild** zeigen die Druckdatei.
- **Zeitraffer** abspielen. Mit **Zeitraffer herunterladen** (Einstellungen › Erfassung) liegt er nach dem Druck auf
  dem Rechner, sonst kommt er beim Abspielen vom Drucker. **Speichern …** sichert ihn; auf dem Mac wird ein AVI dabei
  zu einer `.mov`, die QuickTime abspielt. War der Zeitraffer beim Drucken aus, steht das hier.
- **Filament** je Spule mit Menge und Kosten; **Kosten** aufgeschlüsselt nach Material, Strom und Maschine, netto
  und brutto.
- **In Bambu Studio öffnen** öffnet die aufbewahrte Druckdatei. Stammt das Modell von MakerWorld, führt ein Link
  dorthin.
- Menü **…**: Foto ersetzen, **Als Ausschuss markieren** (Teil unbrauchbar – zählt in der Auswertung als Fehldruck),
  Buchung zurücknehmen und, solange nicht gebucht ist, **Druckdatei neu suchen**.
- Jede Druckdatei prüft FilMaNH am Inhalt: Schichtzahl und die Filamente, die der Drucker tatsächlich nutzt. Eine
  ältere Datei gleichen Namens wird so nicht verwendet.
- **Nicht gebucht – Spule wählen.** erscheint, wenn der Drucker für ein Filament keinen Slot gemeldet hat. Die Spule
  wählst du selbst; FilMaNH rät sie nicht.
- Bei Abbrüchen steht die Meldung des Druckers dabei.

### Ende offen

![Ende offen](bilder/16-druck-offen.png)

Konnte FilMaNH das Ende eines Drucks nicht beobachten und auch später nicht sicher klären: **Fertig gedruckt**
oder **Abgebrochen …** mit der Schicht wählen. Danach wird gebucht.

## 9. Modelle

![Modelle](bilder/17-modelle.png)

Alle Drucke nach Modell zusammengefasst, mit Anzahl, Kosten und Abbrüchen.

![Modell](bilder/18-modell.png)

Kosten je Druck, Material, Erfolgsquote und alle Drucke des Modells. Unter **Quelldateien** lässt sich die
Projektdatei (`.3mf`) anhängen; FilMaNH schlägt dafür die zuletzt in Bambu Studio geöffneten Dateien vor.

## 10. Auswertung

![Auswertung](bilder/19-auswertung.png)

Drucke, Filament, Kosten und Ausschuss (abgebrochene und als Ausschuss markierte Drucke), Kosten je Monat, je
Material und je Drucker, Abbruchgründe und die teuersten Modelle. Filter nach Drucker und Zeitraum, Brutto oder Netto.

## 11. Einkauf

![Einkauf](bilder/20-einkauf.png)

Für ein Filament einen **Mindestbestand** festlegen (hier oder unter Spule › Bearbeiten). Fällt der Bestand
darunter, steht es unter **Nachkaufen**, mit Händler und letztem Preis. **Gekauft** legt die neue Spule mit den
Daten des letzten Kaufs an. **Liste kopieren** kopiert die Einkaufsliste. Sterne zeigen deine Bewertung des
Filaments.

## 12. Einstellungen

**Allgemein:** Darstellung (hell, dunkel, wie das System), **Hintergrundbild**, Sprache (Deutsch, English), Weiterlaufen beim Schließen,
Start mit dem Rechner (empfohlen), Mitteilungen (Druck fertig, Spule reicht nicht, neue Spule erkannt).

**Drucker:** verbundene Drucker; weitere Drucker suchen oder per IP-Adresse hinzufügen.

![Drucker-Einstellungen](bilder/22-einst-drucker.png)

**Kosten:** Währung, Mehrwertsteuer, Anzeige brutto oder netto, Strompreis je kWh. Unter **Eigene Werte je Drucker**
lassen sich die Leistung beim Drucken und ein Maschinenstundensatz eintragen. Ohne eigenen Wert rechnet FilMaNH mit
Bambus gemessenem Durchschnitt für das Modell und das Material des Drucks (z.B. A1 mini mit PLA 80 W, P2S 200 W) –
nicht mit der Höchstleistung, die der Drucker nur kurz beim Aufheizen braucht.

![Kosten](bilder/23-einst-kosten.png)

**Erfassung:** Grenze für „fast leer“, Korrektur aus Wiegungen lernen, Bambu-Spulen mit RFID automatisch anlegen,
Druckdateien aufbewahren (Datei und Bild, oder nur Bild), Zeitraffer herunterladen und wie viel Platz Druckdateien
und Zeitraffer höchstens belegen.

![Erfassung](bilder/24-einst-erfassung.png)

- **Zeitraffer herunterladen:** einmal nach dem Druck, sobald der Drucker ihn fertig geschrieben hat. Foto,
  Abspielen und Speichern brauchen dann den Drucker nicht mehr.
- **Druckdateien aus Bambu Studio übernehmen:** Druckst du aus Bambu Studio auf diesem Rechner, legt Bambu Studio
  die Druckdatei kurz ab, und FilMaNH übernimmt sie. So wird auch gebucht, wenn der Drucker die Datei nicht
  herausgibt. Einzurichten ist nichts.

**iPhone:** Verbindung zur FilMaNH-App auf dem iPhone (aus ab Werk; die App erscheint demnächst im App Store).
**QR-Code zeigen** öffnet das Koppeln: In der App **Mit Rechner koppeln** antippen und den Code scannen. Die
Verbindung bleibt im Heimnetz und ist verschlüsselt; gekoppelte iPhones lassen sich hier wieder **Entfernen**. Beim
ersten Einschalten fragen macOS bzw. Windows, ob FilMaNH Verbindungen annehmen darf: **Erlauben** (unter Windows für
private Netzwerke).

![iPhone](bilder/28-einst-iphone.png)

![iPhone koppeln](bilder/29-iphone-koppeln.png)

Der Bereich gilt für iPhone und Android. Was die Apps können, steht in den Handbüchern für [iPhone](iphone.md) und
[Android](android.md).

**Daten:** tägliche Sicherung (die letzten 14 Stände), Export und Import aller Daten, Druckverlauf als CSV, Datenordner. Sicherung und Export enthalten die Datenbank: Spulen, Buchungen,
Drucke und Einstellungen – nicht Fotos, Druckdateien, 3D-Ansichten, Zeitraffer und Quelldateien. Die liegen im
Datenordner (`drucke`, `modelle`); wer umzieht, kopiert ihn mit. **Aus Spoolman übernehmen** liest Spulen aus einem
Spoolman-Server oder einer Spoolman-Exportdatei.

![Daten](bilder/25-einst-daten.png)

**Über FilMaNH:** Version, Filament-Katalog aktualisieren, Updates, **Diagnose › Kopieren** (für die Hilfe, ohne
Seriennummern, Adressen und Codes), Lizenzen. Die installierte Version steht auch oben in der Seitenleiste; ist
ein Update da, wird sie rot.

![Über FilMaNH](bilder/26-einst-ueber.png)

**Updates:** FilMaNH sucht stündlich nach einer neuen Version. Gibt es eine, steht **Update …** in der Seitenleiste;
ein Klick auf **Version … installieren** lädt, prüft, installiert und startet neu. Ohne Klick wird nichts
installiert.

## 13. Im Hintergrund

Das Fenster zu schließen beendet FilMaNH nicht – Drucke werden weiter verfolgt.

- **macOS:** Symbol oben rechts in der Menüleiste, während eines Drucks mit Fortschritt. Ganz beenden mit ⌘Q oder
  **Beenden** im Menü des Symbols.
- **Windows:** Symbol unten rechts im Infobereich. Windows 11 legt neue Symbole zunächst unter den Pfeil **^**; von
  dort lässt es sich auf die Taskleiste ziehen. Ganz beenden mit **Beenden** im Menü des Symbols (Rechtsklick).

Mit **Mit dem Rechner starten** (Einstellungen › Allgemein) läuft FilMaNH nach dem Hochfahren gleich im Hintergrund.

## 14. Tastatur und Scanner

![Befehle](bilder/27-befehle.png)

- **⌘K** (Mac) bzw. **Strg+K** (Windows): Suche nach Spulen, Drucken, Modellen und Befehlen.
- Eine `.gcode.3mf` auf das Fenster ziehen: Druckdatei prüfen.
- Ein Barcodescanner, der den QR-Code eines FilMaNH-Etiketts liest, öffnet direkt die Spule.
- Scannt er die EAN einer Spule oder ihres Kartons, öffnet sich **Neue Spule** – bei einer bekannten EAN mit dem
  Filament schon gewählt.

## 15. Daten und Datenschutz

- Alle Daten liegen auf deinem Rechner, auch Druckdateien, Fotos und Zeitraffer, im Datenordner der App
  (Einstellungen › Daten › **Datenordner** › **Öffnen**).
- Mit **Druckdateien aus Bambu Studio übernehmen** liest FilMaNH die Druckdateien, die Bambu Studio beim Drucken
  auf diesem Rechner ablegt – nichts sonst.
- Kein Konto, keine Cloud. FilMaNH liest die Drucker nur aus und steuert sie nicht. Zugangscodes liegen im
  Schlüsselbund des Systems.
- Ist die **Verbindung zum iPhone** eingeschaltet, nimmt FilMaNH im Heimnetz verschlüsselte Verbindungen von
  gekoppelten iPhones an (Port 47474). Ins Internet geht dabei nichts.
- Ins Internet geht FilMaNH nur für die Update-Suche, die Katalog-Aktualisierung (auf Klick), einen
  Spoolman-Import, wenn du einen startest, und für einen Shop-Link, wenn du einen einfügst (dann ruft FilMaNH genau
  diese Seite ab).

Die vollständige Datenschutzerklärung für Programm und Apps: [DATENSCHUTZ.md](../DATENSCHUTZ.md).

## 16. Häufige Fragen

**Der Drucker wird nicht gefunden.** Drucker eingeschaltet und im selben Netzwerk? Liegt er in einem anderen Netz,
unter Einstellungen › Drucker das Netz („auch in Netz“) oder die IP-Adresse eingeben. Ist schon ein Drucker aus
diesem Netz eingerichtet, sucht FilMaNH dort von selbst mit.

**Bei einem Drucker steht „verbinde …“, obwohl er an ist.** Drucker nehmen nur wenige direkte Verbindungen aus dem
Netzwerk gleichzeitig an. Dazu zählen auch Bambu Studio oder Orca Slicer (wenn sie direkt mit dem Drucker verbunden
sind), Home Assistant und ähnliche Programme – die Bambu-Handy-App nicht, sie läuft über Bambus Cloud. FilMaNH
versucht es selbst weiter und holt den Druck nach, sobald es wieder verbunden ist; der Druck wird dadurch nicht
gestört. Bleibt es dabei, ein anderes verbundenes Programm schließen oder die Firmware des Druckers aktualisieren.

**Muss ich am Drucker den LAN-Modus oder Entwicklermodus einschalten?** Nein.

**Der Bestand stimmt nicht.** Spule wiegen. Mit der Zeit lernt FilMaNH aus den Wiegungen und rechnet genauer.

**Der Rechner war während eines Drucks aus.** FilMaNH holt den Druck beim nächsten Start nach.

**Wie bekomme ich ein Foto vom fertigen Teil?** Beim Senden des Drucks in Bambu Studio den Zeitraffer einschalten –
das gilt für jeden Druck einzeln (**Druckplatte drucken › Zeitraffer**).
Zeichnet der Drucker mit der Kamera auf, kommt das Foto auch ohne Zeitraffer. Sonst ein eigenes Foto im Druck
hinzufügen.

**Etwas funktioniert nicht.** Auf GitHub unter [Issues](https://github.com/NikolausH76/FilMaNH/issues/new/choose) das
Formular **Fehler melden / Report a bug** ausfüllen. Hilfreich ist die Diagnose: in der App unter Einstellungen ›
Über FilMaNH › **Diagnose** › **Kopieren**, dann in das Formular einfügen – ohne Seriennummern, Adressen und Codes.

---

© 2026 N. Hass. FilMaNH ist ein unabhängiges Projekt und nicht mit Bambu Lab verbunden.
