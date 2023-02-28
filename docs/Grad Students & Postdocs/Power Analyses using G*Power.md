G*Power* is used to estimate minimum sample size needed based on effect size.

Download the [G*Power](https://approachingblog.wordpress.com/2018/01/24/powering-your-interaction-2/)

![[File Images Holder/Power Analyses/poweranalyses_gpower.png]]

1. **Test family** and **Statistical test**: Choose the test.

2. **Type of power analysis:** Calculate sample size base on these factors.

3. Input numbers in the **Input parameters**. In this example, we used effect size _dz_ because it is a _within-subjects_ effect size. For _between-subject_ effect sizes, we use _ds_.
	- See [[File Images Holder/Power Analyses/Lakens 2013 Calculating effect sizes Frontiers.pdf]] for more information about these effect sizes and [this Excel spreadsheet](file:///Volumes/SIBL/0%20Handbook.Tutorials/2%20Graduate:Postdoc%20Handbook/Tutorials/Lakens%20calculating%20effect%20sizes.xlsx) [[SC2]](#_msocom_2) for how to calculate them (also see [https://osf.io/ixgcd/](https://osf.io/ixgcd/) for most up-to-date information).

4. Click **Calculate**.

To calculate effect size for an ANOVA, we use the [Powering Your Interaction blog](https://approachingblog.wordpress.com/2018/01/24/powering-your-interaction-2/).

- That means you would start with the effect size for your main hypothesis and then multiply the number on “Total sample size” by 16 if it’s attenuation interaction, 4 for a knockout and by 2 for crossover.
- Then, the number will be the minimum sample size needed in the study.

If there are **multiple predictions**, we do multiple power analyses for each one and use the highest minimum sample size. For mediation, we use [Goh et al., (2016)](file:///Volumes/SIBL/0%20Handbook.Tutorials/2%20Graduate:Postdoc%20Handbook/Tutorials/Goh%20et%20al.%202016%20Mini%20meta-analysis%20SPPC.pdf) paper to estimate minimum sample size.

#### Power Analysis Resources

[G*Power Guide](file:///Volumes/../Users/linhpham/Downloads/G_Power%20Guide.pdf) breaks down the steps for different statistical tests.

To see an example of how we write up a power analysis for OSF, check out [this](https://osf.io/uwgmj)  or [this](https://osf.io/2dzns) preregistration (must log in to see).
