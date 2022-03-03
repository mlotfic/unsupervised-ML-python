# Unsupervised ML Techniques in python

## Introduction:
1- All your variables are numeric: use principal component analysis (PCA)
2- You have a contingency table: use correspondence analysis (CA)
3- You have more than 2 variables and they are all categorical: use multiple correspondence analysis (MCA)
4- You have groups of categorical or numerical variables: use multiple factor analysis (MFA)
5- You have both categorical and numerical variables: use factor analysis of mixed data (FAMD)

## Usful Information 
#### Contingency Table:
- A contingency table is a tabular representation of categorical data.
- A contingency table usually shows frequencies for particular combinations of values of two discrete random variable s X and Y. 
- Each cell in the table represents a mutually exclusive combination of X-Y values.

- For example, consider a sample of N=200 beer-drinkers. 
- For each drinker we have information on sex 
- (variable X, taking on 2 possible values: "Male" and "Female") and 
- preferred category of beer 
- (variable Y, taking on 3 possible values: "Light", "Regular", "Dark"). 
##### A contingency table for these data might look like the following

|        	| Light 	| Regular 	| Dark 	| Total 	|
|:------:	|-------	|---------	|------	|-------	|
| Male   	| 20    	| 40      	| 50   	| 110   	|
| Female 	| 50    	| 20      	| 20   	| 90    	|
| Total: 	| 70    	| 60      	| 70   	| 200   	|

- This is a two-way 2x3 contingency table (i.e. two rows and three columns).
- Sometimes three-way (and more) contingency tables are used. 
- Suppose the beer-drinkers data, besides sex and preference, are also stratified by age group. 
- The third discrete variable Z ("Age") in this case might, for example, take on 4 values: "65".
- In this case we would have a three-way 2x3x4 contingency table, equivalent to 4 two-way 2x3 contingency tables (one 2x3 table for each of the 4 age-groups).

#### Linear discriminant analysis
Linear discriminant analysis (LDA), normal discriminant analysis (NDA), or discriminant function analysis is a generalization of Fisher's linear discriminant, a method used in statistics and other fields, to find a linear combination of features that characterizes or separates two or more classes of objects or events. The resulting combination may be used as a linear classifier, or, more commonly, for dimensionality reduction before later classification.

#### Eigenvalue
- Eigenvalues are a special set of scalars associated with a linear system of equations 
- (i.e., a matrix equation) that are sometimes also known as characteristic roots, characteristic values (Hoffman and Kunze 1971), proper values, or latent roots (Marcus and Minc 1988, p. 144).


## 01-Prince
- Prince is a library for doing factor analysis. 
- This includes a variety of methods including principal component analysis (PCA) and correspondence analysis (CA). 
- The goal is to provide an efficient implementation for each algorithm along with a scikit-learn API.

### Installation
- Prince doesn't have any extra dependencies apart from the usual suspects (sklearn, pandas, matplotlib) which are included with Anaconda.

#### Via PyPI
$ pip install prince

### Guidelines

#### You are supposed to use each method depending on your situation:
- All your variables are numeric: use principal component analysis (prince.PCA)
- You have a **contingency table: use correspondence analysis (prince.CA)
- You have more than 2 variables and they are all categorical: use multiple correspondence analysis (prince.MCA)
- You have groups of categorical or numerical variables: use multiple factor analysis (prince.MFA)
- You have both categorical and numerical variables: use factor analysis of mixed data (prince.FAMD)
