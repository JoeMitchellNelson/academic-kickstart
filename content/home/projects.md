+++
# A Demo section created with the Blank widget.
# Any elements can be added in the body: https://sourcethemes.com/academic/docs/writing-markdown-latex/
# Add more sections by duplicating this file and customizing to your requirements.

widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 35  # Order that this section will appear.

title = "Data Viz"
subtitle = ""

[design]
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns = "1"

[design.background]
  # Apply a background color, gradient, or image.
  #   Uncomment (by removing `#`) an option to apply it.
  #   Choose a light or dark text color by setting `text_color_light`.
  #   Any HTML color name or Hex value is valid.

  # Background color.
  # color = "navy"
  
  # Background gradient.
  # gradient_start = "DeepSkyBlue"
  # gradient_end = "SkyBlue"


  # Text color (true=light or false=dark).
  text_color_light = false

[design.spacing]
  # Customize the section spacing. Order is top, right, bottom, left.
  padding = ["20px", "0", "20px", "0"]

[advanced]
 # Custom CSS. 
 css_style = ""
 
 # CSS class.
 css_class = ""
+++

Below are some "extra-curricular" data vizualizations I'm especially proud of.

<HR>

I originally made the app below to help my wife think about where we might move after grad school.  It's a strictly unscientific tool that's meant to be played with, to get a sense of where you might like to live. Move the sliders right or left to indicate the importance of each characteristic to you and receive a list of the counties that maximize those characteristics. You can also impose hard cut-offs for some variables. Behind the scenes, each slider controls a parameter in a linear utility function. The variables are transformed to be z-scores, to give them (somewhat) comparable units. Code/data are on my <a href="https://github.com/JoeMitchellNelson/location-preferences">Github</a>. You'll need an API key from the Census Bureau to run the code, which can be obtained <a href="https://api.census.gov/data/key_signup.html">here</a>.


<iframe style="padding-left:-100px; margin-left:-120px" height="750" width="150%" frameborder="no" src="https://joemitchellnelson.shinyapps.io/location/"> </iframe>

<p style="line-height:1.2;"><font size=2><i>Notes: Climate security</i> uses county estimates from <a href="1362.full?ijkey=x3wZ8kcgtomUM&keytype=ref&siteid=sci">Hsiang, Solomon, et al. (2017)</a>. <i>High school graduation rate</i> data comes from <a href="https://www.countyhealthrankings.org/sites/default/files/media/document/analytic_data2020_0.csv">Countyhealthrankings.org</a>, and partially imputed using demographic information from the Census Bureau. <i>Air quality</i> data also comes from Countyhealthrankings.com. Countyhealthrankings.com also provides incomplete <i>violent crime</i> data, which I supplemented with data from the FBI's <a href="https://www.fbi.gov/services/cjis/ucr">Uniform Crime Reporting</a>.  <i>Mild summers</i> and <i>mild winters</i> calculate the highest average monthly maximum temperature in the hottest month (for summers) and lowest average  minimum temperature (for winters), which are then each averaged over the last decade in each county. Data comes from NOAA. <i>Distances to MSAs</i> are calculated as distance from county-centroid to MSA-centroid using shape files provided by the Census Bureau. <i>Politics</i> is determined by 2016 vote shares in each county, as reported by the <a href="https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ">MIT Election Lab</a>. <i>Housing affordability</i> is measured as median monthly housing cost, as reported by the Census Bureau's 5-year American Community Survey. My wife and I (separately) consistently receive recommendations for counties in Oregon, Washington, and Colorado. Sometimes we also get counties in the Great Lakes area or the suburbs of D.C.</font></p>



<HR>

Some recent studies have found significant effects of COVID-19 lockdowns on air quality, especially in cities like <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7189867/">Delhi</a>, <a href="https://www.sciencedirect.com/science/article/pii/S0048969720326024">Rio de Janeiro</a>, and <a href="https://www.thelancet.com/pdfs/journals/lanplh/PIIS2542-5196(20)30107-8.pdf">Wuhan</a>. I was curious to see if similar effects were apparent in urban areas in the U.S., so I plotted 2020's PM<sub>2.5</sub> data for New York City, compared to recent years. The code and data to produce this plot are on my <a href="https://github.com/JoeMitchellNelson/pm25_covid">Github</a>.


<a href="https://raw.githubusercontent.com/JoeMitchellNelson/pm25_covid/master/pm25_plot.png"> ![](https://raw.githubusercontent.com/JoeMitchellNelson/pm25_covid/master/pm25_plot.png)</a>

<HR>

I handled technical implementation to produce the animation below, in a joint effort with <a href="https://www.linkedin.com/in/jo-sherrod-50975014/">Joanne Sherrod</a>. It was featured in <a href="https://www.fastcompany.com/90492485/this-detailed-map-graph-traces-a-damning-trump-timeline-as-covid-19-spread-through-the-u-s">Fast Company</a>, tweeted by AFT president <a href="https://twitter.com/rweingarten/status/1252410845557997568?s=20">Randi Weingarten</a>, and shared on Facebook more than 7,000 times. You can find the code on my <a href="https://github.com/JoeMitchellNelson/Covid-19-map">Github</a>.
<br>

<strong>"I don't take responsibility at all"</strong>

![](https://i.imgur.com/rZzmKnh.gif)



