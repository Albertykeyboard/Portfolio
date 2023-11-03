9/30/23
Protein Designations from the MCLP were used as the naming nomenclature.

Went through all the data and reassigned them such that the protein labels were labeled the same as MCLP Nomenlature

This was done in excel under the uniformity set.


11/2/23
The indication data would also be useful to match.
In this case MCLP doesn't have any indication. However because many of the same cell lines maych the CCLE dataset we will use CCLE
Tumor indications.

I am unsure if this is wise, but some kind of categorical classification on the tumor indication is needed. 

We can't use the patient indicatioin data from the TCGA-pan32 even though MCLP and TCGA-pan32 were tabulated by the MD anderson team.
They have set more specific indication sets that are clinically diagnosed. 
This may limit my models ability if I decide to use the TCGA-pan32 as a supervised test set, since I want my model to be more generalized

It may be worth considereding after building a predictive model to run a reverse set with the patient data predicting cell lines.
This would be the reverse where we use patient data to figure out which cell lines could be used for invitro study to mimic the patient.

I Need to think about this more because it may be more useful for diagnosing and selecting a therapy for a clinician.
However, from the standpoint of drug development and design the use of cell line outcomes to predict clinical outcome is more logical when defining indications.


It's become clear that I will be unable to to simply match cancer types for MCLP to the CCLE.

Although the CCLE does provide a decent basis, I still have around 359 samples that need to be classified manually.

I will reconvert the MCLP data into a CSV and manually search and enter the samples.

To do this manually I am using Cellosarus
