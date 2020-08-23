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

@media screen and (max-width: 500px) {
  iframe {
    padding-left:0px !important; 
    margin-left:0px !important;
    width: 100%;
  }
}
</style>

Below is an example choice task. <strong>Try it!</strong> (Note: it's not yet optimized for mobile browers.)

<iframe style="padding-left:-100px; margin-left:-100px" height="800" width="140%" frameborder="no" src="https://joemitchellnelson.shinyapps.io/survey-instrument/"> </iframe>

Stated preference methods attempt to value goods and services that are not traded in markets and for which no price information exists. A common technique involves presenting subjects with <u>two or three alternatives<span>Typically one alternative is "the status quo" or the option to forgo all costs and benefits associated with the good or service being valued.</span></u>, described in terms of several <u>attributes<span>For example, a subject may be given a choice among three alternatives: <i>car A</i>, <i>car B</i>, or <i>no car</i> (the status quo alternative). Each alternative might then be described in terms of the attributes horsepower, fuel economy, and cost. The <i>no car</i> alternative comes with no horsepower or fuel economy, but also no cost. Cars A and B are assumed not to differ except in their described attributes.</span></u>, and allowing them to choose their most preferred alternative. However, many subjects find this survey method unfamiliar, and extensive introductory language is often necessary to prepare subjects for the choice tasks and to avoid scenario rejection. Additionally, this survey method rarely identifies the peak of a subject's utility maximization problem.

<strong>I (re-)propose an interactive survey instrument</strong> in which subjects choose the levels of relevant attributes and receive feedback about the associated costs. After some experimentation, subjects can express their ideal mix of attributes, conditional on a convex behind-the-scenes cost constraint. A similar survey method, using continuous attributes, was proposed and piloted in Ready et al., 2005. In the continuous case--which the authors call "continuous attribute-based stated choice method" or CABSCM--marginal willingness to pay can be identified uniquely for each respondent, provided their response is <u>an interior solution<span>"Interior" meaning the respondent did not choose the highest or lowest allowed values for any attributes. When this occurs, it is still possible to say that a subject's willingness to pay for that attribute is <i>at least</i> or <i>at most</i> a particular value.</span></u>. 

Each CABSCM subject provides a tremendous amount of information, and subjects in the pilot studies reportedly preferred CABSCM to more traditional stated preference methods. Despite these advantages, Ready et al.'s method appears <u>not to have caught on<span>2005 may have been too early for a strictly computer-based instrument to gain traction. Plus "CABSCM" doesn't really roll of the tongue.</span></u> among stated preference researchers. I hope to revive interest in this method and to demonstrate its applicability to a more complicated choice architecture.

The example choice task above is a discrete-attribute variation of CABSCM. Subjects express their ideal pandemic policy using sliders to control the level of restrictions on 10 businesses and activities, choosing one for four levels for each. Moving any slider automatically updates the estimated deaths and cases in their community, and the estimated loss of income per household, due to job losses and a slowed local economy. The functions mapping the restrictions to cost, cases and deaths are governed by 30 parameters, randomly generated for each subject. The discrete version of CABSCM <u>doesn't permit precise identification<span>In the present case, precise identification for every parameter of interest wouldn't be possible even with continuous attributes because attribute levels determine not only cost, but also cases prevented and deaths avoided.</span></u> of each subject's marginal willingness to pay for each attribute, but still provides far more information than traditional methods. 

This survey instrument accommodates <u>standard econometric techniques<span>When the levels of alternatives are discrete (as above) multinomial logistic regression can identify the relevant parameters in subjects' indirect utility function, and heterogeneity analysis can be performed in the usual way. In a typical contingent valuation framework, however, subjects choose among a small number of alternatives. Here, the "alternative-space" is very large (there are 4^10 in the above example), so a random sample of unchosen alternatives in each choice task can be selected by the researcher for use in estimation.</span></u>, but we can do better. (Write up coming soon.)



