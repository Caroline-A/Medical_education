# Searches in Web of Science

Preliminary test searches, done 15.03.2022. Final searches done 04.05.2022. 
* Platform: Web of Science
* Databases: Web of Science Core Collection (SCIE 1945-present, SSCI 1956-present, AHCI 1975-present, ESCI 2017-present).
* Filters for the final results:
    * Document type: Articles, Review Articles, Book chapters. Books would have been included if there were any. 

#### 1 - Medical education and medical groups in training - 136776 (all documents)

```
TS=
(
"medical educat*" OR "medical teach*" OR "medicine training" 
OR "surgical educat*" OR "surgery educat*" OR "surgical train*" OR "surgery train*" 
OR "medical school*" OR "medical degree*" OR "medicine degree*" OR "medical diploma*" 
OR "medical student*" OR "medicine student*"
OR "undergraduate medic*" OR "postgraduate medic*" 
OR "medical clerkship*" OR "clinical clerkship*"
OR "medical rotation*" OR "medical placement*" 
OR "registrar*" OR "medical intern*"
OR "resident physician*" OR "medical residen*" 
OR "junior doctor*" OR "foundation doctor*" OR "trainee doctor*" OR "trainee surgeon*"
)
```

#### 2 - Education and medical - 50634 (all documents)

`clinical` and generic education terms are combined with *medical/doctor* terms to avoid results from nursing/dentistry.

```
TS= 
(
   ("clinical educat*" OR "clinical teach*"
   OR "clinical rotation*" OR "clinical placement*"
   OR "simulation training" OR "teaching simulation$"
   OR "teaching practic*" OR "teaching method*" 
   OR "teaching and learning" OR "problem based learning" OR "work based learning" 
   OR "curricul*"
   OR "educational supervis*" OR "undergraduate supervis*" OR "postgraduate supervis*" OR "clinical supervis*"
   OR "undergraduate student$" OR "undergraduate training" 
   OR "postgraduate student$" OR "postgraduate training" OR "postgraduate speciali*"
   OR "continuing education" OR "on the job training" OR "in work training"
   ) 
   AND ("medicine" OR "medical" OR "medic$" OR "doctor$" OR "physician$" OR "surgeon$" OR "surgery" OR "psychiatry" OR "psychiatrist$")
 )
```

#### 3 - 1 OR 2 AND limit to Norway = 772, 708 after limiting by document type

Search URL: https://www.webofscience.com/wos/woscc/summary/492a401c-9c5c-4613-bd78-9bd940eb7d85-357e0e8e/relevance/1

```
(#1 OR #2) AND CU="Norway"
```
