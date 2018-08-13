# Boston- Green Scope Map


## Datasets
**Bike Network Data from Boston Maps Open Data**

**Neighborhood Data from Analyze Boston**

**Hubway Station Data from Analyze Boston**

**Charging Station Data from Boston Maps Open Data**

**Open_Space.csv from BostonMaps: Open Data;**


## Narrative
Expanding public transportation and car sharing are two of the most popular solutions to reduce emissions in urban environments. However, these options are not necessarily zero emission options and may still pollute the environment. Therefore it's important that more effective measures be considered to reduce emissions.

By looking at charging stations, hubway stations, biking networks, and open space data in each Boston neighborhood we determined a green score for each neighborhood. From here we created a statistical analysis in an attempt to find out if there exists any correlation between subset entities of our data and if these correlations corresponded to the number of placements of select entities in each neighborhood. To do this, we iterated through all the possible subsets of two entities within neighborhoods and calculated correlations.

Finally we took the green scores we computed initially and set up a constraint satisfaction problem where we attempted to optimize the green score for each neighborhood given a budget of $1,000,000. The constraints we added attempted to make the computation realistic, meaning that solutions of 0 or less than 0 were not acceptable, in an effort to deplete the budget.We also randomized the maximum and minimum number of specific entities that could be built in neighborhoods in an effort to create a unique solution for each neighborhood.

Moreover, we have made a web visualization which uses flask to retrieve the data from our mongo db collections, and presents the data using leaflet js , and an interactive slider made using D3.js which invokes our modified constraint satisfaction algorithm which we tweaked to include a higher range of budgets and more constraints. The interactive visualization lets the user pick through a range of budgets and watch the number of green facilities/services change as well as the score with each budget. 

There is a supplemental report and presentation as well. 



## Setting Up
Please run neighborhoodscores.py, followed by budgets.py, and then run app.py ** it must be in this order to work. 
The web visualization will be made available at localhost:3000



Notes:
Our Z3 files are modified slightly:
For Z3core, Z3printer and Z3 we removed the ". import" lines
If you do not have z3 on your machine we have added a supplementary folder which contains z3, all that needs to be done is to move the files inside the folder to the parent file titled francis_jrashaan. Additionally, we set the trial parameter to true.






