# Notes

## Deduplication process

Step 1: The CRISTIN results cannot be imported into EndNote. Therefore I did a deduplication in Tableau before any other work. I took the Web of Science results and joined this data to the CRISTIN data, by exact matching on the doi. This detected 161 duplicates between the CRISTIN and WoS sets, that were removed. I then did the same with PubMed, where there were 134 duplicates. Once both were removed, there remained 304 results from the CRISTIN set (of 488 originally). These were then exported to Excel, and added to Zotero using the doi-lookup function (for those with doi). The remaining references were added manually. 297 were added (7 were removed for being obvious conference proceedings) - these were then exported from Zotero, and added to EndNote along with the exports from PubMed, WoS and ProQuest.

Step 2: After all was in EndNote, I followed first steps of the procedure in Bramer, W. M., Giustini, D., de Jonge, G. B., Holland, L., & Bekhuis, T. (2016). De-duplication of database search results for systematic reviews in EndNote. Journal of the Medical Library Association : JMLA, 104(3), 240–243. https://doi.org/10.3163/1536-5050.104.3.014. Then used doi (together with manual checking). Due to the order of import, the order of preference for retention was WoS > PubMed > ProQuest > CRISTIN. 

I then ran "Find reference updates" on the final set, to find PubMed IDs for any records that did not have a WOS ID or PubMed ID in the Accession Number field. Other data was added for empty fields (e.g. Keywords) or overwritten in the case of ProQuest records (to reformat the DOI to a standard format, and get the PubMed accession number instead of ProQuest for later analysis). 

## Import/Export to Rayyan
We can retain the WOSID/PMID throughout the screening process by 
1. Importing to EndNote - PMID and WOSID both end up correctly in the Accession number field. In Zotero they end up in different fields. Therefore I used EndNote.
2. Deduplicating
3. Copying Accession number field contents over to the URL field, and the doi, separated by a ";". Do this by 1) Copy accession number field to the URL field (replace what is there), 2) Use "change fields" to add a semicolon after the text in the URL field, 3) Copy the doi to the URL field (after existing text)
4. Import into Rayyan via RefMan (Export, txt, Refman output style)
5. Export from Rayyan (csv/EndNote). DOI is lost in some formats, but the URL field is retained. Thus by copying accession number and doi into the URL field, after export from Rayyan we can take and split this field in Excel, and used the accession numbers to find the publications again in databases (and then re-download for analysis with full metadata). 

## Example articles to test search against
Should be found
* Kristin Wigen, Are Holen & Øyvind Ellingsen (2003) Predicting academic success by group behaviour in PBL, Medical Teacher, 25:1, 32-37, DOI: 10.1080/0142159021000061396
* Gude, T., Hjortdahl, P., Anvik, T., Bærheim, A., Fasmer, O. B., Grimstad, H., ... & Vaglum, P. (2005). Does change from a traditional to a new medical curriculum reduce negative attitudes among students? A quasi-experimental study. Medical teacher, 27(8), 737-739.
* Smeby, S. S., Espeland, T., Berg, E. A. R., Samstad, E., Lillebo, B., & Slørdahl, T. S. (2021). Examining the educational impact of the mini-CEX: a randomised controlled study. BMC.

## Limitations

### Affiliations

PubMed is not the best source for matching publications to country of the authors because they only indexed the first-author affiliation between 1988-2013, and from 2014 began to index the affiliation for all authors (https://www.nlm.nih.gov/bsd/mms/medlineelements.html#ad). At this point, they also stopped quality-control of the affiliation data, and affiliation data is dependent on what the publisher submits. This is difficult to do anything with as we cannot hand search all relevant works for Norwegian affiliations; but some are covered in Web of Science, and the data there is assumed to be of better quality there. The main limitation is therefore that we may miss publications not indexed in Web of Science or CRISTIN published pre-2014 which had Norwegian-affiliated authors in a non-first-author position. 
See https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4816483/ and https://dl.acm.org/doi/abs/10.1007/s11192-018-2714-x

There is however a significant affiliation problem for the relevant journal *Tidsskrift for den Norske Legeforening* (TNLF). This journal seems to be indexed with **incomplete affiliation data** in PubMed. The vast majority of works lack country in the affiliation, and a good number lack all affiliation data. ca. 34000 works from this journal are found in PubMed, but just over 1100 are found when the journal is combined with `"Norway"[Affiliation]`. This journal is poorly covered in Web of Science: only 4756 works from the journal are covered as of today (09/11/22), with 3145 being found when also limiting by `CU="Norway"`. It is mostly not covered until 2017, and thus Web of Science can't be used as an alternative data source. When doing our search in PubMed:
* With affiliation = Norway, 32 works are found by the MedEd search in TNLF.
* Without affiliation = Norway, 882 works are found by the MedEd search in TNLF.

### Indexing of central Medical Education journals
The coverage comment below is from Maggio, L.A., Costello, J.A., Norton, C. et al. Knowledge syntheses in medical education: A bibliometric analysis. Perspect Med Educ 10, 79–87 (2021). https://doi.org/10.1007/s40037-020-00626-9
> "While all of these journals are indexed in PubMed, seven of them are not included in their entirety, namely: 
> Advances in Health Sciences Education, Canadian Medical Education Journal, Clinical Teacher, Medical Education Online, Medical Teacher, Teaching and Learning in Medicine, and The Journal of Continuing Education in the Health Professions. For example, Clinical Teacher first appeared in PubMed in 2010, but the journal started publishing articles in 2003.".

From below, I can see that 12 of them have the same start/index date. 9 have gaps (2 x 2 years, 3 x 6-7 years, 4 x 11+ years), 3 are not indexed. We will find any missing publications from 2011 and onwards in the Cristin search. Other publications before this may be missing.

#### Data I have checked from PubMed, start date and indexed from date:
* academic medicine, 1989, 1989
* advances in medical education and practice, 2010, 2010
* anatomical sciences education, 2007, 2008
* bmc medical education, 2001, 2001
* gms journal for medical education, 2016, 2016
* international journal of medical education, 2010, 2010
* journal of educational evaluation for health professions, 2006, 2006
* journal of graduate medical education, 2009, 2009
* journal of surgical education, 2007, 2007
* medical education, 1976, 1976
* perspectives on medical education, 2012, 2012
* simulation in healthcare-journal of the society for simulation in healthcare, 2006, 2006

--

* journal of medical education and curricular development, 2014, 2016 (not in MEDLINE)
* canadian medical education journal, 2010, 2012 (not in MEDLINE)
* advances in health sciences education, 1996, 2001
* clinical teacher, 2004, 2010
* education for health, 1996, 2003
* teaching and learning in medicine, 1989, 2000
* journal of continuing education in the health professions, 1988, 2000
* medical education online, 1996, 2008
* medical teacher, 1979, 2002

--

* african journal of health professions education, 2009, not indexed in MEDLINE, only selected citations from PMC
* bmj simulation & technology enhanced learning, 2015, not indexed in MEDLINE, only selected citations in PubMed
* focus on health professional education, 1999, not indexed
