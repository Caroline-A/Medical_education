# Preliminary searches in Web of Science

Preliminary test searches, done 15.03.2022. Web of Science Core Collection (SCIE 1945-present, SSCI 1956-present, AHCI 1975-present, ESCI 2017-present).

#### 1 - Terms to limit to medical education - 129234
Here I am testing with phrases used in PubMed, but could also consider using a proximity search here to help with variations in terminology.
`clinical` is combined with `medic* OR doctor$` to avoid many results from nursing/dentistry.

The downside with this strategy is that you get results about e.g. stress levels in medical students.

```
TS=
(
"medical educat*" OR "medical teach*"
OR "medical degree*" OR "medicine degree*"
OR "medical diploma*" OR "medicine training"
OR "medical school*"
OR "medical student*" OR "medicine student*"
OR "undergraduate medic*" OR "postgraduate medic*" 
OR "medical clerkship*" OR "clinical clerkship*"
OR "medical rotation*" OR "clinical rotation*"
OR "medical placement*" OR "clinical placement*"
OR "registrar*" OR "medical intern*"
OR "resident physician*" OR "medical residen*" 
OR "junior doctor*" OR "foundation doctor*" OR "trainee doctor*" 
OR (
      ("clinical education" OR "clinical teach*" OR "simulation training" OR "teaching simulation$") 
      AND ("medic*" OR "doctor$")
   )
)
```

#### 2 - Limit to Norway - 668
See the results here: https://www.webofscience.com/wos/woscc/summary/aad76c84-d5d9-4f3f-8dd2-10229b6ce511-2ac4a343/relevance/1
```
#1 AND CU="Norway"
```

## Old search

Terms to limit to teaching and learning - 3 246 536

`educational`should cover e.g. educational activities. `assessment$` is a little tricky as it is used outside education, but seems to work fairly ok.
``` 
TS=(  "pedagog*" OR "teaching" OR "learning" OR "learn" 
      OR "educational" 
      OR "curricul*" OR "programme design" 
      OR "classroom*" OR "lecture*" OR "assessment$"
   )
```
