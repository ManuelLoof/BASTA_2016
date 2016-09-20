# BASTA! 2016 #

## Flexbox (CSS) ##

> Speaker: Timo Korinth  (MAXIMAGO)
> Date: 29.09.2016

### CSS ###

- `display: flex;`
- `flex-direction: row | row-reverse | column | column-reverse`
- `flex-row: <number>;` // Wie groß soll der Container wachsen
    - 0 nicht wachsen (default)
    - 1 nimmm alles (strech)
- flex-basis: <length> | auto;
    - auto nimmt die größe des Inhalts
- `flex-shrink: <number>;` // Darf das Element schrumpfen
    - `flex <grow> <shrink> <basis>` // Kurzschreibweise
- äußersten Container width und height auf 100 % setzten.



### Beispiel ###

Container
{

Header:
{
`flex: 0 0 auto;`

Nicht schrumpfen nicht wachsen und Anfangsgröße wie Inhalt.
}

Main:
{

`flex: 1 1 100%;`

Wächst.
}
}


### Beispiel 2 ###

Container
{
    NAV

    flex: 0 0 auto;

    CONTENT

    flex: 1 1 100;

}

#### Beispiel 4 ####


    .applicationRoot{
        display: flex;
        flex-direction: column;
    }

    .header, .footer{
        flex: 0 0 auto;   
    }

    .holygrail-body{
        flex: 1 1 100%;
        display: flex;
    }

    nav, aside{
        flex: 1 1 15%;
    } 

    nav{
        order: -1;
        overflow: auto;
    }


### Browser Prefix ###

- Mixins
- Autoprefixer

- display: flex;
- display: moz-...
- display: ...

### Flexbox Alternative => Gridlayout ###

- Wird zurzeit nicht unterstützt.


### Best Practises ###

- Less und Sass
- Mixins für Browser Prefixe oder Autoprfixer
- Überall nutzen (auch tiefe Verschahatelungen)
- Wichtigste Einstellungen:

    flex: 0 0 auto;
    flex: 1 1 100%;


### Resonsive ###

**ToDo Folien Grafik hier einfügen**


### Performance ###

- Old flexbox `display:box` ist sehr langsam `display flex:` ist besser!!!!!
- Flexbox ist 4 mal schneller als float

### Zukunft ###


### Urls ###


### Tipps und Tricks ###

- Angular cli
. Bei angular2 nach Start Projekte gucken.
- CSS Animations angucken.
- Media Queries
- Angular Material