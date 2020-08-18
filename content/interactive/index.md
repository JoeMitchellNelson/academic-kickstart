---
title: Open-ended contingent valuation
summary: An alternative to dichotomous choice survey instruments
date: "2018-06-28T00:00:00Z"

runtime: shiny
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

Contingent valuation methods attempt to value goods and services that are not traded in markets and for which no price information exists. A common technique involves presenting subjects with two or three alternatives, described in terms of several attributes, and allowing them to choose their most preferred alternative. However, many subjects find this survey method unfamiliar, and extensive introductory language is often necessary to prepare subjects for the choice tasks and to avoid scenario rejection. Additionally, this survey method rarely identifies the peak of a subject's utility maximization problem. 

I propose an alternative survey instrument in which subjects choose the levels of relevant attributes and receive feedback about the associated costs. After some experimentation, subjects can express their ideal mix of attributes, conditional on a behind-the-scenes cost constraint.

Below is an example choice task. Subjects express their ideal pandemic policy using sliders that govern the level of restrictions on 10 businesses and activities. Moving any slider automatically updates the estimated deaths and cases in their community, and the estimated loss of income per household, due to job losses and a slowed local economy.

<iframe style="padding-left:-100px;" height="800" width="140%" frameborder="no" src="https://joemitchellnelson.shinyapps.io/survey-instrument/"> </iframe>

