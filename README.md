
This repository provides the data that was produced for the experiment reported in the paper by Iana Atanassova and Marc Bertin, submitted to the workshop BIR 2024. 


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
-  OK: correct
- DIFF: parser's output is present and different from original bibtex entry
- MISS: parser's output is missing
- ADDED: parser's output is present, and the field is not is the original bibtex entry
- NONE: the field is not is the original bibtex entry, nor in the parser's output
- PP: problem of parsing the bibtex output of the parser (incorrect syntax), or no labeled output provided by the parser

The details on the processing and the normalization of the fields and labels that is done before the comparison of the outputs are presented in the paper cited below.

## To cite this work

To use this dataset and/or the results in this repository, please cite the following article:

@inrpoceedings{atanassova2024citparse,
	title = {}, 
	author = {Iana Atanassova and Marc Bertin},
	year = {2024},
	...  paper under review at BIR 2024 workshop ...
}
