# Preliminary searches in Web of Science

Preliminary test searches, done 15.03.2022. Web of Science Core Collection (SCIE 1945-present, SSCI 1956-present, AHCI 1975-present, ESCI 2017-present).

#### 1 - Medical education and medical groups in training - 135163

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

#### 2 - Education and medical - 48104
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

#### 3 - 1 OR 2 AND limit to Norway = 772
See the results here: https://www.webofscience.com/wos/woscc/summary/2083ea21-13e1-4d82-b7fd-432d2b441ddd-357dd10e/relevance/1
```
(#1 OR #2) AND CU="Norway"
```
