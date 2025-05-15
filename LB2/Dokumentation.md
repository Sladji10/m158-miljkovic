## Sladjan Miljkovic M158 LB2 

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
