# Preliminary search in Cristin via Tableau DUCT

# Journal search
Used 24 central journals in Medical Education from  Maggio, LA, Ninkov, A, Frank, JR, Costello, JA, Artino, AR. Delineating the field of medical education: Bibliometric research approach(es). Med Educ. 2022; 56( 4): 387- 394. https://doi.org/10.1111/medu.14677 

Searched for all publications in these journals within Cristin timeframe (2011-2020). Searched with filters:
* NVI subset

Note coverage comment from Maggio, L.A., Costello, J.A., Norton, C. et al. Knowledge syntheses in medical education: A bibliometric analysis. Perspect Med Educ 10, 79–87 (2021). https://doi.org/10.1007/s40037-020-00626-9
> While all of these journals are indexed in PubMed, seven of them are not included in their entirety, namely: Advances in Health Sciences Education, Canadian Medical Education Journal, Clinical Teacher, Medical Education Online, Medical Teacher, Teaching and Learning in Medicine, and The Journal of Continuing Education in the Health Professions. For example, Clinical Teacher first appeared in PubMed in 2010, but the journal started publishing articles in 2003. Therefore, for these seven journals we identified citations from these periods by hand searching the journal’s website or Web of Science (WoS).

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
