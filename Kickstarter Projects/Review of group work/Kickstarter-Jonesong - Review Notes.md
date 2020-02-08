# Kickstarter EDA Review of Jonesong (ouakitomo)'s Notebook
## Brian's notes and comments...

1, 2 - Perfect, this is excellent work.  Especially adding a launched year column to the DF to make the competition calc easier.

3 - It looks like you missed my note saying that all calculations going forward should be done on the `completed` dataframe.  That's a simple change but makes a big difference overall so hopefully you can go back and make the change.

4 - I see you said you're confused by the questions. Everyone else was able to answer these so let me know what part is confusing you and I'll see what I can do to help.

5 - Looks like you're still referencing the original df instead of the completed df so these are going to be different.  But that aside most of the work looks correct.

6 - Love what you did to compare successful vs not successful months.  Clean, efficient code here.

7 - It doesn't look like you calculated the expected value here.  exp_value should be the median of usd_pledged_real multiplied by the successRate

8 - On your note "couldn't understand the pct_of_goal", it just takes the pledged amount divided by the goal amount.  Other than that, this is perfect.