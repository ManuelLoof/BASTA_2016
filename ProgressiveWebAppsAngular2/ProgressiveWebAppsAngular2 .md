# BASTA! 2016 #

## Offlinefähige Webanwendungen: Progressive Web-Apps mit Angular 2 ##

> Speaker: Manfred Steyer  (Software Architekt.at | it-visions.de)
> Date: 21.09.2016

### Überblick  ###

- Service Worker
- Wep App Manifest
- IndexdDB & Co
- 

### Service Worker ###

- Hintergrund-Tasks
- Werden vonder Web App installiert
- Kann ohne Web App laufen
- Können sich sehr deaktivieren und wieder aktivieren.
- nur https (außer localhost)
- kein XHR, aber fetch

#### Service Worker und Offline ####

- Anfragen abfangen
- Entscheiden, wie auf Anfragen zu antworten ist.
- Caching Muster
    - Cache only
    - Network only
    - Try cache first, then network
    - Try network first, then cache

** ToDo Service Worker Code von Folie holen **


### Service Worker Toolbox ###

### AppCache ###

- weniger feature
- cache only- network only

### Daten offline speichern ###

- LocalStorage
- WebDB
- IndexedDB (NOSQL)
- Gute Ideee: Abstraction nutzen, z.B. *PouchDB*
- Herausforderung: Quotas! (Speichergröße)

- **!Kein langfristiger Offlinebetrieb!**

** ToDo Service Worker Code von Folie holen **


### App Shell ###

- Shell im Chache (Service Worker)
- Daten aus Cache (PouchDB)
- Kann sofort angezeigt Werden- Daten aus dem Cahceh danach werden aktuelle Daten heruntergeladen.

### Insatllation am Homescreen ###

** ToDo Service Worker Code von Folie holen **


- `<link rel=manifest" href="manifest.json>`
    - Für Apple eigene Metadaten

### Background Sync ###

- App fordert Background Sync angezeigt
- Service Wrker führt Sync Event aus, wenn es passend erscheint (Netzwer, Akku)
- Pläne für periodisches Aufrufen


### Push Notifications ###

### Angular Mobile Toolkit ###

- Beta
- Angluar CLI => Angular command line interface
- `npm install -g angular-CLI`
- `ng new hello-mobile --mobile`



### Urls ###

### Tipps und Tricks ###