# Introduction

*"scanw and ccdc69w may encode a protein comprising 628 amino acid residues containing a SCAN domain and a protein of 48 amino acid residues that shares the highest similarity with coiled-coil domain-containing protein 69, respectively. capn5z encodes a predicted protein of 65 amino acid residues with a partial calpain III domain".* ([Mawaribuchi et al. 2017](https://www.sciencedirect.com/science/article/pii/S0012160616301142#s0095))

# NCBI domain prediction

Using `blastx` research on NCBI.

## Scanw
```
List of domain hits
	Name 	Accession 	Description 	Interval 	E-value
	SCAN 	cd07936 	
SCAN oligomerization domain; The SCAN domain (named after SRE-ZBP, CTfin51, AW-1 and Number 18 ...
	538-783 	9.18e-09
	SCAN 	pfam02023 	
SCAN domain; The SCAN domain (named after SRE-ZBP, CTfin51, AW-1 and Number 18 cDNA) is found ...
	538-783 	9.07e-08
	SCAN 	smart00431 	
leucine rich region;
	538-783 	1.71e-05
```
## Ccdc69w
```
No putative conserved domains have been detected
```
## Capn5z
```
List of domain hits
	Name 	Accession 	Description 	Interval 	E-value
	Calpain_III 	pfam01067 	
Calpain large subunit, domain III; The function of the domain III and I are currently unknown. ...
	7-156 	1.40e-10
	Calpain_III 	cd00214 	
Calpain, subdomain III. Calpains are calcium-activated cytoplasmic cysteine proteinases, ...
	16-156 	2.33e-10
	calpain_III 	smart00720 	
calpain_III domain;
	16-156 	1.33e-07
```

# [Interpro](https://www.ebi.ac.uk/interpro/)

Translated the mRNA sequence using geneious. After obtaining the same amino acid sequences paper, use interpro to obtain the border of important domains. 

- scanw: 177 - 267 (nucleotides: 528-801): Scan domain superfamily, 338 - 361 (nucleotides: 1011-1083): Zinc finger, CCHC-type superfamily

- ccdc69w: 4 - 24 (nucleotides: 9-72): COILS 

- capn5z: 4-54 (9-162): Calpain large subunit, domain III superfamily, 3 - 52 (6-156): Peptidase C2, calpain, large subunit, domain III
