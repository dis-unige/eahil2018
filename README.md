# Dissecting PubMed: which content is covered by the Library? and Open Access?

**Floriane Muller**<sup>1</sup> and **Pablo Iriarte**<sup>2</sup>, University of Geneva, Switzerland

<sup>1</sup> floriane.muller@unige.ch - Scientific Information Division, University Library of Geneva, Medicine and Pharmaceutical Sciences Unit (CMU). Rue Michel-Servet 1, 1211 Geneva - Switzerland

<sup>2</sup> pablo.iriarte@unige.ch - Scientific Information Division, University Library of Geneva, Coordination Unit (CODIS). Rue du Général-Dufour 24, 1211 Geneva - Switzerland

Study presented at the **European Association for Health Information and Libraries (EAHIL) Conference**, Cardiff, 9-13 July 2018.
https://eahilcardiff2018.wordpress.com/

This repository is intended to give access to the code and Jupyter notebooks used in this research. Others academic libraries are invited to use their own data and reproduce all the calculations in order to improve the methodology and compare the results with the cover of PubMed references we found for the Geneva University library.

To reproduce the calculations you need two files :

 1. Paper Journals holdings exported from the library catalogue
 2. e-journals holdings exported from the link resolver or ERM software
 
The data sources for PubMed, Crossref and unpaywall are not included here because of their big size but they can be downloaded using the links provided in the notebooks. 

### Abstract
#### Objective
Our project aims to uncover accessibility to PubMed's contents. By downloading all PubMed metadata, enriching it with missing DOIs and confronting it to our e-journal and paper collection and Open Access tools we dissect the full-text accessibility at our institution: How does the library fare, with its online subscriptions and paper collections of journals? And which portion of PubMed is accessible to the general public via Open Access (OA)?

#### Methods / Description
We parsed the whole XML content of PubMed metadata and extracted all reusable identifiers (such as PMID, DOI, ISSNs, PubYear, Volume, Issue, Pages, etc.). We stored them in a Python/Pandas DataFrame in order to mine, query, merge and enrich it with external relevant sources of data.

Confronting PubMed metadata and extractions from our paper and electronic collection holdings allowed us to evaluate the coverage provided by our institution.

Despite the efforts of the publishers to rescan the journal archives and the implementation of a commercial offer on backfiles, the proportion of DOIs remains very low in PubMed metadata of articles published before 2000 (9%),leading us to believe that some articles might be disconnected from their identifiers. Indeed, a first analysis revealed that only 43% of articles in PubMed contain DOIs (11'931'616 of 27'836'723 citations). Most of OA tools relying on DOIs, we first had to try to reconnect PubMed's articles with their DOIs to make sure as many OA versions as possible were found.

Missing DOIs were obtained by merging Crossref and PubMed metadata. A dataset published by EuropePMC (discovered midway through our research) proved to be a wealth of information and allowed us to evaluate and complete the DOIs found. OA information was obtained from unpaywall, PMC and DOAJ, evaluating full-text availability for the public and practitioners not affiliated with the university. We finally used the NLM e-utilities "ELink" API to import all the links provided by publishers and displayed in PubMed references, in order to compare our results.

#### Results
PubMed metadata enriched with DOIs and OA information provided us with precise breakdowns of PMIDs accessibility, either through institutional access, or through Open Access sources.

With its print or electronic collections, our university library provides its users with access to the full-text of 73% of PubMed's articles. This precise indication gives us a much more informed insight into adequacy and efficacy of our past and present collection choices and can provide an effective tool for future development of our collection but also for the promotion of our library resources and services (Institutional repository, ILL services...).

Moreover, our research allowed us to identify 7'510'309 DOIs that could be added to PubMed's data. Those missing keys sometimes link to OA versions of the articles and we hope that our work of finding/locating missing PubMed DOIs can be useful to the community at large.

Merging all DOIs (available in PubMed metadata and those found by EuropePMC or by our method) with Unpaywall, we found that 33% of PubMed's content is available to everyone (gold or green OA). More detailed figures and the distribution of different access roads by publication date will be presented at the conference.

#### Keywords
PubMed; Digital Object Identifiers; Open Access; Data mining; Subscription coverage
