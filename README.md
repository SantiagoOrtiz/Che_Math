# Che_Math
This repository was created to collect all the coded-related homework and projects developed within the course $Mathematical$ $Methods$ $in$ $Chemical$ $Engineering$ from the Chemical and Petroleum Engineering Department at the University of Pittsburgh. The programming languages used for this purpose are Julia and Python.

## Project 2: Kinetic Parameter Estimation from Experimental Dataset using Julia

This case study is based on the work done by Schenk et al. (2020) in the Paper titled Introducing KIPET: A novel open-source software package for kinetic parameter estimation from experimental datasets including spectra [1]. The project's first objective was to replicate the parameter estimation of one of the provided datasets in the Paper. The first step involved extracting and visualizing the raw data using a plot digitizer tool. The subsequent task was to solve the system of ordinary differential equations. Next, the kinetic model's parameters in the differential equations system were fitted to the experimental dataset. Finally, two further examinations were performed, which included a bifurcation and a global sensitivity analysis considering interactions. 

### 1. Extracting and Plotting data:

During the process of recovering data using WebPlotDigitizer, some limitations worth mentioning were identified.
- Missing data: The legend covers one of the lines and makes it impossible to recover this data.
- Color overlapping: Due to the presence of multiple profiles and hence colors, in some cases, the profiles overlap. If we were to zoom in, it would be evident that some fragments of the curves overlap others.
- Dotted lines: Also, the style of the line becomes an additional constraint when it is dotted, and thus, its trend is difficult to follow.

Together these three factors generate additional noise, which leads to slightly different results when fitting the parameters. Nevertheless, despite these limitations, the tool extracted the information with some additional noise, in some cases more than others. It is fair to say that all species follow the original trajectory.

<img src="Project%202/results/digitized_data.png" width="400">

As shown in the figure, some random points were generated to replace the missing data, following the previous trend and with the same number of points as the other curves.

### 2. Solving ODE system:
The ordinary differential equations were solved succesfully. Since this case study exemplifies a hypothetical situation, the species D was selected as the product of interest among the six different profiles. The compound D is an intermediate compound and therefore presents a maximum.

### 3. Fitting data:
The Paper states that the estimation of k5 has lower confidence considering that its estimated value is farther from its actual value than other parameters. This situation is reflected in the results obtained herein with Julia, where the estimate for k5 is even less accurate. The lack of precision may be due to the noise introduced in the digitization of the data.

<img src="Project%202/results/fitted_data.png" width="400">

### 4. Bifurcation analysis:

A bifurcation analysis was performed by solving the kinetic model's steady-state problem. The six concentration roots were calculated for each 𝒌_𝒊 in a range between 0.0 and 1.0.

<img src="Project%202/results/k5_bifurcation_analysis.png" width="400">

### 5. Sensitivity analysis:

The maximum concentration of D was selected as object of study for this analysis.

<img src="Project%202/results/global_parametric_sensitivity.png" width="400">
<img src="Project%202/results/GS_linear_regression.png" width="400">

## References
[1] Schenk, C., Short, M., Rodriguez, J. S., Thierry, D., Biegler, L. T., García-Muñoz, S., & Chen, W. (2020). Introducing KIPET: A novel open-source software package for kinetic parameter estimation from experimental datasets including spectra. Computers & Chemical Engineering, 134, 106716.
