Please aslo double check the [[Pre-Launch Checklist]] for your online launching platform.

---

- Make sure that the consent question has “Force response” selected.
- Check that participants are redirected to the end of the survey when they do not consent to participate.
	- **Note**: If you are running this study on ORPP online, make sure they get redirected to the default “End of Survey” message, not the one that will grant them credit.
- Double (and triple and quadruple) check survey flow
	- Check that blocks and/or questions are randomized correctly
	- Direct participants into conditions using embedded data, not a simple randomizer
	- Check any within-subjects randomization several times by previewing the survey. (It’s easy to make errors with this kind of randomization.)

| Do this     | NOT this |
| :-----------: | :-----------: |
| ![[qualtrics_do.png]]      | ![[qualtrics_notDo.png]]    |


- Test randomization to make sure it’s correct (e.g. preview the study until you’ve seen all of the conditions)
- Name variables using camel case (e.g. variableNameExample)
- Check demographic questions (gender and race are multi-response questions; 4 options for gender, 8 options for race)
	- SIBL’s standard demographic questions can be found in the “Lab Manager” folder in a survey titled “SIBL Demographics”
	- Insert SIBL’s standardized demographics by selecting “Import Questions From…” at the bottom of a block, then searching, “SIBL Demographics.” Don’t forget to select “Keep Question Export Tags” to export the variable _names_ too!
- Check the response validation of every question (force response, request response, and/or only allow certain entries)
- Check content validation for open-ended questions (e.g. restrict participants to only entering numeric or text responses)
	- Under “Add Validation”, select “Content Type”, and then under “Content Type” select the option you want (e.g., Number)
- Check for unusual font/bolding/typos
	- Have Qualtrics export survey to Word by selecting “Tools” -> “Import/Export” -> “Export Survey to Word”
	- The spell check on Word will serve as an additional spell check
- Export data to check variable names and survey flow
- Have Qualtrics prevent participants from taking the survey multiple times by selecting “Survey Options” -> “Security” -> “Prevent multiple submissions”
- Have Qualtrics stop collecting IP addresses by selecting “Survey Options” -> “Security” -> “Anonymize responses” (this is mandatory unless you get IRB approval to collect them)
- Have Qualtrics delete incomplete/partial responses by selecting “Survey Options” -> “Responses” -> “Incomplete survey responses” responses in progress “1 Week” after respondent’s “last activity”
- Have Qualtrics spell check the survey for you by selecting “Tools” -> “Review” -> “Spell Check”
- Have Qualtrics reset the response codes by selecting “Tools” -> “Reset Recode Values” -> “Reset recode values to sequential numbers for all questions”
	- Note: If you forget to do this step, then some questions could have the wrong numeric values in the data (e.g. “7 – Very likely” could be coded as a 10).
	- Note: If you do have 9s, 10s, etc in your data you can still fix it! You don’t need to spend hours manually recoding your variables in Qualtrics. Just select “Tools” -> “Reset Recode Values” -> “Reset recode values to sequential numbers for all questions” and it will override the existing codes. Re-export the data and your data is fixed!
- Have Qualtrics generate test responses for you by selecting “Tools” -> “Review” -> “Generate test responses” (Note: Qualtrics inserts Latin responses to open-ended questions so it will be easy to tell if you forget to delete them before launching the study)
	- Export data as Excel file and select “Use numeric values”. Go to consent question and filter for everyone who said no. All columns after this should be blank. Then filter for those who said yes to the consent question, and there should be test data for all variables
		- If there are missing blocks of data, something is wrong with the survey
- Delete preview responses, test responses, and responses in progress.
- Publish survey

IMPORTANT NOTEs:
- After data collection is completed, make sure to close the Qualtrics survey right away to avoid unwanted extra participants.
![[qualtrics_closeSurvey.png]]