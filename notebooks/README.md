# Dissecting PubMed: which content is covered by the Library? and Open Access?

## Jupyter Notebooks

This folder contains the jupyter notebooks used in this research. Others academic libraries are invited to use their own data and reproduce all the calculations in order to improve the methodology and compare the results with the cover of PubMed references we found for the Geneva University library.

### 1. PubMed dissection

 - pubmed_xml2csv.ipynb

This notebook details the process of extracting data in csv format from XML PubMed data. Parsing of the XML files is not done with a Jupyter Notebook because of memory limits. Instead, the useful data is extracted via a Cygwin shell script using the XMLstarlet toolkit (https://en.wikipedia.org/wiki/XMLStarlet). The CSV files extracted are then used into the other notebooks to analyse the data.

### 2. Hunting for DOIs

 - pubmed_merge_crossref.ipynb
 - pubmed_merge_crossref_results.ipynb

Match between PubMed metadata and CrossRef metadata (downloaded via API) using our APD strategy: * First **a**uthor + first **p**age + publication **d**ate. We use the EuropePMC match as gold standard to evaluate our method. Finally we add the article title and similarity comparison criteria to improve our APD method and use both DOIs sources to enrich the PubMed DOIs 

### 3. PubMed content covered by library collection

 - pubmed_merge_library_coverage.ipynb
 - pubmed_merge_library_coverage_results.ipynb
 
PubMed and print journals / ejournals matched by journal ISSN-L and boundary years of subscriptions --> standardising / normalizing print holdings coded in free text and ejournals as activtated in SFX. Then enriching this data with ISSN-L before matching it against PubMed using journal ISSN-L and boundary years of subscriptions

### 4. Which PubMed content is OA ?

To get the Gold and Green OA figures, we matched PubMed metadata with OA datasets publicly available using 3 strategies :

#### unpaywall: merged by DOI after we enriched the PubMed metadata with new DOIs provided by EuropePMC and those found using our APD strategy used above

 - pubmed_merge_unpaywall.ipynb
 - pubmed_merge_unpaywall_results.ipynb
 
#### DOAJ: merged by ISSN-L and publication year

 - pubmed_merge_doaj.ipynb

#### PMC: merged by PMID

 - pubmed_merge_pmc.ipynb
 - pubmed_merge_pmc_doaj_results.ipynb

#### Swiss National Licences: merged by ISSN-L and publication year. It is not OA for all, but free access for any citizen living in Switerland

 - pubmed_merge_national_licences_ch.ipynb
 - pubmed_merge_national_licences_ch_results.ipynb
 
 

