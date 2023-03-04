Questionnaires vs. Results Checking

**Note:** Data checking process has to be done by publication but getting an early start is highly recommended (before submission) because reconciliation frequently takes over 3 months per study.

---

## Getting the files

The analyzer should inform the checker about where to find the raw data files for the data checking . Those files can often be found in Qualtrics or on the sibl server, but they can also be from our lab server or another checker. Regardless of the source, checkers should go back to the most original files they can find. Keep in mind that the analyzer should only share the data file they worked on with the checkers in rare cases when reconciliation is stuck to avoid repeating possible  errors that were originally made.

## Data Analysis

While assigning checkers, make sure that at least one person has analyzed or will analyze the data using SPSS. This is because based on past experience, people often make more mistakes in R than in SPSS, and many R defaults are not set to match SPSS.

While running the analysis, the first thing that needs to be matched is N. Do not continue the checking process until the N is reconciled.

We always exclude anyone who 1) does not consent, 2) asks to have their data withdrawn (if that was asked), and/or 3) is under 18 for adult studies (if age was asked). For responses with missing data, we leave in anyone who answered at least one question (not including the consent question). The analyzer should let checkers know if there are additional exclusion criteria for their study and point the checker to the preregistration (if applicable).

The naming of variables on the data files is not always very straightforward. To avoid mistakes, checkers should always reference the questionnaire for what variables refer to and not just assume from their name.

Checkers should be liberal about commenting on their own syntax or the script. They should also put a header on their syntax to record their name, date, the name of the project, and who they are reconciling with. This information will be very helpful when people are looking back to see what went wrong, or for other checkers to pick up the unfinished data checking work.

Many analyses involve checking effect size using the Lakens spreadsheet. Checkers should download the spreadsheet from this [link](https://osf.io/ixgcd/), find the most suitable section based on the test they are running, and enter the values from their output. When entering values, use as many digits as possible (e.g., by double-clicking on the SPSS output to copy values).

## Results Checking

The analyzer should share the write up with checkers so they can highlight it. The matching parts should be highlighted in green, and discrepancies in red with a comment of the checker’s result, as shown in the example below:

![[datachecking_highlight.png]]

To avoid mistakes, the checkers should read the text of the results and then look at their own output to find the appropriate numbers, rather than focusing on simply scanning the output for matching numbers. For example, in the figure, the checker would say to themselves, “What is the mean for Arab male applicants,” identify that number in their own output, and make sure the number they have in their head matches what is in the writeup.

Checkers using SPSS should also double click the output table and be extra careful with numbers that end in 5, since this is where rounding errors might happen. For example, the number 370.1945 should be 370.19 after rounding, but it could be shown as 370.195 on the default output table, which might mislead the analyzer to round it to 370.20.

Mediation analysis involves bootstrapping, which will make the CI slightly different each time the analysis is run. If checkers notice small discrepancy between the CI on the write up and their output, they should rerun their mediation analysis 5 times to see if they can get the result match before marking the write up in red.

Checkers should also make sure that the direction that is described on the write up matches with the numbers. For example, if a sentence says “White applicants (_M_ = 1.80, _SD_ = 1.11) are stereotyped as significantly more culturally foreign than Black applicants (_M_ = 3.05, _SD_ = 1.41)”, the checkers should highlight the word “more” in red, and leave a comment to explain what was wrong.

Results checking also involves checking figures. Checking figures means eyeballing bars and also error bars to make sure they look right (e.g., the biggest error bar corresponds to the largest standard error in the output). Because figures cannot be highlighted, checkers should leave a comment like the example below after it’s checked:

![[datachecking_figures.png]]

Results checking also involves checking procedures. To check the procedure, the analyzer should give the checkers the original questionnaire. This can be a word version of Qualtrics if the study was done online, or photos of a physical questionnaire if it was done in person. The checkers should highlight matching sentences that describe the procedure in green and highlight any discrepancies in red and leave comments to offer explanation.

## Resolving Discrepancies

Discrepancies can be resolved by having both the original analyzer and the checker double check the data again and see if their results match. If the results match, the red should be changed to green and the comment resolved. If they don’t, discrepancies can be resolved by commenting or working synchronously. One important first step is to make sure the analyzer and checker are using the same N in their analysis.

After the reconciliation is done, the checker should upload their syntax, datasets, check files, and any other relevant documents to the server.

## Timeline

Checkers do not have to check everything before publication, but they at least need to match all the participant numbers. The whole process should be done before proofs come out.