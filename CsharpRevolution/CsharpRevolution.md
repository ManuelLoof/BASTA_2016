# BASTA! 2016 #

## C#-Revolution ##

> Datum: 19.09.2016
> Dozent: Rainer Stropek


### Slides und Code Beispiel: ###

- [https://github.com/rstropek/samples](https://github.com/rstropek/samples)
- `git clone https://github.com/rstropek/Samples.git` 

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

- [https://hub.docker.com/microsft/dotnet](https://hub.docker.com/microsft/dotnet) ist sowas wie GitHub für Docker.


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

    cmd> dotnet publish

> Erzeugt eine Veröffentlichungsverzeichnis. Die Json Files
    und die dll und exe Files kopieren. Nicht die Debug Dateien.


- .Net Standard stellt die Basis der Sprache da. Es gibt einen
    eine Übersichtstabelle von Microsoft welches Framework
    ob .Net Core und .NET Framework.

#### Simples Beispiel 2 (Library) ##

    cmd> dotnet new -t Lib

> Consolen Programm => Microsoft.NetCore.App
> Library => netstandard1.6
> Der Unterschied ist das eine Consolen Anwendung auch auf .Net Core läuft.
> Libaries können auch von Programmen die den Net Standard unterstüzen, 
> also auch das ganz normale Framework.    

    cmd> dotnet pack

> Erzeugt ein NuGet Package.


#### Beispiel 3 Shared ####

- project.json

    "shared": true

> Sorgt dafür das internal Klassen in NuGet Package hinzugefügt werden.
> So ähnlich wie linked Klassen in bisherigen Projekten.


> Eigenschaften/Dependencies werden im normal Fall pro Framework definiert.
> Man kann diese aber auch global definieren.

> ** projet.json Folie anschauen **
> Commands:
> testRunner
> shared
> dependencies
> tools
> scripts
> buildOptions
> publishOptions
> runtimeOptions


> project.json wird leider sterben und die alte *.csproj wird wieder neu aufleben.


####  Beispiel 4 ####
    
    cmd> dotnet new -t Lib

> Legt eine Library an.
> Der Parameter -t sorgt für dafür das es sich um eine Libaray handelt.

    cmd> dotnet new consoleProgName 

> Legt ein Konsolen Programm an.

- global.json

    {
        "projects":{
            
        }
    }

*Nochmal die genaue Syntax anschauen.*

> Hier kann ich alle Biblioteken angeben. Muss ich aber nicht. Falls nicht
> da, dann geht er vom Root Knoten aus.


> *Self-contained* Deployment erzeugt wieder eine schöne *.exe File.
> Ansonsten immer dotnet starten.
> Wird in der Projekt File eingetragen?
> **Nochmal im Slide nachschauen**


#### Beispiel 5 Roslyn Magic ####

- Beispiel 45-custom tool .... classcount


#### Beispiel 6 Nur die benötigten Dlls verwenden  ####

> Für das Beipsiel in die Slides schauen.


#### Beispiel 7 Integration in bisherige Anwendungen ####

> Man kann über NuGet auf eine Core Library zugreifen. Sollte man aber nicht
> machen. Lieber Micro Services.


### ASP.NET Core 1 Basics ###

- Kestrel ist der Webserver von ASP.NET. (cross platform)
- Owin
    - Pipeliner im normalen ASP.net.
    - 
- katana


### Docker ###

    docker run -it --rm ubuntu

> Startet einen Docker Ubuntu Container.


    cmd> docker run -it --rm -v C:\temp\..\..\hello-aspnet-core:/app -p  5000:5000 microsoft/dotnet

    bash> dotnet restore

    bash> dotnet build

    bash> dotnet run

> Startet einen Docker Container mit dem Microsoft .net Core
> Framework unter Linux als eigenen Server.

**Dockker Tools für Visual Studio angucken.** 

- dockerfile anlegen


    FROM microsoft/dotnet

    COPY *.* /src/

    WORKDIR /src
    RUN dotnet restore
    RUN dotnet build

    CMD ["dotnet", "run"]

- Build ausführen

    docker build -t NameVerzeichnis? .

    docker images

> Zegt alle erzeugten Images.

    docker run -d -p 5000:50000 imageName

    docker push

> Läd den Docker Container auf DockerHub hoch.


### Letzter Punkt am Nachmittag (55_Conviguration)  ###

- `ConfigurationBuilder()`


    var builder = new ConfigurationBuilder();
    builder.AddInMemoryCollection(new Dictionary<string, string>)
    {
        {"color", "Red"}
    });

    var config = builder.Build();
    Console.WriteLine($"Color is {config["color"]} ");


> Liest und schreibt in die Config.

- Ich kann auch .json, .xml oder .ini Files einlesen.
- Auch per commandline args.


**Für weitere Informationen die Beispiel-App angucken.**

### Logging ###

- 58-Logging Beispiel 
- ApplicationInsights
    - Logging Clouddienst von Microsoft.
    - Aber auch Telemetry und Performance.
- Dependencie Injection System in Dot Net noch einmal ansehen angucken.



### ToDo: ###

- Unbedingt auf 1.0.1 updaten. Security Patch.
- mstest anschauen. Ganz neu. Was ist dann der Alte?
- Was ist ein NuGet Server
- Docker Tools für Visual Studio angucken.

### ToRead: ###

- Windows Nano Server anschauen (sowas Windows embeded für Server)
- [docs.microsoft.com](docs.microsft.com) die Adresse für die Microsoft
    Dokumentation. MSDN kommt nichts mehr neues.
- Semantic Versioning 2.0.0
- GitHub Issues anschauen.



### Tips und Tricks ###

    private string name;
    public string Name => this.name.ToUpper();

    var nameLength = name?.Length ?? 0;

- C# Analyses and Refectore .... Extenseion in Visual Studio zuhause installieren.
- `nameof()` Operator verwenden.
- `catch (Exxeption ex) when (ex.InnerException == null)`
- `using static System.Console` dadruch muss ich die Klassen
    nicht mehr davor schreiben.
- **Auf NuGet Überschreibungen achten!**