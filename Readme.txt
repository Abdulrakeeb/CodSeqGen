**********************************************************************
**********************************************************************
*                                                                    *
*                     CodSeqGen Tool                                 *
*                                                                    *
**********************************************************************
**********************************************************************

- This C# program was written for generating synonymous coding sequences
  with the desired GC-content.
- The software is command line and windows based written in VC# 2010
- The tool is presented in the paper: 
  Abdulrakeeb M. Al-Ssulami, Aqil M. Azmi, and Muhammad Hussain. 
  CodSeqGen: A tool for generating synonymous coding sequences with
  desired GC-contents, Genomics, 2019, https://doi.org/10.1016/j.ygeno.2019.02.002.
***********************************************************************
*                                                                     *
*     Copyright: 2019 by Dr.Abdulrakeeb M. Al-Ssulami                 *
*                                                                     *
************************************************************************

Usage:
- Put all files: Amino Acid Sequence (e.g. Zika_virus_AA.fasta), 
  Reference Coding Sequence (e.g. Zika_virus_Nuc.fasta), 
  the CSV file containing probabilities (e.g. Amino_Acid_Usage.csv), 
  and the executable file CodSeqGen.exe) in the same directory.
- Open command line window
- Set the current path to the directory containing files
- Run the tool as:
  > CodSeqGen.exe [-l <t|d>] [-n <m|d>] [-aa <f> | -csv <s>] [-seq <q> | -gc <k>] >out.txt
  t|d : t is the length of Amino Acid Sequence and  d is a char for default value 1000.
  m|d : m is the number of required synonymous coding sequences 
        and d is a char for default value 10.
    f : The name of fasta file containing the primary amino acid sequence.
    s : The CSV file containing probabilities of amino acids usage--
        Computed as a fraction of amino acid occurrences to the total length 
	where sum of all probabilities equals 1.
    q : The DNA nucleotide fasta file--Reference Coding Sequence--
        for generating synonymous coding sequences as its gc-content.
    k : the desired GC-content in the range between 0 and 100.

- Examples
    > CodSeqGen.exe -l 1000 -n 10 -csv Amino_Acid_Usage.csv -gc 55 >out.txt
    > CodSeqGen.exe -l d -n 10 -aa Zika_virus_AA.fasta -gc 48.35 >out.txt
    > CodSeqGen.exe -l d -n 10 -aa Zika_virus_AA.fasta -seq Zika_virus_Nuc.fasta >out.txt
