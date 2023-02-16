# Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users

This repository contains complementary information to the study described in the paper \emph{Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users}, \url{https://doi.org/10.1145/3544548.3580863}. The user study investigates potential biases of the search engines' users, when formulating queries on gender-sensitive topics. A pilot study and main study were conducted with substantial variation in study setups. This is described in detail in the main paper. Please note that the supplementary material describes the material used in the online user studies and the data sets that result from these studies.

## Pilot study

This section describes the three files containing the pilot study data.

** DocumentsPilot.csv **

The file `DocumentsPilot.csv` contains a set of 22 documents that were used in the pilot study. Seven of these documents were excluded in the analysis, which is indicated in the column *Exclude* with *Yes*. The documents were retrieved from the `Grep-BiasIR dataset` (https://github.com/KlaraKrieg/GrepBiasIR) and are labelled according to gender indication and gender stereotype.

** DatasetPilot.csv **

The file contains the results from the pilot study, where one query formulation was defined as one task. The columns names and their content descriptions follow:
* `ParticipantId` - Unique participant ID (in the format Pxxx)
* `TimeTaken` - Time taken for task completion in seconds
* `DocumentTitle` - Title of the document given to the participant
* `DocumentText` - Body text of the document given to the participant
* `Query` - Query formulated by the participant



```
@inproceedings{krieg2022grep,
  title={Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users},
  author={Kopeinik, Simone and Mara, Martina and Ratz, Linda and Krieg, Klara and Schedl, Markus and Rekabsaz, Navid},
  booktitle={Proceeding of the ACM Conference on Human Factors in Computing Systems (CHI)},
  year={2023}
}
```
