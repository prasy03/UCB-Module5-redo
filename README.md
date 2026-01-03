# UCB-Module5-redo ==> Module 5 of UCB AI and ML - Resubmission based on feedback
`Project Readme` (revised submission: Jan 2026
`Prepared by:` Sylvester Prasanna 
`Project Title:` **Coupon Acceptance Analysis**
`Project Summary:`  
- The "coupons" dataset was analyzed using pandas and other standard packages. This analysis extracted meaningful information, providing a better understanding of the data and aiding in the prediction of future customer behaviors based on observed patterns.
  
### Steps used to extract and visualize (CRISP-DM) 
This project utilizes exploratory data analysis (EDA) and visualization techniques to identify the demographic and situational factors that influence whether a driver accepts a mobile coupon. The analysis focuses on two specific use cases: Bar coupons and Coffee House coupons.

#### Business Understanding: 
##### Project Scope: The project involves importing and analyzing data provided in CSV format.

#### Data Understanding: 
- The coupons.csv file was imported as a CSV.
- A sub-dataframe containing specific columns was created for particular use cases.

#### Data Cleaning: Identification of missing values. 
- The car column was removed due to 99% missing data. Specific rows with null values in frequency columns were dropped to ensure statistical integrity.
- Exploratory Data Analysis (EDA): Calculated global acceptance rates and visualized distributions of temperature and coupon types.

#### Data Preparation: 
##### Segmented Analysis: Created filtered subsets of the data (dataframes) to isolate specific business types (Bars and Coffee Houses).
- The dataframe was thoroughly checked for null values, incomplete strings, missing data, and incorrect data types. No deviations or misalignments were found.
- The .index was incorporated to improve the accuracy of the .count() function. 
- Wherever needed, the following functions were used to validate incomplete data : .isnull 
Some columns were dropped as they were not relevant for this specific use case. 
Utilizing standard libraries for data extraction and visualization. 
'pandas', 'numpy', 'Matplotlib', 'seaborn', and 'plotly.express' were used.

#### Hypothesis:  
An initial assessment was conducted using a subset of coupon usage data specifically for 'Bar' locations. Hypothesis Testing: Compared acceptance rates between various driver segments (e.g., age groups, passenger types, and visit frequencies) to find the "ideal" customer profile.

### 2. Libraries Referenced
The project was developed in Python using the following industry-standard libraries:
- Pandas: Used for data manipulation, cleaning, and filtering.
- NumPy: Used for numerical operations and handling logical masks.
- Matplotlib.pyplot: Used for creating the base visualization figures.
- Seaborn: Used for advanced statistical visualizations, including countplot and barplot with categorical color palettes.

### 3. Functions and Methods Used
- pd.read_csv(): To load the dataset.
- df.dropna() / df.drop(): To handle missing data.
- df.groupby(): To aggregate acceptance rates across different categories.
- sns.barplot() / sns.countplot(): To visualize the probability of acceptance across variables like time, weather, and frequency.
- Boolean Masking: Used extensively to filter segments (e.g., (df['age'] < 30) & (df['Bar'] > 1)).

### 4. Key Findings
- Use Case 1: Bar Coupons
- The overall acceptance rate for Bar coupons was 41.2%.
- The "Regular" Effect: Drivers who visit bars more than 3 times a month accepted the coupon at a rate of 76.2%, compared to 37.3% for infrequent visitors.
- Social Context: Drivers with no kids in the car and a habit of visiting bars had a high acceptance rate of 70.9%.
- Age Demographic: Frequent bar-goers under the age of 30 were the most likely to accept (72.0%).

- Use Case 2: Coffee House Coupons
- The overall acceptance rate for Coffee House coupons was 49.6%.
- Timing of the day: The highest acceptance occurs at 10 AM (63.5%) and 2 PM (54.5%).
- Social Influence: Drivers with friends or partners are significantly more likely to accept coffee coupons than those driving alone.
- Environmental influence: A "High-Probability" segment was identified (Frequent visitors + Sunny weather + No urgent destination) which boasted an acceptance rate of 74.4%.

### File hierarchy: 
1. prompt-Mod5-Response-Jan2026.ipynb: The Jupyter Notebook containing all Python code and visualizations.
2. coupons.csv: The raw dataset.
3. README.md: Project summary and findings.
prompt.ipynb: The Jupyter Notebook containing all Python code and visualizations.
coupons.csv: The raw dataset.
README.md: Project summary and findings.
