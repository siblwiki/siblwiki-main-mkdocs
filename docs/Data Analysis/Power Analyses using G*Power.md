G*Power* is used to estimate minimum sample size needed based on effect size.

Download the [G*Power](https://www.psychologie.hhu.de/arbeitsgruppen/allgemeine-psychologie-und-arbeitspsychologie/gpower.html)

![[File Images Holder/Power Analyses/poweranalyses_gpower.png]]

1. **Test family** and **Statistical test**: Choose the test.

2. **Type of power analysis:** Calculate sample size base on these factors.

3. Input numbers in the **Input parameters**. In this example, we used effect size _dz_ because it is a _within-subjects_ effect size. For _between-subject_ effect sizes, we use _ds_.
	- See [Lakens, 2013](https://www.frontiersin.org/articles/10.3389/fpsyg.2013.00863/full) for more information about these effect sizes and download [this Excel spreadsheet](https://osf.io/vbdah) for how to calculate them (also see [Lakens' OSF](https://osf.io/ixgcd/) for most up-to-date information).

4. Click **Calculate**.

To calculate effect size for an ANOVA, we use the [Powering Your Interaction blog](https://approachingblog.wordpress.com/2018/01/24/powering-your-interaction-2/).

- That means you would start with the effect size for your main hypothesis and then multiply the number on “Total sample size” by 16 if it’s attenuation interaction, 4 for a knockout and by 2 for crossover.
- Then, the number will be the minimum sample size needed in the study.

If there are **multiple predictions**, we do multiple power analyses for each one and use the highest minimum sample size. For mediation, we use [Goh et al., (2016)](https://compass.onlinelibrary.wiley.com/doi/pdfdirect/10.1111/spc3.12267) paper to estimate minimum sample size.

#### Resources

[G*Power Guide*](https://www.psychologie.hhu.de/fileadmin/redaktion/Fakultaeten/Mathematisch-Naturwissenschaftliche_Fakultaet/Psychologie/AAP/gpower/GPowerManual.pdf) and [UCLA G*Power*](https://stats.oarc.ucla.edu/other/gpower/) breaks down the steps for different statistical tests.

To see an example of how we write up a power analysis for OSF, check out [this](https://osf.io/uwgmj)  or [this](https://osf.io/2dzns) preregistration (must log in SIBL account to see).
