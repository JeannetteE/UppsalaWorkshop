OpenRefine exercises - with great thanks to Mr. Thomas Padilla, from which inspiration to the  course material is coming
[http://thomaspadilla.org/dataprep](/http://thomaspadilla.org/dataprep/)
Datasæt are from [*British Library*](http://www.thomaspadilla.org/data/dataprep/Readme.txt) - we send our gratitude

## Create a Project from a known, imported file
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

Each column contains a *'text filter'* option. The **'text filter'** is useful for identifying entries similar Data content
- and will provide you with information on, whether the data are correct, similar and/or valid (registered in the same way )

1. For instanse you can easily edit in-correct entries/records one by one, or as clusters

- we begin with **edit**
- and then continue with **cluster**
( both for the *publisher column*, *year* and *place of publication* )

See more in the [GitHub guide](https://github.com/OpenRefine/OpenRefine/wiki/Clustering-In-Depth)

### Transform data

Can be done the same way as **filtering** - but OpenRefine uses a command *language* called GREL ( Google Refine Expression Language ).
We will not work too much on the *language* but use **simple commands** to *clean up basic irregularities* from the entries like __blank signs, punctuation and the like__ (to start with from the *author field* )

1. Return to OpenRefine and your project
1. Choose the column __[ Author ]__ -> choose __[ EDIT CELLS ]__ and then click on __[Transform]__
- a new window opens
1. Then add the command **value.replace('.', ' ')**
- this command means, that every punctuation will be replaced with a blank = nothing ( similar to **search and replace** known from Excel, but now expressed in a GREL command )

GREL is a *bit* more advanced, and demands more in depth knowledge than this workshop will cover, but for later please have a look at [https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions](https://github.com/OpenRefine/OpenRefine/wiki/Understanding-Regular-Expressions)
or other [recipes and experiences](https://github.com/OpenRefine/OpenRefine/wiki/Recipes)

1. Try working with __Edit__, __Cluster clean up__ and __Transform data__ in your own pace.

### Save the generated **CODE** as a json file for later / reuse.

1. Click on __UNDO/RESET__ - and choose [ Extract ]
- two pages appears, You have to mark is (*cut and paste*) with __CTRL+A and CTRL+C__ - then open an Editor __Notepad or ATOM__ and paste the CODEN in __CTRL+V__
- Save it for later, because we will re-do the whole process once more with the same __*.csv fil__


### Eksport the final **cleaned** dokument

1. Remove all the used filters, Click at **EXPORT** in the top right corner ( choose __*.excel__ and open your *EXCEL* to see how the document looks like )


### Starting OVER ...

1. Open the file once more - create a new project, follow the few steps and VOILA ( your dataset is ready to start over ... )
1. Cut and paste from your editor __Notepad or ATOM__ the json CODE you generated and place it via __UNDO/REDO__ -> __APPLY__ og __[ Perform Operations ]__
1. then everything happens __*Automatically*__ :)
