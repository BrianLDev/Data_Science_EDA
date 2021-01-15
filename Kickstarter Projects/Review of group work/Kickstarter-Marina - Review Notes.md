# Kickstarter EDA Review of Marina's Notebook
## Brian's notes and comments...

1a. Please display the unique values and counts.  Looks like you stored them in the `states` variable so if you just put `states` at the bottom of the cell, then Jupyter will display them.

1c. Nice filter out using the `~` symbol

2b. It helps to see the pledged amount too when showing the top 5 most pledged

2c. Same here, helps to see the number of backers on the top 5 results

3a. It looks like theres a math error here because your success rates are different from mine and Bojan's.  For example, we got .491 (49.1%) for Music and you got .181 (18.1%).  Also, be careful when storing percentages in the human readable format (* 100) because it will cause problems with any calculations on those percentages unless you convert them back again by dividing by 100.  I usually just store them in standard decimal format (e.g. .491).

3b. The bar chart looks good but it's thrown off by the calc issue in 3a.  Once that's fixed this should automatically work itself out.

3c. Similar math issue here on the Games sub-categories. e.g. Bojan and I got .204 (20.4%) for Video Games but you got .191 (19.1%).  Check out either of our notebooks to see what's different.

3d. Same here, chart is good, just needs corrected values from 3c.

4a. Good job using the usd_real amounts to calculate the pct of goal.  That's key since those are the normalized amounts.  Your numbers match mine but again be careful storing in human readable percent format.  Better to store as normal decimals.

4c. I love that median line! :)  And interesting approach using the log of values to make the chart more readable.  Only recommendation would be to split the data in two: not successful and successful and have 2 separate charts for those.  Bojan did that pretty nicely on his.

5f. Excellent work on the recommendation!  You combined success rates and dollar amounts well.

6a. Pleae display some of the `months` data after calculating so we can see how it turned out.

7a. Looks like there's a math error here on the exp_val calc.  The video games success rate of .204 matches me and Boja, but for some reason we got different expected values.  We got $85 and you got $2,291. Big difference so it's worth double checking this.

7b. Please display the results for exp_value broken down by deadline year

7c. Chart looks great. Will automatically be fixed when you updtae 7a.

### FINAL NOTES:
Awesome work!  There were a few minor math issues, and I'd recommend saving percentages in their decimal format, but overall you got through the full project and presented the visualizations really well.  Especially a big fan of the median lines on your histograms.  

Suggestion to minimize the math issues that you were running into: create separate columns in a dataframe and then use those to calculate percentages.  e.g. on success rate, create one column with the total count, another column with a successful count, and then calculating the SuccessRate is as simple as dividing one column from another.