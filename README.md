# Testumgebung

## Architektur
- Basissnapshot mit installiertem System, Diensten und Grundkonfiguration
- Runner 1: Schnellprüfung
- Runner 2: Detailprüfung
- Zentrale Datenbank
- Getrennte Ordner pro Testlauf

## Ablauf
1. VM aus Basissnapshot starten
2. Testinput ausführen
3. Runner 1 prüft grob
4. Ergebnis in Datenbank schreiben
5. Bei relevantem Treffer:
   - Ordner anlegen
   - Details sammeln
   - Runner 2 ausführen
   - Datenbank ergänzen

## Zweck
- schnelle Triage
- geringe Laufzeit
- saubere Trennung von Baseline, Schnellcheck und Detailanalyse

## Datenablage
Pro Testlauf:
- Input-Datei
- Hashes
- Logs
- Status
- Bewertung
