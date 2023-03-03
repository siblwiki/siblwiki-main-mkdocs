### General Procedure
Make sure all of the materials have been created:

	- Logsheet
	- Script
	- Consent form (aka Information Statement)
	- Debrief form (optional)
- Save all materials to the server
- Print materials on the first floor of Guthrie using the Xerox machine
- Print logsheet and script on colorful paper
- Information statement should be stamped if the study is not exempt and run on paper (doesn’t need to be stamped for online studies according to correspondence with Deborah Dickstein from HSD).
- Check that information statements correspond to the location where the study is run (e.g. the form shouldn’t mention credit if the study is being run on campus)
- If the same survey is being run in multiple locations (e.g. on campus and online):
	- Check that the surveys match by going through them simultaneously and comparing them word-for-word. For instance, preview the survey on Qualtrics and compare it to the hard copy of the questionnaire.
	- Make sure the variable names are the same across surveys so that it is easier to combine datasets for analyses.
	- Check that the information statements match across locations.

---

### On Campus:

- Check the demographics section to make sure that the bullets were printed correctly
- Have someone in lab take the survey (like a participant) to check for typos

### In lab studies:

- Bookmark the survey (and debrief if there is one) on all of the subject running computers. Make sure it is descriptive enough to distinguish it from other bookmarks (e.g. include the quarter and year in the name).

--- 

### Online ORPP studies:

- Make sure there is a consent form
- Check consent question in Survey Flow (should skip to the end of the survey if the participants do not consent)
	- Under “Customize” for the End of Survey branch logic, check “Override Survey Options” and leave “Default end of survey message” selected
- To automatically grant ORPP online participants credit when they finish the survey:
	- Insert an embedded data element that has the word “id” in it to collect IDs from ORPP.
	- Next, navigate to “Survey Options” -> “Survey Termination” -> “Redirect to a full URL” and add a redirect URL to the end of the survey link. 
		- You can find and copy this redirect URL from ORPP, which should look something like this: “https://uwpsychology.sona-systems.com/webstudy_credit.aspx?experiment_id=908&credit_token=eca3e4225b3c43fcbf1335ff352ea2b3&survey_code=${e://Field/id}”
	- Insert **?id=%SURVEY_CODE%** at the end of the Qualtrics survey URL on the ORPP webpage.

**NOTE**: If you’re setting up the survey yourself or asking someone else in the lab to do it for you (e.g., lab manager), please remember to *give instructions on the filters* you want added

- Some common filters include: gender, age, and participation in previous ORPP studies (this is to filter out participants from previous iterations of the project)

- If you’re trying to recruit equal numbers of different groups (e.g., gender), you will have to duplicate the Qualtrics to have as many copies as there are groups (e.g., women and men participants -> 2 surveys). This is because each study on ORPP provides a unique redirect link, and only 1 redirect link can be entered per Qualtrics


### Online MTurk studies:

- Make sure there is a consent form
- Check consent question in Survey Flow (should skip to the end of the survey if the participants do not consent)
	- Under “Customize” for the End of Survey branch logic, check “Override Survey Options” and leave “Default end of survey message” selected
- Add end of survey challenge codes to make sure participants finish the survey in order to receive compensation.
	- Done by adding three “End of Survey” blocks in Survey flow and selecting the challenge codes under “Customize”.
- Determine the time it takes to complete the survey (this estimate is needed to set up the HIT on TurkPrime)
- Top up the lab balance and MTurk balance, as needed
	- The lab balance is the fund that pays for MTurk’s lab fees
		- Add just enough money so that after launching the study, the amount is close to $0.00
	- The MTurk balance is the fund that pays participants for taking the survey

### Online Prolific Studies

- Make sure there is a consent form
- Check consent question in Survey Flow (should skip to the end of the survey if the participants do not consent)
	- Under “Customize” for the End of Survey branch logic, check “Override Survey Options” and leave “Default end of survey message” selected
- To redirect participants to the Qualtrics survey, copy and paste the anonymous survey link from the “Distributions” section of Qualtrics into the “STUDY LINK” section on Prolific
- To grant Prolific online participants credit when they finish the survey:
	- Insert an embedded data element that has the word “**PROLIFIC_PID**” in it to collect IDs from Prolific.
	- Next, navigate to “Survey Options” -> “Survey Termination” -> “Redirect to a full URL” and add a redirect URL to the end of the survey link. 
		- You can find and copy this redirect URL from Prolific. The URL should look something like this: [https://app.prolific.co/submissions/complete?cc=8355A0F2](https://app.prolific.co/submissions/complete?cc=8355A0F2)
	- Also, add a block within the survey where you explicitly ask participants for their Prolific ID, the instructions should be as follows “Please enter your Prolific ID in the box below. (Note: If there is already a response in the box below, please continue to the next page of the survey.)”
- Determine the time it takes to complete the survey (this estimate is needed to set up the study on Prolific)
	- The default pay is the equivalent of $8.00/hour (or as close to that as possible)
- Top up the account by clicking on the dollar amount in the top-right
- Add just enough money so that after launching the study, the amount is close to $0.00

**NOTE**: if you’re setting up the survey yourself or asking someone else in the lab to do it for you (e.g., lab manager), please remember to give instructions on the filters you want added.

- Prolific is based in the UK, so without any filters, you may get many participants from the UK

- Some common filters include: gender, race, ethnicity, country of residence, and participation in previous Prolific studies (this is to not recruit participants who have participated in previous iterations of the project)

- If you’re trying to recruit equal numbers of different groups (e.g., racial groups), you will have to duplicate the Qualtrics to have as many copies as there are groups (e.g., Black and White participants  2 surveys). This is because each study on Prolific provides a unique completion code link, and only 1 completion code link can be entered per Qualtrics

