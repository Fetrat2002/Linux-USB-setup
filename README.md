# Ubuntu Dual-Boot Installation mit bootfähigem USB-Stick

## Projektübersicht

In diesem Projekt wurde ein bootfähiger USB-Stick erstellt, um Ubuntu Linux neben Windows auf einem Desktop-PC zu installieren. Ziel war es, praktische Erfahrungen mit Linux, BIOS/UEFI, Bootloadern und Betriebssysteminstallation zu sammeln.

---

# Ziel des Projekts

- Erstellung eines bootfähigen Ubuntu-USB-Sticks
- Installation von Ubuntu Linux
- Einrichtung eines Dual-Boot-Systems mit Windows
- Verständnis von BIOS/UEFI und Boot-Menüs
- Grundlagen von Linux und Systemadministration lernen

---

# Verwendete Hardware

- HP Pavilion Gaming Desktop
- AMD Ryzen 7 2700
- 16 GB RAM
- Samsung SSD 980 PRO 2TB
- Philips USB-Stick 64 GB

---

# Verwendete Software

- Windows
- Ubuntu 26.04 LTS ISO
- Rufus Portable
- GRUB Bootloader

---

# Projektablauf

## 1. USB-Stick vorbereiten

Zunächst wurde ein 64-GB-USB-Stick an den Windows-PC angeschlossen.

---

## 2. Ubuntu herunterladen

Die Ubuntu-ISO-Datei wurde von der offiziellen Ubuntu-Webseite heruntergeladen.

Verwendete Version:

Ubuntu 26.04 LTS (Intel/AMD)

---

## 3. Rufus herunterladen

Zur Erstellung des bootfähigen Mediums wurde Rufus Portable verwendet.

---

## 4. Bootfähigen USB-Stick erstellen

In Rufus wurden folgende Einstellungen vorgenommen:

### Einstellungen
- USB-Stick ausgewählt
- Ubuntu-ISO-Datei ausgewählt
- ISO-Image-Modus verwendet
- Standardpartitionierung verwendet

### Durchführung
- Warnung zur Datenlöschung bestätigt
- Schreibvorgang gestartet
- USB-Stick erfolgreich bootfähig gemacht

---

# 5. Boot-Menü aufrufen

Nach der Erstellung des USB-Sticks wurde der PC neu gestartet.

## Verwendete Tasten
- ESC → HP Startmenü
- F9 → Boot Device Options

Im Boot-Menü wurde folgendes Gerät ausgewählt:

UEFI: PHILIPS 5.00

Dadurch startete Ubuntu direkt vom USB-Stick.

---

# 6. Ubuntu installieren

Im Ubuntu-Installer wurden folgende Optionen ausgewählt:

## Installationstyp
- Interaktive Installation
- Vollständige Installation

## Zusätzliche Optionen
- Drittanbieter-Software installieren
- Unterstützung für zusätzliche Medienformate aktivieren

## Betriebssystem
- Ubuntu neben Windows installieren

---

# 7. BitLocker-Problem

Während der Installation wurde erkannt, dass Windows BitLocker verwendet.

Dadurch erschien eine Warnung bezüglich verschlüsselter Partitionen.

Trotzdem konnte Ubuntu erfolgreich neben Windows installiert werden.

---

# 8. GRUB Bootloader

Nach der Installation startete der PC zunächst automatisch in Ubuntu.

Später wurde erkannt, dass Windows weiterhin vorhanden ist und über den GRUB-Bootloader gestartet werden kann.

## Wichtiger Befehl

```bash
sudo update-grub
