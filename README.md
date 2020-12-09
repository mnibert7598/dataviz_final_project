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

Originally, I had created a scatterplot of the number of births for each month of each year over the 15 year period. I had colored the scatterplot so each year had a different color. Overall, you could see the same arch that we see in my first visualization. However, my professor suggested that it was hard to see the color differences in the scatterplot for each year and countered that I provide a lollipop graph instead. My first attempt at a lollipop graph yielded mixed results. I could now definitively see the different years, but the pattern was lost as the stick of each lollipop was so tall and there were so many of them. 

I then adjusted my y axis boundaries and used ggplotly in the plotly library to create an interactive graph, which I think is the best one of the iterations: 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/births_interactive_01.PNG" width="70%" height="70%">

In conclusion, from my initial exploratoy graphs to my enhanced graphs, you can see that in this fifteen year period, 2007 had the highest number of births. As well, you can see that August is the month of the year with the most births overall, which in turn tells us that December, October, November and January are the months with the highest  number of conceptions. 

Throughout this first project and the learning modules that followed, I was able to create the most useful graphic, my final graphic to display the number of births from 2000 to 2014. I needed time to learn more skills as well as time to listen and absorb feedback from a mentor, my professor. This was a valuable lesson as any feedback can help you create a better product. 


## Project 02: Exploring Atlanta Weather

In this second mini project, I explored the 2019 Atlanta Weather dataset. This dataset included 39 variables for an entire (365 datapoints) year. Variables ranged from the description of the icon used to depict the weather for a given day to precipitation, humidity, wind speed, temperature and visibility information. 

While working on this second mini project, I further practiced how to clean data and I learned that to create a good visualization, you had to keep your story simple. This is why I chose the weather data in the first place, I didn't want to let my brain wander too far and (initially) I thought weather wouldn't be too complicated. 

Find the code and report in the `project_02/` folder.

**First Visualization: High Temperatures in Atlanta** 

First graph I wanted to look at was the high temperatures over the entire year. Here, we can see they shape a nice bell-like curve with the highest of temperatures in the middle of the year during the summer months. 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/high_temp_02.PNG" width="70%" height="70%">


**Second Visualization: Precipitation in Atlanta** 

The next visualization I wanted to produce was a basic histogram plot to look at the precipitation over Atlanta for the year of 2019. 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/precip_02.PNG" width="70%" height="70%">

In this graph, we can see that the month with the highest amount of precipitation is February and the lowest month is September for Atlanta in 2019.


**Third Visualization: Precipitation & Temperature in Atlanta** 

Although I made several graphs beforehand depicting this same information, one just for temperature, one for precipitation by month, this last visualization would be the one that I would show to an audience. It contains all of the information I was trying to relay. 

<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/precip_heat_02.png" width="70%" height="70%">

Some improvements that could be made would be inputting a range selector like from dygraphs. This would allow a user more of a tool to get any information they were interested in. It would also add more information to the graph itself because we could then see each individual date. 



## Project 03: Recreating Graphics for Tampa Weather

In this mini project I explored recreating multiple types of graphs that could be used to express the same variable to an audience. All different types of graphs than I knew prior to use, much better than what I used in my mini project 2. 


**Maximum Temperatures by Month (counts):** 
<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/max_temp_month_03.png" width="80%" height="80%">


**Maximum Temperatures by Month Density Ridges:** 
<img src="https://github.com/mnibert7598/dataviz_final_project/blob/main/figures/geom_ridges_03.png" width="80%" height="80%">

This project was helpful as an exercise. I had to learn how to not only create these graphs just from visuals provided, but also how to design them. I decided (creatively) that my first graph is better than the one provided, but that may be just because I'm blind and it's hard to read histograms that small for me so gridlines help. 

This project also showed me that there can be many types of graphs that can represent the same information, here we created 5 different plots to represent maximum temperatures in Tampa, mainly by month. The lesson would be that you shouldn't settle on your first visualization or type of, you should play around with different versions and pick the one that relays to the audience the message you want the best. 

## Moving Forward

_add here a short reflection on what you learned and what you plan to continue exploring in terms of data visualization, data storytelling, reproducible research, and/or related topics_

This semester I learned a lot of extremely useful things. I'm so glad I took it before I start my Master's project next semester. Top five things learned:
1. **Decide what you're trying to say.** Ensure your content is tailored to the most essential idea you want your audience to leave with. Use the KISS (Keep it Simple Stupid) method. 
2. **Choose the Right Chart Type.** This may take multiple tries and different attempts. Don't be afraid to try different things and research new methods. 
3. **Take advantage of color theory.** Keep color schemes consistent throughout and use clear contrasting, yet complementary, colors to distinguish important elements. 
4. **Know Your Audience.** Your audience doesn't know anything more about the data other than what you're presenting to them. It should be fitted to their understanding and same as when you are deciding on your story.... KISS.
5. **Resources. Resources. Endless Resources.** There are SO many resources out there for data visualization techniques. Keep up to date and learn new things often. Don't be afraid to seek out opinions on your first run, second run, n run... room for improvement doesn't mean failure. 
