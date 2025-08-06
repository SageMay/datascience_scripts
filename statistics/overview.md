# Overview

Statistics are a core element of sharing scientific data, but it is a complicated field and can be challenging to know where to begin. 
The notebooks here are intended to guide some basic analyses that we commonly perform. 

# Core ideas before diving in
# 1. p values aren't everything
Statistics are more about characterizing data than proving hypotheses.
This is why we use the wording "We reject the null hypothesis" rather than "we prove the alternative hypothesis". 
The second statement is false -- stats can't prove a hypothesis, but they can demonstrate that a null hypothesis probably doesn't explain the data. 
So, when you see a p value of .04, it is saying "If my null hypothesis is true, there would be a 4% chance of this outcome."
Usually, 5% chance, or a p value of .05 is the criteria (also called alpha level) for "statistical significance," but inherently this is an arbitrary choice.
And that's only the first choice we make. 

# 2. Effect size is a key measurement to report
While we often default to talking about p-values, the statistical significance of data is often aside from the point of the science. 
We have to measure effect sizes, which tell us more about the importance of a change (see (1) for more on effect sizes -- this referenced informed this section). 
There are different measures of effect sizes. 
Commonly, for correlating variables, the r2 values is the effect size we'd look at. 
And an effect size called Cohen's d is used in the powerAnalysis notebook to estimate the number of samples that would be needed if the differences observed in a pilot study are representative of the underlying data. 
A core idea behind effect size is that the differences observed between two groups is normalized agains the standard deviation. 

# 3. Power level
In order to perform a power analysis, you will need to set a threshold beta, which is the liklihood of concluding there is no effect (null) when in reality there was an effect. 
This is a type II error, and usually, we are more lenient in allowing type II errors (falsely accepting the null hypothesis) than of falsely rejecting the null hypothesis.
Commonly beta is chosen as .2 (or 20%), but this value may not be appropriate for your study and is grounded in the assumption that a type II error is not as serious as a type I error. 
It is critical to think this through for each study -- are there large risks associated with type II error? 
For example, if you are designing software to identify potential tumors from imaging data, it would be far better to flag more images as potential tumors than to falsely accept the null (the null being that the tissue does not have a tumor). 
A power analysis will help determine how many samples are needed -- it should be run at the beginning of a study and inform the study design, not performed after the study has been run. 

# 4. p hacking
And, we've all heard about p-hacking, where more samples are gathered just to achieve statistical significance. 
It turns out this can be a challenge for MD data. 
At times, we have so many individual data points that a statistical test shows a significant difference, but in reality, the effect size may be very small. 
And, the physical changes in conformation may or may not be important to function, regardless of the statistical significance of the data.



# References
1. https://pmc.ncbi.nlm.nih.gov/articles/PMC3444174/
Using Effect Size—or Why the P Value Is Not Enough
Gail M Sullivan, Richard Feinn