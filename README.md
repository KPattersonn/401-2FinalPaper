# 401-2FinalPaper
Applied Regression Methods II - Categorical Regression Final Paper

## Description 
Using logistic and negative binomal regression models, I draw on necropolitical theory, borrowing the term feminicide, from Latin American feminist scholars, which “refers not only to the killing of women for being female, but to the systematic nature of these killings… as a political operation” (Federici et al., 2021) to hypothesize an epidemic of Black feminicides as it pertains to unhoused experiences. Here, I ask: What are the odds of Black women experiencing death by homicide? And more generally, I question: What is the expected count of unhoused deaths across different levels of demographic and contextual variables.
## Data
In exploring gender- based violence among the unhoused in Seattle, WA, USA (2008 - 2024),  I utilize: Seattle homeless death count data from the Women’s Housing, Equality & Enhancement League. This is a private data set that has been informed by the King COunty Medical Examiner’s Office (Seattle, WA, USA). As this data set is private, I am not able to share access to the working dataset, however, you may contact the Women’s Housing, Equality & Enhancement League if interseted in utlizing their dataset (wheelforwomen.org)

[Data Disclosure Notice: This work was completed with data collected and provided by the Women’s  Housing Equality and Enhancement League (WHEEL). WHEEL is a non-profit and non-hierarchical  grassroots group of homeless and formerly homeless women that 4has worked for justice and to end  homelessness in King County, WA, since 1993. More information about WHEEL’s work can be found at  wheelforwomen.org] 

## Variables 
## Death Count Variable (count/numerical)
Includes: counts of unhoused deaths from 2008 to 2024 in Seattle, WA, USA — accounting for 2706 Individual cases of unhoused deaths. 
For the logistic regression model, the 2706 Individual cases of unhoused deaths are uniquely aggergated at the zipcode level across different levels of demographic and contextual variables of age, sex, race, and manner of death — thus dropping to 1154 observations. 
For the negative binomal regression model, the 2706 Individual cases of unhoused deaths are kept at the individual level — thus accunting for all 2706 cases.
## Season Variable (categorical)
Includes: Summer (June, July, August), Winter (December, January, February), Fall/Spring (March, April, May, November, October, September)
The fall and spring months are collapsed into one reference category to compare the expected count of unhoused deaths during periods of extreme temperature, as often experienced within summer and winter months. 
## Age Variable (categorical)
Includes: Ranges from birth years 0 - 82 that were catorgorized in five age groups of: Child/Youth (0-17), Young Adult (18-29), Adult (30-49), Older Adult (50-64), and Senior (65-82).
## Race/Ethnicity Variable (categorical)
Includes:  American Indian/Alaska Native, Black/African American, Hispanic, Mixed/Other, Pacific Islander. 
For the logistic regression model, the Race/Ethnicity variables are collapsed into two categories of “Black/African American” and “Other”. The “Other” category represents everyother racial category aside from Black/African American. Doing so, allows for a clearer interrogation of my question of: What are the odds of Black unhoused women experiencing death by homicide. Because I am intersted in the relationship between Blackness, Sex, and death by homicide, such a collapsing of racial caregories easily demonstrates the Black unhoused womens unique experince to homicide. 
## Manner of Death Variable (categorical)
Includes: Homicide, Suicide, Natural Deaths, Undetermined Deaths and Fetal Deaths.
The “Manner of Death” classifications are based on the results of the Seattle Medical Examiners Office. 
## Year Variable
Includes: 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022, 2023, 2024.

## Methods 

## Logistic Regression Model ( Outcome variable = Homicide Deaths ; Perdictor Variables = Race/Ethnicity and Sex)
In asking: What are the odds of Black women experiencing death by homicide? I use a logistic regression model as the outcome variable of death by homicide is binary ( 0 = no, 1 = yes). Moreover, this model is designed to inform the probability of an event occurring, suting my question of the odds of experiencing a death by homicide well. Additionally, I estimate two negative binomial models: one with an interaction between “Race/Ethnicity” and “Sex”, and one without. Based on the model fit statistics, the lower BIC and AIC results of the Race and Sex interaction model, as compared to the non-interaction model, indicates that the interaction model is perferred. With this, I will be reporting results from the preferred model in the results section of the paper. 

## Negative Binomal Regression Model ( Outcome variable = Unhoused death count; Perdictor variable = Season, Homicide Deaths, AgeGroup, Sex, RaceEthnicity, and  Manner of Death) 
In asking: What is the expected count of unhoused deaths across different levels of demographic and contextual variables? I used a negative binomal regression model because the variance in my count data exceeds the mean. This is evidence of overdispersion, also indicated within my likelihood ratio test, where the variance is greater than the mean, violates the assumptions of a Poisson regression model, which assumes the variance and mean are equivalent. Due to this violation, the negative binomial model is better suited for modeling my data on unhoused death counts. Additionally, I estimate two negative binomial models: one with an interaction between “Race/Ethnicity” and “Sex”, and one without. Based on the model fit statistics, the non-interaction model has a slightly lower AIC value, whereas, the BIC value for the  Race and Sex interaction model is signfigantly lower. Because BIC penalizes for model complexity more strongly than the AIC, and given the minimal AIC difference (only 1 point), the  Race and Sex interaction model is perferred. With this, I will be reporting results from the preferred model in the results section of the paper. 


## Limitations
The models analyze the experience of death relative to the overall pool of unhoused deaths, rather than the total count of unhoused individuals in Seattle. Consequently, these models do not accurately reflect the disparities in unhoused death rates across varying levels of demographic and contextual variables. However, based on the share of unhoused deaths by race, we can infer that unhoused communities of color, particualy Balck and indigenous unhoused populations are disproportionately represested. Black unhoused individuals make up 17% of unhosed deaths, despite only making up 7% of Seattle's population. Similarly, Indigenous individuals represent 5.4% of unhosed deaths, while only comprising 0.8% of Seattles population. 
