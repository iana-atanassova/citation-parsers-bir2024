# A Comparative Study of Generative LLMs and Traditional Out-of-the-box Citation Parsers

This repository provides the data that was produced for the experiment reported in the paper:

Iana Atanassova and Marc Bertin, 2024. "Breaking Boundaries in Citation Parsing: A Comparative Study of Generative LLMs and Traditional Out-of-the-box Citation Parsers", Bibliometric-enhanced Information Retrieval workshop (BIR), collocated with the 46th European Conference on Information Retrieval (ECIR 2024), Glasgow, Scotland. 


## Data

The data is organised as follows:


── cermine-output						: output produced by the CERMINE citation parser

│   ├── alphabetic			: alphabetic citation style

│   │   ├── 2024_TestPaper_experiment_BIR_ECIR_100refs.pdf		: test paper generated with this citation style

│   │   ├── alphabetic.txt 										: CERMINE output for the bibliographic referencces in txt format

│   │   └── alphabetic.xml										: CERMINE output in XML NLM format

│   ├── apa

│   ├── authortitle

│   ├── authoryear

│   ├── chem-acs

│   ├── chicago-authordate

│   ├── ieee

│   ├── mla

│   ├── nature

│   ├── numeric

│   ├── phys

│   └── science

├── input

│   ├── dummy-latex-paper		: latex code for generating dummy papers with 100 references to test the parsers

│   └── txt-input				: citation strings that were generated for each citation style in txt format

├── LICENSE

├── parsers-output-comparison.csv		: results of the comaprison of the parsers' output with the original bibtex entries. 

├── parsers-output.csv					: output from the parsers ChatGPT, Llama, and Neural ParsCit

└── README.md

## Description

Tags used in file parsers-output-comparison.csv: 
- OK: correct
- DIFF: parser's output is present and different from original bibtex entry
- MISS: parser's output is missing
- ADDED: parser's output is present, and the field is not is the original bibtex entry
- NONE: the field is not is the original bibtex entry, nor in the parser's output
- PP: problem of parsing the bibtex output of the parser (incorrect syntax), or no labeled output provided by the parser

The details on the processing and the normalization of the fields and labels that is done before the comparison of the outputs are presented in the paper cited below.

## To cite this work

To use this dataset and/or the results in this repository, please cite the following article and its dataset:

@inproceedings{atanassova2024citparse,
	title = {{Breaking Boundaries in Citation Parsing: A Comparative Study of Generative LLMs and Traditional Out-of-the-box Citation Parsers}}, 
	author = {Iana Atanassova and Marc Bertin},
	year = {2024},
	booktitle = {{International Workshop on Bibliometric-enhanced Information Retrieval (BIR 2024) co-located with the 46\textsuperscript{st} European Conference on Information Retrieval (ECIR 2024)}},
	address = {Glasgow, Scotland}
}

@dataset{bertin_2024_10839503,
  author       = {Bertin, Marc and
                  Atanassova, Iana},
  title        = {Synthetic Dataset of Citation Strings in 12 Styles},
  month        = mar,
  year         = 2024,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.10839503},
  url          = {https://doi.org/10.5281/zenodo.10839503}
}

Authors:
- Iana Atanassova, ORCID https://orcid.org/0000-0003-3571-4006 URL https://iana-atanassova.github.io/
- Marc Bertin, ORCID https://orcid.org/0000-0003-1803-6952 URL https://elico-recherche.msh-lse.fr/membres/marc-bertin
