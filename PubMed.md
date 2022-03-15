# Preliminary searches in PubMed

# MeSH search

Ideas from https://sites.google.com/site/mededlit2/tidbits

Preliminary search 15.03.2022

#### 1 - Medical education groups - 51771 
```
"students, medical"[MeSH Terms] 
OR "students, premedical"[MeSH Terms]
OR "faculty, medical"[MeSH Terms] 
```

#### 2 - Terms for education - 883870
The education MeSH term includes assessment, simulation training, etc.
```
"Education"[MeSH Terms] 
OR "models, educational"[MeSH Terms] 
OR "Program Development"[MeSH Terms] 
```

#### 3 - 1 AND 2 - Combined medical educational groups AND terms for education - 38624
```
("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms])  
```

#### 4 - Medical education terms - 178219
```
"education, medical"[MeSH Terms] 
```

#### 5 - 4 OR 3 - Medical education terms OR the combined education + groups - 189924
```
"education, medical"[MeSH Terms] OR (("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms])) 
```

#### 6 - Norway - 140260
```
"Norway"[Affiliation] 
```

#### 7 - 6 AND 5 - 382
```
"Norway"[Affiliation] AND ("education, medical"[MeSH Terms] OR (("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms]))) 
```

# Free text search

## Option 1
Simple search for papers including terms indicating medical education, either through use of terms for medical education, medical school/qualifications or medical trainees.

Preliminary search 15.03.2022. When combined with the MeSH search above = 699 results (511 since 2011)

#### 1 - Medical education - 53577
```
"medical education"[Title/Abstract] 
```

#### 2 - Medical school / education, or people in training - 95376
Using `"resident*"[Title/Abstract]` alone is tricky due to surveys about residents of an area. 
Tested `"out-placement*"`, it did not find anything but noise. 
Used `medicine training` rather than `medical training` as the latter is more general.
```
"medical degree*"[Title/Abstract] OR "medicine degree*"[Title/Abstract] 
OR "medical diploma*"[Title/Abstract] OR "medicine training"[Title/Abstract] 
OR "medical school*"[Title/Abstract] 
OR "medical student*"[Title/Abstract] OR "medicine student*"[Title/Abstract]
OR "undergraduate medic*"[Title/Abstract] OR "postgraduate medic*"[Title/Abstract] 
OR "medical clerkship*"[Title/Abstract] OR "clinical clerkship*"[Title/Abstract]
OR "medical rotation*"[Title/Abstract] OR "clinical rotation*"[Title/Abstract]
OR "medical placement*"[Title/Abstract] OR "clinical placement*"[Title/Abstract]
OR "registrar*"[Title/Abstract] OR "medical intern*"[Title/Abstract] 
OR "resident physician*"[Title/Abstract] OR "medical residen*"[Title/Abstract] 
OR "junior doctor*"[Title/Abstract] OR "foundation doctor*"[Title/Abstract] OR "trainee doctor*"[Title/Abstract]  
```

#### 3 - 1 OR 2 and Norway - 480
```
("medical education"[Title/Abstract] OR ("medical degree*"[Title/Abstract] OR "medicine degree*"[Title/Abstract] OR "medical diploma*"[Title/Abstract] OR "medicine training"[Title/Abstract] OR "medical school*"[Title/Abstract] OR "medical student*"[Title/Abstract] OR "medicine student*"[Title/Abstract] OR "undergraduate medic*"[Title/Abstract] OR "postgraduate medic*"[Title/Abstract] OR "medical clerkship*"[Title/Abstract] OR "clinical clerkship*"[Title/Abstract] OR "medical rotation*"[Title/Abstract] OR "clinical rotation*"[Title/Abstract] OR "medical placement*"[Title/Abstract] OR "clinical placement*"[Title/Abstract] OR "registrar*"[Title/Abstract] OR "medical intern*"[Title/Abstract] OR "resident physician*"[Title/Abstract] OR "medical residen*"[Title/Abstract] OR "junior doctor*"[Title/Abstract] OR "foundation doctor*"[Title/Abstract] OR "trainee doctor*"[Title/Abstract])) AND "Norway"[Affiliation] 
```

## Option 2 - combine the people above with teaching terms
This option cuts around 100 from the results list. What are we losing here? 

However, when we combine with the MeSH terms, the results are not so different: 615 total results.

#### 4 - Teaching terms -1167095
```
"pedagog*"[Title/Abstract] OR "education*"[Title/Abstract] 
OR "medical educator*"[Title/Abstract]
OR "teaching"[Title/Abstract] 
OR "learning"[Title/Abstract] OR "learn"[Title/Abstract] 
OR "curricul*"[Title/Abstract] OR "programme design"[Title/Abstract] 
OR "classroom*"[Title/Abstract] OR "lectures"[Title/Abstract] OR "lecturing"[Title/Abstract] 
OR "medical train*"[Title/Abstract] OR "clinical train*"[Title/Abstract] OR "surgical train*"[Title/Abstract] OR "specialist train*"[Title/Abstract]
```

#### 5 - Instruction/evaluation terms - 2488537
```
"instruction*"[Title/Abstract] OR "assessment"[Title/Abstract] OR "evaluation"[Title/Abstract] OR "feedback"[Title/Abstract] 
```

#### 6 - Supervision terms - 52265
```
"supervision"[Title/Abstract] OR "mentoring"[Title/Abstract] OR "mentorship"[Title/Abstract] OR "coaching"[Title/Abstract] 
```

#### 7 - Simulation - 407028
```
"simulation*"[Title/Abstract] 
```

#### 8 - 3 AND (4 OR 5 OR 6 OR 7) - 373
```
("simulation*"[Title/Abstract] OR ("supervision"[Title/Abstract] OR "mentoring"[Title/Abstract] OR "mentorship"[Title/Abstract] OR "coaching"[Title/Abstract]) OR ("instruction*"[Title/Abstract] OR "assessment"[Title/Abstract] OR "evaluation"[Title/Abstract] OR "feedback"[Title/Abstract]) OR ("pedagog*"[Title/Abstract] OR "education*"[Title/Abstract] OR "medical educator*"[Title/Abstract] OR "teaching"[Title/Abstract] OR "learning"[Title/Abstract] OR "learn"[Title/Abstract] OR "curricul*"[Title/Abstract] OR "programme design"[Title/Abstract] OR "classroom*"[Title/Abstract] OR "lectures"[Title/Abstract] OR "lecturing"[Title/Abstract] OR "medical train*"[Title/Abstract] OR "clinical train*"[Title/Abstract] OR "surgical train*"[Title/Abstract] OR "specialist train*"[Title/Abstract])) AND (("medical education"[Title/Abstract] OR ("medical degree*"[Title/Abstract] OR "medicine degree*"[Title/Abstract] OR "medical diploma*"[Title/Abstract] OR "medicine training"[Title/Abstract] OR "medical school*"[Title/Abstract] OR "medical student*"[Title/Abstract] OR "medicine student*"[Title/Abstract] OR "undergraduate medic*"[Title/Abstract] OR "postgraduate medic*"[Title/Abstract] OR "medical clerkship*"[Title/Abstract] OR "clinical clerkship*"[Title/Abstract] OR "medical rotation*"[Title/Abstract] OR "clinical rotation*"[Title/Abstract] OR "medical placement*"[Title/Abstract] OR "clinical placement*"[Title/Abstract] OR "registrar*"[Title/Abstract] OR "medical intern*"[Title/Abstract] OR "resident physician*"[Title/Abstract] OR "medical residen*"[Title/Abstract] OR "junior doctor*"[Title/Abstract] OR "foundation doctor*"[Title/Abstract] OR "trainee doctor*"[Title/Abstract])) AND "Norway"[Affiliation]) 
```

## Old search

I first tried combining Search (1 AND (2 OR 3 OR 4)) AND (6 OR 7 OR 8 OR 9) - this lead to very much noise. Medical and education need to be more closely linked in phrases. See alternative above.

1 - Medicine/Doctor 
```
"medical"[Title/Abstract] OR "doctor*"[Title/Abstract] 
```

2 - Education and courses 
```
"education"[Title/Abstract] OR "training"[Title/Abstract] 
OR "course*"[Title/Abstract] OR "degree*"[Title/Abstract] OR "diploma*"[Title/Abstract] 
OR "medical school"[Title/Abstract] 
```

3 - People being educated
```
"student*"[Title/Abstract] OR "undergraduate*"[Title/Abstract] OR "postgraduate*"[Title/Abstract] 
OR "trainee*"[Title/Abstract] OR "learner*"[Title/Abstract] 
OR "resident*"[Title/Abstract] OR "registrar*"[Title/Abstract] OR "junior doctor*"[Title/Abstract] OR "foundation doctor*"[Title/Abstract] 
```

4 - People who educate
```
"educator*"[Title/Abstract] OR "teacher*"[Title/Abstract] 
OR "supervisor*"[Title/Abstract] OR "mentor*"[Title/Abstract] 
OR "lecturer*"[Title/Abstract] 
```

5 - Teaching terms 
```
"pedagog*"[Title/Abstract] OR "education*"[Title/Abstract] 
OR "medical educator*"[Title/Abstract]
OR "teaching"[Title/Abstract] 
OR "learning"[Title/Abstract] OR "learn"[Title/Abstract] 
OR "curricul*"[Title/Abstract] OR "programme design"[Title/Abstract] 
OR "classroom*"[Title/Abstract] OR "lectures"[Title/Abstract] OR "lecturing"[Title/Abstract] 
OR "medical train*"[Title/Abstract] OR "clinical train*"[Title/Abstract] OR "surgical train*"[Title/Abstract] OR "specialist train*"[Title/Abstract]
```

6 - Instruction/evaluation terms - not sure about these
```
"instruction*"[Title/Abstract] OR "assessment"[Title/Abstract] OR "evaluation"[Title/Abstract] OR "feedback"[Title/Abstract] 
```

7 - Supervision terms 
```
"supervision"[Title/Abstract] OR "mentoring"[Title/Abstract] OR "mentorship"[Title/Abstract] OR "coaching"[Title/Abstract] 
```

8 - Simulation - not sure 
```
"simulation*"[Title/Abstract] 
```

9 - Placement terms
Could also consider `practice OR praxis` here but these are very general
```
"clinical placement*"[Title/Abstract] OR "out-placement*"[Title/Abstract] 
OR "clerkship*"[Title/Abstract] OR "rotation*"[Title/Abstract] OR "residency"[Title/Abstract] 
OR "internship*"[Title/Abstract] 
```
