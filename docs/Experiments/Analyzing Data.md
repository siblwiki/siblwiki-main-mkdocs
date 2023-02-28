Once the data management has been done, there are several steps involved in performing data analysis, as follows:

[[#Step 1: Gathering the data]] (off participants’ computers, if necessary).

[[#Step 2: Merge logsheet and data, review debriefs]] (Prepare the Excel data sheet by merging the logsheet and data together)

[[#Step 3: Making the data SPSS compatible]]

[[#Step 4: Reviewing data in SPSS]]

[[#Step 5: Selecting cases, labeling values, recoding variables, computing variables]], check computed variables with correlations/reliabilities.

[[#Step 6: Determining appropriate analyses]]

[[#Step 7: Running Analyses]] in SPSS

[[#Step 8: Pasting output]] and make a data report.

## Step 1: Gathering the data

Getting data either entered or checked from paper questionnaires or downloaded from Qualtrics is the first step to analyzing the data. All of the data collected through Qualtrics can be saved as an SPSS file. NOTE: If you are downloading data from Qualtrics, skip to Step 5: Selecting cases, labeling, etc. Other important documents, such as the log sheet, need to be incorporated with the consolidated data. Researchers must review debrief information (either entered/checked from paper debriefs or downloaded from Qualtrics).

Normally, getting the data off the computers is done at the end of the study. This process requires you to do the following:
a. Create a soft copy of the logsheet from the hard copy
b. Retrieve the data from paper questionnaires or Qualtrics and consolidate them into one excel sheet with the logsheet data.
c. Check the retrieved data, making sure it matches with the logsheet.

**Creating the logsheet**

1. Start by opening a new Excel document
2. Take the logsheet from the study you are consolidating data from and then replicate it on the first tab on the Excel document. Label this tab “logsheet.”
3. To replicate the data, use the cells on the top row for each of the items on the logsheet (i.e. subj #, experimenter, date...).
    
    ![[File Images Holder/Analyzing Data/createLogsheet.png]]
    
4. Then fill each cell with the appropriate information that corresponds to the above column variable and the logsheet.
5. Freeze the top row by going to View > Freeze Panes > Freeze Top Row
    
    ![[File Images Holder/Analyzing Data/excelFreezePanel.png]]
    
6. Creating the logsheet is finished once the hard copy has been fully duplicated in Excel.

**Getting data off the computers**

1. Go on [Qualtrics.com](http://qualtrics.com/) and sign into SIBL’s account using the lab’s email address and password.
2. After signing in, you should now be able to see the homepage which contains a list of all the questionnaires or surveys that are being administered by our lab.
3. To retrieve the data, we then need to click the name of the questionnaire that we are interested in.
4. We will be directed to the “Edit Survey” page which gives us the option to edit the survey. Then, proceed to click “Data & Analysis” on the grey navigation bar located at the top of the page.
5. After being directed to the “Data & Analysis” page, click on the button that says “Export & Import”. The button is located on the right side of the screen.
6. Then, proceed to click “Export Data” and then click “Download Data Table” shown in pop up box.
7. Then, make sure that you are downloading a CSV/SPSS/Excel file and have “Download all fields” checked before you click the green “Download button.”
8. At this point, the data will be downloaded automatically.

**Checking the data**

Compare the retrieved data to information on the logsheet. You should make sure of the following:

1. Filter out participants with subject numbers/data that say “999 or 9999” (indicating a test run done by an RA or a no-show by a participant) when selecting cases.

![[File Images Holder/Analyzing Data/excelDelete999.png]]
<figcaption align = "center"><b>Line number 17 has a subject number of 1, so we would need to exclude this line in the data analysis.</b></figcaption>

2. Make sure that there isn’t any missing data (i.e. if the logsheet says that subject 805 was run on 1/16/08, but there is no trace of subject 805 in the retrieved data).

	If there is missing data, try looking for it in the data you retrieved (it may have just been a typo) or try looking for it on the other computers and double check the computer it was supposed to come from. If you still cannot find it, then make a note of it, and then ask the RA who ran that subject.

Once all the data has been consolidated and everything matches up with the logsheet, save your Excel file into the data folder in the appropriate study you collected from as ***Name of study* Consolidated data *date***.

## Step 2: Merge logsheet and data, review debriefs

For studies conducted on Qualtrics, data will be on the results page for download and we need to combine it with logsheet data if it was ran in lab. If the study was run online there will be no logsheet. The first step is to merge them together by bringing the logsheet information onto the data sheet. For this we use Excel formulas.
1. Open the Excel data file to be analyzed. 
2. Copy all the variable names from the logsheet except the first one (subject number) and paste them on the “data” sheet in the first row after the last variable on that sheet. 
![[File Images Holder/Analyzing Data/excelDataEntering.png]]

3. Put your cursor in the top rightmost empty cell (in this case column DN row 2). Click insert function (fx) and find the “VLOOKUP” function.

![[File Images Holder/Analyzing Data/excelInsertFunc.png]]

4. Enter the values as described below. Press okay.
    
    ![[File Images Holder/Analyzing Data/excelFunctionArg.png]]
    
5. The formula should look up the subject number and enter the appropriate value from the logsheet. Double check to make sure this is working.
6. Copy-paste the cell with the formula down for all the subjects.
7. Copy-paste the cell with the formula over to the other variables. Change the column from “2” to “3”, etc.
8. If there are missing values (i.e., a subject number that doesn’t have an entry on the logsheet), #N/A will show up in the cell. Those values need to be checked to figure out why they are not showing up.
9. If there are blanks on the logsheet, they show up as “0” on the data sheet, which of course is a big problem because we don’t want missing values to be counted as “0” when we are calculating our statistics. To fix this, you have to edit the formula, by adding two more formulas to it: IF() and ISBLANK(). You can do this in the formula bar after clicking on one of the cells.

![[File Images Holder/Analyzing Data/excelIF.png]]
<figcaption align = "center"><b>This new formula says the following: If you look up the subject number in B2 on the logsheet and go over two columns and that cell is blank, then just put a blank in my cell. If the cell is not blank, then put the value that is in that cell in my cell.</b></figcaption>

10.	You’ll need to recopy that formula down to the other rows and across to the other variables. Don’t forget to change the column numbers from “2” to “3”, “4”, etc.
11.	When using Excel formulas, make sure to carefully check several values to make sure they are working the way they are supposed to. Although formulas can save a lot of time, if even slightly incorrect, they can cause systematic errors that can contaminate an entire dataset.

**Check Debrief Data/Questions

Check debriefs to look for any red flags; the debrief questions (and responses) will either be included in the same Qualtrics survey as the original study as a set of debriefing questions or as an entirely separate Qualtrics survey.

In either case, check the set of debriefing questions for any anomalies or red flags (e.g., 999s, odd participant responses).

## Step 3: Making the data SPSS compatible

There are a couple of things you need to do to make the datasheet SPSS-compatible: 

- (1) Get rid of values that SPSS cannot read
    
    This step involves going through the data sheet and making sure there are not any values that SPSS cannot read. This includes doing the following:
    
    1. Checking to make sure there is no text in numerical fields. Text in numerical fields can occur for the following reasons:
    a.	Participants wrote an answer (e.g., “I don’t know”)
    b.	Coders entered a symbol (%)
    c.	Participants entered a range of values (5-6)
    In the case of (a) and (b), delete the text and put any interesting comments in the notes column. In the case of (c), convert it to a number by taking an average.
    2. Change any problematic variable names, including duplicate names and variable names with funny symbols or spaces.
- (2) Eliminate Excel formulas
    
    The next step in making the data SPSS compatible is to get rid of the Excel formulas.
    
    1. Create a new tab called “toSPSS”
    2. Copy all the values on the “data” tab
    3. Select the “toSPSS” tab
    4. Go to Paste > Paste Values
    5. Check to make sure the formulas are gone.
    6. You can also just download it as an SPSS file.

**Importing data into SPSS from Excel

Importing data into SPSS is very straightforward. Open SPSS and use the **File > Open** command to navigate to the Excel file. (A dialog box may open on top of SPSS when you first open it, and you can also use that interface to open your file by selecting “Open an Existing Data Source” and selecting “More Files”.) Use the File Types drop down to select .xls. Select the “toSPSS” sheet.

## Step 4: Reviewing data in SPSS

SPSS has three windows:

1. Main window – what you see now
    1. Data View tab – rows of data, like excel; one subject per row
    2. Variable View tab - where you see and edit information about your variables; one variable per row
2. Output window – after you run an analysis
3. Syntax – recording analyses. Using syntax is an alternative to the point-and-click interface and is optional.

Next, you’ll want to review the data to make sure it looks okay. Delete any extra rows and columns that SPSS may have brought in (signified by periods in the cells).

Calculate frequencies for all the variables and scan through the output to make sure there aren’t any wacky unexpected values. To calculate frequencies, go to **Analyze > Descriptive Statistics > Frequencies** and enter in the variables you would like frequencies for. You can also compute frequencies to see, for instance, how many males and females were in the study or what the majors were of the students. To calculate crosstabs (e.g., condition by gender), go to **Analyze > Descriptive Statistics > Crosstabs**.

## Step 5: Selecting cases, labeling values, recoding variables, computing variables

This section demonstrates a variety of operations in SPSS that deal with cases (subjects) and variables.

**Selecting cases

<aside>
Many times, you will need to include only a subset of the participants (e.g., all the non-computer science majors or only U.S. citizens).
</aside>

**Data > Select Cases > Click “If…”**

![[File Images Holder/Analyzing Data/spssSelectCases.png]]

In box, type the criteria you want (e.g., gender = “M” for males only OR ~ANY(major,"Computer Engineering", "Computer Science") for no CS or CE majors)

- Use Boolean logic (&, |, ~=, ANY())
- String variables needs quotes around their values.

<aside>
📍 String variables are case sensitive, so you will need to include any variants of participant responses (e.g., “computer science”, “Computer science”, “Computer Science”, etc.)

</aside>

To select everyone, go back to **Data > Select Cases and select “All Cases”**

**Labeling variable values

It is good practice to label variable values so that the output is easier to understand. Let’s say you want to change the gender values from “M” and “F” to “male and “female.”

In Variable view: label gender value s with “male” and “female”. Click on grey box in Values column.

![[File Images Holder/Analyzing Data/spssValueLabels.png]]

Enter M for Value and Male for Label; repeat for Female.

In Data View: **View > Value Labels**. When you do computations, the old values must still be used, but the labels will be shown in the output.

**Recoding variables

Sometimes, you need to recode variables from string to numeric, reverse-code a variable, or group participants together based on their answers. For instance, let’s say you want to change the year values from “Freshman,” “Sophomore,” etc to 1, 2, etc.

Go to **Transform > Recode > Into Different Variables**

![Untitled](File%20Images%20Holder/Analyzing%20Data/spssRecode.png)

Highlight “year” move it into the box
Type “year_r” in Name > Change

![Untitled](File%20Images%20Holder/Analyzing%20Data/spssRecode2.png)

Click on **Old and New Values**
In **Old Value**, type Freshman
In **New Value**, type “1”
Click **Add**
Repeat for Sophomore (1), Junior (2), and Senior (2)
In Data View, scroll over to the right and you will see your new variable

**Computing variables

Anytime you need to create a new variable by performing a computation (e.g., adding two variables together), you use **Transform > Compute**.

![[File Images Holder/Analyzing Data/spssComputeVar.png]]

In **Target Variable**, type new variable name (weightedgpa)
In **Numeric Expression**, type computation (MEAN(currentgpa, majorgpa)

When computing variables, RAs should check the new variable to see if it has good correlation/reliability (e.g., Pearson’s r, Cronbach’s alpha).

**When a new variable is created by combining *just* two variables** (as in this example), we use correlation to check the computed variable. To do this, go to **Analyze > Correlate > Bivariate.** 

The default settings should be sufficient, but to be explicit, you should select “Pearson”, “two-tailed”, and “flag significant correlations”. Any other statistical options are not necessary for the purposes of checking the correlation.

**When a new variable is created by combining *more* than two variables**, we use reliability to check the computed variable. To do this, go to **Analyze > Scale > Reliability Analysis.** Again, the default settings should be sufficient, but to be explicit, you should select “Alpha” for the reliability model. Any other statistical options are not necessary for the purposes of checking the reliability.

## Step 6: Determining appropriate analyses

Next, you’ll want to determine what statistical analyses you need to perform. This can be a complicated question that can be assisted by a previous class or two in statistics. Below is a **flowchart outlining** the basic tests that social psychologists often conduct; note that it does not represent all the statistical tests out there, so you should use this as a guide rather than a definitive resource.

![[File Images Holder/Analyzing Data/statsTreeDecision.png]]

## Step 7: Running Analyses

Once you have determined the analyses you want to run, you can point-and-click your way through almost all of the analyses.

- ***T-tests* -** Compare the means of two groups to each other

		Analyze > Compare Means > Independent samples t-test

![[File Images Holder/Analyzing Data/spssIndTtest.png]]

Click on **Define Groups** and put M and F (or whatever your original male/female values are) in Groups 1 and 2
    

Reading output

![[File Images Holder/Analyzing Data/spssOutput_IndTtest.png]]

Women and men report being equally likely to major in computer science, t(3) = -1.63, ns.
    
- ***2 x 2 ANOVA (one+ within subjects factor)* -** Assess how two independent variables interact to impact a dependent variable

		Analyze > General Linear Model > Repeated Measures

![[File Images Holder/Analyzing Data/spssRepeatedMeasures_define.png]]
Type in the name of the within-subjects factor and the number of levels (conditions) it has. Click **Add**, then click **Define**.

 ![[File Images Holder/Analyzing Data/spssRepeatedMeasures.png]]
Select the within-subjects variable for (1) and (2). Select the between-subjects variable.

Click on **Plots**
Gender in **horizontal axis**
Year_r as **separate lines**
Click **Add**

 **Reading output:**
![[File Images Holder/Analyzing Data/spssOutput_Multivariate.png]]
    There is a significant gender x condition interaction, F(1, 40) = 7.24, p < .05. Women are more interested in room 2 than room 1 while the opposite is true for men. (Look at the “room*sex_dc” column for the interaction of gender x condition.)
    
- ***2 x 2 ANOVA (both between subjects factors)*** - Assess how two independent variables interact to impact a dependent variable

    Analyze > General Linear Model > Univariate

   ![[File Images Holder/Analyzing Data/spssUnivariate.png]]

Click on **Plots**
Gender in **horizontal axis**
Year_r as **separate lines**
Click **Add**

![[File Images Holder/Analyzing Data/spssUnivariatePlot.png]]

**Reading output:**
![[File Images Holder/Analyzing Data/spssOutput_Between.png]]
    Gender * Year_r interaction not significant
    
- ***Chi squared analyses*** – Compares frequencies to each other

		Analyze > Descriptive Statistics > Crosstabs

    ![[File Images Holder/Analyzing Data/spssCrossTabs.png]]
    Enter one independent variable in **row(s)** and another in **column(s)**

    Click **Statistics…**

    Check **Chi Square**

    Reading the output:
    ![[File Images Holder/Analyzing Data/spssOutput_chiSquare.png]]

**When you don’t have enough expected count, it means that the sample size is too small to be calculated**

Gives the frequency of choice by gender and the p value (called “Asymp. Sig.” under Pearson Chi-Square)


## Step 8: Pasting output

Saving your output is an option, but pasting the relevant parts of the output into a Word file is preferred so that you can annotate the results. To paste, select the relevant parts of the output and hit **ctrl-K**. Then simply paste into Word.  Sometimes you can also use the regular **ctrl+C and ctrl+V** to copy and paste. Researchers should be creating data reports to summarize their results. Talk to your lab manager/supervisor about giving you a data report template if they do not provide one.