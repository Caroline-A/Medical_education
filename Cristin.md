# Preliminary search in Cristin via Tableau DUCT

We ran a search in the national CRIS in Norway (current research information system; CRISTIN). This is a complete record of all Norwegian scientific publications from CRISTIN institutions since 2011, with "NVI subset" limiting the set to publications which are deemed "scientific" in the national system. The definition of "scientific" effectively covers the publication types interesting for our review; the criteria are that the work gives new insight, is presented in a form which makes the results verifiable or usable in new research, is presented in a language and have a distribution which makes it accessible for the majority of researchers interested in it, and is in a publication channel with routines for "peer review" (copied from CRISTIN [n.d.] Reporting instructions (NVI) . https://www.cristin.no/english/resources/reporting-instructions/ (retrieved 02.06.2022)). 

This datasource (FOR_data_sted_total) was accessed via a Tableau-based server available via login to Norwegian Cristin institutions (DUCT). The data is also available publicly via an API (https://www.cristin.no/tjenester/api/). Searches were run using Tableau, by creating an IF CONTAINS variable in the data.

# Journal search
We used 24 central journals in Medical Education, from  Maggio, LA, Ninkov, A, Frank, JR, Costello, JA, Artino, AR. Delineating the field of medical education: Bibliometric research approach(es). Med Educ. 2022; 56( 4): 387- 394. https://doi.org/10.1111/medu.14677 

An issue using journals is that not all medical education research is published in medical education journals - thus we do title/abstract searches too. 
See below comment from  Kyungjoon Lee, Julia S. Whelan, Nancy H. Tannery, Steven L. Kanter & Antoinette S. Peters (2013) 50 years of publication in the field of medical education, Medical Teacher, 35:7, 591-598, https://doi.org/10.3109/0142159X.2013.786168 
> "However, importantly, more than 80% of all ME articles were not published in ME journals. The 13 ME journals that existed, even briefly, during the 50 year period published only 18% of all ME articles (n = 14 753)".

#### Search
Note that this search will also find any journals containing "academic medicine", "medical education"

Searched for all publications in these journals within Cristin timeframe (2011-2020). Searched with filters:
* NVI subset

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

# Title search
Searched all publications within Cristin timeframe (2011-2020). Searched with filters:
* NVI subset

Terms in this search are automatically truncated both forwards and backwards, unless manually prevented by including a space before/after the term. 

In English, we have searched for terms in the title (either terms for trainee doctors, or generic terms for education AND doctors/medicine).
In Norwegian we have a slightly different approach. All education terms are linked to medical/doctor terms, OR to medical NPI subject fields (which limits the terms to their use in medical journals; https://npi.hkdir.no/fagfeltoversikt). This approach works much less well in English as terms such as "assessment" are so generic (e.g. there are lots of irrelevant results about medical assessments when searching for "assessment" in a oncology journal). 

### Title search, English

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

### Title search, Norwegian

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
```
