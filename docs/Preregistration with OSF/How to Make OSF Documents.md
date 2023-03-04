
When creating OSF documents, our main goal is to end up with 3 files for each study: a materials file, a data dictionary (previously known as codebook), and a public dataset. Before starting your public dataset, you will need to do a process known as [[Data Entry Checking]].

---

Below are some guidelines that should be the same across all of the OSF files.

1.  Header should have the document type (i.e. materials/codebook) and study number on the left, and (author, journal, in press) on the right
2.  Add a line on the title page that indicates who created the document and who checked it.
3.  Date in the title page should correspond with the date the document was created
4.  Make sure the font is 11 point Times New Roman (fonts in the materials doc should match what the participant saw in the study)
5.  Titles follow this format:  
![[osf_titleFormat.png]]

#### Materials (for both RAs and authors):

This document shows the questionnaire in the format it was presented to participants. Here’s a [link](https://osf.io/bh76u/) to a completed OSF materials doc from our lab.

-   For paper surveys, find the original file that was used to print off the surveys 
-   For Qualtrics surveys, download the survey as a word doc from Qualtrics 


1.  The description of the ANOVAs (e.g. “2 (gender, between) X 2 (interest, within) ANOVA”) should be formatted in the same way that they are in the paper. In other words, make sure that the levels of the ANOVA are labeled the same way across the paper and materials.
2.  Page breaks are indicated by lines.
3.  Text in square brackets ([]) indicate descriptions of something that the participants saw. For example, “***[Image of manipulation presented here]***”.
4.  Text in curly brackets describes parts of the survey for the reader. For example, “***{Participants were directed to the following page if they answered questions on this page accurately.}***”

#### Dataset:

This file presents all of the data used in the write-up. There are two datasets that need to be created, both in xlsx format. The first one is the questionnaire checking file that can be used for checking that there were no errors from the original to the final dataset. The second one is the public dataset that only provides information readers would need if they wanted to reanalyze the data (example [here](https://osf.io/754p8/)).

##### Questionnaire checking file (created by the analyst):

1.  In SPSS/R
	1.  Remove exclusions (sometimes we keep them in and provide a column that says whether they were excluded but usually easier to exclude). Remove participants who didn’t consent (1), duplicates, elected to withdraw their data, are under 18 (depending on IRB permissions), or didn’t answer any questions.
	2.  Remove any calculated variables that are not used in the paper (e.g., ones that were exploratory) (can be done in Excel)
	3.  Sort rows in order of collected (or in an order that makes sense, e.g., population)
	4.  Sort columns in order of questionnaire, with calculated variables at the end
	5.  Add a column in first position with subject numbers starting at 1 if you don't have them or if your subject numbers are identifiable (e.g., Prolific Ids)

2.  Export to Excel and then:
	1.  If exported from SPSS, search and replace all the #NULL!s with blank
	2.  Size columns so all the text is visible (can make exceptions for really long text fields)
	3.  Freeze first row and subject number column

3.  When sending the file to the RAs, include the methods section of the study that says which questions the calculated vars represent with the file, if needed add detail from questionnaire. For example:

	**PassionImpMajor:** five questions on the extent to which they believe it is important to follow their passions in choosing their major (e.g., “It is important to me to follow my passions to guide my choice of major", "I should pursue a major that I am passionate about", "I should do what I love when it comes to picking a major", "I should follow my passions when choosing my major.", "Following my passions should drive my choice of major.")

	**Resource-driven ideology factor**: averaged income potential, sensible and realistic, and job security to form a single 

	**FirstGen**: no parent with a 4-year college degree

  
##### How to questionnaire check (RAs)
There is a multi-step process for approaching these larger datasets.

1.  Create a column within the Excel file containing the clean data named “randNumber” and enter the function “=RAND()”. Drag this function down for all cases and now all participants should have a randomly generated number from 0-1.
	- Create a second column titled “randNumberStatic” and copy and paste the values from the first column as values. This will prevent the numbers from regenerating.
2.  Calculate the number of responses that make up 10% of the total (For example, if there are 236 responses, we will check 24 of them). These will make up the 10% of cases we check.
	-  Remember to include the first and last case as part of this 10%.
3. Sort the “randNumberStatic” column from largest to smallest and select the remaining number of cases to select the 10% we will check.
4.  Use either the participant ID (for paper surveys) or Response ID (for Qualtrics surveys) to match the cases needing to be checked from a raw data file. 
	- For Qualtrics surveys, you may need to revisit what the recode values for an item were to make sure you’re interpreting them correctly. For example, is a “1” for variable “gender1” for “woman” or “man”?
5. Recalculate any calculated variables either using excel formulas or a calculator based on information provided by the analyst.
6.  Highlight the cases/rows that you’ve checked green and put your initials at the end of each row you check. If any values do not match, highlight those values in red
7.  Save the questionnaire checked file to the server, send the file to the analyst/lab manager, and let them know if you found any inconsistencies.
8.  If the 10% of checked cases have no mistakes, then we stop data checking there. If we find mistakes within the 10%, then we will either data check another small batch from the larger dataset and/or data check all responses.

#### Public data file 
(highly recommend creating in R; see R data template for example code):

1.  Use the original analyst’s questionnaire checked dataset to make the public dataset
2.  Remove “ResponseId” and “id” variables if they potentially identifiable (from Prolific, MTurk, etc)
3.  All calculated variables (e.g. composites, reverse-scored variables) are usually removed from the public data set unless the analyst has told you to leave them in. 
4.  Common variables to take out of the public dataset: ResponseId, id, age, sexualOrientation, bornUS, yearsUS, monthsUS, usCitizen, countryCitizen, year_other, gender_other, race_other
5.  Remove the second major,  minors, or concentrations listed in the “major” variable if included. If a major seems like it might be identifiable (e.g., small program that only one school has), remove specifics (e.g., computer programming and system analysis -> computer programming). You might need to Google to figure out if two listings separate majors or a single program. If in doubt, remove the second listing.
6.  Bold the variable names. 
7.  Sort rows in order of collected (or in an order that makes sense, e.g., population).
8.  Freeze first row and subject number column.
9.  Format column width by selecting the whole sheet and double clicking between the “A” and the “B” at the top. (Can manually adjust open-ended width if too long)
10.  Under notes, clarify why there are people who have decimal answers (e.g., 3.5) in each variable when the scales aren’t continuous (e.g. for Likert scales)
11.  Use the recoded columns for race and gender and any other demographic variables that were recoded (so that we’re presenting the clean versions of them) and drop the original unrecoded columns
12.  Make sure there are no spaces between race entries (e.g. “3,5” not “3, 5”)
13.  Labels in the data file (e.g., man/woman, Hispanic/Latino or Hispanic/Latino American) should correspond with the original survey (not necessarily the labels from the main analyst’s file)

#### Data dictionary (formerly known as codebook)

This document lists all of the variable names, the text of the questions shown to participants and the values that correspond to the answer choices. Variables should be listed in the same order that they are listed in the dataset. Here’s a [link](https://osf.io/2sqga/) to a completed OSF data dictionary from our lab.

**For RAs:** you will receive a dataset from the authors to create the codebook. You will create the codebook in a new word doc.

1.  Variable names should be bolded
2.  Add “:” after each variable name
3.  Check that the variables that say “text specification for #_” are referencing the correct variable number
4.  Common response characteristic variables and their descriptions (automatically downloaded from Qualtrics):
	a.       subNum: Individual participant identifier
	b.       StartDate: Date and time that the participant started the survey
	c.       EndDate: Date and time that the participant finished the survey
	d.       Status: Type of response collected
	e.       Progress: Progress that the participant made before finishing the survey
	f.       Duration (in seconds): Length of time it took the participant to complete the survey
	g.       Finished: Indicates if the participant completed the entire survey

		0: Did not answer any questions
		1: Finished the survey

	h.       DistributionChannel: Method of survey distribution
	i.       UserLanguage: Language in which the participant took the survey
	j.   RecordedDate: Date and time that the participant submitted the survey

5.  Include consent in the data file and codebook.
6.  Use RaceRecoded, and GenderRecoded instead of race and gender.
7.  Take out participants who did not answer any questions and mention it in the notes.
8.  If the responses were just previews or 999s then don’t mention it in the codebook. If the responses were from participants, then make a note about them in the codebook (e.g. “Response removed based on id”)
9.  All variable codes (recode values in Qualtrics) in the data file should correspond with the original numbers downloaded from Qualtrics, not corrected codes (e.g. any 9s and 10s from Qualtrics errors should be left in the public file)
10.  In general, one file for the materials is better than multiple (they can be combined using footnotes)
11.  Consistently indent all the variables in the codebook
12.  Every variable (including recoded variables) should have the question listed and possible responses listed under it (ex. ‘Open-ended’, ‘Female, Male’, ‘1-not at all to 7-very much’)
13.  Every recoded variable has an explanation of how it was recoded

**For authors:** the dataset you give to the RAs to begin creating the codebook needs to be your final, analyzed dataset. When formatting your dataset, make sure you:

1.  Reorder your variables in the order of how they are presented in your questionnaire/survey (excpt calculated variables - place those at the end)
2.  Include an explanation of how each calculated or recoded variable was calculated or recoded  
3.  If you have any numbers that represent names/something specific, replace those values with the actual names/specs (e.g. Labor Market)

#### Race Recodes:

The race and gender responses should be recoded in the RaceRecoded/GenderRecoded variables, **NOT** into the original race/gender variables directly. Below are some responses and how they have been recoded in previous studies.

1.  Turkish→ White
2.  South Asian→ Asian
3.  Slavic→ White
4.  Mixed→ More than one race
5.  Greek→ Other
6.  Foreigner→ Base response on birthplace
7.  Somali→ Black 
8.  Chinese→ Asian
9.  Indian→ Asian
10.  Indian-American→ Asian
11.  East Indian→ Asian
12.  Jewish American→ White
13.  American→ Other
14.  Middle Eastern Christian→ Other