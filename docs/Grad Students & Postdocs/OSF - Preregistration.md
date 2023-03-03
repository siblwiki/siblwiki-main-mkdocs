All our studies (that aren’t pilots) are pre-registered on the [Open Science Framework](https://osf.io/) (OSF) portal. 

- OSF is a free, open-source platform that connects and supports the research workflow, enabling scientists to increase efficiency and effectiveness of their research.
- Researchers use OSF to collaborate, document, archive, share, and register research projects, materials, and data

All preregistrations should be approved by Sapna over email/Teams before they are posted.

Please contact lab manager for SIBL login information, but are also encouraged to create your own account.

---

### Posting Dataset, Codebooks and Materials

We post 3 types of documents before papers are published. [Examples](https://osf.io/azxgv/) on OSF.  
- As the process of creating datasets, codebooks, and materials is a very time intensive and laborious process that requires a lot of detail-oriented work, it is recommended to have careful RAs help you by starting early with creating these documents AND/OR add an author to the paper (e.g., a lab manager) who can manage this process. 
- Some publications (e.g., JPSP) now also require making code public.

Please see the [[#Checklist for Publishing Paper]] for things that should occur before the paper are posted. 

- Sapna will also need to approve all OSF documents before they are posted and needs a minimum of 2 weeks to do the first round of checking of all the documents. 
- Sapna typically does 3-4 times back and forth on these documents so leave yourself at least a couple of months once they are completed to having them posted. This time can be shortened if Sapna’s list of checks is done carefully and few to no errors are found.

**Resources**

You can find tutorials for making all of these materials (including pre-registrations) at [[OSF - How to Make OSF Documents]] OR visit this [public template](https://osf.io/k5wns/) to find 2 documents: a template and directions on how to preregister.

---

### Checklist for Posting Pre-registration

- Create a pre-registration document using the OSF template, our tutorial, or [Pre-registration Template](file:///Volumes/SIBL/0%20Handbook.Tutorials/Tutorials/Preregistration%20Template%206.4.2019.docx).
	- Pre-registrations should NOT have names or identifying info (e.g., UW) on them in case we make them public when the paper is under review.
- Create a project in OSF.
	- Each project should be thought about roughly like a paper.
- Add both SIBL and Sapna as contributors (administrator level) to the project.
	- SIBL has two linked accounts (@uw and @u.wash), please **add both**.
- Create a component within the larger project. Each component can be thought of as a separate study. I usually select “Other” for category, or you can leave it blank.
- Upload the pre-registration file to the component.
- Permanently register that component by going to Registrations and selecting “OSF-Standard Pre-Data-Collection....".
	- Do NOT permanently register the entire project because you will not be able to change it (e.g., add Study 2). (I made this mistake already a couple of times.)
	- Choose an embargo date that is ~4 years away.
	- It takes up to 48 hours for it to show up as registered (but you don’t have to wait for that to start data collection).
- Once a study concludes, a brief summary of the results should be added to the project within a timely manner.
	- These do not need to be pre-registered, but they will need to be made public when the embargo ends so that we don’t have “floating pre-registers”. If you want to pre-register your results so that it happens automatically, that is fine.

At some point when the paper is ready (we can discuss when exactly on a case-by-case basis), you should make the project public. If you log into our SIBL account, you’ll see examples of permanent/embargoed pre-registrations and results write-ups.

---

### Checklist for Publishing Paper

Please follow this list to check your papers before submitting:

1. Compare procedures to preregistration, including why N differs from preregistration

2. Check that OSF links to main registration page (should say “registration” at top)

3. Compare codebooks to data files
	- var names
	- var order

4. Compare codebooks to materials
	- missing vars

5. Compare materials to paper writeup
	- Programming errors should be footnoted in materials

6. Check data file N matches paper N

7. Conditional formatting on data file to look for weird values (e.g., vars > 7)

8. Add filter to all columns in data file and look at all values

9. Check for duplicates in data files

10. If syntax/code provided, run and compare to paper. Only analyses in paper should be in syntax.
	- Syntax should be well commented and have a header with info