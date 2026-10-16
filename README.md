# SpeakUp! – Plattform zur Meldung von Diskriminierungsvorfällen

Webplattform, über die Betroffene und Zeug:innen Diskriminierungsvorfälle anonym melden können. Entwickelt 2026 im Rahmen des Softwareentwicklungsprojekts an der HTW Berlin für den Verein **ZAkï e.V.**

> Dieses Repository ist eine Projektübersicht. Der Quellcode ist ein Teamprojekt und liegt im internen GitLab der HTW Berlin.

## Funktionen

- **Meldung per Formular oder Sprache:** Vorfälle können getippt oder eingesprochen werden.
- **Spracherkennung in Echtzeit:** lokal betriebenes Whisper-Modell (Python), damit keine Audiodaten an Dritte gehen.
- **KI-gestützte Auswertung:** Die Mistral API (EU-Anbieter) kategorisiert und fasst Meldungen automatisch zusammen.
- **Kartenansicht:** Visualisierung der Meldungen mit Leaflet.js und OpenStreetMap.
- **Datenschutz:** DSGVO-konforme, anonymisierte Speicherung der Meldungen.

## Tech-Stack

| Bereich | Technologie |
|---|---|
| Frontend | React.js, Leaflet.js, OpenStreetMap |
| Backend | Python, Django, Django REST Framework |
| Datenbank | MySQL |
| KI | Mistral API (LLM), Whisper (Speech-to-Text, lokal) |

## Architektur

```
React-Frontend  ──REST──▶  Django REST API  ──▶  MySQL
      │                        │
  Leaflet/OSM-Karte            ├──▶ Whisper (lokal): Audio → Text
                               └──▶ Mistral API: Kategorisierung & Zusammenfassung
```

## Mein Beitrag

Teamprojekt mit 3 Personen. Ich habe das Backend und die KI-Funktionen verantwortet:

- **Backend:** Aufbau der REST-API mit Django und Django REST Framework
- **KI-Analyse:** Anbindung der Mistral API zur automatischen Kategorisierung und Zusammenfassung von Meldungen
- **Sprache-zu-Text:** Integration eines lokal betriebenen Whisper-Modells, damit Meldungen auch eingesprochen werden können

## Kontakt

Ahmed Al-Amwi · Student der Ingenieurinformatik (B.Eng.), HTW Berlin
