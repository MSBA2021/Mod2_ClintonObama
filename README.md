Topic:                Regression Trees, Regularization

Case:                 Segmenting Clinton and Obama Voters (QA-0807.pdf)

Data:                 Obama.csv, ObamaTOC.xlsx

Code:                 ObamaStarter.ipynb

Assignment:

We will study this case over two days. On the first day, we will explore the case data using Tableau and introduce three new regression techniques in Python. On the second day, teams will compete to forecast Obama’s vote margin in the testing set.

Day 1:

1. Read the case. The case data are in the file Obama.csv. Obama.csv contains data on both primaries that have already ocurred and those yet to occur. For those primaries that have already ocurred, the data set contains both demographic/county and vote data. For primaries that are yet to occur, the data set only contains demographic/county data. See the table below. A table of contents for the data is given in the file ObamaTOC.xlsx. 
2. In Tableau, create a line chart of the vote-margin time series.
    a. First, create a calculated field for Obama’s vote margin: Analysis > Create Calculated Field > enter the title “ObamaPercentMargin” and enter the formula “([Obama] − [Clinton]) / [TotalVote]”. 
    b. Put ElectionDate in the Columns shelf and ObamaPercentMargin in the Rows shelf. 
    c. Is Obama’s vote margin trending up or down through time?  
3. In Tableau, create a scatter plot of vote margin by demo and geo. See http://onlinehelp.tableau.com/current/pro/online/windows/en-us/buildexamples_scatter.html.
    a. Put MalesPer100Females in the Columns shelf and ObamaPercentMargin in the Rows shelf.
    b. Then drag State and County onto Detail and Region onto Color on the Marks card.
    c. Right click anywhere on the chart, Trend Lines > Show Trend Lines.
    d. Do gender and region interact? In what way? Are there other demographic variables that interact with region?
4. In Tableau, create a map of vote margin. 
    a. On the Marks card, select Filled Map from the dropdown. 
    b. Drag State and County onto Detail on the Marks card.
    c. Drag ObamaMarginPercent onto Color on the Marks card. 
    d. Zoom in. Click on any county to see the Obama margin.
    e. What was the margin in Albemarle County, VA? Where is Obama winning?
5. In Jupyter, run through the starter code provided. This code will introduce you to three types of advanced regression models: Lasso regression, ridge regression, and regression trees. Be prepared to discuss how they work in class. There are readings listed in the Jupyter Notebook from the Introduction to Statistical Learning textbook that you will want to read through. In preparation for the second day on this case, teams will want to use one (or more) of these models to compete in the forecasting challenge.
    
|                                                                                        | Vote data           | Demographic/county data |
|----------------------------------------------------------------------------------------|:-------------------:|:-------------------------:|
| Training set: Primaries and caucuses before February 19, 2008 (1737 rows)              | Available           | Available               |
| Testing set: Primaries and caucuses on or after February 19, 2008 (1131 rows)          | Not available yet   | Available               |


Day 2:

1. Prepare your team’s submission to the forecasting challenge. Your team’s goal is to develop accurate forecasts of Obama’s margin percent in the testing set, as measured by RMSE. 
2. Submit your team’s forecasts to the class Kaggle leaderboard at https://www.kaggle.com/t/bff6e936843740c6a40e79f167b4bffb before class. 
    1. Before uploading, create a team with your team name followed by your section letter (the 10 am class is section A and 12 pm class is section B). To create a team, go to the teams tab and choose a team name. Then invite others in your group using the name they have on Kaggle.
    2. You can only submit two times a day.
    3. To develop forecasts for the competition, teams may only use models that we have covered so far in the course.
    4. Please do not use any external information. 
    5. Only teams with reproducible Python code in a Jupyter notebook are eligible for the competition. We ask that the winning team be willing to share their notebook with the rest of the class.
3. Be prepared to show your notebook and discuss your team's modeling strategy.
4. Pick a side: either Clinton or Obama. Suppose you are the candidate’s campaign manager. 
    * What advice would you give about segmentation? 
    * How can a regression tree’s partitions be used as a segmentation tool? 
    * Which segments should your candidate target with their campaign messages? 
    * Were the two messages described in the beginning of the case—Clinton’s “Night Shift” ad and Obama’s “Down on the Farm” speech—well positioned?
5. How would you communicate to your candidate the insights you gained from your model and its forecasts?
6. The top two teams from the forecasting competition and a randomly selected third team will be given 15 minutes to share the insights from their models as if they were advising either the Obama or Clinton campaign. The class will then vote on who has the best combined model and insights. A prize will go to the winning team. Visualizations suppporting your insights are strongly encouraged.