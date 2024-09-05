# Effects-of-having-children-on-parents-cognitive-function

Codes to replicate Eric Bonsang's dataset from his scientific paper from 2022 "Does Childbearing Affect Cognitive Health in Later Life? Evidence From an Instrumental Variable Approach"

Starting from the description provided in the Data chapter in Bonsang's paper, I replicated the dataset utilizing SHARE waves 1, 2 , 4 , 5 and 6, with each wave corresponding to a different year. Here's the sample description: The analytic sample includes allparticipants aged 65 or older (N = 127,036) who had only biological children (N = 100,073) and at least two children (N = 79,483). We exclude individuals whose age at the first child’s birth was below the 0.5 percentile of the gender- specific distribution and individuals whose age at the second child’s birth was above the 99.5 percentile of the gender- specific distribution (leaving N = 77,178). We exclude 478 participants who had missing values for one or more of the explanatory variables and 3,347 participants who had missing data on at least one cognitive measure. Thus, the final sample comprises 73,353 participants.

I then created a cognitive score index by Principal Component Analysis, and estimated the impact of having many children on the cognitive index through a 2SLS model and by utilizing Pearl's non-parametrical bounds, revealing a significant negative effect.  
