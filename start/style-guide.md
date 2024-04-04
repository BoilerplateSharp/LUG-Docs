---
title: Style-Guide
description: Unsere generellen Regeln und Richtlinien für neue Inhalte.
---

Du hast dich dafür entschieden bei diesem Projekt mitzuhelfen! 💪

:::note

Falls du es noch nicht getan hast, solltest du unserem [Discord Server](https://discord.gg/NzHk4m7d5w) beitreten. Dort kannst du Fragen zu den hier dargestellten Themen beantwortet bekommen, Themen- oder Verbesserungsvorschläge einbringen oder dich mit gleichgesinnten austauschen.

:::

## Regeln zum Markdown-Format

Wir verwenden für unsere Docs den erweiterten Markdown Standard. Ein Cheat-Sheet mit den wichtigsten Regeln findest du [hier](https://www.markdownguide.org/cheat-sheet/). Ausgenommen davon sind:

- ~~Definition List~~
- ~~Emoji mit `:joy:` oder ähnliche~~
- ~~Heading-IDs~~

**Emojis können als UTF8 Text hinzugefügt werden**, beispielsweise über das Windows Emoji Keyboard `<WIN>+.`

### Heading Links

Heading-IDs werden von der Website automatisch für alle **Überschriften (ab H2)** generiert. Beachte bitte, dass die Art wie Obsidian automatisch Links erstellt `[[]]` noch nicht mit unserer Website kompatibel ist.

Hier ein paar praktische Beispiele für interne Links:

```markdown
## Table of Content

- [Einleitung](#einleitung)
- [Hauptteil](#überschrift-mit-leerzeichen)
- [Zusammenfassung](#zusammenfassung)
- [Link auf andere Seite](/start/contribution#)

## Einleitung

## Überschrift mit Leerzeichen

## Zusammenfassung
```

### Links zu anderen Dokumenten

Links auf andere Dokumente auf LUG-Learn folgen ebenfalls einer gewissen Konvention, basierend auf dem URL-Parser. Hier ein Beispiel für funktionierende Links auf ein anderes Dokument:

```markdown
[Übersichtsseite](/git/uebersicht)
[Heading in Übersichtsseite](/git/uebersicht#3-die-objekte)
```

### Zusätzliche Features

Neben den Features des Markdown-Specs, haben wir einige weitere Features, welche zwar nicht von allen Markdown-Editoren unterstützt werden, aber auf unserer Learn-Seite funktionieren und korrekt angezeigt werden. Im folgenden werden die wichtigsten Elemente aufgezeigt. Eine Liste mit allen Komponenten, die Astro Starlight uns anbietet, findest du [hier](https://starlight.astro.build/guides/components/#built-in-components).

#### Frontmatter

Jedes Markdown oder MDX Dokument **muss mit einer Frontmatter-Sektion** mit *mindestens dem `title`* der Seite beginnen. Das sieht dann wie folgt aus:

```markdown
---
title: Meine Überschrift
description: Hier könnte deine Werbung stehen!
---
```

Es gibt neben dem Title weitere Eigenschaften, welche es sich zu setzen lohnen. Eine Liste mit allen Optionen findet sich in den [Starlight-Docs](https://starlight.astro.build/de/reference/frontmatter/).

#### Asides

Asides (Auch "Admonitions" oder "Callouts" genannt) sind Bemerkungen, welche sekundäre Informationen, neben dem eigentlichen Inhalt darstellen. Der Inhalt eines Aside-Elements wird in dreifachen Doppelpunkten `:::`, gefolgt von dem Typ des Asides, umschlossen. Folgende Typen sind möglich:

- `note`: Eine generelle Nebeninformation
  - Blaue Farbe mit Info-Icon
- `tip`: Ein praktischer aber optionaler Tip, welcher helfen kann, aber nicht muss
  - Lila Farbe mit Raketen-Icon
- `caution`: Wichtige Information, welche nicht überlesen werden darf
  - Gelbe Farbe mit Warnungs-Icon
- `danger`: Essentielle Information, welche nicht überlesen werden darf
  - Rote Farbe mit Gefahren-Icon

```markdown
:::note

Hier könnte was wichtiges stehen!

lorem ipsum dolor est

`git commit && git push && git out`

:::
```

So sehen die Asides auf der Webseite aus:

![asides](../assets/Pasted%20image%2020240403140753.png)

Asides können außerdem benutzerdefinierte Überschriften haben:

```markdown
:::note[Wusstest du schon?]

Hier könnte was wichtiges stehen!

lorem ipsum dolor est

`git commit && git push && git out`

:::
```

#### Expressive Code

todo

## Lesbarkeit

Jeder Leser profitiert von klarer und einfacher Sprache in geschriebenen Texten. Die Dokumentationen auf dieser Seite haben die folgenden Ziele:

1. Leser sollen möglichst schnell an spezifische Informationen kommen können.
2. Jedes Dokument soll möglichst einfach zu verstehen sein.
3. Die Dokumente sollen für alle so zugänglich wie möglich sein.
4. Die Dokumente bauen aufeinander auf und enthalten dementsprechend angemessene Referenzen.

Aus diesen Zielen leiten wir die folgenden generellen Regeln für unsere Dokumente ab:

- Kurze Sätze und Absätze
- Möglichst einfaches Vokabular
- Fachbegriffe werden unmittelbar erläutert, im Dokument oder per Verweis
- Weniger Annahmen über das Vorwissen der Leser treffen
- Abkürzungen möglichst meiden und wo notwendig konsistent halten ("eg.", "z.B.", "Beispiel:")
- Absatz-Gruppen immer wieder mit Bullet-Points, Bildern, Codeblöcken oder ähnlichem abwechseln

## Headings

```markdown
## Sektion 1

### Subheading 1.1

### Subheading 1.2

#### SubSubheading 1.2.1

## Sektion 2
```

- Neue Sektionen beginnen mit Heading 2 und aufwärts! **Heading 1 ist für die Seitenüberschrift reserviert.**
- Headings sollten möglichst kurz und bezeichnend sein.
- Headings dürfen nicht mit Satzzeichen enden (Beispiel ":" oder ".")

## Listen

```markdown
Listen sind:

- Gut um eine Gruppe von zusammenhängenden Punkten sinnvoll darzustellen.
- Schlecht um große Absätze mit langen Sätzen zu schreiben.
- Eine Alternative zu Sektion-Überschriften.

Eine Aufzählung könnte eine Anleitung zum Mitmachen:

1. Lade das Repository mit `git clone <URL>` runter
2. Erstelle einen neuen Branch mit `git checkout -b <Branchname>`
3. Erstelle deine Änderungen
4. Speichere deine Änderungen mit `git commit --all -m "<Nachricht>"`
5. Lade deinen Branch mit den Änderungen hoch mit `git push -u origin <Branchname>`
6. Warte auf Feedback der Contributors
```

Aufzählungen und Listen helfen mehrere Punkte gut leserlich darzustellen. Nutze sie für Gruppen von zusammenhängenden Punkten wie Vor- und Nachteile, Konfigurationsoptionen, kurze Anleitungen und ähnliches.

Wenn individuelle Punkte einer Aufzählung zu lang werden, oder andere Elemente (wie Bilder, Videos oder Codeblöcke) benötigt werden, solltest du die Aufzählung mit Sektionen und Unterüberschriften gestalten. 

## Lokale Bilder

Lokale Bilder lassen sich über den einfachen Markdown-Syntax in Dokumente einbauen. Bilder müssen in `/assets` oder einem beliebigen Unterordner von `/assets` abgelegt werden.

```markdown
...
Das folgende Bild wird auf der Seite mit der Originalgröße gerendert.
![MyImage](../assets/my-image.png)
Das folgende Bild wird auf der Seite in Größe 800px x 600px gerendert.
![MyImage|800x600](../assets/my-image.png)
```

## Lokale Videos

Um lokale Videos (in `/assets`) auf der Seite anzuzeigen, müssen wir die Dateiendung von `.md` auf `.mdx` ändern.

MDX lässt uns neben dem Standard-Markdown Syntax auch `JSX` in der Textdatei nutzen. **JSX ist der Syntax**, welcher in der moderner Webentwicklung für sogenannte *Webkomponenten* verwendet wird.

Da wir die **Videos im Source-Code** zur Build-Time des Webservers inkludieren, müssen wir diese innerhalb einer `.mdx` Datei **importieren und dann in ein HTML-Video Element im `src` Attribut hinzufügen**. Dafür ist grundsätzlich *kein JavaScript Wissen notwendig*.

```markdown
import demoVF from "../assets/demo-variable-fonts.mp4";

<video src={demoVF} alt="Variable font demo with nav-links" controls></video>
```

- Mehr über [MDX](https://mdxjs.com/)
