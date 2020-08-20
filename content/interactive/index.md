---
title: Fluid stated preference
summary: An alternative to dichotomous choice survey instruments
date: "2018-06-28T00:00:00Z"

#runtime: shiny
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

<style>

u {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black;
  text-decoration: none;
}

u span {
visibility: hidden;
  width: 350px;
  background-color: #795548;
  color: #fff;
  text-align: left;
  text-color: white;
  font-size: 15px;
  border-radius: 6px;
  padding: 10px 10px 10px 10px;
  
  /* Position the tooltip */
  position: absolute;
  z-index: 1;
  top: 100%;
  left: 50%;
  margin-left: -60px;
  
  opacity: 0;
  transition: opacity 1s;
  }

u:hover span {
  visibility: visible;
  opacity: 1;
}
</style>


Stated preference methods attempt to value goods and services that are not traded in markets and for which no price information exists. A common technique involves presenting subjects with <u>two or three alternatives<span>Typically one alternative is "the status quo" or the option to forgo all costs and benefits associated with the good or service being valued.</span></u>, described in terms of several attributes, and allowing them to choose their most preferred alternative. However, many subjects find this survey method unfamiliar, and extensive introductory language is often necessary to prepare subjects for the choice tasks and to avoid scenario rejection. Additionally, this survey method rarely identifies the peak of a subject's utility maximization problem. 

<strong>I propose an interactive survey instrument</strong> in which subjects choose the levels of relevant attributes and receive feedback about the associated costs. After some experimentation, subjects can express their ideal mix of attributes, conditional on a behind-the-scenes cost constraint.

<HR>

<iframe style="padding-left:-100px; margin-left:-100px" height="800" width="140%" frameborder="no" src="https://joemitchellnelson.shinyapps.io/survey-instrument/"> </iframe>

<HR>

Above is an example choice task. <strong>Try it!</strong> Subjects express their ideal pandemic policy using sliders to control the level of restrictions on 10 businesses and activities. Moving any slider automatically updates the estimated deaths and cases in their community, and the estimated loss of income per household, due to job losses and a slowed local economy. The functions mapping the restrictions to cost, cases and deaths are governed by 30 parameters, randomly generated for each subject. (In the widget above, the parameters are redrawn every 24 hours. At survey rollout, parameters will be randomly drawn for each choice task.)

This survey instrument accommodates standard econometric techniques. When the levels of alternatives are discrete (as above) conditional logistic regression can identify the relevant parameters in subjects' indirect utility function, and heterogeneity analysis can be performed in the usual way. In a typical contingent valuation framework, however, subjects choose between a small number of alternatives. Here, the "alternative-space" is very large (there are 4^10 in the above example), so a random sample of unchosen alternatives in each choice task is selected by the researcher for use in estimation.

When levels of alternatives are continuous, the relevant parameters can also be estimated via maximum likelihood estimation, where the likelihood function is derived from the first order conditions of the hypothesized utility function. (Proof coming soon.)


