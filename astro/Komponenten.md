---
title: Wiederverwendbare Komponenten
description: Simple und wiederverwendbare Komponenten mit AstroJS
prev:
  label: Projektstruktur
  link: /astro/projektstruktur
next:
  label: Interaktive Inseln
  link: /astro/interaktive-inseln
---

# Komponenten

Stellen wir uns vor wir wollen auf unsere Webseite ein Kartendesign bauen und auf mehreren Unterseiten verwenden. Wir erstellen also eine `card.astro` Datei.
Eine `.astro` Datei enthält nicht nur unser **HTML**, spezifisch nur für die Karte, sondern auch die zugehörigen **Styles** und **JavaScript**.

**navbar.astro**
```astro
---
interface Props {
	title: string;
	body: string;
	href: string;
	color: string;
}
const { href, title, body, color } = Astro.props;
---

<li class="link-card">
	<a href={href}>
		<h2>
			{title}
		</h2>
		<p>
			{body}
		</p>
	</a>
</li>

<style define:vars={{color}}>
	.link-card {
		list-style: none;
		display: flex;
		background-color: #23262d;
		border-radius: 7px;
		transition: background-position 0.6s cubic-bezier(0.22, 1, 0.36, 1);
	}
	.link-card > a {
		width: 100%;
		text-decoration: none;
		line-height: 1.4;
		padding: calc(1.5rem - 1px);
		border-radius: 8px;
		color: var(--color);
		background-color: #23262d;
		opacity: 0.8;
	}
	h2 {
		margin: 0;
		font-size: 1.25rem;
		transition: color 0.3s ease;
	}
	p {
		margin-top: 0.5rem;
		margin-bottom: 0;
	}
	.link-card:is(:hover, :focus-within) {
		background-position: 0;
		background-image: var(--accent-gradient);
	}
	.link-card:is(:hover, :focus-within) h2 {
		color: rgb(var(--accent-light));
	}
</style>
```

Im folgenden  gehen wir weiter auf die einzelnen Bestandteile einer `.astro` Datei ein.

## JavaScript Block

Der oberste Block einer `.astro` Datei enthält unseren JavaScript Code. Oder eben **TypeScript**, falls wir uns bei der Installation dafür entschieden haben. Ich würde TypeScript empfehlen, da es einfach nur eine sinnvolle Erweiterung von JavaScript ist.

```astro
---
interface Props {
	title: string;
	body: string;
	href: string;
	color: string;
}
const { href, title, body, color } = Astro.props;
---
html...
```

### Interface `Props`

Das Interface `Props` ist, da Interfaces ein TypeScript Feature sind, logischerweise optional. Es gibt uns allerdings Type-Definitions für unsere selbst erstellten Komponenten. In vielen Fällen wollen wir von der Stelle, wo wir die Komponente aufrufen, Parameter übergeben. Mit diesem Interface kann unser Code-Editor Warnungen zu fehlenden Parametern (oder besser gesagt **Attributen**) anzeigen.

### `Astro.props`

Die eben erwähnten **Attribute**, welche als Parameter an unsere Komponente übergeben werden sollen, bekommen wir, indem wir **Object-Destructoring** auf den `Astro.props` anwenden. Der oben dargestellte Code ist funktional-gleich zu folgendem Code:

```astro
const href = Astro.prop.href;
const title = Astro.prop.title;
const body = Astro.prop.body;
const color = Astro.prop.color;
```

## HTML Block

Diese Variablen stehen uns dann im HTML der Komponente zur Verfügung. In Astro können wir im HTML mit `{bezeichner}` auf den Wert einer Variablen zugreifen. Besser gesagt: In den geschweiften Klammern können wir arbiträre JavaScript-Codeblöcke einsetzen.  

```astro
<li class="link-card">
	<a href={href}>
		<h2>
			{title}
		</h2>
		<p>
			{body}
		</p>
	</a>
</li>
```

In diesem Fall machen wir nichts komplexes und setzen nur die Variablen in das HTML ein. Bedenkt jedoch, dass `Astro` by Default nur statisches HTML zurückgibt. Heißt, wenn sich eine dieser Variablen verändert, aktualisiert sich die Darstellung nicht. Wie wir unsere Komponenten interaktiv machen können? Stichwort: **Interaktive Inseln**.

## Style Block

Euch ist vielleicht aufgefallen, dass wir im HTML-Template nur die Variablen `href`, `title` und `body` verwendet haben. Wir haben jedoch auch eine `color` Variable als Parameter (oder Attribut) definiert. Diese verwenden wir im CSS Code für die Farbe der Links in der Karte. Schaut dazu im folgenden Code mal auf die Erste Zeile und in den Selektor `.link-card > a` in die Regel für die `color:`

```astro
<style define:vars={{color}}>
	.link-card {
		list-style: none;
		display: flex;
		background-color: #23262d;
		border-radius: 7px;
		transition: background-position 0.6s cubic-bezier(0.22, 1, 0.36, 1);
	}
	.link-card > a {
		width: 100%;
		text-decoration: none;
		line-height: 1.4;
		padding: calc(1.5rem - 1px);
		border-radius: 8px;
		color: var(--color);
		background-color: #23262d;
		opacity: 0.8;
	}
	h2 {
		margin: 0;
		font-size: 1.25rem;
		transition: color 0.3s ease;
	}
	p {
		margin-top: 0.5rem;
		margin-bottom: 0;
	}
	.link-card:is(:hover, :focus-within) {
		background-position: 0;
		background-image: var(--accent-gradient);
	}
	.link-card:is(:hover, :focus-within) h2 {
		color: rgb(var(--accent-light));
	}
</style>
```

Wir können jede beliebige Variable als Text in der Form übergeben