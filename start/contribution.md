---
title: Mitmachen
description: Eine Anleitung, wie man dieses Projekt unterstützen kann.
---

Im Aufbau...

## Headings

- Neue Sektionen beginnen mit Heading 2 und aufwärts! **Heading 1 ist für die Seitenüberschrift reserviert.**
- Headings sollten möglichst kurz und bezeichnend sein.
- Headings dürfen nicht mit Satzzeichen enden (Beispiel ":" oder ".")

## Lokale Videos

Um lokale Videos (in `/assets`) auf der Seite anzuzeigen, müssen wir die Dateiendung von `.md` auf `.mdx` ändern.

MDX lässt uns neben dem Standard-Markdown Syntax auch `JSX` in der Textdatei nutzen. **JSX ist der Syntax**, welcher in der moderner Webentwicklung für sogenannte *Webkomponenten* verwendet.

Da wir die **Videos im Source-Code** zur Build-Time des Webservers inkludieren, müssen wir diese innerhalb einer `.mdx` Datei **importieren und dann in ein HTML-Video Element im `src` Attribut hinzufügen**. Dafür ist grundsätzlich *kein JavaScript Wissen notwendig*.

```markdown
Hier das Ergebnis unserer Arbeit:

  

import demoVF from "../assets/demo-variable-fonts.mp4";

  

<video src={demoVF} alt="Variable font demo with nav-links" controls></video>
```

- Mehr über [MDX](https://mdxjs.com/)
