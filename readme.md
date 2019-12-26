# (Loan Prosper Dataset)
## by (Hatim Alsulami)


## Dataset

> This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv.), with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).

The wrangling process:
- In EmploymentStatus variable, we replace nan values with 'Not Available'.
- To find the missing value of BorrowerAPR, we calculated the median difference between BorrowerAPR and BorrowerRate. Then we add the difference to BorrowerRate.
- Rename ProsperRating (Alpha) to ProsperRating.
- Dropping the nan records. We are only intrested in loans originated after July 2009.

## Summary of Findings

> In the exploration, I found that there was a negative relationship between the
Borrower APR of a loan and its amount. Borrowers with high prosper rating have the lowest APR. I found a
somewhat surprising results. I noticed when the prosper rating is the highest ratings (A,AA), the correlation between APR and loan amount will be positive unlike when the rating starts from B down to HR in which the relation will be negative as expected.

Outside of the main variables of interest, I verified the relationship between
loan amount and the stated income. For the dataset given,
there was an interesting interaction in the categorical features. There are more 60 months term on rating B and C. And only 36 months for HR borrower rating. Borrowers with high prosper rating tend to have high stated income and large loan amount. As a results of large loan amount, the monthly loan payments are high with high prosper rating accounts


## Key Insights for Presentation

> For the presentation, I focus on just features that could affect the borrower APR. I start by introducing the
distribution of borrower APR and loan amount. Then I presented the relationship between borrower Apr and loan amount. Alsom APR and Prosper Rating. Afterwards, I introduce each of the categorical variables one by one. To start, I use the box plots of APR and Term, PrsperRating, and EmploymentStatus. Then I look into the possible effects of Prosper Rating on APR and loan amount. 