
# Capstone Project 1: Milestone Report

## Contents
1. Problem definition
2. Client description
3. Data overview
4. Data wrangling
    - A. Data cleaning
    - B. Missing values
5. Initial findings: Inferential statistics
    - A. Demographic variables
        - i. Gender
        - ii. Age
        - iii. Region
    - B. Cybersecurity habits vs. incidents
        - i. Two-factor authentication
        - ii. Public wifi use
6. Initial findings: Modeling

## 1. Problem definition
Businesses often promote habits to increase individuals’ personal cyber-safety.  In order for these campaigns to be effective, it is important to demonstrate a clear link between good cybersecurity habits and actual increased cyber-safety.  In addition, it is possible that certain groups of individuals are at increased risk for cyber-security incidents.  If so, education efforts should target these particular groups.  Thus, this project will show (a) whether engaging in better cybersecurity practices adequately protects individuals from online attacks, and (b) whether certain groups of individuals are more vulnerable to such attacks.

## 2. Client description
There are two groups of clients that may profit from this project.  The first group of clients comprises organizations that promote cybersecurity, such as the U.S. Department of Homeland Security or the National Integrated Cyber Education Research Center (https://nicerc.org/).  These groups seek to educate Americans about good cybersecurity habits.  The second group of clients is businesses that strive to increase their customers’ cybersecurity efforts to improve their company’s overall security.  For both types of clients, this project will provide evidence to be shared with consumers that may help encourage better habits.  In addition, this project will highlight particular groups of individuals that these organizations should focus their efforts on.

## 3. Data overview
The data for this project come from a Pew Research Center survey conducted in June 2016.  The survey respondents consisted of 1,040 adult internet users in the U.S.  All data are publically available via the Pew Research Center (http://www.pewinternet.org/2017/01/26/americans-and-cybersecurity/).  The complete dataset contains 1040 rows (observations) and 121 columns (variables).  Of these 121 columns/variables, seven are related to security incidents an individual has experienced; all data are categorical (1 = yes, 2 = no).  Twenty variables are related to individuals’ cyber-security habits.  All of these data are categorical; some are binary (1 = yes, 2 = no) and some have more than two responses (e.g., type of security feature used to access phone: pin, password, thumbprint, other).  Finally, there are sixteen variables containing demographic information.  Some of these data are continuous (e.g., age), some are ordinal (e.g., highest level of education), and some are categorical (e.g., race).

## 4. Data wrangling

As a first step, the relevant columns in the dataset were identified.  These columns included data about respondents’ (a) cybersecurity habits, (b) cybersecurity incidents experienced, and (c) demographics.  The data in these columns largely consisted of 1s (“yes” responses), 2s (“no” responses), 8s (“don’t know” responses), and 9s (“refused”).  The data wrangling steps performed on these columns are described below.

### A. Data cleaning

1.	Some of the relevant columns contained strings instead of numbers.  However, because machine learning algorithms require all values to be numeric, these columns were converted to integers.  For example, one column encodes whether the respondent lives in a rural (“R”), suburban (“S”), or urban (“U”) region.  These values were converted as follows: R = 1, S = 2, and U = 3.

2.	The dataset included some numbers as integers, but also some numbers as strings.  All values were converted to integers for consistency and to be able to perform machine learning algorithms.

3.	For all yes/no items, 2s (“no” responses) were converted to -1s.  This means that after replacing blanks with 0s (see below), all yes/no items contain three response values: -1 (no), 0 (blank/other), and 1 (yes).  By doing this, the blank/other responses fall in between the “yes” and “no” responses.
 
### B. Missing values
1.	The dataset contained many blank values.  All blank values in the relevant columns were replaced with zeros.  Zero does not correspond to any other response in these columns.

2.	All 8 (“don’t know”) and 9 (“refused”) responses were also replaced with zeros.  

3.	For some of the missing values, a response could be inferred from another item.  When this was the case, the inferred response was entered instead of the missing value.  For example, one of the security incident items asks whether the respondent’s email account has ever been hacked.  However, this question was only asked if the respondent previously indicated they use the internet.  If they didn’t use the internet, this item was left blank.  Importantly, if a respondent doesn’t use the internet, then they’ve also never had their email account hacked, so it makes sense to replace the missing value with a “no” (2) response for this item. 

## 5. Initial findings: Inferential statistics

### A. Demographic patterns
Three demographic variables were examined: gender, age, and U.S. region.  For each variable, analyses focused on cybersecurity habits and cybersecurity incidents experienced.

#### i. Gender
##### Cybersecurity habits
There were several statistically significant differences between each gender's cybersecurity habits.  First, a significantly larger percentage of men reported using a phone password compared to women (56% vs. 46%, respectively).  Second, a significantly larger percentage of men reported using two-factor authentication compared to women (52% vs. 44%, respectively).

##### Cybersecurity incidents
In spite of the significant differences in cybersecurity habits, there were no significant differences in each gender's cybersecurity incident experiences.  Specifically, there were no differences in a) fraudulent card charges, (b) the likelihood of the respondent's social security number being compromised, or (c) the likelihood of someone opening a line of credit or applying for a loan in the respondent's name.

#### ii. Age
Respondents were divided into eight groups based on their age:
* Under 21 (*n* = 41)
* 21-30 (*n* = 148)
* 31-40 (*n* = 153)
* 41-50 (*n* = 142)
* 51-60 (*n* = 222)
* 61-70 (*n* = 162)
* 71-80 (*n* = 105)
* Over 80 (*n* = 67)

##### Cybersecurity habits
There were several statistically significant differences in cybersecurity habits between the age groups.  First, younger adults are more likely to use a phone password compared to older adults.  Of adults under 50, 62-71% use a phone password, while less than 50% of adults over 50 do so.  Age was also related to the use of two-factor authentication.  Of adults between the ages of 21 and 60, 50-66% reported using two-factor authentication, making them the most likely.

##### Cybersecurity incidents
There were additionally several significant differences in cybersecurity incidents between the age gropus.  Adults under 21 were the least likely to have experienced fraudulent credit or debit card charges (15%).  However, adults between the ages of 31 and 40 were the most likely (56%).  Adults under 21 were also the least likely to have had their social security number compromised (2%), and to have someone open a line of credit or apply for a loan in their name (0%).  Adults at the highest risk of having their social security number compromised were between the ages of 31 and 50 (22%).  Adults at the highest risk of having someone open a line of credit or apply for a loan in ther name were 50 to 60 years old (19%).

#### iii. Region
Respondents were divided into three U.S. regions:
* Rural (*n* = 202)
* Suburban (*n* = 503)
* Urban (*n* = 325)

##### Cybersecurity habits
Overall, individuals in rural regions were the least likely to use a phone password (34%) or two-factor authentication (37%).  Adults in suburban and urban areas were about equally likely to use a phone password (57% and 52%, respectively) and to use two-factor authentication (50% and 52%, respectively).

##### Cybersecurity incidents
Surprisingly, individuals in rural areas were the least likely to have had fraudulent charges on their credit or debit card (35%).  Individuals in suburban and urban areas were about equally likely (49% and 48%, respectively).  However, there was no significant difference between regions' experience of having their social security number compromised (values ranged 12-15%), or having someone open a line of credit or apply for a loan in their name (values ranged 36-56%).

### B. Cyber security habits vs. incidents
The effect of two sets of cybersecurity habits on the likelihood of experiencing a cybersecurity incident were analyzed: (a) the use of two-factor authentication and (b) the use of public wifi to perform various types of transactions.

#### i. Two-factor authentication
Surprisingly, while 23% of individuals who use two-factor authentication have had their email account taken over, only 11% of those who don't use two-factor authentication have had their email taken over.  Similarly surprising, while 56% of individuals who reported using two-factor authentication have had fraudulent credit/debit card charges, only 36% of those who didn't use two-factor authentication have had fraudulent charges.  In contrast to these findings, there was no statistically significant relationship between the use of two-factor authentication and the likelihood of having someone open a line of credit or apply for a loan in one's name.

#### ii. Public wifi use
The use of public wifi to make online purchases was significantly related to the experience of fraudulent credit or debit card charges.  While 63% of individuals who made online purchases on public wifi experienced fraudulent charges, only 47% of those who didn't make online purchases had fraudulent charges.  There was no statistically significant relationship between whether an individual used public wifi to check their email and the likelihood of their email account being taken over.

## 6. Initial findings: Modeling

As a first pass at modeling, I fit a linear regression model using (a) the cybersecurity habits variables and (b) the demographic variables to predict each cybersecurity incident variable.  I then calculated the root mean square error for a range of initial learning rates (*eta0*) and number of iterations (*n_iter*).  Regardless of the initial learning rate or the number of iterations, all root mean square error values were greater than 1 trillion, suggesting that a linear model is not appropriate for these variables.
