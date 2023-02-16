# Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users

This repository contains supplementary materials from study described in the paper *Show me a \"Male Nurse\"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users*, <https://doi.org/10.1145/3544548.3580863>. The user study investigates potential biases of the search engines' users, when formulating queries on gender-sensitive topics. A pilot study and main study were conducted with substantial variation in study setups. This is described in detail in the main paper. Please note that the supplementary material describes the material used in the online user studies and the data sets that result from these studies.

## Pilot study

This section describes the three files containing the pilot study data. The formatting and contents of each file are described below.

**DocumentsPilot.csv**

The file `DocumentsPilot.csv` contains a set of 22 documents that were used in the pilot study. Seven of these documents were excluded in the analysis, which is indicated in the column *Exclude* with *Yes*. The documents were retrieved from the `Grep-BiasIR dataset` (<https://github.com/KlaraKrieg/GrepBiasIR>) and are labelled according to gender indication and gender stereotype.

**DatasetPilot.csv**

The file `DatasetPilot.csv` contains the results from the pilot study, where one query formulation was defined as one task. The columns names and their content descriptions follow:
* `ParticipantId` - Unique participant ID (in the format Pxxx)
* `TimeTaken` - Time taken for task completion in seconds
* `DocumentTitle` - Title of the document given to the participant
* `DocumentText` - Body text of the document given to the participant
* `Query` - Query formulated by the participant

**DatasetPilotLabeled.csv**

The file `DatasetPilotLabeled.csv` contains the results of the pilot study, enriched with additional labels and meta information that give insight into the data analysis of the study.

* `ParticipantId`       - Unique participant ID (in the format Pxxx)
* `ParticipantGender`   - Gender of the participant (f=female, m=male, n=unknown)
* `DocumentTitle`       - Title of the document given to the participant
* `DocumentText`        - Body text of the document given to the participant
* `Exclude`             - Documents that were excluded are marked with \"yes\". Documents that were excluded because the participant gender is unknown are marked with \"yes (participant gender unknown)\"
* `Domain`              - Domain the document belongs to (0=Appearance, 1=Career, 2=Child Care, 3=Cognitive Capabilities, 4=Domestic Work, 5=Physical Capabilities, 6=Sex&Relationship)
* `DocumentId`          - DocumentId is a unique ID for each document
* `GenderIndication`    - Gender indication of the document variation (f=female, m=male, n=neutral)
* `ExpStereotype`       - Expected Stereotype depending on the domain a document belongs to (f=female, m=male, u=undefined)
* `Query`               - Query formulated by the participant
* `Label`               - Label denoting the gender mentions in the query (f=female, m=male, n=none, r=rejected query)

## Main study

This section describes the three files containing the main study data. The formatting and contents of each file are described below.

**DocumentsMain.csv**

The file `DocumentsMain.csv` contains the documents used for the main study. The documents were taken from the `Grep-BiasIR dataset` (<https://github.com/KlaraKrieg/GrepBiasIR>). We used a set of eight documents originating from four domains. Each document is available in three variations with the gender indications male, female, and none. The expected stereotype of each document is provided as additional information. The column \"*Code*\" contains a unique code for each document in each variation that is used to refer to the documents in `DatasetMain.csv` as explained below.

**DatasetMain.csv**

The file `DatasetMain.csv` contains the results from the main study. The column names containing the *codes* referring to the documents (e.g. 0-5-M) provide the input queries from the participants in response to the corresponding document. The *codes* and the documents can be found in `DocumentsMain.csv`. The descriptions of the content of each column follows. Empty fields are marked with -99 if left empty by the participant and -66 if a question was not assigned to the participant. For the questions using the likert scale the encoding is: 1=Stronlgy disagree, 2=Disagree, 3=Neither agree nor disagree, 4=Agree, 5=Strongly agree.

* `ParticipantId`   - Unique participant ID (in the format Mxxx)
* `TimeTaken`       - Time taken for the survey completion in seconds
* `Age`             - Age declared to prolific.co
* `Sex`             - Sex declared to prolific.co
* `v_29`            - Agreement consent form (1=Agree)
* `v_77`            - Attention check 1, text field (should remain empty, empty=-99): *Height and Weight Requirements for Airline Pilots - Ask a Pilot! This is an attention check. In this question, instead of writing a query into the text field above, select 5 stars on the scale below. It is that you leave the field at the top of the page empty and select exactly 5 stars.*
* `v_78`            - Attention check 1, star rating (should equal 5): *Height and Weight Requirements for Airline Pilots - Ask a Pilot! This is an attention check. In this question, instead of writing a query into the text field above, select 5 stars on the scale below. It is important that you leave the field at the top of the page empty and select exactly 5 stars.*
* `v_80`            - Attention check 2 (should be 1): *I have never used the internet.* (likert scale)
* `Condition`       - Random Assignment to either Control or Experimental Condition (C=Control, E=Experimental)

Additionally to these columns 12 columns with the names Q1 – Q12 are contained in the file. which contain answers to the questions listed below. For each question the answer format is given in brackets. For the questions using the likert scale the encoding is: 1=Stronlgy disagree, 2=Disagree, 3=Neither agree nor disagree, 4=Agree, 5=Strongly agree.

* `Q1`            - What is your age? (Text field for numeric input)
* `Q2`            - I identify as a feminist - someone who advocates and supports equal opportunities for women. (Likert scale)
* `Q3`            - How would you describe your political view? (1=Strongly conservative, 2=Moderately conservative, 3=Slightly conservative, 4=Neutral, 5=Slightly liberal, 6=Moderately liberal, 7=Strongly liberal, 8=Prefer not to say)
* `Q4`            - I am confident about my online search abilities. (Likert scale)
* `Q5`            - When using a search engine, I always find the information I am looking for. (Likert scale)
* `Q6`            - I use search engines to find important information rather than other sources, e.g., books, newspapers. (Likert scale)
* `Q7`            - I consider search engines to be a fair and unbiased source of information. (Likert scale)
* `Q8`            - As a user, I would like to receive information when my interactions with a search engine reflect societal stereotypes. (Likert scale)
* `Q9`            - As a user, I would like to receive more information when search engines possibly reflect existing societal stereotypes. (Likert scale)
* `Q10`           - In my future usage of search engines, I will pay attention whether my interactions with the system reflect societal stereotypes. (Likert scale)
* `Q11`           - What gender do you identify with? (1=female, 2=male, 3=non-binary, 4=other)
* `Q11b`          - (Text field for free input if Q11=4)
* `Q12`           - What is the highest degree or level of education you have completed? (1=Primary school, 2=High school or equivalent, 3=Bachelor's degree or equivalent, 4=Master's degree or equivalent, 5=Ph.D. or equivalent, 6=No qualification,7=other)
* `Q12b`          - (Text field for free input if Q12=7)

**DatasetMainLabeled.csv**

`DatasetMainLabeled.csv` contains the labelled results from the main study.

* `ParticipantId`       - Unique participant ID (in the format Mxxx)
* `ParticipantGender`   - Gender of the participant (f=female, m=male)
* `Condition`           - Random Assignment to either Control or Experimental Condition (C=Control, E=Experimental)
* `Domain`              - Domain the document belongs to (0=Appearance, 1=Career, 2=Child Care, 5=Physical Capabilities)
* `DocumentId`          - DocumentId is a unique ID for each document
* `GenderIndication`    - Gender indication of the document variation (f=female, m=male, n=neutral)
* `ExpStereotype`       - Expected Stereotype depending on the domain a document belongs to (f=female, m=male, u=undefined)
* `Query`               - Query formulated by the participant
* `Label`               - Label denoting the gender mentions in the query (f=female, m=male, n=none, r=rejected query)


```
@inproceedings{krieg2022grep,
  title={Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users},
  author={Kopeinik, Simone and Mara, Martina and Ratz, Linda and Krieg, Klara and Schedl, Markus and Rekabsaz, Navid},
  booktitle={Proceeding of the ACM Conference on Human Factors in Computing Systems (CHI)},
  year={2023}
}
```
