# KYC-based-Customer-Segmentation
Machine Learning solution to segment customers using KYC information


Customer segmentation aggregates the data captured in the KYC details and creates customer groups. The KYC data comes in various categories such as Geographic, Demographic, Behavior and Financial variables.  This solution leverages machine learning to identify patterns in the data and segment the customers. These segments can be utilized for marketing analytics and campaigns.

**Max number of samples** = 100000

**Min number of samples** = 1000

#### **Type of clustering**: 
Default = hdbscan
-	hdbscan
-	kmeans
-	kmodes


#### **Type of segmentation**:
Default = Combined
-	Geographic segmentation
-	Demographic segmentation
-	Behavior segmentation
-	Financial segmentation
-	Combined

#### **Recommended clustering parameters for different clustering**:
**Note:** 
-	hdbscan: (Integer)
    -	min_cluster_size = (Default  = 1000)
    -	min_samples  = (Default = 80)
-	kmeans: (Integer)
    -	n_clusters = (Default  = 5)
-	kmodes: (Integer)
    -	n_clusters = (Default = 5)

**All the attributes must be one of below mentioned:**

***Note***: if other columns are added they will be not considered

-	'customer_code': Unique ID for customers

-	Columns allowed for Geographic segmentation columns:
(any two from the following needs to be present for Geographic segmentation)
    -	'area_type': Type of area (Categorical variable)
    -	'new_territory': yes or no (Categorical variable)
    -	'country': Country code (US) (Categorical variable)
    -	'city': City code (Ex: NY) (Categorical variable)
    -	'population_density': Density of population (Numeric variable) 

-	Columns allowed for Demographical segmentation columns:
(any two from the following needs to be present for Demographical segmentation)
    -	'age': Age in years/month (Numeric variable)
    -	'gender': M/F/Others/Unknown (Categorical variable)
    -	'race': Race (Categorical variable)
    -	'religion': Religion (Categorical variable)
    -	'years_of_education': In years/months (Numeric variable)
    -	'income': Gross income/ Avg.income (Numeric variable)

-	Columns allowed for Behavioral segmentation columns:
(any two from the following needs to be present for Behavioral segmentation)
    -	'customer_seniority': Seniority of customers in years/Months (Numeric variable)
    -	'customer_status': Active customer (1)/ Inactive customer(0)/…. (Categorical variable)
    -	'new_customer': New customer or not 0/1 (Categorical variable)
    -	'employee': Person is an existing employee or not ex: current_emp (1)/ previous_emp(0)/ not_emp(-1)(Categorical variable)


-	Columns allowed for Financial segmentation columns:
(any two from the following needs to be present for Financial segmentation)
    -	'loan_amount': Loan Amount (Numeric variable)
    -	'credit_rating': Credit card Rating (Categorical variable)
    -	'yearly_spend': Amount spend in a (year/month) (Numeric variable variable)
    -	'income': Amount of money earned (Year/month) (Numeric variable)
