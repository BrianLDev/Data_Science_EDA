# Kickstarter EDA Review of Bojan's Notebook
## Brian's notes and comments...

1c. I like your method of removing the live, undefined and suspended projects using the `~` symbol:  `completed = df[~df['state'].isin(['live', 'undefined', 'suspended'])].copy()`

2c. Using .nlargest doesn't show the name, so it makes it hard to see which projects had the most backers.  I recommend sorting by backers and then just showing the top 5.

4a. It looks like you used `pledged` and `goal` instead of `usd_pledged_real` and `usd_goal_real` in this one.  Pledged and Goal are all in mixed up currencies, and the `usd_real` amounts are normalized in US dollars and adjusted for inflation.  That will make a big difference in the rest of the project since a lot of calculations are driving off of these numbers.  I'll reword the question to make it more clear but if you have some time, change this one over to reference the `usd_real` amounts.

4b. Same situation as 2c. here with .nlargest on pct_of_goal.  It helps to have a name attached so we know the projects are associated with the ID.

4c. Good job zooming in on the 2 groups: unsuccessful and successful 100%-200%.  I also love the mean and median lines :)

5a. You used a pivot table, perfect!  That was my intention for a lot of these questions when writing them, especially towards the end.

5f. You're thinking about this one the right way, but the calculations are thrown off by the `pct_of_goal` issue from 4a. above.  Update the pct of goal calc to use usd_real amounts and it should fix this.

6a. Please display the results of the calculation with a .head() or similar so we can see if the months calc worked as expected

6b, 6c. Perfect, I found the length of a project has no impact either

7a. Everything is good on this but 1 small issue that is inflating expected value.  You multiplied success rate by 100 to get it into "human readable" percent format, but then forgot to divide by 100 again when multiplying by the median pledged to get expected value.  So the expected value is 100x too big.

7b. Nice job on this one. This in particular took me a while to complete because I was calculating it on all the Games subcategories using a Pivot Table.  But as with previous, the success rate * 100 is inflating the numbers so just need to adjust for that.

7d. Skipped this one, huh? :)

### FINAL NOTES:
Overall, great job on this.  You answered the majority of the questions correctl and used some good pandas techniques to do it.