---
title: Data visualizations
summary: 
date: "2018-06-28T00:00:00Z"

output: html_document

reading_time: false  # Show estimated reading time?
share: false  # Show social sharing links?
profile: false  # Show author profile?
comments: false  # Show comments?

# Optional header image (relative to `static/media/` folder).
header:
  caption: ""
  image: ""
---


<HR>

I originally built this app to help both my own household and my graduate classmates think about where we/they might like to make a home after finishing graduate school. This tool is for "recreational" use only.   It is not completely scientific (and is, of course, provided without warranty).  Directions for use:  Move the sliders right or left to indicate the importance (weight) of each characteristic in your utility function and the app will return a list of the counties that maximize that function.  It is possible to impose hard cut-offs for some variables.  How it works:  Behind the scenes, each slider controls a parameter in a simple linear utility function. The variables are first transformed into Z-scores, to put them in (somewhat) comparable units.  Archive for code/data: <a href="https://github.com/JoeMitchellNelson/location-preferences">Github</a>.  Other necessary components:  An <a href="https://api.census.gov/data/key_signup.html">API key</a> from the Census <a name="live">Bureau</a>.


<iframe style="padding-left:-100px; margin-left:-120px" height="770" width="150%" frameborder="no" src="https://joemitchellnelson.shinyapps.io/location/"> </iframe>

<p style="line-height:1.2;"><font size=2><i>Notes: Climate security</i> uses county estimates from <a href="1362.full?ijkey=x3wZ8kcgtomUM&keytype=ref&siteid=sci">Hsiang, Solomon, et al. (2017)</a>. <i>High school graduation rate</i> data comes from <a href="https://www.countyhealthrankings.org/sites/default/files/media/document/analytic_data2020_0.csv">Countyhealthrankings.org</a>, and partially imputed using demographic information from the Census Bureau. <i>Air quality</i> data also comes from Countyhealthrankings.com. Countyhealthrankings.com also provides incomplete <i>violent crime</i> data, which I supplemented with data from the FBI's <a href="https://www.fbi.gov/services/cjis/ucr">Uniform Crime Reporting</a>.  <i>Mild summers</i> and <i>mild winters</i> calculate the highest average monthly maximum temperature in the hottest month (for summers) and lowest average  minimum temperature (for winters), which are then each averaged over the last decade in each county. Data comes from NOAA. <i>Distances to MSAs</i> are calculated as distance from county-centroid to MSA-centroid using shape files provided by the Census Bureau. <i>Politics</i> is determined by 2016 vote shares in each county, as reported by the <a href="https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ">MIT Election Lab</a>. <i>Housing affordability</i> is measured as median monthly housing cost, as reported by the Census Bureau's 5-year American Community Survey. My wife and I (separately) consistently receive recommendations for counties in Oregon, Washington, and Colorado. Sometimes we also get counties in the Great Lakes area or the suburbs of D.C.</font></p>





<HR>

I handled technical implementation to produce the animation below, in a joint effort with <a href="https://www.linkedin.com/in/jo-sherrod-50975014/">Joanne Sherrod</a>. It was featured in <a href="https://www.fastcompany.com/90492485/this-detailed-map-graph-traces-a-damning-trump-timeline-as-covid-19-spread-through-the-u-s">Fast Company</a>, tweeted by AFT president <a href="https://twitter.com/rweingarten/status/1252410845557997568?s=20">Randi Weingarten</a>, and shared on Facebook more than 7,000 times. You can find the <a name="covid">code</a> on my <a href="https://github.com/JoeMitchellNelson/Covid-19-map">Github</a>.
<br>


![](https://i.imgur.com/rZzmKnh.gif)



<HR>

<a name="air">Some recent studies have found significant effects of COVID-19 lockdowns on air quality, especially in cities like <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7189867/">Delhi</a>, <a href="https://www.sciencedirect.com/science/article/pii/S0048969720326024">Rio de Janeiro</a>, and <a href="https://www.thelancet.com/pdfs/journals/lanplh/PIIS2542-5196(20)30107-8.pdf">Wuhan</a>. I was curious to see if similar effects were apparent in urban areas in the U.S., so I plotted 2020's PM<sub>2.5</sub> data for New York City, compared to recent years. The effect of the (first) COVID-19 lockdown is visually apparent but smaller than one might hope for. The code and data to produce this plot <a name="air">are</a> on my <a href="https://github.com/JoeMitchellNelson/pm25_covid">Github</a>.


<a href="https://raw.githubusercontent.com/JoeMitchellNelson/pm25_covid/master/pm25_plot.png"> ![](https://raw.githubusercontent.com/JoeMitchellNelson/pm25_covid/master/pm25_plot.png)</a>
