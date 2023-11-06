9/30/23
Protein Designations from the MCLP were used as the naming nomenclature. This was done for all th databases.
Went through all the data and reassigned them such that the protein labels were labeled the same as MCLP Nomenlature
This was completed manually in excel under the uniformity set.

Note: MCLP dataset from Raw -> Edit was Unchanged. This was only so I could pull from the Edit Data.


11/2/23
My main dataset for MCLP doesn't have any indication. However because many of the same cell lines match the CCLE dataset we will use CCLE Tumor indications classifications.

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


11/4/23
I reorganized the original code for the preprocessing of the data so that it flow in a logical manner.
The next step for me is going to be to figure out what graphs to generate as well as what model I want to run to model predict
I may run unsupervised classification as well as this may be useful for finding tumor lines that could potentially share sensitivity even if they are a different indication altogether. However, this project should seek to NOT use deep learning style algorithms. This means most of the prediction analysis should be run in scikit learn.