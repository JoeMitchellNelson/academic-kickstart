+++
# A Demo section created with the Blank widget.
# Any elements can be added in the body: https://sourcethemes.com/academic/docs/writing-markdown-latex/
# Add more sections by duplicating this file and customizing to your requirements.

widget = "blank"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 50  # Order that this section will appear.

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

<table style="width:100%; border: 0px solid black;" >
  <tr>
    <td width="200"><img src="https://www.joemitchellnelson.com/img/websitethumbnail1.png" width="200"></td>
    <td style="text-align:left;vertical-align:top;border: 0px solid black; padding:10px;">I originally built this app to help both my own household and my graduate classmates think about where we/they might like to make a home after finishing graduate school. This tool is for “recreational” use only. It is not completely scientific (and is, of course, provided without warranty). Directions for use: Move the sliders right or left to indicate the importance (weight) of each characteristic in your utility function and the app will return a list of the counties that maximize that function. It is possible to impose hard cut-offs for some variables. How it works: Behind the scenes, each slider controls a parameter in a simple linear utility function. The variables are first transformed into Z-scores, to put them in (somewhat) comparable units. Archive for code/data: Github. Other necessary components: An API key from the Census Bureau.</td>
  </tr>
  <tr>
    <td width="200"><img src="https://www.joemitchellnelson.com/img/websitethumbnail2.png" width="200"></td>
    <td style="text-align:left;vertical-align:top;border: 0px solid black; padding:10px;">I handled technical implementation to produce the animation below, in a joint effort with Joanne Sherrod. It was featured in Fast Company, tweeted by AFT president Randi Weingarten, and shared on Facebook more than 7,000 times. You can find the code on my Github.</td>
  </tr>
    <tr>
    <td width="200"><img src="https://www.joemitchellnelson.com/img/websitethumbnail3.png" width="200"></td>
    <td style="text-align:left;vertical-align:top;border: 0px solid black; padding:10px;">Some recent studies have found significant effects of COVID-19 lockdowns on air quality, especially in cities like Delhi, Rio de Janeiro, and Wuhan. I was curious to see if similar effects were apparent in urban areas in the U.S., so I plotted 2020’s PM2.5 data for New York City, compared to recent years. The effect of the (first) COVID-19 lockdown is visually apparent but smaller than one might hope for. The code and data to produce this plot are on my Github.</td>
  </tr>
</table>
