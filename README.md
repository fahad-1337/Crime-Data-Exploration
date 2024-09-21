# Crime Data Exploration

Project Overview
This project involves analyzing crime data using Python, focusing on data cleaning, exploration, and visualization. The dataset contains over 319,000 crime records, including details such as the incident number, offense code, district, date, and geographical coordinates. The objective of this project is to clean the dataset, handle missing values, and prepare it for analysis. The code uses libraries such as pandas, numpy, matplotlib, and seaborn to perform various tasks.

__Data Details__

The dataset is stored in a CSV file named crime.csv which was obtained from kaggle. 

__Steps Taken__

1. Data Loading and Initial Inspection<br>
The dataset was loaded into a pandas DataFrame using the pd.read_csv() function with the specified encoding (ISO-8859-11).
The first few rows of the data were displayed using df.head() to get an overview of the dataset.
The shape of the dataset was checked using df.shape, revealing 319,073 rows and 17 columns.

2. Handling Duplicates<br>
The dataset contained 23 duplicate rows, which were identified using df.duplicated().sum().
Duplicates were removed using df.drop_duplicates(), reducing the dataset to 319,050 rows.


3. Data Structure and Missing Values<br>
The df.info() function was used to get details about the data types and missing values in the columns.
Key observations:
Several columns had missing values, including DISTRICT, SHOOTING, UCR_PART, STREET, Lat, and Long.
The OCCURRED_ON_DATE column, initially stored as an object, was converted to a datetime64 data type using pd.to_datetime() to enable time-based analysis.


4. Exploratory Data Analysis<br>
Unique incident numbers were counted using df.INCIDENT_NUMBER.nunique(), which revealed 282,517 unique incidents in the dataset.
Descriptive statistics for categorical columns were obtained using df.describe(include='object'), providing insights into the most frequent values in each category.
Analyzed crime data using Python (pandas, numpy) to identify crime patterns and trends.
Answered key questions like when crime rates were highest, visualizing findings with Seaborn and Matplotlib.


5. Visualization Setup<br>
Libraries like matplotlib and seaborn were imported to prepare for data visualization, which will be used to analyze trends such as crime rates by year, month, and location.


__Libraries Used__
pandas: For data manipulation and cleaning.
numpy: For numerical operations.
matplotlib: For basic plotting and visualizations.
seaborn: For advanced statistical data visualization.
