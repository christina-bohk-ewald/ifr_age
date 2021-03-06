# Scenarios for the COVID-19 infection fatality rate in Germany and worldwide

Enrique Acosta [1], Christina Bohk-Ewald [2,1], Christian Dudel [1], Tim Riffe [1], Mikko Myrskylä [1,2]

[1] Max Planck Institute for Demographic Research, Germany
[2] Center for Social Data Science, University of Helsinki, Finland

## Summary

In a recent study, Levin et al. provide metaregression estimates of the COVID-19 infection fatality rate (IFR) by age. Building on these results we calculate the total IFR for Germany under several scenarios. This includes scenarios based on observed COVID-19 prevalence in Germany, and an alternative method relying on age-specific death counts instead of prevalence. In our scenarios the resulting total IFRs for Germany range from 0.7% to 2.4%. Thus, the IFR of COVID-19 in Germany could be much larger than the IFR of influenza. However, our results come with considerable uncertainty, and they depend on the specific assumptions made and data used. Moreover, they are not directly comparable to the scenarios reported by Levin et al. for the United States. Applying our methods and scenarios to further countries shows a wide range of resulting IFRs, but the mean age of the population seems to be a reliable predictor of the levels of the IFR.

## Background

In a recent study, Levin et al. [1] provide metaregression estimates of the COVID-19 infection fatality rate (IFR) by age. Based on these estimates, they calculate several scenarios for the total IFR in the United States. However, the scenarios they provide are based on rather strong assumptions. Among other things they assume a rectangular age structure of the U.S. population; i.e., the number of individuals in each age is the same across all ages. This goes against recent findings which show that the age structure of populations can have a substantial impact on COVID-19 mortality [2,3].


## Aim

Building on the results of Levin et al. we provide estimates of the total IFR for Germany taking into account the real age structure of the population, and including additional scenarios and methodological approaches. We also apply our scenarios and methods to further countries.

## Method

Age-specific IFRs are calculated using the exponential function provided by Levin et al. [1]. The age structure of the the German population is taken from the Human Mortality Database [4]. We implement the three scenarios used by Levin et al.: (1) Approximate age-specific prevalence as recently in the U.S.; (2) Constant prevalence across the age range; and (3) a scenario which assumes a low prevalence at higher ages, reflecting a protection of vulnerable groups. Moreover, we implement two additional scenarios, which take the exact age structure of (5) cumulative counts of reported COVID-19 cases, and (6) the age structure of COVID-19 cases in the last week of data available to us; this data is taken from the COVerAGE-DB project [5]. Finally, (7) we also implement a method which does not require us to make assumptions on the age structure of cases, but which instead infers the age distribution of cases based on age-specific death counts combined with age-specific IFRs [6]. For all variants we calculate the total IFR.

## Results

The estimates of the total IFR for Germany range from 0.7% to 2.4%. This is considerably higher than the estimates found by Levin et al. In particular, the scenarios based on German data (5,6) and the method not requiring assumptions on the age structure of cases (7) are all around or above 1.5%. However, the uncertainty of these estimates is large. For instance, using the prediction intervals provided by Levin et al. the prediction interval for scenario 2 ranges from 0.5% to 6.6%. Results for additional countries also show a wide range, although the mean age of the population seems to be a good predictor of the level of IFRs.

## Limitations

Our estimates come with considerable uncertainty. This, first, includes the uncertainty as expressed through prediction intervals as provided above. Second, the age-specific IFR estimates of Levin et al. are based on a model and as such depend on several assumptions, and it is not clear whether they can be directly applied to Germany. Also, estimates of age-specific infection fatality rates coming from other studies sometimes differ considerably, in particular for higher ages [7] which are very important for the final result, as we show in additional analyses. Third, the age-specific prevalence of COVID-19 as implemented in several scenarios could turn out to be rather different from what we assume, and currently no reliable estimates are available. Finally, the results also depend to some extent on minor modelling choices, such as using an open age interval and the age-specific IFR used for this interval.

## Conclusions

The IFR of COVID-19 in Germany could be considerably larger than the IFR of influenza, and this also seems to hold for other countries. However, our results come with considerable uncertainty, and in the future updated results based on improved and more complete data could potentially show diverging results.

## Code and data

All code needed to reproduce our findings can be found in the folder 'R Code'. All data is freely available online. The data from the Human Mortality Database requires a registration, but is also free. As alternatives to the R code a spreadsheet for some of the calculations is also available: https://docs.google.com/spreadsheets/d/1OmC36c_TRXrP6S3LfBUKQK8X7vcYEdKCLeRHWleE8Bc/edit#gid=2118683091

## References

[1] https://doi.org/10.1101/2020.07.23.20160895

[2] https://doi.org/10.1371/journal.pone.0238904 

[3] https://doi.org/10.1073/pnas.2004911117

[4] https://www.mortality.org/ 

[5] https://dx.doi.org/10.4054/MPIDR-WP-2020-032  

[6] https://arxiv.org/abs/2004.12836 

[7] https://doi.org/10.1016/S1473-3099(20)30243-7 
