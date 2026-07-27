# Blutdruck-Trainer

**Blutdruckmessung nach der Korotkoff-Methode üben — für die Pflegeausbildung**

[![Code: MIT](https://img.shields.io/badge/Code-MIT-green.svg)](LICENSE) [![Inhalte: CC BY-SA 4.0](https://img.shields.io/badge/Inhalte-CC%20BY--SA%204.0-blue.svg)](LICENSE-CONTENT.md)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue)](https://florianloyns.github.io/blutdruck-trainer/)
![Keine Abhängigkeiten](https://img.shields.io/badge/Abh%C3%A4ngigkeiten-keine-brightgreen)
![Mobile](https://img.shields.io/badge/Mobile-optimiert-brightgreen)
![Dark Mode](https://img.shields.io/badge/Dark%20Mode-unterst%C3%BCtzt-darkblue)
![PWA](https://img.shields.io/badge/PWA-offline--f%C3%A4hig-blueviolet)

**[Jetzt üben →](https://florianloyns.github.io/blutdruck-trainer/)**

---

> Ein interaktives Lernwerkzeug für die generalistische Pflegeausbildung. Der Trainer simuliert eine realistische Blutdruckmessung mit animiertem Manometer und Korotkoff-Tönen — Lernende lesen den Wert von der Skala ab, statt ihn digital abzulesen.

---

## Was die App macht

- Animiertes Manometer mit farbigen Druckzonen (grün / gelb / rot)
- Korotkoff-Töne über den Browser (Web Audio API, synthetisiert)
- Nadel zuckt bei jedem Herzschlag — kein digitaler Zahlenwert sichtbar
- Variabler Herzrhythmus (55–95 bpm) pro Messung
- 26 Blutdruckwerte aus allen Bereichen (normal bis hypertensiv III)
- Adaptives Wiederholen: schwierige Werte erscheinen häufiger (gewichtete Zufallsauswahl, persistent via localStorage)
- Auskultatorische Lücke: bei hypertensiven Werten mit ~35 % Wahrscheinlichkeit simuliert
- Sofortige Auswertung mit Toleranzbereich ±8 mmHg
- Normwerte-Popover (ESH/ESC 2018) direkt in der Ergebnisansicht
- Session-Score über mehrere Messungen

## Didaktisches Konzept

Beim echten Korotkoff-Verfahren hört die Pflegeperson auf auskultatorische Töne und liest gleichzeitig vom Manometer ab. Genau das simuliert diese App: Der Druck ist nur an der Skala ablesbar — nicht als Zahl. So üben Lernende die gleichzeitige Wahrnehmung von Ton und Skala unter realistischen Bedingungen.

Werte, bei denen Lernende daneben lagen, werden durch ein adaptives Gewichtungssystem häufiger wiederholt — nach dem Prinzip der Spaced Repetition, ohne dass dies sichtbar wird.

## Technik

- Einzelne HTML-Datei, Vanilla JavaScript, keine Frameworks, kein Build-Tool
- Kein externes CDN, keine Abhängigkeiten zur Laufzeit
- **PWA**: installierbar auf iPhone und Android, offline-fähig via Service Worker
- `safe-area-inset` für iPhone-Notch und Home-Indicator
- DSGVO-konform: keine Tracker, keine externen Ressourcen, keine Datenübertragung

## Dateien

| Datei | Funktion |
|---|---|
| `index.html` | Gesamte App (HTML, CSS, JS) |
| `sw.js` | Service Worker für Offline-Betrieb |
| `manifest.json` | PWA-Manifest |
| `icon.svg` | Vektorgrafik-Icon |
| `icons/` | PNG-Icons in allen Größen (inkl. maskable) |
| `og-image.png` | Vorschaubild für Social Media |

## Impressum

Verantwortlich: Florian Loyns. Pflichtangaben nach § 5 DDG: [Impressum](https://florianloyns.com/Impressum/)

## Lizenz

[MIT](LICENSE) für den Quelltext · [CC BY-SA 4.0](LICENSE-CONTENT.md) für die didaktischen Inhalte (Fälle, Fragen, Texte, Grafiken).

Nutzen, anpassen und weitergeben ist ausdrücklich erwünscht — auch im kommerziellen Kontext. Bei den Inhalten gilt: Namensnennung und Weitergabe bearbeiteter Fassungen unter denselben Bedingungen.
