# Dissecting PubMed: which content is covered by the Library? and Open Access?

## Jupyter Notebooks

This folder contains the jupyter notebooks used in this research. Others academic libraries are invited to use their own data and reproduce all the calculations in order to improve the mothodology and compare the results with the cover of PubMed references we found for the Geneva University library.

### 1. PubMed dissection

 - pubmed_xml2csv.ipynb

This notebook details the process of extracting data in csv format from XML PubMed data. Parsing of the XML files is not done with a Jupyter Notebook because of memory limits. Instead, the useful data is extracted via a Cygwin shell script using the XMLstarlet toolkit (https://en.wikipedia.org/wiki/XMLStarlet). The CSV files extracted are then used into the others notebooks to analyse the data.

### 2. Hunting for DOIs

 - pubmed_merge_crossref.ipynb
 - pubmed_merge_crossref_results.ipynb

Match between PubMed metadata and CrossRef metadata (downloaded via API) using the combinations of first author name + start page

### 3. PubMed content covered by library collection

 - pubmed_merge_library_coverage.ipynb
 - pubmed_merge_library_coverage_results.ipynb

PubMed and print journals / ejournals matched by journal ISSN-L and boundary years of subscriptions

### 4. Which PubMed content is OA ?

After PubMed metadata was enriched with DOIs we could merge with several OA data providers:

#### unpaywall (merged by DOI)
 - pubmed_merge_unpaywall.ipynb
 - pubmed_merge_unpaywall_results.ipynb
 
#### DOAJ (merged by ISSN-L and publication year)
 - pubmed_merge_doaj.ipynb
 
#### EUPMC (PMC merged by PMID)
 - pubmed_merge_pmc.ipynb
 - pubmed_merge_pmc_doaj_results.ipynb
 
#### Switzerland National Licences
 - pubmed_merge_national_licences_ch.ipynb
 - pubmed_merge_national_licences_ch_results.ipynb
 
 

