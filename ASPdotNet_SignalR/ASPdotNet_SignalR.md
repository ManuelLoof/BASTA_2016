# BASTA! 2016 #

## Leichtgewichtige Architekturen mit ASP.NET Web API & SignalR ##

> Speaker: Christian Weyer  (Thinktecture AG)
> Date: 20.09.2016

** Folien Url einfügen **

### Architekturen  ###

- ASP.NET Web API eigenes Framework
- Hat nichts mit ASP.NET zutun und kann auchni anderen Programmen verwendet werden.
- Owin nutzen um Anwendung selber zu hosten. Abstraktionslayer.  Dann brauche ich keinen IIS.
    `Microssoft.Owin.Host.SystemWeb`
- SignalR => Pushservice
- Periodic Polling
- Long Polling der Client fragt
- WebSockets der Server antwortet


### Urls ###



### Tipps und Tricks ###

- Token basierte Sicherheit
    - Anmelden, Token bekommen und der WebAPI mitgeben.
- Visual Studio Tools für node.js