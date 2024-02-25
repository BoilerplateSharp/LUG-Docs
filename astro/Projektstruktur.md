---
title: Projektstruktur
description: Eine Übersicht über die wichtigsten Dateien und Ordner eines Astro-Projekts.
---

# 🌲Projektstruktur

Astro hat ein bereits vordefiniertes Layout für die Projektstruktur. Ihr könnt natürlich weitere Unter-Ordner hinzufügen und euer Projekt strukturieren wie es für euch am Besten ist. Allerdings gibt es einige kleine Vorgaben.

- `src/*` Source-Code der Website (Komponenten, Seiten, Styles, usw.)
- `public/*` Alle öffentlichen statischen Dateien. Diese Dateien werden einfach durch den Webserver veröffentlicht (Fonts, Icons, usw.)
- `package.json` Das Projekt-Manifest. Hier werden alle Abhängigkeiten deklariert sowie der Projekt-Name, der Author, usw.
- `astro.config.mjs` Eine Astro Konfigurationsdatei
- `tsconfig.json` Eine TypeScript Konfigurationsdatei

## Tree

Output von `tree -I node_modules` (Linux):
```shell
.
├── astro.config.mjs # Astro Config Datei
├── package.json # Das Manifest des Projekts / "Lieferschein"
├── package-lock.json
├── public # Ordner für statische Dateien
│   └── favicon.svg # z.B. Ein Icon für die Registerkarte
├── README.md # Projektinformationen
├── src # Source-Code der Website
│   ├── components # Wiederverwendbare Komponenten
│   │   └── Card.astro
│   ├── env.d.ts # Definitionen für TypeScript Datentypen
│   ├── layouts # Templates/Vorlagen für die "pages"
│   │   └── Layout.astro # Die Standart-Vorlage
│   └── pages # URL-Mapped Webpages
│       └── index.astro
└── tsconfig.json # TypeScript Projekt-Config

6 directories, 10 files
```
