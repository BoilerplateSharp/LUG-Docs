---
title: Einleitung
description: Ein kurzer Überblick zu AstroJS
next: 
- link: /astro/projektstruktur
- label: Übersicht zur Projektstruktur
---

# 🤔Was Ist Astro?

Astro ist ein Webserver-Framework, wie z.B. auch ***ASP.NET***, **Springboot**, **Django**, **Express.js**, **RubyOnRails**, **Laravell** oder ähnlichen.

Cool, aber was macht denn Astro so besonderst?

Astro ist ein All-in-One Framework. Heißt, dass es alles inkludiert, was man braucht um fast jede beliebige Seite umzusetzen. Man mag jetzt denken: "Das sagen sie alle".
Allerdings sprechen einige Punkte für Astro, im speziellen:

- Geringer Ressourcenverbrauch, bei Client und Server.
- Einfaches SEO Setup... Ja, wirklich! :)
- Simpel, mit sinnvollen Defaults.

Das alleine sind schon gute Argumente, aber hier einige Features, welche richtig `nice` sind:

- Fokus auf Content - Inhalte können in den verschiedensten Formaten ganz einfach hinzugefügt werden. Am einfachsten mit `Markdown` oder `MDX`.
- Inseln/Islands - So werden in Astro interaktive Komponenten genannt (eg. CSR). Mehr zu Komponenten, später.
- Speed als Default - Astro-Pages sind erstmal Static-HTML, was die Seite besonderst schnell laden lässt.
- Easy - Astro ist besonderst Einsteigerfreundlich
- Flexibel - Es gibt für die meisten Use-Cases passende Integrationen, die einem die Arbeit vereinfachen.
- Unterstützt verschiedene UI-Frameworks wie `React`, `Svelte`, `Solid`, `Lit` und mehr.


## Komponenten

Bisher haben wir mit statischen HTML-Seiten gearbeitet. Das heißt wir haben einen einfachen Webserver, der auf eingehende HTTP-GET-Requests mit einer HTML-Datei antworten. Dann verlinken wir in diesen HTML-Dateien noch ein paar Stylesheets und schicken noch ein Script mit und das war's.

Das hat in den 90er Jahren gut funktioniert und kann man heute auch noch machen. Es ist einfach, schnell und kostet quasi nichts.
Allerdings haben wir heute meist höhere Ansprüche an unsere Webseiten. Wir wollen ein einheitliches Design, Interaktivität und teilweise bauen wir ganze Apps wie ein `Discord` oder `Spotify` im Browser.
Das ganze ist, mit so einer einfachen Struktur, aber sehr mühselig.

Für genau diesen Zweck hat man sich Webkomponenten ausgedacht.

Um eine Seite mit solchen Komponenten zu bauen, brauchen wir ein UI-Framework wie React, Svelte, Angular oder andere. Diese Frameworks unterscheiden sich in Syntax, Konventionen und Konfiguration. Die Idee bleibt die gleiche:

`HTML`, `CSS` und `Javascript` in einer Datei, für eine wiederverwendbare Komponente vereinen, und diese dann auf mehreren Seiten oder sogar in anderen Projekten wiederverwenden.

