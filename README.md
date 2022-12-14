# Che_Math
This repository was created to collect all the coded-related homework and projects developed within the course $Mathematical$ $Methods$ $in$ $Chemical$ $Engineering$ from the Chemical and Petroleum Engineering Department at the University of Pittsburgh. The programming languages used for this purpose are Julia and Python.

## Project 2: Kinetic parameter estimation from experimental dataset using Julia

1. Plotting data:
2. Solving ODE system:
3. Fitting data:
4. Bifurcation analysis:
5. Sensitivity analysis:

Missing data: The legend covers one of the lines and makes it impossible to recover this data.
Color overlapping: Due to the presence of multiple profiles and therefore colors, in some cases there is an overlapping of the profiles. If we were to zoom in, it would be evident that some fragments of the curves overlap others.
Dotted lines: Also, the style of the line becomes an additional constraint when it is dotted, and its trend is difficult to follow.

Together these three factors generate additional noise which leads to slightly different results when fitting the parameters.

Despite these limitations the tool was able to extract the information with some additional noise, in some cases more than in others. However, we can say that all species follow the original trajectory.

In the case of missing data, I simply generated randomized data that continued the trend and with the same number of points as the other curves. Of the six different curves I chose species D, an intermediate compound that therefore presents a maximum. Since we are evaluating a hypothetical situation, I considered that D is our product of interest, and we want to maximize its concentration while several of the other reactions are secondary. 

The Paper states that the estimation of k5 has the lower confidence, its estimated value is farther from its true value than other parameters. This situation is reflected in the results obtained with Julia, where the estimate is even less accurate. Perhaps because of the noise introduced in the digitization of the data.

<img src-"Project%202/results/digitized_data.png" width-"100">

![](Project%202/results/digitized_data.png)
