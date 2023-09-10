# ICC-Cricket-Data-Analysis-
ICC cricket data analysis using python and machine learning. 

Table of Contents
Introduction
Load Cricket Data
Player Statistics
3.1 Extract Player-Level Statistics
3.2 Determine Player Type
Cell 3 (Markdown):
Overview
This Jupyter Notebook presents a comprehensive analysis of cricket data, focusing on player performance, match outcomes, and venue statistics. The notebook is structured into various sections addressing data preparation, player performance analysis, match outcome analysis, venue statistics, player performance by venue/phase/opposition, performance score calculation, and a conclusion.

Cell 4 (Markdown):
Section 1: Importing Libraries and Loading Data
In this section, the notebook imports essential Python libraries for data analysis and visualization. It also describes the loading of the latest cricket dataset, which consists of match information (matches) and detailed ball-by-ball data (deliveries) using the Pandas library.

Cell 5 (Code):
This cell imports necessary libraries such as Pandas, Numpy, Matplotlib, and Plotly. It also loads two datasets: match_info_data.csv and match_data.csv.

Now, I'll continue to review the subsequent cells in the notebook and provide comments and suggestions for improvements.

Finished working
Show work
Let's continue our review:

Cell 6 (Markdown):
Section 2: Preprocessing Deliveries Data
This section defines a function, preprocess_deliveries_data, which preprocesses the 'deliveries' DataFrame. The preprocessing includes:

Replacing NaN values with 0 in specific columns.
Calculating the 'total_runs' for each ball.
Restructuring the DataFrame to a standardized format.
Cell 7 (Code):
This cell defines the function preprocess_deliveries_data. This function's primary tasks include:

Replacing NaN values in columns like 'runs_off_bat', 'extras', 'wides', etc., with zeros.
Computing the 'total_runs' for each ball by summing the above-mentioned columns.
Splitting the 'ball' column into separate 'over' and 'ball' columns.
Reordering the columns for a standardized format.
Cell 8 (Markdown):
Section 3: Cleaning Team Names and Venues
This section aims to clean the team names and venue names in both 'deliveries' and 'matches' DataFrames. It addresses inconsistencies in team names by mapping them to standardized names. Additionally, venue names are cleaned by removing location information and renaming certain venues. A function, clean_data, is invoked to clean both DataFrames.

Cell 9 (Code):
This cell defines the function clean_team_names, which cleans team names in a DataFrame. It corrects inconsistent team names to standardized ones. For example, "Rising Pune Supergiant" is changed to "Rising Pune Supergiants", "Delhi Daredevils" is changed to "Delhi Capitals", and "Kings XI Punjab" is changed to "Punjab Kings".

Cell 10 (Code):
This cell defines the function clean_venues, which cleans the venue names in a DataFrame. It removes location details after commas and renames specific venues. For instance, "Sardar Patel Stadium" is renamed as "Narendra Modi Stadium", and "Feroz Shah Kotla" is renamed as "Arun Jaitley Stadium".

Comments:
Good Practices Observed:
Clear section headers and explanations make it easy to understand the purpose of each section.
Use of docstrings for functions provides clarity on their purpose, parameters, and expected outputs.
Use of consistent naming conventions and structure promotes readability.
Improvement Suggestions:
While preprocessing, it might be beneficial to include visualization, such as histograms or bar plots, to understand the distribution of data before and after cleaning.
Consider adding error-handling mechanisms, especially when working with data manipulations, to ensure the notebook doesn't break in case of unexpected data values.
For functions that modify the data in place (like clean_team_names and clean_venues), it might be useful to return a deep copy of the DataFrame instead of modifying the original to ensure data integrity and allow for rollback in case of errors.
