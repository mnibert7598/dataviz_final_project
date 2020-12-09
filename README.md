# Data Visualization and Reproducible Research

> Morgan Nibert

Learn more about me from my [profile](https://github.com/mnibert7598)


The following is a sample of visualizations I created from the three projects I worked on during my semester in the _"Data Visualization and Reproducible Research"_ course offered at Florida Polytechnic University in Fall 2020.


## Project 01: Exploring US Births

<br>

In the `project_01/` folder you can find my full report exploring U.S. Births from 2000 to 2014. While working on this particular mini project, I practiced how to clean data that included dates and times on top of how to create meaningful and visually appealing graphs that represent the story of the data. 

<br>

**First Visualization: Births per Year** 

Below we have my first created visualization that shows us the number of births in millions for each year in the dataset. 

Given the shape of the graph as well as the coloring applied we can see that there is a spike in births in 2007 followed by a lower number of births in the latter half of the dataset. 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/birthsbyyear_01.png" width="70%" height="70%">

**Second Visualization: Births per Month and Year**
<br>
Originally, I had created a scatterplot of the number of births for each month of each year over the 15 year period. I had colored the scatterplot so each year had a different color. Overall, you could see the same arch that we see in my first visualization. However, my professor suggested that it was hard to see the color differences in the scatterplot for each year and countered that I provide a lollipop graph instead. My first attempt at a lollipop graph yielded mixed results. I could now definitively see the different years, but the pattern was lost as the stick of each lollipop was so tall and there were so many of them. 

I then adjusted my y axis boundaries and used ggplotly in the plotly library to create an interactive graph, which I think is the best one of the iterations: 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/births_interactive_01.png" width="70%" height="70%">

In conclusion, from my initial exploratoy graphs to my enhanced graphs, you can see that in this fifteen year period, 2007 had the highest number of births. As well, you can see that August is the month of the year with the most births overall, which in turn tells us that December, October, November and January are the months with the highest  number of conceptions. 

Throughout this first project and the learning modules that followed, I was able to create the most useful graphic, my final graphic to display the number of births from 2000 to 2014. I needed time to learn more skills as well as time to listen and absorb feedback from a mentor, my professor. This was a valuable lesson as any feedback can help you create a better product. 


## Project 02: Exploring Atlanta Weather

In this project, I explored ... _[short description of your revised project goes here]_ Find the code and report in the `project_02/` folder.

**Sample data visualization:** 

_[include your favorite visualization from this project here]_
<img src="https://github.com/reisanar/dataviz_final_project/blob/main/figures/fl_higher_ed.png" width="60%" height="60%">

(you can also place your figures in the `figures/` folder and use the `![](path_to_picture)` option to add the pictures here)


## Project 03

In this project, I explored ... _[short description of your revised project goes here]_

**Sample data visualization:** 

_[include your favorite visualization from this project here]_
<img src="https://github.com/reisanar/figs/raw/master/jackie_jessie_marion.png" width="80%" height="80%">


### Moving Forward

_add here a short reflection on what you learned and what you plan to continue exploring in terms of data visualization, data storytelling, reproducible research, and/or related topics_
