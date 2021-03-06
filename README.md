[![Build Status](https://travis-ci.org/frenzymadness/FastQ_converter.svg?branch=master)](https://travis-ci.org/frenzymadness/FastQ_converter)

# FastQ_converter
Simple Python app to convert FastQ files to CSV

## Usage

```
$ ./FastQ_converter.py <input_file> <output_file>
```

## Example

```
$ head example_input.fq
@cluster_2:UMI_ATTCCG
TTTCCGGGGCACATAATCTTCAGCCGGGCGC
+
9C;=;=<9@4868>9:67AA<9>65<=>591
@cluster_8:UMI_CTTTGA
TATCCTTGCAATACTCTCCGAACGGGAGAGC
+
1/04.72,(003,-2-22+00-12./.-.4-
@cluster_12:UMI_GGTCAA
GCAGTTTAAGATCATTTTATTGAAGAGCAAG

$ ./FastQ_converter.py example_input.fq example_output.csv

$ head example_output.csv
"SeqID","sequence","quality"
"@cluster_2:UMI_ATTCCG","TTTCCGGGGCACATAATCTTCAGCCGGGCGC","9C;=;=<9@4868>9:67AA<9>65<=>591"
"@cluster_8:UMI_CTTTGA","TATCCTTGCAATACTCTCCGAACGGGAGAGC","1/04.72,(003,-2-22+00-12./.-.4-"
"@cluster_12:UMI_GGTCAA","GCAGTTTAAGATCATTTTATTGAAGAGCAAG","?7?AEEC@>=1?A?EEEB9ECB?==:B.A?A"
"@cluster_21:UMI_AGAACA","GGCATTGCAAAATTTATTACACCCCCAGATC",">=2.660/?:36AD;0<14703640334-//"
"@cluster_29:UMI_GCAGGA","CCCCCTTAAATAGCTGTTTATTTGGCCCCAG","8;;;>DC@DAC=B?C@9?B?CDCB@><<??A"
"@cluster_34:UMI_AGCTCA","TCTTGCAAAAACTCCTAGATCGGAAGAGCAC","-/CA:+<599803./2065?6=<>90;?150"
"@cluster_36:UMI_AACAGA","TCCCCCCCCCAAATCGGAAAAACACACCCCC","5?:5;<02:@977=:<0=9>@5>7>;>*3,-"
"@cluster_37:UMI_GAGGAG","GTCTTTGTACAAAATTTTATTAAAGGTCTTT","?B?DEC@A=?ADDAEEEC?EC@D6A@@>DE4"
"@cluster_39:UMI_GAACCG","CCTTCCATCACCAGATCGGAAAAACACACGC","00>7;8@5<192?/8;0;;>=3=/3239713"
```
