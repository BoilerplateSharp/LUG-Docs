---
title: Dotnet CLI
description: Wie man C# Projekte mit dem Dotnet CLI managen kann.
---
# Projekte erstellen und managen mit dem Dotnet-CLI

In diesem Artikel konzentrieren wir uns darauf, wie du deine WebAPI-Projekte mit dem `dotnet` CLI erstellen und managen kannst. 

## Projekte erstellen

### 1. Neues Projekt erstellen

Öffne die Konsole und navigiere zum Ordner, in dem du das Projekt erstellen möchtest. Gib dann den folgenden Befehl ein:

```shell
dotnet new webapi -n awesome-api
```

Hier wird ein neues WebAPI-Projekt mit dem Namen "awesome-api" erstellt. Du kannst den Namen nach deinen Wünschen anpassen.

### 2. In das Projektverzeichnis wechseln

Navigiere in das Verzeichnis des erstellten Projekts:

```shell
cd awesome-api
```

## Das Projekt managen

### 1. Das Projekt öffnen

Verwende einen Code-Editor oder eine integrierte Entwicklungsumgebung (IDE) deiner Wahl, um das Projekt zu bearbeiten. Öffne dazu den Projektordner:

```shell
code .
```

### 2. Das Projekt kompilieren und ausführen

Um sicherzustellen, dass alles reibungslos funktioniert, kompiliere und führe das Projekt aus:

```shell
dotnet build
dotnet run
```

### 3. Dev-Server

Um dafür zu sorgen, dass der Server automatisch neustartet, sobald wir eine Änderung speichern, nutze diesen Command:

```shell
dotnet watch run
```

## Weitere nützliche Befehle

### 1. Referenzen hinzufügen

Wenn du Abhängigkeiten zu deinem Projekt hinzufügen möchtest, verwende:

```shell
dotnet add package DeinPaketName
```

### 2. Projektabhängigkeiten wiederherstellen

Wenn du mal Probleme mit den Projektabhängigkeiten hast, führe folgenden Befehl aus:

```shell
dotnet restore
```

