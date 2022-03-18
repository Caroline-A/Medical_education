# Preliminary searches in Web of Science

Preliminary test searches, done 15.03.2022. Web of Science Core Collection (SCIE 1945-present, SSCI 1956-present, AHCI 1975-present, ESCI 2017-present).

#### 1 - Medical education and medical groups in training - 135163
Here I am testing with phrases used in PubMed, but could also consider using a proximity search here to help with variations in terminology. 
The downside with this strategy is that you get results about e.g. stress levels in medical students.

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
A number of `clinical` and generic education terms are combined with *medical/doctor* terms to avoid many results from nursing/dentistry.
```
TS= 
(
   ("clinical educat*" OR "clinical teach*"
   OR "clinical rotation*" OR "clinical placement*"
   OR "simulation training" OR "teaching simulation$"
   OR "teaching practic*" OR "teaching method*" OR "teaching and learning"
   OR "curricul*"
   OR "educational supervis*" 
   OR "undergraduate student$" OR "undergraduate training" 
   OR "postgraduate student$" OR "postgraduate training" OR "postgraduate speciali*"
   OR "continuing education"
   ) 
   AND ("medicine" OR "medical" OR "medic$" OR "doctor$" OR "physician$" OR "surgeon$" OR "surgery")
 )
```

#### 3 - 1 OR 2 AND limit to Norway = 750
See the results here: https://www.webofscience.com/wos/woscc/summary/2e2114c5-a001-4956-b235-4210ccdfc2b8-2ad8b5fd/relevance/1
```
(#1 OR #2) AND CU="Norway"
```
