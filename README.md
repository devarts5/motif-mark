motif-mark

A python program to visualize the locations and prevalence of particular motifs in a fastq sequence

Motif-Mark
A program to convert sequences motifs to a visual representation of the locations of motifs in sequences.  This script can take DNA or RNA sequence input.  It requires
a fasta file and a text file with the motifs.  This script can take up to 13 motifs. This script returns a visual image displaying the sequence (Motif_marker_Results.svg)
 as a line with exons overlapped on the line as empty black boxes and motifs as solid colored areas.  It alo returns a text list of motif locations on the genes given. (Motifs_text.txt)
 For each sequence the entire fasta header line (with chromosome, location and such) is given.

 To start the program in an Ubuntu shell:
 Make sure that you are in the directory where your files are at. Ex: cd  /mnt/c/Users/david/OneDrive/Documents/Winter_Genomics_2020
conda install -c conda-forge pycairo
Start program, including entering arg parse for fasta file and motifs.text file as follows:
./motif_mark.py -s -s <directory path>/<sequence_file>.fasta -m <directory path>/<motif_file.text
For me that, once in the correct directory, is ./motif_mark.py -s ./motif_mrker_sequence.fasta -m ./motif_marker_motifs.txt.text
Your motif file should look something like the following:

AACTGYat
YYYSYYN
AAaaggcR
ccgtgtca

