<a name="br1"></a> 

W207 Final Project:

Home Price Prediction

Donaton, Gomez, Jacobson, and Qian

04/12/2021



<a name="br2"></a> 

Project Description

The purpose of this project is to predict home prices as best we can using the

given data set from Kaggle.

The data consists of almost three thousand samples of housing sales data for the

years 2006 to 2010 from the Ames, Iowa city Assessor’s office. The data set

consists of 80 features related to property sales which include categorical

(nominal), ordinal, continuous, and discrete values. All features are information

that a typical home buyer would want to know, such as the neighborhood,

condition of the garage, number of bedrooms, square feet of living area, and year

built.



<a name="br3"></a> 

EDA - First Look

Shape of the Data

Sale Price Distribution

Samples

Features

Training Data

Testing Data

Total Data

1460

1459

2919

81

80

81



<a name="br4"></a> 

EDA - Feature Values

Heat Map

Organize Features

Numerical

X

Categorical

LotArea

BldgType

X

X

SalePrice

X

X

MSSubClass



<a name="br5"></a> 

EDA - Deep Dive into the Data

Validate Values Feature Stats

Patterns

Incorrect

<sup>Data</sup>Range

Min

Max

Neighborhoods

Out of Range

Values

\-

\-

Dates, SqFt & Ratings

Unreasonable

Mean

Mode

Values Not in Valid (Typos)

Description

Sort & Count

Uniques

\-

Duplic<sub>N</sub>a<sub>o</sub>t<sub>n</sub>e<sub>e</sub> Entries

get\_dummies

Numerical

\-

Data Collection

Count nan’s

Categorical

Train or Testing

Missing



<a name="br6"></a> 

Data Cleaning

Replace Nan values with Means and Modes on Neighborhood.

None and 0 based on data description.

Feature Discrepancies:

● Zoning classification subjective vs. quantitative.

● One story home with second floor square feet.

Outlier removal for a 10x improvement in RMSE.



<a name="br7"></a> 

Feature Selection

Correlation Heat Map

● OverallQual (0.79) - Rates the

overall material and finish of the

house.

● GrLivArea (0.71) - Above grade

living area square feet .

● GarageCars (0.64) - Size of

garage in car capacity.



<a name="br8"></a> 

Pre-processing

One-Hot Encoding

Shuffle

Train, Dev, and Test

Categorical Classification

Id

Cond

--->

Excellent Good Poor

Id

1

5

3

6

2

4

1

2

3

4

5

6

Good

Ex

0

1

0

0

0

1

1

0

1

0

0

0

0

0

0

1

1

0

Train

80%

Test

Good

Poor

Poor

Ex

Dev

20%



<a name="br9"></a> 

Model Results & Conclusions

Dev Score

RMSE (Kaggle)

$15,709

Models

RMSE (Dev)

$29,714

Linear Regression

0\.863

0\.906

Linear Regression with

IsolationForest

$23,490

$14,223

Rank =

2002/64,846

Linear Regression with Features with 0.866

Correlation above 0.5

$29,463

$18,805

Lasso

Enet

0\.860

0\.887

\---------

$31,015

$28,554

\---------

$20,906

$19,258

$18,384

XGBoost



<a name="br10"></a> 

Challenges & Lesson Learned

● Coordinating shared coding on Google’s colab

● Synchronizing feature engineering

● Flexibility with cleaned data

● Reluctance to remove data



<a name="br11"></a> 

Future Improvements

Feature Engineering

● Transform the

distributions of individual

features

● PCA

● Deliberation over outliers

● Time-Series and Trends

● More robust/advanced modeling

techniques (Decision Tree,

Neural Net)



<a name="br12"></a> 

QUESTIONS?

