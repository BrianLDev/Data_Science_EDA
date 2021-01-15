# Kickstarter EDA Review of Austin Booth's Notebook
## Brian's notes and comments...

1-2 - Perfect work on these, nice job.

2b. Ah, you caught those 1970s error projects too!  Most people missed them.

3a. Success rate calc is all good, but be careful storing percentages in human readable format (* 100) since that can cause issues with calculations.  Recommend leaving them in the normal deciman format e.g. .6258 instead of 62.58%.

3c, 4a - Same here. Careful with the percentages stored * 100

4c. This one threw everyone for a loop, but you did a great job with it by aggregating the > 300% into one column to make the histogram readable.

5f. Excellent analysis and combining various info to recommend the best main_category.

6b. I like your approach using .describe() to compare the months/days in successful vs not successful.

7a. Ah, here's where storing the percentages in human readable format came back to bite. Your expected values are inflated 100x (e.g. Video games should be $85 instead of $8,513).  I recommend switching any percentages to standard decimal format to avoid this.

7b. The exp_value by year for Video games is a lot different than mine and others in the group. And it's not just the * 100, so something else may be going on here.  Recommend double checking this one and comparing against the rest of the group.

8 - This is perfect.