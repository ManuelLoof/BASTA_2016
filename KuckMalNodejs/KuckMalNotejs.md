# BASTA! 2016 #

## Kuck mal, Node.js! ##
### Einstieg für .NET-Entwickler ###


> Speaker: Gregor Biswanger  
> Date: 21.09.2016

### Beispiel  ###

    import http = require("http");

    http.createServer((request, response) =>{
        response.write("Hallo world");

    }).listen(3000);


    typings init node  --sourde dt --global --save

> Installiert die typings

- tsconfig.json

    {
        compileroptions ...
    }

> Damit das Proje die Bibliotheken kennt.

- task einstellen TypeScript im Watch mode oder über Konsole

- --save erzeugt den Wert in der Dependencies Datei.

### Urls ###

- [nodejs.org](nodejs.org)

### Tipps und Tricks ###

- nodewebkit
- Electron
- node.js als Framework für Rasberry und Arduiona und Co.