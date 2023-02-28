Step 1: Log into Qualtrics

Step 2: Create a survey

Step 3: Make questions

Step 4: Checklist before launching

Step 5: Download the data after data collection

---

## Step 1: Log into Qualtrics

To log into Qualtrics, go to [https://www.qualtrics.com/](https://www.qualtrics.com/)

Contact lab manager for SIBL log-in credentials.

**Note:** Qualtrics will open on the page last opened by anyone on that folder and study.
This is what Qualtrics looks like when you are logged in. On the left hand side, there are different folders that are organized by project or by graduate student. In the middle, are all the studies that have been created in that folder. You can see the titles of the surveys, the last time it was modified, when it was created, and even the number of responses.

## Step 2: Creating a Survey

To create a survey, find the folder that corresponds to your project or graduate student. Click “Create New Project.” There are 4 options that will pop up:

1. From scratch: this option will give you a fresh and blank canvas to work with. This option also includes the ability to copy a previous survey and transfer it into the new one under the ‘How do you want to start your survey?’ tab.
2. Project templates: this option allows you to use one of the many templates developed by subject-matter experts
3. COVID-19 projects: this option allows you to use a template that considers the changing expectations as a result of COVID-19
4. Academic project templates: this option provides templates that are developed by experts in education
	- To keep the naming consistent, refer to your project manager or follow the following format:
		>Study name – description or location #
			
			For example: 
				- Foster Pre-Test II Fall 2018 MTurk
				- “Foster Pre-Test” is the title, “II” indicates the version number, and “MTurk” indicates where the study is being run at.
				- Bridging Historical and Current Events III Pilot 2 – Debrief
				- “Bridging Historical and Current Events” is the title, “III” is the version, “Pilot 2” is the version of the pilot, and “Debrief” specifies that this is the debriefing form rather than the actual study.

This is what your survey should look like. The main portion of the screen should have all the questions and blocks that you have added. On the left-hand side, there’s a bar with different options related to the question; you can change the question type and add other functions here. You can also click the “Preview” button to see what your survey looks like, through a participant’s perspective. You would use this bar the most to validate questions (requesting a response from participants) and to change the question type.

Blocks are the different pages of questions that the participants see. For example, block 1 consists of all the questions participants will see on the first page of the survey. To add a new block, click “Add Block.”

## Step 3: **Making Questions**

Click “Add New Question,” and Qualtrics should give you a choice of question format. The most common question types are: descriptive text, multiple choice, and text entry.

### **Survey Flow**

Click on the “Survey Flow” bubble in the left-hand bar, and the following screen should appear.

This gives you a more graphic view of your survey. Grey blocks hold your questions and each block corresponds to the blocks you created for the survey. Be sure to save your changes in survey flow before trying to use your survey or clicking out of it. If you don’t, nothing you added to survey flow will be saved.

### **Randomizer**

This allows you to randomize the number of times a participant can see block(s). This is the purple block in the picture above. Clicking “Evenly Present Elements” would allow the different elements underneath the randomizer block to appear an even number of times.

### **Embedded Data**

This allows you to assign a word or number to the participant when they take the study. This is the green block in the picture above. For example, if you have 2 conditions (short and long), you would take the following steps:

1. Type in “Condition into the “Create New Field or Choose from Dropdown” box
2. The box should change to “Condition = Custom Value”
3. Type in “Short” for the short condition
4. Repeat this for the “Long” condition by creating another embedded data block

### **Branch**

This allows you to select which parts of the survey participants see, depending on their condition or how they answer a certain question. This is the blue block in the picture above. For example, Under the Branch block, the following would be presented to you:
“This branch will not be triggered until you Add a Condition”
If you click on “Add a Condition,” the following should appear:
“Question	Select Question”

To branch based on a question, click on “Select Question” and select the question that you want.
For example, you would use this for consent. If the participant did not consent to taking the survey, you can branch their survey to the end and they would not be able to take it.

1. Click the consent question and a select choice option should appear
2. Click on the “Do not consent” option and the following should appear
    
    ```
     “Question
         Q# Please indicate one of the following:
     I do not consent… in this study
         Is Selected”
    ```
    

This indicates that if the answer to the consent question is selected, you’re able to redirect the participant. To redirect them to the end of the survey:

1. Click “Add a New Element Here”
2. Click on “End of Survey”

You can preview how this works by saving the flow first and then clicking on the preview button. When you get to the question and you click “Do not consent,” you should be redirected to the end of the survey.

To branch based on embedded data, click on “Question” and change it to “Embedded Data.” The following should appear:

```
“Embedded Data _____________ Is Equal to ___________”
```

Taking the example from embedded data and incorporating randomizer into it, we would be able to randomly present one of the two conditions. Branch would allow you to specifically present one of the two conditions IF it is equal to a specific condition.

For example:

```
1. Enter “Condition” is equal to “Short”
2. Drag the corresponding “Short” condition block under the branch

```

This means that if the participant was randomized into the Short condition, they would only see that block and not the Long condition.

**Getting the Link for Subject Running**

Go to “Distribution” and then click “Anonymous Link.”
This will give you the link that you will use whenever you are running subjects. You can bookmark this page on the subject running computers you will be using for easy and handy access to the surveys when you are running participants.

## Step 4: Checklist before launching

## Step 5: Downloading Data

Go to “Data & Analysis” and then click “Export & Import.” Click “Export Data.”

From here, you can choose what type of file you want your data to be downloaded as. Usually, you will export data in the CSV format or SPSS format. Be sure to always choose “Use numeric values” whenever you export data.

---

## FAQ

- Can I copy questions from other surveys into my new survey?

    **Yes, you can!** 
    
    When you want to import questions in from other surveys, make sure that these questions are **already in the SIBL library** on Qualtrics. 
    
    <aside>
    🖱️ Add a block → Click “Import From Library…” → Click “Sibl Sibl” → Choose either the survey, block, or question library (this would depend on what you’re trying to import)
    
    </aside>
    
    This can be used to import a **demographic section** into your survey. 
    
    <aside>
    🖱️ Click on “Import From Library…” → Click on the search bar → Type in “demographics” and scroll down until you see “SIBL Demographics.”
    
    </aside>
    
    This survey has all of SIBL’s standard demographic questions. You can either select a few or import all of them.
    
- How do I name questions?
    
    You can change the names of the questions in the main section of your survey. If you see on the top of every question you’ve created, there’s a title or name that comes with it. It’s typically going to say “Q#” where the # is replaced with an actual number and the number correlates to how many questions you’ve added into your survey.
    To change this, just click on the name and it should allow you to change this.
    When naming variables we typically use Camel Case, lowercaseUppercaseUppercase (e.g. howLikelyApply). 
    
    In the demographics section, we use the naming scheme used in the SIBL Demographics survey. Look at this survey for the standard names we assign each demographics question.
    
- How do I randomize a set of questions across participants but present them in the same order within the survey (e.g. randomize the order of conditions, while keeping the order the same within the survey)?
    
    First create embedded data fields for all the possible orders of the items and put them under a randomizer. Note you’ll want to name these embedded fields the exact same way that you want them shown (e.g. capitalized, spaced correctly).
    
    Next, within each of the questions in your survey, click “insert piped text” and select “embedded data” and the correct field to be inserted. Simply do this for all of the questions with the items to be randomized. Make sure to preview your survey to check for errors!