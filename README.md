#	** KICKSTARTER DATA CHALLENGE - Written Analysis of the Results**

##	**Overview of the project:**
Louise’s play Fever came close to its fundraising goal in a short amount of time. Now, she wants to know how different campaigns fared in relation to their launch dates and their funding goals. 

### 	**Purpose of the Analysis:**
Using the Kickstarter dataset, analyze and visualize campaign outcomes based on their launch dates and their funding goal.

##	Analysis and Challenges: Explain how you performed your analysis using images and links to code, as well as any challenges you encountered and how you overcame them. If you had no challenges, describe any possible challenges or difficulties that could be encountered.

### 	Analysis of Outcomes Based on Launch Date
	Theater outcome by launch date analysis: Analyze the successful, failed and canceled theater outcomes and visualize the campaign outcomes – successful, failed, and canceled based on the launched date.  The steps I took to accomplish this:
-	Added a new column ‘Years’ by extracting the year from the ‘date created conversion’ column using the YEAR().
![Analysis1a](https://github.com/veenapu/kickstarter-analysis/blob/main/Resources/Screenshots/Analysis%201a.png)	
-	Inserted a pivot table with the ‘parent category’ and ‘Years’ as filters, Outcomes in the columns, Months in the rows and Count of Outcomes in the Value field.
-	Then filtered the parent category to Theater
-	Changed the row labels to display Months
![Analysis1b](https://github.com/veenapu/kickstarter-analysis/blob/main/Resources/Screenshots/Analysis%201b.png)	
-	Then inserted a pivot chart to display a line chart for each of the outcomes based on launch date, which is by month
-	Copied the chart to Paint and saved it as a .PNG file
![Analysis1c](https://github.com/veenapu/kickstarter-analysis/blob/main/Resources/Screenshots/Analysis%201c.png)
###	Analysis of Outcomes Based on Goals	
	Outcomes based on Goals analysis: Analyze the percentage of successful, failed and canceled plays and visualize these outcomes based on goal amounts. The steps I took to accomplish this:
-	Created different columns to show the different outcomes for 12 different goal ranges.  Then used COUNTIFS() for counting each of the outcomes for those dollar amount changes by filtering on the Kickstarter "outcome" column, on the "goal" amount column using the ranges created in Step 3, and on the "Subcategory" column using "plays" as the criteria.
-	Then used the SUM() to sum total of these outcomes in the Total Projects column
-	Then three other columns to calculate the percentages of each of the outcomes for various dollar amount ranges
![Analysis2a](https://github.com/veenapu/kickstarter-analysis/blob/main/Resources/Screenshots/Analysis%202a.png)
-	Then inserted a line chart to display the outcomes based on the goals
-	Copied the chart to Paint and saved it as a .PNG file

###	Challenges and difficulaties Encountered
	I did not face any challenges for the Theater Outcomes by Launch Date. 

	However, I did face a couple of challenges when analyzing the Outcomes based on Goals but overcame them when I reviewed and fixed them.
-	While populating the table and using the COUNTIFS() function. It took me a couple of tries before I could work the COUNTIFS() to populate the columns correctly. I had to reread the instructions on the challenge before I could make sure I am factoring in all of the parameters, to get the numbers right.  Then, I was able to get it to work correctly.
-	While charting the Outcomes based on goal, I was fine with the line for canceled projects as there were none and was fine for the successful projects.  But I had trouble with the failed projects line.  After thinking through and going back to the calculations, I realized that when I dragged the formula from %successful to %failed, I had not locked the column.  Once I fixed that, the calculations for the %failed was correct, as it was a mirror image of the successful outcomes.

##	**Results: Answer the following questions in complete and coherent sentences.**

-	What are two conclusions you can draw about the Theater Outcomes by Launch Date?
­	The success rate of launching theater campaign is highest in Mau, followed by June, with projects of 100 or more
­	November and December months show a decline in successful campaigns while there is an increase in failed campaigns from November to December
­	October was the only month that did not have any canceled projects, but overall steady over the given period

-	What can you conclude about the Outcomes based on Goals?
­	The graph of the successful projects is a mirror image of the failed projects
­	The goal range of Less than 1000 shows the highest success rate of 76% while the goal range of 50000 or more shows the least, 13%
­	The goal range of 45000 to 49999 had the highest failure rate of 100%

-	What are some limitations of this dataset?
-	Does not include current data to analyze the trends. The data goes only from 2009 to 2017. 
-	There were only 1369 theater outcomes out of 4064 outcomes.  Adding few more data points of the same kind of data would show a more relevant trend or analysis

-	What are some other possible tables and/or graphs that we could create?
­	A clustered column chart or a separate histogram for each of the different outcomes could be another way to display this data
­	A comparison table could also be created to analyze different categories and sub categories

