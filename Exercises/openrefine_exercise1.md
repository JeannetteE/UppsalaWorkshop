OpenRefine exercises - with great thanks to Mr. Thomas Padilla, from which inspiration to the  course material is coming
[http://thomaspadilla.org/dataprep](/http://thomaspadilla.org/dataprep/)
Datasæt are from [*British Library*](http://www.thomaspadilla.org/data/dataprep/Readme.txt) - we send our gratitude

## Creatae a Project from a known, imported file
1. Open your **OpenRefine client** in order to do so, click on **[Create Project]**

1. Download the data [openrefine_authors-people.csv](openrefine_authors-people.csv) - and remember where you save it on your computer.
- Get the file & name your project
- Then click **[Next]** and the project is being created, incl all the data/fields/information, already *hidden* in the __*.csv filen__

1. **WE GO TROUGH** the different facets, funktions, features together on the board - in order to learn the TOOL and the Dataset

### FACETS

Perhaps you like to investigate, which authors there is (overview), perhaps you which to investigate, which publisher is most common

1. Click on **Publisher column** > **Select Facet** > **Select Text Facet**
- a facet/filter window pops up, and you can now start working / analyzing / cleaning up the dataset [being familiar with the data]

1. Then try to click on **Facet by 'count'** to the left > Observe the amount of hits/records from the publisher *Titan*

1. Next step can be clicking at **Facet by 'name'** *next to facet by count* - > Scoll down to *Titan* > Observe the many different representations of the publisher *Titan*


### Filtrering the data

Each column contains a *'text filter'* option. funktion. A **'text filter'** is useful for identifying similar Data content
- will provide you with information on, whether the data are correct, alike and valide (registered in the same way )

1. eksempelvis kan man editere ukorrekte poster een for een, eller i clusters
- vi tager hul på edit
- vi tager hul på cluster
( både publisher kolonne, samt årstal og sted for udgivelse renses op )

se evt. mere via [GitHub vejlednings siden](https://github.com/OpenRefine/OpenRefine/wiki/Clustering-In-Depth)

### Transformér data

Kan ske enten som ovenfor, via enkelte ændringer i konkrete poster, eller man kan anvende et kommando "SPROG" kaldet GREL ( Google Refine Expression Language ).
I dag skal vi blot tjekke tegn fra forfatterfeltet, som forstyrrer - herunder et punktum, blanktegn..

1. gå tilbage til jeres projekt
1. vælg kolonnen [ Author ] -> vælg [ EDIT CELLS ] og dernæst [Transform]
- et vindue popper op
1. klik følgende kommando ind **value.replace('.', ' ')**
- det betyder, at alle punktummer erstattes af et blankt tegn = ingenting ( en form for **søg og erstat**, men blot udtrykt i GREL kommando )

GREL er et sprog for sig, som kræver mere af os end vi kommer til at nå i dag, men når vi skal lege mere med dette senere hen
så kan man med fordel finde hjælp via gode sider som [https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions](https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions)
eller andres [opskrifter og erfaringer](https://github.com/OpenRefine/OpenRefine/wiki/Recipes)

### gem vores **KODE** som en json fil til en anden gang..

1. klik på UNDO/RESET - og vælg [ Extract ]
- to sider popper op, og I klikker CTRL+A og CTRL+C og åbner en Notepad og klipper KODEN ind CTRL+V
- gem til senere, når vi gentager processen med samme __*.csv fil__


### Eksporter vores dokument

1. fjern alle filtre, klik på EXPORT i øverste højre hjørne ( vælg .excel og åbn i excel for at se dokumentet heri.. )
- forsøg evt. at lave "søg og erstat" på årstal i dokumentet via excel..

### Forfra ...

1. åben filen igen - og opret et nyt projekt, følg de få trin og VOILA ( tilbage til start... )
1. klip fra Notepad den KODE ind via UNDO/REDO -> APPLY og [ Perform Operations ]

#### Er der mere tid, så kan I foretage samme tjek af en fil med PhD afhandlinger fra DTU ORBIT/PURE
