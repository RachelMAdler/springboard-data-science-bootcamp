
# Capstone Project 1: Inferential Statistics

## 1. Overview
This document describes the inferential statistics performed on the 2016 Pew Research Center cybersecurity survey data.  The analyses are broken into two main sections: demographic patterns and relationships between security habits and experience of security incidents.  Because all of the variables are categorical, all of the analyses performed are chi-square tests of independence.

## 2. Demographic patterns
Three demographic variables were examined: gender, age, and U.S. region.  For each variable, analyses focused on cybersecurity habits and cybersecurity incidents experienced.

### A. Gender
The number of respondents of each gender was approximately equal (male *n* = 509, female *n* = 531).

#### Cybersecurity habits
There was a significant difference between genders in their use of a phone password, *χ²*(1, *N* = 932) = 4.02, *p* = .045.  A larger percentage of men (56%) reported using a phone password compared to women (46%).

Analyses also revealed a significant difference between genders in their use of two-factor authentication, *χ²*(1, *N* = 1026) = 6.14, *p* < .05.  A larger percentage of men (52%) reported using two-factor authentication compared to women (44%).

#### Cybersecurity incidents
Chi-square tests of independence were conducted to examine the relationship between gender and (a) frauduluent card charges, (b) the likelihood of the respondent's social security number being compromised, and (c) the likelihood of someone opening a line of credit or applying for a loan in the respondent's name.  In all cases, there was no significant difference between genders (*p*s > .05).

### B. Age
Respondents were divided into eight groups based on their age:
* Under 21 (*n* = 41)
* 21-30 (*n* = 148)
* 31-40 (*n* = 153)
* 41-50 (*n* = 142)
* 51-60 (*n* = 222)
* 61-70 (*n* = 162)
* 71-80 (*n* = 105)
* Over 80 (*n* = 67)

For the below analyses, it is important to keep in mind that the distribution of respondents was not even among these groups.

#### Cybersecurity habits
There was a significant difference between age groups' use of a phone password, *χ²*(7, *N* = 932) = 81.03, *p* < .0001.  Overall, younger adults were more likely to use a phone password than older adults.

Analyses also revealed a significant difference between age groups' use of two-factor authentication, *χ²*(7, *N* = 1026) = 84.50, *p* < .0001.  Adults between the ages of 21 and 60 were the most likely to use two-factor authentication.

#### Cybersecurity incidents
There was a significant difference between age groups' experience of having fraudulent credit/debit chard charges, *χ²*(7, *N* = 1036) = 37.01, *p* < .0001.  Adults under 21 were the least likely to have experienced fraudulent credit/debit card charges (15%), while individuals between 31 and 40 were the most likely (56%).

Analyses also revealed a significant difference between age groups' likelihood of having their social security number compromised, *χ²*(7, *N* = 1034) = 24.82, *p* < .0001.  Adults between the ages of 31 and 50 were the most likely to have had their social security number compromised (22%), while adults under 21 were the least likely (2%).

Finally, there was a significant difference between age groups' lihelihood of having someone open a line of credit or apply for a loan in the their name, *χ²*(7, *N* = 1024) = 14.2, *p* = .048.  Adults between 51 and 60 were the most likely to have had someone open a line of credit or apply for a loan in their name (19%), while no adults under 21 reported having this experience.

### C. Region
Respondents were divided into three U.S. regions: rural (*n* = 202), suburban (*n* = 503), and urban (*n* = 325).  For the below analyses, it is important to keep in mind that the distribution of respondents was not even among these regions.

#### Cybersecurity habits
There was a significant difference in the frequency of phone password use among individuals from different U.S. regions, *χ²*(1, *N* = 932) = 25.51, *p* < .0001.  While only 34% of respondents in rural regions reported using a phone password, 57% of those in suburban areas and 52% of those in urban areas reported using one.

Analyses also revealed a significant difference in the use of two-factor authentication among individuals from different U.S. regions, *χ²*(1, *N* = 1026) = 13.70, *p* = .001.  While only 37% of respondents in rural regions reported using two-factor authentication, 50% of those in suburban areas and 52% of those in urban areas reported using it.

#### Cybersecurity incidents
There was a significant difference between U.S. regions' likelihood of having fraudulent credit/debit chard charges, *χ²*(2, *N* = 1036) = 11.59, *p* = .003.  Individuals from rural regions were the least likely to have had fraudulent charges (35%), while individuals from suburban and urban regions were the mostly likely (49% and 48%, respectively).

There was no signfiicant difference between regions' experience of having one's social security number compromised (*p* > .05). Similarly, there was no significant difference between regions' experience of having someone open a line of credit or apply for a loan in their name (*p* > .05).

## 3. Security habits vs. incidents
The effect of two sets of cybersecurity habits on the likelihood of experiencing a cybersecurity incident were analyzed: (a) the use of two-factor authentication and (b) the use of public wifi to perform various types of transactions.

### A. Two-factor authentication
There was a significant relationship between the use of two-factor authentication and the likelihood of having one's email acount taken over, *χ²*(1, *N* = 1016) = 27.64, *p* < .0001.  Surprisingly, while 23% of individuals who use two-factor authentication had their email account taken over, only 11% of those who don't use two-factor authentication had their email taken over.

Analyses additionally revealed a significant relationship between the use of two-factor authentication and the likelihood of having fraudulent credit/debit card charges, *χ²*(1, *N* = 1022) = 43.48, *p* < .0001.  Also surprisingly, while 56% of individuals who reported using two-factor authentication had fraudulent credit/debit card charges, only 36% of those who didn't use two-factor authentication had fraudulent charges.

There was no statistically significant relationship between the use of two-factor authentication and the likelihood of having someone open a line of credit or apply for a loan in one's name (*p* > .05)

### B. Public wifi use
There was a significant relationship between whether an individual used public wifi to make online purchases, and the likelihood of having fraudulent credit/debit card charges, *χ²*(1, *N* = 917) = 9.05, *p* = .003.  While 63% of individuals who made online purchases on public wifi experienced fraudulent charges, only 47% of those who didn't make online purchases had fraudulent charges.

There was no statistically significant relationship between whether an individual used public wifi to check their email and the likelihood of their email account being taken over (*p* > .05).
