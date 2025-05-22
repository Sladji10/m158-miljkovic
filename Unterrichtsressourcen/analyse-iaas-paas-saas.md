# Analyse: IaaS, PaaS, SaaS vs. On-Premises

## Einleitung

Cloud-Computing-Modelle wie **IaaS**, **PaaS** und **SaaS** bieten unterschiedliche Ebenen an IT-Services, die Unternehmen nutzen können – im Gegensatz zu klassischen **On-Premises**-Lösungen, bei denen alles im eigenen Rechenzentrum betrieben wird. Zwei Diagramme stellen diese Modelle auf unterschiedliche Weise dar. Ziel dieser Analyse ist es, Gemeinsamkeiten und Unterschiede dieser Darstellungen zu erkennen, Schwerpunkte zu identifizieren und beide in Beziehung zueinander zu setzen.

## 1. Gemeinsamkeiten und Unterschiede

### Gemeinsamkeiten:
- **Alle Modelle** zeigen eine Abstraktion von IT-Komponenten wie Netzwerk, Speicher, Server, Betriebssysteme, Middleware, Daten und Anwendungen.
- **Vergleichbarkeit der Verantwortung**: Beide Diagramme machen deutlich, wer für welche Schichten der IT-Infrastruktur verantwortlich ist (Kunde vs. Anbieter).
- **Abgrenzung On-Prem vs. Cloud**: Beide betonen den Übergang von vollständiger Eigenverantwortung (On-Premises) zur vollständigen Dienstnutzung (SaaS).

### Unterschiede:
| Aspekt                   | Diagramm 1                                     | Diagramm 2                                      |
|--------------------------|------------------------------------------------|-------------------------------------------------|
| Darstellung              | Stufenmodell mit Farben                        | Balkendiagramm (Schichtenmodell)                |
| Schwerpunkt              | Wer übernimmt Verantwortung                    | Technische Komponenten nach Stack-Ebene         |
| Detailgrad               | Höherer Fokus auf Nutzerverantwortung          | Detailliertere Darstellung einzelner Komponenten |
| Perspektive              | Fokus auf Services als Pakete                  | Fokus auf technische Architektur (Stack)        |

---

## 2. Unterschiedliche Schwerpunkte

- **Diagramm 1** hebt hervor, **welcher Anteil der IT durch den Anbieter übernommen wird**. Es zeigt: Je weiter man Richtung SaaS geht, desto weniger muss der Nutzer selbst verwalten.
- **Diagramm 2** betont die **technischen Komponenten** und deren Abdeckung durch die einzelnen Modelle. Es visualisiert, welche konkreten Elemente in PaaS/IaaS enthalten sind (zB. Runtime, Middleware etc.).

---

## 3. Verknüpfung der Diagramme

Die Inhalte lassen sich wie folgt verknüpfen:

- Diagramm 1 zeigt den **Grad der Verantwortung** (Nutzer vs. Anbieter), während Diagramm 2 erklärt, **was genau** übernommen wird (technisch).
- Man kann die **Layer aus Diagramm 2** (wie Runtime oder Storage) den jeweiligen **Verantwortlichkeitsstufen in Diagramm 1** zuordnen.
- Ein gemeinsames Verständnis entsteht, wenn man **beide kombiniert**: 
  - Wer ist zuständig? (Diagramm 1) 
  - Für welche Schicht genau? (Diagramm 2)

---

## Fazit

Die beiden Diagramme ergänzen sich in idealer Weise: Das erste zeigt **die Verteilung der Zuständigkeiten** zwischen Kunde und Anbieter, das zweite zeigt **die technologische Tiefe** der verschiedenen Modelle. Durch die Kombination beider Darstellungen erhält man ein vollständiges Bild darüber, was IaaS, PaaS und SaaS im Vergleich zu On-Premises bedeuten – sowohl in Bezug auf Verantwortung als auch technische Komponenten.
