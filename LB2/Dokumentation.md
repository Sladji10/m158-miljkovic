# Projektdokumentation – M158 LB2 WordPress-Migration

## Aufgabe 1 – Projektplan erstellen

```mermaid
%%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryTextColor': '#000000'
    }
  }
}%%

gantt
    dateFormat  DD-MM-YYYY
    axisFormat  %d-%m-%Y
    title       WordPress Migration Projektplan M158
    excludes    weekends

    section Planung
    Projektplan erstellen       :a1, 15-05-2025, 4d
    Architekturdiagramm         :a2, after a1, 3d
    Testkatalog erstellen       :a3, after a2, 2d
    Dokumentation schreiben     :a4, after a3, 2d

    section Umgebung
    Ubuntu WSL installieren     :b1, after a4, 3d
    NGINX, MySQL, PHP Setup     :b2, after b1, 3d
    Hosts-Datei anpassen        :b3, after b2, 1d

    section Zielsystem
    Webserver konfigurieren     :c1, after b3, 3d
    Datenbank einrichten        :c2, after c1, 3d
    Adminer installieren        :c3, after c2, 1d
    SSL optional               :c4, after c3, 1d

    section Migration
    Backup herunterladen        :d1, after c4, 2d
    Backup importieren          :d2, after d1, 2d
    wp-config.php anpassen      :d3, after d2, 1d

    section Tests
    Tests durchführen           :e1, after d3, 4d
    Health Check                :e2, after e1, 1d
    Backup Automatisieren       :e3, after e2, 2d

```

## Aufgabe 2 – Architekturdiagramm erstellen

<img src="https://github.com/Sladji10/m158-miljkovic/blob/main/LB2/Screenshots_Beweise/Architekturdiagramm_Sladjan.drawio.png?raw=true" width="750" />

## Aufgabe 3 – AWS-Umgebung einrichten

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 4 – DNS-Konfiguration

Ändern Sie die Stufe, für die Sie sich entschieden haben, selbst.

### Stufe ?

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 5 – Webserver konfigurieren

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 6 – PHP einrichten

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 7 – MySQL/MariaDB aufsetzen

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 8 – Web-Datenbanktool (phpMyAdmin/Adminer)

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 9 – FTP-Zugang einrichten

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 10 – WordPress migrieren

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 11 – Backup-Konzept umsetzen

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 12 – Testing der Webapplikation

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 13 – Deployment automatisieren

### Stufe 1

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 2

Fügen Sie hier Ihre Ergebnisse ein

### Stufe 3

Fügen Sie hier Ihre Ergebnisse ein

---

## Aufgabe 14 – Docker verwenden

### Stufe 1 - 3

Fügen Sie hier Ihre Ergebnisse ein

---

