---
title: "Übung npm"
author: "Alexander-David Beck | 5ABIFT"
date: "04.02.2025"
geometry: "margin=1in"
fontsize: 12pt
---

# Über npm
Node Package Manager ist ein Paketmanager für Node.JS, es ermöglicht die Verwaltung von JS-Bibliotheken. 

Es ermöglicht folgende Tätigkeiten:
1. Installation von Paketen
2. Verwaltung von Abhängigkeiten
3. Veröffentlichung eigener Pakete
4. Ausführung von Skripten

## Wichtige Befehle
### Wichtige `npm`-Befehle

| Befehl | Bedeutung |
|--------|------------|
| `npm init` | Erstellt eine `package.json` für dein Projekt |
| `npm install <paket>` | Installiert ein npm-Paket |
| `npm install` | Installiert alle Abhängigkeiten aus `package.json` |
| `npm update` | Aktualisiert installierte Pakete |
| `npm uninstall <paket>` | Entfernt ein Paket aus dem Projekt |
| `npm run <script>` | Führt ein Skript aus `package.json` aus |


## Ordnerstruktur
- mein-projekt
  - src
  - .gitignore
  - node_modules
    - cowsay
      - ...
    - chalk
      - ...
    - ...
  - package.json
  - package-lock.json
  - README.md

### .gitignore
Pfade und Dateien die in dieser Datei angegeben werden, werden nicht durch "git add" mit gestaged. D.h. die Dateien und Ordner werden ignoriert. 

### node_modules
In Ordner "node_modules" befinden sich alle Pakete und Abhängigkeiten, der Ordner sollte immer mit der .gitignore ignoriert werden.

### package.json
Hier werden alle Abhängigkeiten, Informateionen über das Projekt, Versionen, Skripte usw. gespeichert. 

Ohne diese Datei kann ein Node.js-Projekt keine Pakete verwalten.

### package-lock.json
Verhindert das verschiedene Entwickler verschiedene Versionen der Abhängigkeiten installieren. Hier wird festgelegt welche Version eines Paketes installiert und verwendet wird.

# Protokoll
## Aufgabe
Ziel war es einen Überblick von npm zu erhalten. Den Umgang mit Paketen, Abhängigkeiten und Versionierung zu üben.

## Tätigkeit
Es wurde ein Ordner angelegt in diesem wurde dann `$ npm init` ausgeführt um den Node Package Manager in einem Projekt zu initialisieren. Dadurch wird eine package.json angelegt. 

Als nächstes wurde mit `$ npm install chalk` das Paket chalk installiert, es wurde automatisch der Ordner "node_modules" erzeugt in dem alle Pakete und Abhängigkeiten gespeichert werden. 

Nun wurde mit `$ npm uninstall chalk` das Paket wieder entfernt und mit `$ npm install chalk@4` das Paket  mit der Version 4 installiert. Eine Funktion der Bibliothek von Chalk wurde verwendet und mit `$ node index.js` wurde die Datei ausgeführt. Das gleiche wurde mit dem Paket Cowsay ebenfalls probiert.