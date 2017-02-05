*********************************************
*                                           *
*              CodSeqGen                    *
*                                           *
*********************************************

- This C# program was written for generating synonymous coding sequences
   with two constraints, pre-defined amino acid sequence and GC content.
- The software is command line and windows based written in VC# 2010
*********************************************
   The author: Abdulrakeeb M. Al-Ssulami
   Copyright: 2017
*********************************************

Usage:
- Put all files (Amino Acid Sequence (AA.fasta), Reference Coding Sequence (Nucleotide.fasta), 
    and the executable file of CodSeqGen) in the same directory.
- Open command line window
- Go to the home directory containg files
- Run the tool as:
    > CodSeqGen.exe <Number of Required Synonymous Coding Sequences> <Amino Acid File> <Nucleotide File or GC content> >out.txt
- Example
    >CodSeqGen.exe 10 Zika_virus_AA.fasta Zika_virus_Nuc.fasta >out.txt
    >CodSeqGen.exe 10 Zika_virus_AA.fasta 37.5 >out.txt

Note that AA.fasta and Nucleotide.fasta files must be correct, 
this means that each codon in Nucleotide file coressponds to its amino acid in AA.fasta file