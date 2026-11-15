<div align="center">

# 📚 Research Lab

**Recherche-One-Pager und Briefs, belegt mit Primärquellen.**

[![Letzter Commit](https://img.shields.io/github/last-commit/otype/research-lab/main?style=flat-square&logo=github&logoColor=white)](https://github.com/otype/research-lab/commits/main)
[![Website](https://img.shields.io/badge/Website-otype.de%2Fresearch--lab-4fd1c5?style=flat-square)](https://otype.de/research-lab/)

[**→ Zur Website**](https://otype.de/research-lab/)

</div>

---

Jedes Paper ist eine in sich geschlossene Recherche zu einem aktuellen Thema (Märkte, Geopolitik, Technik). Es gibt sie in zwei Formen: als **Markdown-Dokument** mit allen Quellen und als **eigenständige Webseite** mit den wichtigsten Zahlen. Die Seiten werden über GitHub Pages unter [otype.de/research-lab](https://otype.de/research-lab/) veröffentlicht.

## 📄 Papers

| Thema | Kategorie | Web | Dokument |
| --- | --- | --- | --- |
| 🥇 Gold als Safe Haven: Wer kauft massiv, und wie hat sich der Preis entwickelt? | Märkte | [Seite](https://otype.de/research-lab/papers/gold-safe-haven-2026/) | [Markdown](docs/2026-11-gold-safe-haven.md) |
| 🏦 Banken auf der Blockchain und Zugang via KI-Agenten | Finanzen, Technik | [Seite](https://otype.de/research-lab/papers/banken-blockchain-ki-agenten-2026/) | [Markdown](docs/2026-11-banken-blockchain-ki-agenten.md) |
| 📉 Wall-Street-Ausverkauf: KI-Trade bricht nach den Midterms ein | Märkte | [Seite](https://otype.de/research-lab/papers/aktiencrash-ki-ausverkauf-2026/) | [Markdown](docs/2026-11-aktiencrash-ki-ausverkauf.md) |
| ⚡ Offizielle Warnungen zu Stromausfällen und Angriffen auf kritische Infrastruktur (Aug–Nov 2026) | Geopolitik | [Seite](https://otype.de/research-lab/papers/stromausfall-warnungen-2026/) | [Markdown](docs/2026-11-stromausfall-warnungen-global.md) |

## 🧭 Anspruch

- **Primärquellen zuerst.** Behörden, Zentralbanken, Pressemitteilungen und große Nachrichtenagenturen und -medien. Zahlen und Zitate stehen mit Quelle und Datum da.
- **Keine Panikmache.** Bei sicherheitsrelevanten Themen zählen nur direkte, überprüfbare Zitate von Amtspersonen oder Behörden.
- **Aufbau.** Jedes Dokument beginnt mit einem Stand-Datum und einer Methodik-Notiz, dann folgt eine **TL;DR**-Liste, danach Tabellen mit Belegen und am Ende ein **Fazit**.
- **KI-unterstützt.** Recherche und Aufbereitung entstehen mit KI-Unterstützung auf Basis von Websuche. Fehler sind trotz Quellenprüfung nicht ausgeschlossen, im Zweifel gilt die verlinkte Originalquelle.

Die Inhalte sind keine Handlungs-, Finanz- oder Vorsorgeempfehlung. Haftungsausschluss und Hinweise zu Zitaten stehen auf der [Website](https://otype.de/research-lab/#disclaimer).

## 🗂️ Aufbau des Repos

```text
research-lab/
├── index.html      Startseite mit der Liste aller Papers (neueste oben)
├── docs/           ein Markdown-Dokument pro Paper: YYYY-MM-<thema>.md
├── papers/         eine eigenständige Seite pro Paper: papers/<thema>-<jahr>/index.html
└── README.md
```

Die Website wird direkt aus dem Hauptzweig `main` gebaut (GitHub Pages, Wurzelverzeichnis). Es gibt keinen Build-Schritt: Dateien ändern, mergen, fertig.

## ✍️ Neues Paper hinzufügen

1. **Frisch von `main` abzweigen**, nie auf einem alten Feature-Branch weiterarbeiten.

   ```console
   $ git switch main && git pull && git switch -c feature/<thema>
   ```

2. **Recherchieren** mit Primärquellen und das Dokument `docs/YYYY-MM-<thema>.md` schreiben: Titel, Untertitel mit Datum, Methodik-Notiz, `## TL;DR`, Belegtabellen, `## Fazit`.
3. **Seite anlegen:** `papers/<thema>-<jahr>/index.html`. Am einfachsten eine bestehende Seite kopieren, sie bringt das Design (dunkel, Kennzahlen-Raster, Zitat-Karten) mit, den Link zurück zur Übersicht und den Fuß mit Link zum Disclaimer.
4. **Startseite ergänzen:** in `index.html` oben in der Liste einen neuen Eintrag `<a class="paper" href="papers/<thema>-<jahr>/">…</a>` mit Kategorie, Datum, Quellen-Hinweis und einem kurzen Teaser.
5. **Pull Request öffnen**, in der Beschreibung die Kernaussage des Papers zusammenfassen.

**Aktualisieren** gehört in denselben Ablauf: Ändert sich die Lage, neuen Abschnitt im Dokument ergänzen und außerdem die TL;DR-Liste, die Kennzahlen der Seite sowie Teaser und Datum in `index.html` anpassen, damit auch Leser, die nur die Übersicht überfliegen, den neuen Stand sehen. Commit-Nachrichten beginnen mit `Add:` für neue Papers und `Update:` für Aktualisierungen.

> [!NOTE]
> Nach dem Mergen erscheint die Änderung nicht sofort auf der Website. GitHub Pages baut zuerst neu, und davor liegt ein Cache von rund 10 Minuten. Wenn etwas nicht sichtbar ist, den Build-Status prüfen:
>
> ```console
> $ gh api repos/otype/research-lab/pages/builds/latest --jq .status
> ```
>
> Sobald dort `built` steht, genügt etwas Geduld.
