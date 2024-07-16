# EV Charging Points Analysis

This project focuses on the analysis of Electric Vehicle (EV) charging points data. The notebook provides a comprehensive overview of the data extraction, cleaning, preparation, transformation, and analysis processes.

## Data Extraction and Loading Process

The data extraction and loading process involves the following steps:
1. **Importing Libraries**: Necessary libraries such as pandas, plotly, and io are imported.
2. **Loading the Data**: The dataset is loaded into a pandas DataFrame using the `pd.read_csv` method.
3. **Previewing the Data**: The first few rows of the dataset are displayed using `df.head()` to understand the structure and content of the data.

## Data Quality Check Techniques

The data quality check techniques include:
1. **Check for None DataFrame**: Ensures the DataFrame is not None before proceeding with further checks.
2. **Check for Missing Values**: Counts and prints the number of missing values in each column.
3. **Check for Duplicate Rows**: Counts and prints the number of duplicate rows in the DataFrame
4. **Check for Data Types of Columns**: Prints the data type of each column.
5. **Ensure Consistent Column Names**: Strips leading/trailing spaces, converts column names to lowercase, and replaces spaces with underscores for consistency.
6. **Check for Negative Values in Numerical Columns**: Identifies and prints the number of negative values in columns where they are not expected.

## Data Cleaning and Preparation Techniques

The data cleaning and preparation techniques include:
1. **Remove Total Rows**: Identify and removes rows containing the word 'Total' in any of the column as those rows shows total for a particular year in between data.
2. **Filter and Modify Rows for 2024**: Swaps the values of 'Vehicle_Make' and 'Vehicle_Class' for the rows where _Year=2024.
3. **Combine Dataframe**: Combine the dataframe from year 2023 and cleaned dataframe from year 2024.

## Data Transformations and Analysis

Data transformations and analysis are performed to extract meaningful insights:
1. **Data Aggregation**: Grouping data by relevant categories to summarize and aggregate information. This involve calculating the sum  of charging points per location for each operator and count of charging points per location for each operator.
2. **Create New AgeKey Column**: Adds a new column, AgeGroupKey, to the DataFrame by mapping existing age group values to the predefined keys.
3. **Visualization**: Creating visualizations to understand the distribution and relationships within the data. Some visualizations used are donut chart and bar charts.

## Conclusion

The notebook provides a thorough analysis of EV charging points data, from extraction and cleaning to transformation and analysis. The insights gained from this analysis help us in knowing that which operators are at forefront of EV charging stations which is ESB and EasyGo. It also tells 65-74 year Female age group is having highest adoption rate of EV. Another important thing we notice is that highest influencing factor during EV purchase is _Making more of a contribution to a better environment_.
