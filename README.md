# Effect of increase in federal minimum wage on unemployment rate in the United states

Causal Inference course final project

## Motivation

The Federal government has recently proposed a minimum wage policy change. The last time when Fed increased its minimum wage rate was 2009 and no changes have been observed in minimum wage rate since then. However, recently Democrats introduced bill to hike federal minimum wage gradually to $15 per hour, more than the double than that of the current minimum wage rate of $7.25 (Source 4).

Considering the scale at which hike has been proposed, we wanted to study what is the causal impact of
raising the Federal minimum wage rate on unemployment. Does hike in the Federal minimum wage rate lead to
more unemployment, as has been suggested by many? Hence, we decided to choose our focus of study on this topic. We believe a coherent and thoughtful study of this topic could help the Fed decide better whether to pursue hike in the Federal minimum wage or not.

## Experiment setting:

__Unit of Analysis__: State    
__Period of Observation__: 2004 - 2013  
__Pre-treatment period__: 2004-2006  
__Years of Treatment__: 2007-2009  
__Post-treatment period__: 2010-2013  
__Treatment Variable__: Increase in Federal Minimum Wage rate  
__Outcome Variable__: Unemployment Rate    
__Treatment group__: State for which minimum wage rate in state was increased to meet guidelines set by Fed.  
__Control group__: State for which state minimum wage rate was not changed following guidelines by Fed.


__Data sources__: We have combined the below two data sources for our analysis.  
[_Unemployment rate source_](https://www.kaggle.com/jayrav13/unemployment-by-county-us/home )  
This data set was built in 2016 by scrapping Local Area Unemployment Statistics from the website of the US Department of Labor Bureau of Labor Statistics. It contains unemployment data at the county and state level from 1990 to 2016.   
[_Minimum wage source_](https://www.dol.gov/whd/state/stateMinWageHis.htm )  
This websites provide us the minimum wage rates for all states in the USA from 1968 - 2018.

## Method 

For this study, we decided to go ahead with observational study rather than conducting experiments as
conducting experiment is not under our control. We have used the difference in differences(DID) method for
our analysis. DID is a quasi-experimental design that makes use of longitudinal data from treatment and
control groups to obtain an appropriate counterfactual to estimate a causal effect. DID is typically used to
estimate the effect of a specific intervention or treatment (such as a passage of law, enactment of policy)
by comparing the changes in outcomes over time between a population that is enrolled in a program (the
intervention group) and a population that is not (the control group). DID requires data from pre-/postintervention,
such as cohort or panel data (individual level data over time) or repeated cross-sectional data
(individual or group level).
DID is used in observational settings where exchangeability cannot be assumed between the treatment and
control groups. DID relies on a less strict exchangeability assumption, i.e., in absence of treatment, the
unobserved differences between treatment and control groups are the same overtime. The parallel trend
assumption is the most critical assumptions to ensure internal validity of DID models i.e., treatment and
control groups have Parallel Trends in outcome in the pre period of the treatment. We observed that the
assumptions of difference in differences was met and hence proceeded with this approach to find an effect of
increase in federal minimum wage on unemployment rate.


## Conclusion and Next steps

From our analysis, We conclude that an increase in Federal minimum wages have no causal effect on the unemployment rate under our set of assumptions. 

However, We are not very confident of saying that we can go ahead with the new policy to increase the federal minimum wage yet. We have assumed a treatment period from 2007-2009. We have not accounted for how states behaved in this treatment period. We would want to observe the effect of treatment separately for all three years i.e., 2007,2008 and 2009. We feel this will give us a more comprehensive result and will help us make the right decision.

## Assumptions and Limitations
1.	Interference: There might be interference as people migrate from state with lower minimum wage rate to neighboring states in search of better opportunities.

2.	Difference in minimum wage rate within State: We rolled up the county unemployment rate to state level for our study. However, some of the counties have different unemployment rate as compared to the State unemployment rate. If we want to account for these differences, we could go one level below by studying impact of Fed minimum wage hike rate at county level. However, in this case interference problem explained in point 1 would increase as it is quite flexible to move from one county to another county than moving from one State to another State. A much more precise way to achieve average unemployment rate would have been to consider weighted average rate by considering population of each country. 

3.	Continuous increase in Federal rate: Treatment effect is assumed to take place on January 1st, 2009, however, Federal hiked minimum wage rate over the period of 3 years i.e. from 2007 till 2009. This limitation could be bypassed by studying period when Fed minimum wage rate was hiked only once a year and it was not followed by another hike. The data that we gathered doesn't contain any such record.

4.	 Dynamic confounders: The systematic differences and static confounds will cancel out by using DID. However, there could be dynamic confounders (like policy change in the state that varied in the post treatment period) that might have affected the output. A much more advance method of dynamic difference in difference could be done to avoid these limitations.
