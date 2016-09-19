# BASTA! 2016 #

## C#-Revolution ##

> Datum: 19.09.2016
> Dozent: Rainer Stropek


### Slides und Code Beispiel: ###

- https://github.com/rstropek/sampels

- Verzeichnis:

    - AspNetCore1Workshop
        - Slides
            - *.pdf
            - Powerpoint

### Workshop ###

- Packages die sich mit dem normalen Framework überschneiden haben die selbe 
    Versinonsnummer 4.1
- .NetCoreApp 1.0 Enthält alle wichtigen Base Abhängigkeiten. (Meta Package)
    
    
    Install-Packege Microsoft.NetCpre.App

> Installiert das Package

- https://hub.docker.com/microsft/dotnet ist sowas wie GitHub für Docker.


    docker run -it --rm microsoft/dotnet

> Startet einen Dokcer Container mit dem Core Framework.

- *Docker for Windwos* freies Tool für Docker zum hosten von Docker Containern.

#### Simples Beispiel ###

    cmd> dotnet
    cmd> dotnet new -- help
    cmd> dotnet new -t Console

> Legt ein neues Projekt an.

- program.cs
- project.json
    - debug.. Standardwert bedeutet läuft auf allen Betriebssystemen
    - entryPoint: true = exe
    - entryPoint: false = dll 
    - Framework und NeGet Package hängen nicht zusammen
        - "frameworks:"{
            - dependencies":{
        - "imports": "dnxcore50" Wichtig für die rückwärts
            Kompatibilität. Alte Versionen basieren darauf.


    cmd> dotnet restore

> Erstellt das Packet neu und läd alle Abhängigkeiten ein.


    cmd> dotnet build

> Kompiliert das Projekt.

    cmd> dotnet run

> Führt das Programm aus. ** Ich muss nicht vorher kompilieren.

    cmd> docker run -it --rm C:\temp\ProjektName **hier fehlt noch das mappen**

> Startet das Tool im Docker Container.


- .Net Standard stellt die Basis der Sprache da. Es gibt einen
    eine Übersichtitstablle von Microsoft welches Framework
    ob .Net Core und .NET Framework.



### ToDo: ###

- Unbedingt auf 1.0.1 updaten. Security Patch.



### ToRead: ###

- Windows Nano Server anschauen (sowas Windows embeded für Server)


### Tips und Tricks ###