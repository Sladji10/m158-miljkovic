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

### Stufe 3

  - EC2-Instanz mit **Ubuntu 22.04** aufgesetzt

  - Zugriff per SSH mit Key-Authentifizierung funktioniert (miljkovic.pem)

  - Planung vollständig umgesetzt ***(Security Group, VPC, Subnetz, Elastic IP)***

## Aufgabe 4 – DNS-Konfiguration

### Stufe 3

  - Domainauflösung über **/etc/hosts** eingerichtet: ```34.232.75.121  miljkovic-m158.local```

## Aufgabe 5 – Webserver konfigurieren

### Stufe 3

  - Apache Virtual Host konfiguriert

  - mod_rewrite aktiviert

  - HTTP → HTTPS-Weiterleitung eingerichtet

  - Keine Apache Default Page sichtbar

## Aufgabe 6 – PHP einrichten

### Stufe 3

  - PHP 8.3 verwendet

  - php.ini angepasst (z. B. upload_max_filesize, post_max_size etc.)

  - PHP-FPM aktiviert (FastCGI Process Manager)

## Aufgabe 7 – MySQL/MariaDB aufsetzen

### Stufe 3

  - Root-Zugriff nur über localhost

  - WordPress-User mit eingeschränkten Rechten erstellt

  - Dedicated Container für MariaDB

## Aufgabe 8 – Web-Datenbanktool (phpMyAdmin/Adminer)

### Stufe 3

phpMyAdmin im eigenen Container

Erreichbar unter ```http://miljkovic-m158.local:8888```

Zugriff erfolgt über HTTPS mit selbst signiertem Zertifikat

## Aufgabe 9 – FTP-Zugang einrichten

### Stufe 3

FTPS-Zugriff eingerichtet (vsftpd + TLS)

Benutzer mit Zugriff nur auf /var/www/html und Unterverzeichnisse

Sichere Konfiguration mit verschlüsselter Übertragung

## Aufgabe 10 – WordPress migrieren

### Stufe 3

Alle Dateien nach /var/www/html kopiert, Rechte korrekt gesetzt (www-data)

Datenbank erfolgreich importiert, inkl. Anpassung von Domainnamen

wp-config.php angepasst

WP_HOME und WP_SITEURL in der Datenbank aktualisiert

Admin-Login funktioniert (Passwort ggf. via SQL auf MD5-Hash gesetzt)

## Aufgabe 11 – Backup-Konzept umsetzen

### Stufe 3

Backup-Skript mit cron eingerichtet

Datenbank- und Datei-Backup erfolgt täglich

Alte Backups werden automatisch gelöscht (Rotation)

Backup-Skript verschickt E-Mail mit msmtp (SMTP konfiguriert mit Gmail)

## Aufgabe 12 – Testing der Webapplikation

### Stufe 3

Mind. 10 spezifische Testfälle erstellt und getestet (z. B. Login, Upload, Beiträge erstellen)

Seite /wp-admin/site-health.php zeigt "Sollte verbessert werden" (min. akzeptabel)

Seite et_support_center_divi getestet (Permissions gefixt, Pfade angepasst)

## Aufgabe 13 – Deployment automatisieren

### Stufe 3

CI/CD-Pipeline mit GitLab CI erstellt

Deploy auf Staging- und Live-Umgebung bei Commit auf main bzw. staging

Automatischer docker-compose up -d --build

## Aufgabe 14 – Docker verwenden

### Stufe 3

Docker Compose verwendet

Alle Services als Container (Apache+PHP, MariaDB, phpMyAdmin, FTP, WordPress)

Volumes für Datenpersistenz, Secrets/Env-Vars für Sicherheit

