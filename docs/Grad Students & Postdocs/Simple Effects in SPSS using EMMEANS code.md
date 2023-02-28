
- **Simple Effects tests** reveal the degree to which one factor is differentially effective at each level of a second factor. (For multi-way analyses, all combinations of levels of the other factors.) Sometimes these are referred to as **Simple Main Effects**.  
- Use a **Test of Simple Effects**. This will produce a table comparing all pairs of levels of one factor, for each level of all the other factors. 
  
This test can be performed with SPSS General Linear Model, using the Estimated Marginal Means option. Unfortunately, at this time to obtain a Simple Effects Test does require the use of *SPSS command syntax*. Here, we will describe how to make the necessary modifications to syntax pasted from the **General Linear Model->Univariate** dialog box.

Example code pasted from SPSS UNIANOVA  

```
UNIANOVA discrimination BY condition
/METHOD = SSTYPE(3)  
/INTERCEPT = INCLUDE  
/EMMEANS = TABLES(discrimination) COMPARE ADJ(LSD)  
/EMMEANS = TABLES(discrimination * condition)  
/CRITERIA = ALPHA(.05)  
/DESIGN = discrimination condition discrimination * condition.
```

We need to modify the subcommand below 
```
/EMMEANS = TABLES(discrimination * condition) 
```

to specify the factor for which we want pairwise comparisons using the subcommand COMPARE(factor) ADJ(LSD).
```
/EMMEANS = TABLES(discrimination * condition) COMPARE(discrimination) ADJ(LSD)
/EMMEANS = TABLES(discrimination * condition) COMPARE(condition) ADJ(LSD)
```
