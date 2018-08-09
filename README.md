# Sun-Models
Predicting the median cost of a solar panel system installation across the U.S. on a zip code basis. Analyzing the expected ROI of the installations and potential environmental impact.    


![Sun Models](https://github.com/jnlevine23/Sun-Models/blob/master/Img/platform_sun_models.png?raw=true "Sun Models")
*Each point represents a unique zip code.*    


Sun Models is the final project I worked on while at Metis. It's a project I was excited to start working on because I was curious about how I could apply some of the data science concepts I learned to a problem within the renewable energy industry.

_**Disclaimer**: All estimates I've provided are pre tax and pre solar incentive. All estimates are also adjusted for inflation. With tax options and solar incentives applied, the cost of a solar panel installation can decrease by up to 50% in certain areas of the U.S. and payback period can potentially be cut in half._

The goal of the project was to predict the median cost of a solar panel installation for particular zip codes in the U.S. Unfortunately I was not able to gather substantial data from 2016, 2017, or 2018, so my predictions were made using test data from 2015. I applied a custom time series autoregressive approach to the problem to make my predictions as accurate as possible. However, there were several zip codes that I did not have multiple past years of pricing information for. I found that focusing on zip codes that had at least 4 years of prior pricing information available allowed me to strike a good balance between the accuracy of my predictions and the number of zip codes I would be able to use. Although this approach did force me to exclude a fair amount of data, I still was able to make accurate predictions for nearly 4,000 unique zip codes.

By gathering additional data on utility rates across the country and annual energy consumption statistics, I performed a Cost-Benefit Analysis to calculate the expected savings over a 25 year period as well as the payback period for homes that installed solar energy systems in the particular zip codes I was looking at. Information about the expected amount of electricity produced and expected value of the electricity produced on an annual basis is also available, as well as information about the median amount of sun exposure for the roofs in a zip code.

I then wanted to include some kind of metric for "scoring" the impact of having a solar energy system on your roof, so I turned to Google's Project Sunroof and scraped data regarding the potential environmental impact of installing solar panels. This data allows us to see the amount of Carbon Dioxide emissions avoided, the equivalent number of cars taken off the road for 1 year, and the equivalent number of new trees grown over a 10 year period for a particular zip code if all viable roofs were to have solar panels installed on them. 

Using CartoDB, I created an interactive platform that allows the user to explore information about the zip codes I gathered on a map of the United States. The user can click or search for specific areas of the U.S. and see the median cost of a solar energy system installation in their respective area along with the full expected ROI results, potential environmental impact, and more. I hope that this tool can give individuals interested in going solar a high level overview of what to expect in their area, and allow vendors to see areas of the U.S. with high potential for solar growth.

_**Explore the [Sun Models](https://jnlevine23.carto.com/builder/1baadc68-df69-4360-8cd3-3d04e5b9fefd/embed) platform.**_

_Full presentation can be viewed [here](https://github.com/jnlevine23/Sun-Models/blob/master/presentation.pdf)._
