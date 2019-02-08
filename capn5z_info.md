## Additional Xl_capn5Z  information

This gene is a bit tricky to knock down and amplify separately the different paralogs.

### NCBI

- capn5.S: NM_001091200.1

- capn5.L: NM_001087339.1

**Problem:** capn5.L sequence does not exactly match the sequences I got from Xenbase from 2L

### Xenbase

Blasting the capn5z sequence on v.9.2 X. laevis genome:

```
Overview of Results
Hit Id 	Hit Description Score 	E value
Scaffold125	Scaffold125 358 	6e-97
chr2L	chr2L 336 	2e-90
chr2S	chr2S 246 	3e-63
```
I assumed the 1st one was capn5z, capn5.L and capn5.S. 

Location results:

```
[JBrowse laevis 9.2: Scaffold125:65935-66132]
[JBrowse laevis 9.2: chr2L:179697453-179697649]
[JBrowse laevis 9.2: chr2S:154207406-154207602]
```
The 2S match was annotated as capn5.S and the sequence similar to NCBI.
But the 2L was not so I assumed the annotation was missing and downloaded 1kb around the matching region. The sequence is not exactly the same as capn5z and the beginning of the aligned region with capn5z, this capn5L matches the one from the paper.

But when I tried to align the NCBI sequences with the xenbase sequences, capn5L are very different...

Looking for capn5:

For X. laevis annotation for v.9.1 pop out. Using `PAC4GC:7353299.CDS.4`

```
chr2L:180235066..180235258 (- strand) class=CDS length=193
```
Blast against v.9.2, best hit for 2L:
```
[JBrowse laevis 9.2: chr2L:180095200-180095392]
[JBrowse laevis 9.2: chr2S:154209508-154209699]
```
When opening the result of 2L:
```
Primary Data
Name	capn5.L
Type	gene
Position	chr2L:180089115..180143177 (- strand)
Length	54,063 bp
```

### Website and genome used in their paper

Using as input the capn5z sequence recovered from xenbase and matching exactly the published sequence.

On the same genome as the one used in the publication, the website (http://xenopus.lab.nig.ac.jp)) moved to [here](http://viewer.shigen.info/xenopus/index.php).
```
##v.9.1 as reference

Blast / Blat Results

Entry 1 : query (198bp)
Subject 	Length(bp) 	HSP(bp) 	Identity 	Score 	E-value 	Alignment 	JBrowse
Scaffold125 	208,957 	198 	100% 	392 	e-107 	Show 	xl_v91
chr2L 	181,296,326 	198 	97% 	353 	2e-95 	Show 	xl_v91
chr2L 	181,296,326 	198 	91% 	258 	9e-67 	Show 	xl_v91
chr2S 	159,817,000 	198 	87% 	194 	1e-47 	Show 	xl_v91
```

Looking at the alignment:

```
Scaffold125 	208,957 	198 	100% 	392 	e-107 	Hide 	xl_v91

 Score =  392 bits (198), Expect = e-107
 Identities = 198/198 (100%)
 Strand = Plus / Minus

                                                                         
Query: 1     atgcaaacccttcagcccaaagtggccagctccatctacattaactctggcagtgtcttc 60
             ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
Sbjct: 66972 atgcaaacccttcagcccaaagtggccagctccatctacattaactctggcagtgtcttc 66913

                                                                         
Query: 61    ctacacgttgacctgaaggaggggagatacgtcgttattcccaccatgtttaatcctggt 120
             ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
Sbjct: 66912 ctacacgttgacctgaaggaggggagatacgtcgttattcccaccatgtttaatcctggt 66853

                                                                         
Query: 121   gacacgggagaattcctgctcagaatttttactgatgtgctttctaacttgcttgtaagt 180
             ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
Sbjct: 66852 gacacgggagaattcctgctcagaatttttactgatgtgctttctaacttgcttgtaagt 66793

                               
Query: 181   caatatggccccaactag 198
             ||||||||||||||||||
Sbjct: 66792 caatatggccccaactag 66775

```

```
chr2L 	181,296,326 	198 	97% 	353 	2e-95 	Hide 	xl_v91

 Score =  353 bits (178), Expect = 2e-95
 Identities = 194/198 (97%), Gaps = 1/198 (0%)
 Strand = Plus / Plus

                                                                             
Query: 1         atgcaaacccttcagcccaaagtggccagctccatctacattaactctggcagtgtcttc 60
                 ||||| ||||||||||||||||||||||||||||||||||||||||||||||||||||||
Sbjct: 179837319 atgcacacccttcagcccaaagtggccagctccatctacattaactctggcagtgtcttc 179837378

                                                                             
Query: 61        ctacacgttgacctgaaggaggggagatacgtcgttattcccaccatgtttaatcctggt 120
                 ||||||||||||||||||||||||||||||||||||||||| ||||||||||||||||||
Sbjct: 179837379 ctacacgttgacctgaaggaggggagatacgtcgttattccaaccatgtttaatcctggt 179837438

                                                                             
Query: 121       gacacgggagaattcctgctcagaatttttactgatgtgctttctaacttgcttgtaagt 180
                 |||||||||||||||||||||||||||||||||||||||| ||||||| |||||||||||
Sbjct: 179837439 gacacgggagaattcctgctcagaatttttactgatgtgccttctaac-tgcttgtaagt 179837497

                                   
Query: 181       caatatggccccaactag 198
                 ||||||||||||||||||
Sbjct: 179837498 caatatggccccaactag 179837515

```
```
chr2L 	181,296,326 	198 	91% 	258 	9e-67 	Hide 	xl_v91

 Score =  258 bits (130), Expect = 9e-67
 Identities = 182/198 (91%), Gaps = 1/198 (0%)
 Strand = Plus / Minus

                                                                             
Query: 1         atgcaaacccttcagcccaaagtggccagctccatctacattaactctggcagtgtcttc 60
                 ||||| |||||||||||||||||||||||||||||||||||||||||  |||||||||||
Sbjct: 180233061 atgcacacccttcagcccaaagtggccagctccatctacattaactcccgcagtgtcttc 180233002

                                                                             
Query: 61        ctacacgttgacctgaaggaggggagatacgtcgttattcccaccatgtttaatcctggt 120
                 ||||   ||||||||||||||||||||||||||||||||||||||| |||| |||| |||
Sbjct: 180233001 ctacgtattgacctgaaggaggggagatacgtcgttattcccaccacgtttgatccaggt 180232942

                                                                             
Query: 121       gacacgggagaattcctgctcagaatttttactgatgtgctttctaacttgcttgtaagt 180
                  |||||| |||||||||||||||||||||||||||||||| ||||||| |||| ||||||
Sbjct: 180232941 cacacggaagaattcctgctcagaatttttactgatgtgccttctaac-tgctggtaagt 180232883

                                   
Query: 181       caatatggccccaactag 198
                 | |||||| |||||||||
Sbjct: 180232882 ccatatggtcccaactag 180232865

```
So looks like they are 2 copies on the 2L (where able to Sanger amplify capn5z and the most similar 2L) --- Need to talk wih BJE: capn5z is what I obtained with my primers, the more similar 2L is what Danielle got with her primers ...

When I sanger sequenced the "capn5z", I obtained some heterozygous sites for some inividuals, that are homozygous for other individuals which is compatible with a gene on the Z chromosome (heteroz in males ZZ, homoz in females ZW since only 1 Z copy).

However Danielle obtain a different sequence for every individual she sequenced, matching exactly one of the capn5.L gene... maybe a W? The sequences are not good enough to be sure all the sites are homozygous or some heterozygous...
