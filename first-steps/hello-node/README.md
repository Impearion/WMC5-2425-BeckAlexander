---
title: "Exercise: First steps with Node.js and npm"
author: "Alexander-David Beck | 5ABIFT"
date: "04.02.2025"
geometry: "margin=1in"
fontsize: 12pt
---


# Protokoll
## Aufgabe
Das Ziel war es ein Gefühl für die Handhabung von Node.js, npm und git zu erlangen.

## Task 1: Tools setup
Die Versionen wurden überprüft, es stellte sich heraus das die Node.js Version veraltet war. Es wurde die neuste LTS installiert.
  ```bash
  $ code --version
  $ git --version
  $ node --version
  ```

Es wurde ein Screenshot gemacht und mit git in die Repo hochgeladen.

## Task 2: Create npm project
Ein Ordner mit den Namen `hello-node` wurde angelegt. In diesem wurde ein neues npm Projekt angelegt. 
  ```bash
  $ npm init 
  ```
In der manuell angelegten .gitignore wurde der `node_modules` Ordner zum Hochladen eine Ausnahme erstellt.

  ```bash
  $ node app.js
  > Hello World
  ```
Mit einem console.log in einer .js Datei wurde mit dem Befehl `node app.js` die Funktionalität von node getestet.

  ```bash
  "start": "node app.js"
  ```
In der `package.json` wurde unter `scripts` dieser Startbefehl hinzugefügt. Immer wenn `npm start` eingegeben wird, wird eigentlich `node app.js` ausgeführt.

Die Änderungen wurden wieder auf die Repo hochgeladen.

## Task 3: Install chalk
  ```json
    "type": "module"
  ```
Durch diese Änderung in der `package.json` wurde von commonjs auf das moderne Modulsystem für Importe und Exporte umgestiegen.

  ```json
    $ npm install chalk@4.1.0
    $ npm uninstall chalk
    $ npm install chalk
  ```
Das Chalk Paket wurde mit diesen Befehlen installiert und deinstalliert. Hierbei wurde zuerst die Chalk Version 4.1.0 installiert.


```json
"dependencies": {
  "chalk": "~4.1.0"
}
  ```
In der `package.json` wurde eingestellt das nur pachtes der Version geupdated werden. Also keine Major oder Minor Änderungen.


## Task 4: Install cowsay
```json
$ npm install cowsay
  ```
Hiermit wird das Paket Cowsay lokal in dem Projekt installiert. 

```json
$ npx cowsay Bla
```

Um Cowsay im Terminal auszuführen muss `npx` verwendet werden, da das Paket nur lokal im Projekt und nicht global installiert wurde. 

```json
  import cowsay from 'cowsay';

  console.log(cowsay.say({
    text: 'Moo'
  }));

  console.log(cowsay.think({
    text: 'Impearion',
  }));
```

Dieser Code wurde in die `app.js` eingefügt um zu testen ob die Installation funktioniert hat.
