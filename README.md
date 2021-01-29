# pandas-challenge
This is the fourth homework for the University of Minnesota Data Visualization and Analytics Boot Camp using python.

##Requirements
This challenge requires use of the Pandas library and a Jupyter Notebook. There must also be a written discription of at least two observable trends based on the data. 

The script must complete the following: 

##PyCitySchools

Analyze the district-wide standardized test results. There are two spreadsheets:
schools: includes an ID for each school, the school name, the type of school, the size and budget. 
students: includes an ID for each student, the student name, gender, grade, the school name, reading and math scores. 

### Set up
The first thing done in this script was to import the pandas library. Then both of the csv files were read and stored as dataframes. The two dataframes were merged on school name to set up the rest of the work. This combined dataframe is the core dataframe used throughout this script. 

### District Summary
To complete the summary total students, average math score, average reading score, total budget, and total schools was then set using either the .count, .mean, or .sum functions. The number of students passing the different subjects was set using the .loc function.

### School Summary
To complete the summary for each school three new columns were added to the combined dataframe: students passing math, reading, and both subjects. The .loc function was used to complete this task. Next the schools were grouped and summed to create the by-school-summary. A new dataframe was set with a limited number of columns and then the dataframe with number of students passing and the by school summary was merged. Then a series of columns were added to get the budget per student, the average scores by number of students, and the percent of students passing by school. 

### Top and Bottom Performing Schools (By % Overall Passing)
The dataframe developed for the school summary was then sorted using the sort_values function. To get the best schools ascending was set to false. To get the worst schools ascending was set to true. To see only ten schools the dataframe was set to .head(5)

### Math Scores and Reading by Grade
To complete these summaries the .loc function was made to create a series of scores for both math and reading based on grade. These were merged together and then grouped. The .mean function was used to come up with the average scores by school by grade. 

### Scores by School Spending and School Size
The dataframe created for the school summary was used. Only a few columns were needed for this summary so a new dataframe was set to be used for these two summaries. The bins for both were set up followed by the labels. Then new columns were generated and added to the dataframe for these summaries. Before each was printed out the dataframe was shortened to only show the relevant colunns and a groupby was done based on the new columns made by the pd.cut function. 

### Scores by School Type
This was a simple groupby table using the .mean() function based on school type. 
