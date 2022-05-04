# Search history

Contents
* Searches in Web of Science
* Searches in PubMed
* Searches in CRISTIN - the national CRIS (current research information system) in Norway. This data source has almost complete coverage of scientific publications from all member institutions 2011-2021, regardless of language or format. All major higher education institutions as well as many research institutes and public health regions are members. 

## Searches in Web of Science

Preliminary test searches done March 2022. Final searches done 04.05.2022. 
* Platform: Web of Science
* Databases: Web of Science Core Collection (SCIE 1945-present, SSCI 1956-present, AHCI 1975-present, ESCI 2017-present).
* Filters for the final results:
    * Document type: Articles, Review Articles, Book chapters. Books would have been included if there were any found. 

The strategy consists of two parts: One part is a search for terms specific to medical education and medical groups in training; a second part combines more generic terms for education and training with terms for medicine, doctors and specialities. The same general approach is used in PubMed, with adjustments for use of MeSH terms. 

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


## Searches in PubMed

Preliminary test searches done March 2022. Final searches done 04.05.2022. 
* Platform: PubMed advanced search interface (https://pubmed.ncbi.nlm.nih.gov/advanced/). Combinations of different search lines were done using the "Actions" function. 
* Databases: PubMed
* Filters for the final results:
    * Document type:  

The strategy consists of two parts: One part is a search for terms specific to medical education and medical groups in training; a second part combines more generic terms for education and training with terms for medicine, doctors and specialities. The same general approach is used in Web of Science (with adjustments for the lack of subject headings).  

Final PubMed search, combination of MeSH and free text, is shown below (04.05.22) = xxx results. See below for explanation line for line.

```

```

### MeSH search

Ideas for suitable MeSH terms were from own exploration, and an online resource ("Useful MeSH terms for medical education research" (2009) University of California San Francisco. https://sites.google.com/site/mededlit2/tidbits). 

#### 1 - Medical education groups - 52392 
```
"students, medical"[MeSH Terms] 
OR "students, premedical"[MeSH Terms]
OR "faculty, medical"[MeSH Terms] 
```

#### 2 - Terms for education - 888706
The education MeSH term includes assessment, simulation training, etc.
```
"Education"[MeSH Terms] 
OR "models, educational"[MeSH Terms] 
OR "Program Development"[MeSH Terms] 
```

#### 3 - 1 AND 2 - Combined medical educational groups AND terms for education - 39026
```
("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) 
AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms])  
```

#### 4 - Medical education terms - 179174
```
"education, medical"[MeSH Terms] 
```

#### 5 - 4 OR 3 - Medical education terms OR the combined education + groups - 191064
```
"education, medical"[MeSH Terms] 
OR  (("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) 
    AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms])) 
```

#### 6 - Norway - 141968
```
"Norway"[Affiliation] 
```

#### 7 - 6 AND 5 - 385
```
"Norway"[Affiliation] 
AND   ("education, medical"[MeSH Terms] 
      OR (("students, medical"[MeSH Terms] OR "students, premedical"[MeSH Terms] OR "faculty, medical"[MeSH Terms]) 
      AND ("Education"[MeSH Terms] OR "models, educational"[MeSH Terms] OR "Program Development"[MeSH Terms]))) 
```

### Free text search

#### 8 - Medical school / education, or people in training - 141569 
* Using `"resident*"[Title/Abstract]` alone is tricky due to surveys about residents of an area. 
* Tested `"out-placement*"`, it did not find anything but noise. 
* Used `medicine training` rather than `medical training` as the latter is more general (e.g. medical training of the general public).
```
"medical educat*"[Title/Abstract] OR "medical teach*"[Title/Abstract] OR "medicine training"[Title/Abstract]
OR "surgical educat*"[Title/Abstract] OR "surgery educat*"[Title/Abstract] OR "surgical train*"[Title/Abstract] OR "surgery train*"[Title/Abstract] 
OR "medical degree*"[Title/Abstract] OR "medicine degree*"[Title/Abstract] OR "medical diploma*"[Title/Abstract] OR "medical school*"[Title/Abstract] 
OR "medical student*"[Title/Abstract] OR "medicine student*"[Title/Abstract]
OR "undergraduate medic*"[Title/Abstract] OR "postgraduate medic*"[Title/Abstract] 
OR "medical clerkship*"[Title/Abstract] OR "clinical clerkship*"[Title/Abstract]
OR "medical rotation*"[Title/Abstract] 
OR "medical placement*"[Title/Abstract] 
OR "registrar*"[Title/Abstract] OR "medical intern*"[Title/Abstract] 
OR "resident physician*"[Title/Abstract] OR "medical residen*"[Title/Abstract] 
OR "junior doctor*"[Title/Abstract] OR "foundation doctor*"[Title/Abstract] OR "trainee doctor*"[Title/Abstract]  
```

#### 9 - General/clinical training and education terms - 
Note, no hyphens are used. PubMed will find the same results whether you use "post-graduate" or "post graduate".

```
"clinical educat*"[Title/Abstract] OR "clinical teach*"[Title/Abstract] 
OR "clinical rotation*"[Title/Abstract] OR "clinical placement*"[Title/Abstract]
OR "teaching simulation*"[Title/Abstract] OR "simulation training"[Title/Abstract] 
OR "teaching practic*"[Title/Abstract] OR "teaching method*"[Title/Abstract] OR "teaching and learning"[Title/Abstract]
OR "problem based learning"[Title/Abstract] OR "work based learning"[Title/Abstract] 
OR "curricul*"[Title/Abstract]
OR "educational supervis*"[Title/Abstract] OR "postgraduate supervis*"[Title/Abstract] OR "post graduate supervis*"[Title/Abstract] OR "clinical supervis*"[Title/Abstract] 
OR "undergraduate student*"[Title/Abstract] OR "undergraduate train*"[Title/Abstract] 
OR "postgraduate student*"[Title/Abstract] OR "postgraduate train*"[Title/Abstract] OR "postgraduate speciali*"[Title/Abstract] OR "post graduate student*"[Title/Abstract] OR "post graduate train*"[Title/Abstract] OR "post graduate speciali*"[Title/Abstract]
OR "continuing education"[Title/Abstract] OR "on the job training"[Title/Abstract] 
```

#### 10 - Medical/doctor terms - 3,457,005 	
```
"medicine"[Title/Abstract] OR "medical"[Title/Abstract] OR "medic"[Title/Abstract] OR "medics"[Title/Abstract] 
OR "doctor"[Title/Abstract] OR "doctors"[Title/Abstract] OR "physician*"[Title/Abstract] 
OR "surgeon*"[Title/Abstract] OR "surgery"[Title/Abstract] OR "psychiatry"[Title/Abstract] OR "psychiatrist*"[Title/Abstract] 
```

#### 11 - 9 AND 10 - 50175
Clinical and generic education terms are combined with medical/doctor terms to avoid results from nursing/dentistry/non-medical fields.
```

```

#### 12 - (1 OR 2 OR 5) - 161987
```

```

#### 13 - Norway
```
"Norway"[Affiliation]  
```

#### 14 - 7 AND 6 = 555
```

```


## Search in CRISTIN via Tableau DUCT

* Platform/tool: The datasource was accessed via a Tableau-based server available via login to Norwegian Cristin institutions ("DUCT"). The data is also available publicly via an API (https://www.cristin.no/tjenester/api/). Searches were run using Tableau (v. 2021.4), by creating an IF CONTAINS variable in the data. NOTE: Phrases/words are automatically truncated both forwards and backwards from the start/end of the phrase, unless manually prevented by including a space before/after.
* Database: We used a file on the server which contains all outputs in CRISTIN, FOR_data_sted_total. This file thus contains a almost complete record of all Norwegian scientific publications from CRISTIN institutions from 2011 up to and including 2021. All major higher education institutions as well as many research institutes and public health regions are members. 
* Filters: Searched for all publications within Cristin timeframe (2011-2020) within a filter called "NVI subset". "NVI subset" limits the set to publications which are deemed "scientific" in the national system. The definition of "scientific" effectively covers the publication types interesting for our review; the criteria are that the work gives new insight, is presented in a form which makes the results verifiable or usable in new research, is in a language and has a distribution which makes it accessible for the majority of researchers interested in it, and is in a publication channel with peer review routines (CRISTIN [n.d.] Reporting instructions (NVI) . https://www.cristin.no/english/resources/reporting-instructions/ (retrieved 02.06.2022)). 

The strategy in CRISTIN takes the same basic form as the Web of Science and PubMed strategies, but was adapted to the fields available in this data source. CRISTIN does not contain abstracts, so free text searches can only be run on publication titles. Therefore, in addition to the title search, two other elements were included: a journal search, and combining education terms with medical journals in the title search. 

### Journal search
We searched for 24 central journals in Medical Education, taken from  Maggio, LA, Ninkov, A, Frank, JR, Costello, JA, Artino, AR. Delineating the field of medical education: Bibliometric research approach(es). Med Educ. 2022; 56( 4): 387- 394. https://doi.org/10.1111/medu.14677. Note that this search will also find any journals containing "academic medicine" or "medical education" in their names due to the automatic truncation.

An issue using journals is that most medical education research is not published in medical education journals (Kyungjoon Lee, Julia S. Whelan, Nancy H. Tannery, Steven L. Kanter & Antoinette S. Peters (2013) 50 years of publication in the field of medical education, Medical Teacher, 35:7, 591-598, https://doi.org/10.3109/0142159X.2013.786168). Thus we do not rely only on this approach. 

```
IF CONTAINS(LOWER([journal]),	"academic medicine"	)
OR CONTAINS(LOWER([journal]),	"advances in health sciences education"	)
OR CONTAINS(LOWER([journal]),	"advances in medical education and practice"	)
OR CONTAINS(LOWER([journal]),	"african journal of health professions education"	)
OR CONTAINS(LOWER([journal]),	"anatomical sciences education"	)
OR CONTAINS(LOWER([journal]),	"bmc medical education"	)
OR CONTAINS(LOWER([journal]),	"bmj simulation & technology enhanced learning"	)
OR CONTAINS(LOWER([journal]),	"canadian medical education journal"	)
OR CONTAINS(LOWER([journal]),	"clinical teacher"	)
OR CONTAINS(LOWER([journal]),	"education for health"	)
OR CONTAINS(LOWER([journal]),	"focus on health professional education"	)
OR CONTAINS(LOWER([journal]),	"gms journal for medical education"	)
OR CONTAINS(LOWER([journal]),	"international journal of medical education"	)
OR CONTAINS(LOWER([journal]),	"journal of continuing education in the health professions"	)
OR CONTAINS(LOWER([journal]),	"journal of educational evaluation for health professions"	)
OR CONTAINS(LOWER([journal]),	"journal of graduate medical education"	)
OR CONTAINS(LOWER([journal]),	"journal of medical education and curricular development"	)
OR CONTAINS(LOWER([journal]),	"journal of surgical education"	)
OR CONTAINS(LOWER([journal]),	"medical education"	)
OR CONTAINS(LOWER([journal]),	"medical education online"	)
OR CONTAINS(LOWER([journal]),	"medical teacher"	)
OR CONTAINS(LOWER([journal]),	"perspectives on medical education"	)
OR CONTAINS(LOWER([journal]),	"simulation in healthcare-journal of the society for simulation in healthcare"	)
OR CONTAINS(LOWER([journal]),	"teaching and learning in medicine"	)
THEN "MedEd"
ELSE "non"
END
```

### Title search
In English, we have searched for terms in the title using the same two part approach as Web of Science and PubMed.

In Norwegian we can take a slighty broader approach as there is less research. We take the same two part approach as before, but also include generic education terms in titles in publications in journals classified as in the medical field by the Norwegian Publishing Indicator (NPI subject fields https://npi.hkdir.no/fagfeltoversikt). This approach is not used in English as it is too broad - terms such as "assessment" are so generic (e.g. there are lots of irrelevant results about medical assessments when searching for "assessment" in a oncology journal). 

#### Title search, English

```
IF (
CONTAINS(LOWER([result_title]),	"clerkship"	)
OR CONTAINS(LOWER([result_title]),	"registrar"	)
OR CONTAINS(LOWER([result_title]),	"junior doctor"	)
OR CONTAINS(LOWER([result_title]),	"foundation doctor"	)
)
THEN "MedEd"

ELSEIF ((
CONTAINS(LOWER([result_title]),	"educat"	)
OR CONTAINS(LOWER([result_title]),	"teach"	)
OR CONTAINS(LOWER([result_title]),	"degree"	)
OR CONTAINS(LOWER([result_title]),	"diploma"	)
OR CONTAINS(LOWER([result_title]),	"train"	)
OR CONTAINS(LOWER([result_title]),	"school"	)
OR CONTAINS(LOWER([result_title]),	"student"	)
OR CONTAINS(LOWER([result_title]),	"graduate"	)
OR CONTAINS(LOWER([result_title]),	"clerkship"	)
OR CONTAINS(LOWER([result_title]),	"rotation"	)
OR CONTAINS(LOWER([result_title]),	"intern"	)
OR CONTAINS(LOWER([result_title]),	"resident"	)

OR CONTAINS(LOWER([result_title]),	"pedagog"	) 
OR CONTAINS(LOWER([result_title]),	"learn"	)
OR CONTAINS(LOWER([result_title]),	"curricul"	) 
OR CONTAINS(LOWER([result_title]),	"programme design"	) 
OR CONTAINS(LOWER([result_title]),	"classroom"	) 
OR CONTAINS(LOWER([result_title]),	"lectur"	) 
OR CONTAINS(LOWER([result_title]),	"assessment"	) 
OR CONTAINS(LOWER([result_title]),	"feedback"	) 
OR CONTAINS(LOWER([result_title]),	"supervis"	)
OR CONTAINS(LOWER([result_title]),	"mentor"	) 
)
AND (		
CONTAINS(LOWER([result_title]),	"medic"	)
OR (CONTAINS(LOWER([result_title]),"doctor") AND NOT CONTAINS(LOWER([result_title]),"doctoral"))	
OR CONTAINS(LOWER([result_title]),	"physician"	)
))

THEN "MedEd"
ELSE "non"
END
```

#### Title search, Norwegian

``` 
IF ((
CONTAINS(LOWER([result_title]),	"utdann"	)
OR CONTAINS(LOWER([result_title]),	"pedagog"	)
OR CONTAINS(LOWER([result_title]),	"undervis"	)
OR CONTAINS(LOWER([result_title]),	"læring"	)
OR CONTAINS(LOWER([result_title]),	"studieplan"	)
OR CONTAINS(LOWER([result_title]),	"studieprogr"	)
OR CONTAINS(LOWER([result_title]),	"student"	)
OR CONTAINS(LOWER([result_title]),	"foreles"	)
OR CONTAINS(LOWER([result_title]),	"klasserom"	)
OR CONTAINS(LOWER([result_title]),	" vurdering"	)
OR CONTAINS(LOWER([result_title]),	"evaluering"	)
OR CONTAINS(LOWER([result_title]),	"veiled"	)
OR CONTAINS(LOWER([result_title]),	"supervis"	) 
OR CONTAINS(LOWER([result_title]),	"ferdighet"	) 
OR CONTAINS(LOWER([result_title]),	"simulering"	)
OR CONTAINS(LOWER([result_title]),	"praksis"	) 
OR CONTAINS(LOWER([result_title]),	"turnus"	) 
OR CONTAINS(LOWER([result_title]),	"utplassering"	) 
)
AND (		
CONTAINS(LOWER([result_title]),	"medisin"	)
OR CONTAINS(LOWER([result_title]),	" lege "	)
OR CONTAINS(LOWER([result_title]),	" leger"	)
OR CONTAINS(LOWER([result_title]),	"fastlege"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "anestesi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "dermatologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "endokrinologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "gastroenter"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "generell medisin"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "geriatri"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "gynekologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "hematologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "hjerte"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "infeksjon"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "kirurgiske"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "nefrologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "nevrologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "onkologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "pediatri"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "radiologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "revmatologi"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "øre-nese"	)
OR CONTAINS(LOWER([scientific_field_npi]),	 "øyesykdommer"	)
))
THEN "MedEd"
ELSE "non"
END
```

