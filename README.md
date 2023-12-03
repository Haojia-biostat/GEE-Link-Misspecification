Motivating example: We would like to assess the performance of the implementation of multifaceted intervention, including clinician-facing reminders and an electronic health record (EHR)-integrated shared-decision-making (SDM) tool, on the lung cancer screening outcome, care-gap closure. The assumed growth pattern of the care-gap closure rate is linear during each of the two 12-month pre- and post-intervention periods.
Simulation study problem: The motivating example could be generalized to a simulation study problem that, what is the consistency of GEE estimates when the distribution of outcome and/or link function is mis-specified.
I added distribution to this question since I found the “binomial” distribution does not accept the identity link function.
According to Park and Weisberg (1995), “Fisher consistent estimates will be obtained as long as certain conditional expectations among the predictors are linear. This condition is always satisfied when predictors are normally distributed, or more generally with elliptically contoured predictors, but the condition may be satisfied at least approximately for many other distributions for the predictors, or for particular values of the regression coefficients.” So I also want to try different distributions of predictors in the simulation study.
The data to be simulated will include the following variables:
1.	Binary outcome Y
2.	Time t from 1 to 24
3.	Binary indicator of intervention (intervention): 0 when t <= 12 and 1 when t > 12
4.	A third predictor from different distributions, including normal, binomial, poisson, and log-normal.
I am going to assume the following:
1.	The monthly growth rate is 1%, 5%, and 20% during baseline period and the effect size of change of slope is 0.2 or 0.4.
2.	The number of subjects is 100 and 1000;
3.	Within subject correlation is 0.1, 0.3.
I am going to perform the following simulation:
1.	For each combination of the simulation variables, I will simulate 1000 data sets.
2.	For each simulated data set, I will fit (1) the correctly specified GEE with binomial distribution and logit link, (2) poisson distribution and identity link, (3) gaussian distribution and identity link.
3.	For each combination of the simulation variables, I will calculate the power of detecting the true rate, type I error and bias.
