# 💰 SmartSpend

Budget-App, mit der man Einnahmen und Ausgaben im Blick behält, Budgets pro Kategorie plant und auf Sparziele hinarbeitet. Teamprojekt aus dem Modul *Human-Computer Interaction* an der Hochschule Darmstadt, mit Fokus auf eine einfache, ansprechende Bedienung.

## Funktionen

- **Konto:** Registrierung und Login, Passwörter werden gehasht gespeichert
- **Budget:** Kategorien anlegen, Budgets festlegen, Einnahmen und Ausgaben erfassen, Auslastung als Kreisdiagramm
- **Übersicht:** alle Buchungen im Wallet auf einen Blick
- **Sparziele:** Ziele anlegen und den Fortschritt verfolgen
- **Spartipps:** automatische Empfehlungen auf Basis des eigenen Ausgabeverhaltens
- **Weekly Wrap:** Wochenrückblick über die Ausgaben
- **Währungsrechner:** Umrechnung mit aktuellen Wechselkursen über die [Frankfurter API](https://www.frankfurter.app)
- **Bankkarte verknüpfen:** Karte mit Kartennummer hinterlegen

## Technik

| Bereich | Umsetzung |
|---|---|
| App | **Flutter** und **Dart**, Material Design, eigenes Theme mit Glassmorphism-Effekten |
| Datenhaltung | lokale **SQLite**-Datenbank mit **Drift** (typsichere Queries, Code-Generierung) |
| Schnittstellen | REST-API für Wechselkurse (`http`) |
| Sicherheit | Passwort-Hashing mit `crypto` |
| Plattformen | Android, iOS, macOS, Linux, Windows |

## Starten

Voraussetzung: [Flutter](https://docs.flutter.dev/get-started/install)

```bash
flutter pub get
flutter run
```

Tests und statische Analyse:

```bash
flutter analyze
flutter test
```

## Projektstruktur

```
lib/
├── data/        # Datenbank (Drift)
├── models/      # Datenmodelle
├── screens/     # Bildschirme: auth, budget, overview, bank, settings, Weekly Wrap
├── services/    # Logik: Budget, Login, Wechselkurse, Spartipps
├── themes/      # Farben und Theme
├── widgets/     # Dialoge, Karten und gemeinsame UI-Bausteine
└── main.dart
```

## Team und mein Beitrag

Entstanden im Team mit drei Studierenden. Ich habe unter anderem die Karte zum Verknüpfen der Bankkarte (mit bearbeitbarer Kartennummer) gebaut, Fehler bei der Berechnung von Budget und Einnahmen behoben, an der Übersicht gearbeitet und die Projektdokumentation zu den Meilensteinen mitgeschrieben.
