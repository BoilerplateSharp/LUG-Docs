---
title: Projektinitialisierung
description: Wie man ein neues Astro-Projekt aufsetzt.
sidebar:
  order: 1
---

Ein neues Astro-Projekt kann mit folgendem Command initialisiert werden. Wenn ihr nicht bereits in einem leerem Ordner für euer Projekt seid, erstellt der Command diesen Ordner automatisch für euch.

```shell
npm create astro@latest
```

Danach müssen wir noch mit dem `cd` Command in den Ordner wechseln.

```shell
cd <Ordner>
```

## 🚀Starten Des Development-Servers

Der folgende Command startet den Dev-Server auf Port `4321`.

```shell
npm run dev
```

## 🏗️Bauen Des Projekts

Um aus unseren einzelnen Source-Files eine an den Kunden auslieferbare Web-App zu generieren, nutzen wir:

```shell
npm run build
```

Die Dateien, welche auf dem jeweiligen Hoster zur Veröffentlichung hochgeladen werden müssen, landen nach Eingabe des Command im `/dist` Ordner. Die Inhalte des Ordners können mit einem beliebigen Web-Server, wie z.B. `Apache` oder `nginx`, veröffentlicht werden.