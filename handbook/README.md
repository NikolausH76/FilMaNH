# FilMaNH – User guide

*[Deutsch](../handbuch/README.md) · English*

FilMaNH keeps track of your filament spools and deducts what every print uses, automatically. It runs locally on
your computer and only reads from the Bambu Lab printers on your network.

1. [Installation](#1-installation)
2. [First setup](#2-first-setup)
3. [How FilMaNH works](#3-how-filmanh-works)
4. [Overview](#4-overview)
5. [Spools](#5-spools)
6. [Printers](#6-printers)
7. [Check print file](#7-check-print-file)
8. [History](#8-history)
9. [Models](#9-models)
10. [Statistics](#10-statistics)
11. [Shopping list](#11-shopping-list)
12. [Settings](#12-settings)
13. [Running in the background](#13-running-in-the-background)
14. [Keyboard and scanner](#14-keyboard-and-scanner)
15. [Data and privacy](#15-data-and-privacy)
16. [FAQ](#16-faq)

---

## 1. Installation

Download from [Releases](https://github.com/NikolausH76/FilMaNH/releases/latest).

**macOS** (Apple Silicon and Intel): open `FilMaNH_…_universal.dmg` and drag FilMaNH into “Applications”. On first
launch macOS warns you because the app is not registered with Apple: choose “Done”, then
**System Settings › Privacy & Security › Open Anyway**.

**Windows 10/11** (64-bit): run `FilMaNH_…_x64-setup.exe`. If you see “Windows protected your PC”:
**More info › Run anyway**. No administrator rights needed.

Your computer and printers need to be on the same network. Nothing has to be changed on the printer.

## 2. First setup

On first launch FilMaNH searches your network for printers and asks for each one whether to add it.

![Printer found](images/02-setup-suche.png)

- **Access code:** If Bambu Studio is set up on the computer, FilMaNH takes the code from there. Otherwise you find
  it on the printer under **Settings › WLAN**.
- **No printer found:** If the printer is on a different subnet (e.g. a separate network for smart-home devices),
  enter that subnet like `192.168.2` or the printer’s IP address.

Next, FilMaNH asks what to do with prints that are already on the SD card:

![Prints on the SD card](images/03-setup-karte.png)

- **Start from now:** older prints are left out.
- **Add earlier prints to the history:** they show up in History and Models, but nothing is deducted from spools.

**Set up later** skips the setup; you can add printers any time under Settings › Printers.

## 3. How FilMaNH works

- Every spool has a number (#001, #002 …) and a remaining amount.
- A spool in the AMS or on the external holder is assigned to that slot. **Bambu spools with RFID** are created
  automatically when loaded. For any other spool FilMaNH asks once which spool it is.
- **When a print ends**, FilMaNH reads from the print file how much filament each slot used and deducts it from
  the spool, including the flushing for colour changes. If a print is cancelled, only the layers actually printed
  are deducted.
- **If your computer was off**, FilMaNH catches up on the next start with whatever the printer did in the meantime.
  Anything it cannot settle for sure appears as a notice that you confirm with one click.
- **Weighing** makes the stock exact. From your weighings FilMaNH learns how far the real consumption of each
  filament differs from the calculation and takes that into account from then on.
- **“~”** in front of a weight means estimated, may be slightly off. Weighing makes it exact again.

## 4. Overview

![Overview](images/01-uebersicht.png)

- **Notices** at the top show what needs your attention: wrong material in a slot, a print whose end is unknown,
  an unassigned spool, moisture, almost empty spools. The matching action sits right next to each one.
- **Printers** with status, current print, remaining time and the slots with their remaining amount. Click to open
  the printer.
- **Recently printed** with costs.

## 5. Spools

![Spools](images/05-spulen.png)

Filter by state (Full, Opened, Almost empty, Empty, Archive), material, brand and location; search; grid or list
view. **Labels** prints labels for all spools shown.

### New spool

![New spool](images/04-neue-spule.png)

Type brand, material or colour into the search field, e.g. “sunlu petg white”. The catalog knows more than 7,000
filaments; picking one fills in colour, net weight and empty spool weight. Optionally add the price (gross or net),
location and **Quantity**: 3 creates three spools, each with its own number. If a filament is not in the catalog:
**Without catalog** and enter it yourself.

Bambu spools with RFID don’t need to be created – just load them.

### Spool details

![Spool](images/06-spule.png)

Remaining amount, location (slot or shelf), material, price, moisture and every deduction in the history. **More**
shows batch, accuracy, learned correction, minimum stock and note. **Use up the rest** lists models you have
printed before that the remaining filament is still enough for.

![Spool menu](images/07-spule-mehr.png)

In the **…** menu: Edit, Correct remaining, Change location, Another spool like this, Print label, Add photo and
Archive. A **photo** of the spool shows its real colour in the centre of the ring.

### Weigh

![Weigh](images/08-wiegen.png)

Weigh the spool including the reel and enter the weight. FilMaNH subtracts the empty spool weight and takes over
the rest.

### Labels

![Labels](images/09-etiketten.png)

Number, colour, material and QR code – for label printers (Brother, Dymo, Niimbot, Phomemo) or A4 sheets.

### Moisture

PETG, PCTG and PET show a notice after 30 days open, TPU after 14 days, PA, PC, PVA and BVOH after 7 days.
**Dried** resets the time.

## 6. Printers

![Printer](images/10-drucker.png)

The current print in 3D – the part already printed is green – plus progress, layer, remaining time and when it
will be done. **adjusted** means: this printer usually takes longer or shorter than it shows, and FilMaNH takes
that into account. This only happens after three prints and only if it is measurably more accurate.

When a print starts, FilMaNH checks:

- **Wrong material or different colour** than the print file expects.
- **Spool will run out:** with the time it will be empty and whether a spare spool is in the AMS.

![AMS](images/11-drucker-ams.png)

Further down: the AMS with its slots, humidity and temperature, the humidity of the last 7 days and the external
spool. Drag a spool from **Spools on the shelf** onto a slot to assign it. Below are all prints of this printer.
**Setup** at the top right opens the printer settings.

### Assign a spool

![Assign spool](images/12-zuordnen.png)

When a spool without RFID is loaded, FilMaNH asks which one it is: matching spools first, all others below.
Clicking the slot opens the selection again at any time, e.g. after changing spools.

## 7. Check print file

![Check print file](images/13-druckdatei.png)

Find out before printing whether the filament is enough: in Bambu Studio export the sliced plate as `.gcode.3mf`
and drop it onto the FilMaNH window or choose it via **Check print file**. FilMaNH shows for each filament which
spools are enough and estimates the cost (material, electricity, machine).

## 8. History

![History](images/14-verlauf.png)

Every print with image, printer, time, duration, consumption and cost. Filter by period, result and printer;
search; gross or net. **CSV** exports the list.

### Print details

![Print](images/15-druck.png)

- **Photo:** the last frame of the timelapse – provided “Timelapse” was switched on when sending the print. Without
  a timelapse you can add your own photo. **3D** and **Image** show the print file.
- **Play timelapse** straight from the printer.
- **Filament** per spool with amount and cost; **Costs** broken down into material, electricity and machine, net
  and gross.
- **Open in Bambu Studio** opens the kept print file. If the model comes from MakerWorld, a link leads there.
- **…** menu: Replace photo, Undo deduction.
- For cancelled prints the printer’s message is shown.

### End unknown

![End unknown](images/16-druck-offen.png)

If FilMaNH could not see a print end and could not settle it later either: choose **Finished** or **Cancelled …**
with the layer. The deduction follows.

## 9. Models

![Models](images/17-modelle.png)

All prints grouped by model, with count, cost and cancellations.

![Model](images/18-modell.png)

Cost per print, material, success rate and all prints of the model. Under **Source files** you can attach the
project file (`.3mf`); FilMaNH suggests the files recently opened in Bambu Studio.

## 10. Statistics

![Statistics](images/19-auswertung.png)

Prints, filament, costs and waste (cost of cancelled prints), costs per month, per material and per printer,
reasons for cancellation and the most expensive models. Filter by printer and period, gross or net.

## 11. Shopping list

![Shopping list](images/20-einkauf.png)

Set a **Minimum stock** for a filament (here or under Spool › Edit). When the stock falls below it, the filament is
listed under **Reorder** with shop and last price. **Purchased** creates the new spool with the data of the last
purchase. **Copy list** copies the shopping list.

## 12. Settings

**General:** Appearance (light, dark, system), Language (Deutsch, English), Keep running when closed, Launch at
login, Notifications (print finished, spool will run out, new spool detected).

**Printers:** connected printers, their power in watts and the machine hourly rate for cost calculation; search
for more printers or add one by IP address.

![Printer settings](images/22-einst-drucker.png)

**Costs:** currency, VAT, show prices gross or net, electricity price per kWh.

![Costs](images/23-einst-kosten.png)

**Tracking:** threshold for “almost empty”, learn correction from weighings, create Bambu spools with RFID
automatically, keep print files (file and image, or image only) and the maximum space they may use.

**Data:** daily backup (the last 14), export and import of all data, print history as CSV, data folder.
**Import from Spoolman** reads spools from a Spoolman server or a Spoolman export file.

![Data](images/25-einst-daten.png)

**About FilMaNH:** version, update the filament catalog, updates, licenses.

![About FilMaNH](images/26-einst-ueber.png)

**Updates:** FilMaNH checks for a new version every hour. If there is one, **Update …** appears in the sidebar;
**Install version …** downloads, verifies, installs and restarts. Nothing is installed without your click.

## 13. Running in the background

Closing the window doesn’t quit FilMaNH – prints keep being tracked.

- **macOS:** icon at the top right of the menu bar, showing progress during a print. Quit completely with ⌘Q or
  **Quit** in the icon’s menu.
- **Windows:** icon at the bottom right in the notification area. Windows 11 first puts new icons under the **^**
  arrow; you can drag it from there onto the taskbar. Quit completely with **Quit** in the icon’s menu (right-click).

With **Launch at login** (Settings › General) FilMaNH starts in the background right after you log in.

## 14. Keyboard and scanner

![Commands](images/27-befehle.png)

- **⌘K** (Mac) or **Ctrl+K** (Windows): search spools, prints, models and commands.
- Drop a `.gcode.3mf` onto the window: check print file.
- A barcode scanner reading the QR code of a FilMaNH label opens that spool directly.

## 15. Data and privacy

- All data stays on your computer:
  macOS `~/Library/Application Support/de.nikolaushass.filmanh`, Windows `%APPDATA%\de.nikolaushass.filmanh`.
- No account, no cloud. FilMaNH only reads from the printers and never controls them. Access codes are stored in
  the system keychain.
- FilMaNH only goes online to check for updates, to update the catalog (when you click) and for a Spoolman import
  if you start one.

## 16. FAQ

**The printer isn’t found.** Is it switched on and on the same network? If it is on a different subnet, enter the
subnet (“also in subnet”) or the IP address under Settings › Printers.

**Do I have to switch on LAN-only mode or developer mode on the printer?** No.

**The stock is off.** Weigh the spool. Over time FilMaNH learns from your weighings and calculates more precisely.

**My computer was off during a print.** FilMaNH catches up on the print at the next start.

**How do I get a photo of the finished part?** Switch on the timelapse in Bambu Studio when sending the print.
Otherwise add your own photo in the print details.

---

© 2026 Nikolaus Hass. FilMaNH is an independent project and not affiliated with Bambu Lab.
