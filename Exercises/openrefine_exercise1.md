Opgavesæt nr. 1 - en stor tak til Thomas Padilla, som har udarbejdet materialet, og som jeg har oversat til "IKON´sk" 
[http://thomaspadilla.org/dataprep](/http://thomaspadilla.org/dataprep/)
Datasæt er fra [*British Library*](http://www.thomaspadilla.org/data/dataprep/Readme.txt) - vi sender en tak 

## Opret Projekt fra kendt, importeret fil
1. Åben din OpenRefine client så du kan oprette dit projet - gøres ved at klikke [Create Project]

1. Download data [openrefine_authors-people.csv](openrefine_authors-people.csv) - og husk hvor I gemmer det på jeres computer.
- hent filen og  navngiv jeres projekt 
- og klik [Next] og projektet oprettes, inkl alle de felter, som allerede er gemt i *.csv filen 
  
1. TAVLE GEMMEMGANG AF datasættets facetter og funktioner  

### FACETTER

måske ønsker man at se, hvilke forfattere der er ( overblik ), måske ønsker man at se, hvilket forlag forekommer mest..

1. Klik eksempelvis i Publisher column > Select Facet > Select Text Facet
- et facet/filter vindue popper op og man kan nu begynde at arbejde med indhold - analysere/rense op..

1. Klik derefter på Facet by 'count' til venstre > Observer antal på forlaget *Titan*

1. Klik derefter på Facet by 'name' lige ved siden af - > Scoll til Titan > Observer de foreskellige repræsentationer af forlaget Titan


### Filtrer data

Hver kolonne indeholder eksempelvis en 'text filter' funktion. Dette 'text filter' er nyttigt til at identificere lignede data indhold 
- giver en god ide om, hvorvidt data er korrekte, ens og valide i registrering )

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
- gem til senere, når vi gentager processen med samme *.csv fil 


### Eksporter vores dokument 

1. fjern alle filtre, klik på EXPORT i øverste højre hjørne ( vælg .excel og åbn i excel for at se dokumentet heri.. )
- forsøg evt. at lave "søg og erstat" på årstal i dokumentet via excel..

### Forfra ...

1. åben filen igen - og opret et nyt projekt, følg de få trin og VOILA ( tilbage til start... )
1. klip fra Notepad den KODE ind via UNDO/REDO -> APPLY og [ Perform Operations ] 

#### Er der mere tid, så kan I foretage samme tjek af en fil med PhD afhandlinger fra DTU ORBIT/PURE 
