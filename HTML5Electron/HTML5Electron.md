# BASTA! 2016 #

## Desktop Anwendungen mit HTML 5 & Electron ##

> Speaker: Dariusz Parys  (Microsoft)
> Date: 22.09.2016

### Intro  ###

- Hilf früher Atomshell
- Cross Platform desktop Anwendungen
- Windows, Linux, Mac
- Anwendungs Layer => Node.js, Chromium => javaScript, HTML, CSS

#### Electron Container ####

- Zugriff aufs Dateisystem
- Integration Task, Tray
- Media Previes
- Notifications
- Windows (Fenster)
- Power management manipulieren
- Netzwerk
- Native menus und tastaturkürzel
- Shell Prozesse
- Offline by default
- Node & Node native module
- Keine Sandbox (Rechte des Nutzers)
- Nur für einen Browser entwickeln

### Beispiel ###

- node project erstllen
- `npm init -Y`
- `npm install electron -Dariusz-`
- package .json anpassen (diehe code beispiel)
- `npm start`


    const electron = require("electron")
    const {app, BrowserWindos} = electron

    let myWindow = null

    app.on("ready", () => {
        console.log('Electron is up and running')

        myWindows = new BrowserWindos({
            width: 640,
            height: 480
    })

    myWindows.loadUrl("http://wwww.minutes.io");


    myWindow.on("closed," () => {
        console.log(window closed")
        myWindow = null
    })

    })


- Nachrichten über IPC zwischen einzelnen Prozessen


### Beispiel lokales HTML ###

- node project erstllen
- `npm init -Y`
- `npm install electron -Dariusz-`
- package .json anpassen (diehe code beispiel)
- `npm start`


    const electron = require("electron")
    const {app, BrowserWindos} = electron

    let myWindow = null

    app.on("ready", () => {
        console.log('Electron is up and running')

        myWindows = new BrowserWindos({
            width: 640,
            height: 480
    })

    myWindows.loadUrl(`file:://${__dirname}/basta.html`);


    myWindow.on("closed," () => {
        console.log(window closed")
        myWindow = null
    })

    })





### Urls ###

- [http://electron.atom.io](http://electron.atom.io)


### Tipps und Tricks ###

- gitshell ansehen
- asar zum packen benutzen
- gulp angucken
- boardz ebenfalls Packet´er

