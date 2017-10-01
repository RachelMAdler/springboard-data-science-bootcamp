
# Capstone Project 1: Data Wrangling

## Overview
The data for this project come from a Pew Research Center survey on cybersecurity conducted in June 2016.  As a first step, the relevant columns in the dataset were identified.  These columns included data about respondents’ (a) cybersecurity habits, (b) cybersecurity incidents experienced, and (c) demographics.  The data in these columns largely consisted of 1s (“yes” responses), 2s (“no” responses), 8s (“don’t know” responses), and 9s (“refused”).  The following data wrangling steps were performed on these columns:

## Data cleaning

1.	Some of the relevant columns contained strings instead of numbers.  However, because machine learning algorithms require all values to be numeric, these columns were converted to integers.  For example, one column encodes whether the respondent lives in a rural (“R”), suburban (“S”), or urban (“U”) region.  These values were converted as follows: R = 1, S = 2, and U = 3.

2.	The dataset included some numbers as integers, but also some numbers as strings.  All values were converted to integers for consistency and to be able to perform machine learning algorithms.

3.	For all yes/no items, 2s (“no” responses) were converted to -1s.  This means that after replacing blanks with 0s (see below), all yes/no items contain three response values: -1 (no), 0 (blank/other), and 1 (yes).  By doing this, the blank/other responses fall in between the “yes” and “no” responses.
 
## Missing values
1.	The dataset contained many blank values.  All blank values in the relevant columns were replaced with zeros.  Zero does not correspond to any other response in these columns.

2.	All 8 (“don’t know”) and 9 (“refused”) responses were also replaced with zeros.  

3.	For some of the missing values, a response could be inferred from another item.  When this was the case, the inferred response was entered instead of the missing value.  For example, one of the security incident items asks whether the respondent’s email account has ever been hacked.  However, this question was only asked if the respondent previously indicated they use the internet.  If they didn’t use the internet, this item was left blank.  Importantly, if a respondent doesn’t use the internet, then they’ve also never had their email account hacked, so it makes sense to replace the missing value with a “no” (2) response for this item. 


```python

```
