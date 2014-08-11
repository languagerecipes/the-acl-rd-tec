-------------------------------------------------------------------------------
THE ACL RD-TEC: a dataset for evaluation of term extraction and classification in computational linguistics
-------------------------------------------------------------------------------

NOTE: This repository only contains the basic manual annotation files. 
To explore and download all the resources available through this dataset please visit http://atmykitchen.info/datasets/acl_rd_tec/. 



A.	DESCRIPTION

The ACL RD-TEC dataset is derived from a pre-processed, segmented, part-of-speech tagged version of the ACL anthology reference corpus (ACL ARC) [1]. To download the source pre-processed segmented corpus (SEPID_CORPUS) and index files, please see [2].
Please attribute the use of this dataset by citing Zadeh and Handschuh (2014) as stated at the end of this document.

This repository will be updated with new annotations. 




B.	FILES AND CONTENTS
This repository contains the following folders and files: 

1. /annotation: 
This folder contains manually annotated terms and the relevant index files that map them into the ACL ARC document ids. 
The annotation guideline documents can be obtained from [3].
The annotated terms are a subset of a larger sets of candidate terms that can be obtained from [4].

Currently these folder contains the following files:

	1.1. /annotation/_all_annotated_candid_term
	This tab-separated text file contains all the manual annotations. Each line of the file is a record with the following tab-delimited data fields:
		* TERM_ID: the given unique identifier to the (candidate) term. As mentioned in [4], the unique ids are the same across all the lists of candidate terms and can be used to trace and map an annotated term in all of these lists and provided index files.
		* TERM_STRING: lexical form that verbalizes the term, e.g. "automatic document categorization".
		* TERM_ANNOTATION: currently limited to 0 for invalid, 1 for valid and 2 for technology term. Please note that "technology terms" are kind of valid terms; thus, if a term is annotated as "technology term" it is also a "valid term".
	
	1.2. annotation/_all_annotation_map_to_acl_arc_id
	This tab-separated text file gives a mapping between the publications in ACL ARC and annotated valid terms as well as technology terms. The structure of the records of the file is as follows:
		* ACL_ARC_ID: standard ACL ARC ID for a publication.
		* TERM_ID: ID of an annotated valid or technology term appeared in this publication. 
	Note: you can create other mappings between annotated terms and resources in ACL ARC (e.g. citation network) using the provided materials in [2]. 

	1.3. annotation/_all_annotation_in_sentence.zip
	This file lists all the sentence ids from the SEPID_CORPUS that contain at least one term annotated as valid or technology term (invalid terms are excluded from the list). If a sentence contains more than one annotated term, then it is listed more than once. The record of the files have the following structure:
		* SENTENCE_ID: the id of the sentence from SEPID_CORPUS
		* SENTENCE: the sentence string, in which exactly one term is annotated by placing the tag <term id="candid_term_id" ann="annotation, either 1 for valid or 2 for technology term"></term> around the term. Please note that all the sentences are not verified manually. Before downloading the zip file, you can see a few examples of this file's entries in the file "_all_annotation_in_sentence_few_lines_example" listed below. 
	
	1.4. annotation/_all_annotation_in_sentence_few_lines_example
	This text file provides an example of the records in the above zip file.

2. /misc:
This folder contains auxiliary materials as follows:
	2.1. /misc/pos_sequence_filter
	This list of part-of-speech sequence patterns that are employed to extract a set of candidate terms. See [4] for further documentations. 

4. /licenses
This folder contains the license files.




C. LICENSES AND DISTRIBUTION
The contents of this repository is released under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 License. 


D. CONTACTS
If you have any question or comment, or if you want to add your own set of candidate terms, annotations, or partial annotations for inter-annotator agreement, please contact me (behrangatoffice AT gmail.com ).



REFERENCES
[1] http://acl-arc.comp.nus.edu.sg/
[2] http://atmykitchen.info/datasets/acl_rd_tec/. 
[3] http://atmykitchen.info/datasets/acl_rd_tec/annotation_guideline/index_guideline.htm
[4] http://atmykitchen.info/datasets/acl_rd_tec/candidate_term/index_candid_term.htm

ACKNOWLEDGEMENT
This resource has emanated from research supported in part by a research grant from Science Foundation Ireland (SFI) under Grant Number SFI/12/RC/2289.


BIBLIOGRAPHY 

Behrang Q. Zadeh and Siegfried Handschuh. "The ACL RD-TEC: A Dataset for Benchmarking Terminology Extraction and Classification in Computational Linguistics." In Proceedings of COLING 2014 CompuTerm 2014: 4th International Workshop on Computational Terminology. 2014.

@InProceedings{zadehbq14computerm,
  author = {Behrang Q. Zadeh and Siegfried Handschuh},
  title = {The ACL RD-TEC: A Dataset for Benchmarking Terminology Extraction and Classification in Computational Linguistics },
  booktitle = {COLING 2014: Proceedings of the 4th International Workshop on Computational Terminology (CompuTerm'14)},
  year = 2014,
  month = {August},
  address = {Dublin, Ireland},
  editor = {Patrick Drouin and Natalia Grabar and Thierry Hamon and Kyo Kageura},
  publisher = {COLING}
  url       = {http://www.aclweb.org/anthology/W14-4807}
}

Steven Bird, Robert Dale, Bonnie Dorr, Bryan Gibson, Mark Joseph, Min-Yen Kan, Dongwon Lee, Brett Powley, Dragomir Radev and Yee Fan Tan. “The ACL Anthology Reference Corpus: A Reference Dataset for Bibliographic Research in Computational Linguistics.” In Proc. of Language Resources and Evaluation Conference (LREC 08). 2008.

@inproceedings{Bird-Dale-Dorr-Gibson-Joseph-Kan-Lee-Powley-Radev-Tan_LREC08.445,
    author = {Steven Bird and Robert Dale and Bonnie Dorr and Bryan Gibson and Mark Joseph and Min-Yen Kan and Dongwon Lee and Brett Powley and Dragomir Radev and Yee Fan Tan},
    title = {The ACL Anthology Reference Corpus: A Reference Dataset for Bibliographic Research in Computational Linguistics},
    booktitle = {Proceedings of the Sixth International Conference on Language Resources and Evaluation (LREC-08)},
    year = {2008},
    publisher = {European Language Resources Association (ELRA)},
    address = {Marrakech, Morocco},
    month = {May},
    url = {http://www.lrec-conf.org/proceedings/lrec2008/pdf/445_paper.pdf},
    note = {ACL Anthology Identifier: L08-1005},
}
	

