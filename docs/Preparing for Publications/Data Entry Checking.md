
After you’ve entered data from paper surveys into the computer, you still need someone to check it. It is important that the data is checked by someone different from the person that entered the data because this prevents mistakes being repeated by the same person and assures us that the data we are analyzing is correct.

1.  Just as with entering data, start by navigating to the appropriate excel document on the server and open it on the desktop.
    
2.  Grab a questionnaire; they will either be in the study box or in the hanging folders. Then, locate its row on the excel file. Usually, this can be done by finding the corresponding subject number.
    
3.  Moving from left to right, check the two documents making sure the responses that have been entered in Excel match the responses on the questionnaire itself.
    
4.  If there is a typo from the person who entered it, change it and highlight the altered cell in yellow. Be sure that blank answers are marked properly and that written responses are entered in the appropriate standardized manner explained in the ‘Entering Data’ section of the handbook.
    
5.  Once finished checking all the data, type your name in the cell in the checked by column.
	- If there were any mistakes or other things you noticed, leave those in a notes column

6.  Continue this process until all entered questionnaires have been checked.
    
7.  Once finished, save the file by replacing the older version on the desktop with your newest one. 
    
8.  Then replace the old version of that file on the server by dragging the newest version from the desktop back into the server’s window where the old file is located.
  

There are some instances in which we data check **previous large datasets**. There is a multi-step process for approaching these larger datasets.

1.  Create a column within the Excel file containing the clean data named “randNumber” and enter the function “=RAND()”. Drag this function down for all cases and now all participants should have a randomly generated number from 0-1.
	- Create a second column titled “randNumberStatic” and copy and paste the values from the first column as values. This will prevent the numbers from regenerating.

2.  Calculate the number of responses that make up 10% of the total (For example, if there are 236 responses, we will check 24 of them). These will make up the 10% of cases we check.  
	- Remember to include the first and last case as part of this 10%.

3.  Sort the “randNumberStatic” column from largest to smallest and select the remaining number of cases to select the 10% we will check.

4.  Use either the participant ID (for paper surveys) or Response ID (for Qualtrics surveys) to match the cases needing to be checked from a raw data file. 
	- For Qualtrics surveys, you may need to revisit what the recode values for an item were to make sure you’re interpreting them correctly. For example, is a “1” for variable “gender1” for “woman” or “man”?

5.  Recalculate any calculated variables either using excel formulas or a calculator based on information provided by the analyst

6.  If the 10% of checked cases have no mistakes, then we stop data checking there. If we find mistakes within the 10%, then we will either data check another small batch from the larger dataset and/or data check all responses.