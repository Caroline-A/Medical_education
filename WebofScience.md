# Preliminary searches in Web of Science

#### 1 - Terms to limit to medical education - 145 950

Tested out with `nurse$`, this seemed to bring in results about continuing education of nurses, hence the inclusion of `student nurse$`. 
I also originally tried with `health` in this phrase, but heath + education brought in a lot of irrelavent results from health education e.g. of the public. 
```
TS=
(
  (
    ("medical" OR "healthcare" OR "nursing" OR "dentistry" OR "pharmacy") 
    NEAR/3 
        ("education" OR "student$" OR "undergraduate$" OR "course$" OR "degree$" OR "diploma$")
  ) 
OR "student nurse$"
) 
```

#### 2 - Terms to limit to teaching and learning - 3 246 536

`educational`should cover e.g. educational activities. `assessment$` is a little tricky as it is used outside education, but seems to work fairly ok.
``` 
TS=(  "pedagog*" OR "teaching" OR "learning" OR "learn" 
      OR "educational" 
      OR "curricul*" OR "programme design" 
      OR "classroom*" OR "lecture*" OR "assessment$"
   )
```

#### 3 - Limit to Norway - 690
```
(#1 AND #2) AND CU="Norway"
```
