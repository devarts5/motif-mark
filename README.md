#motif-mark

A python program to visualize the locations and prevalence of particular motifs in a fastq sequence
This program takes in a fasta file and a text file, that provide a set of genes to analyse and a set of motifs, that you would like to find in the gene sequences.  It converts the given sequences and motif list to a visual representation of the locations of motifs in the sequences.  This script can take DNA or RNA sequence input. This script can take up to 13 motifs. The image returned will be labeled Motif_marker_Results.svg  They will be represented as a line with a length that is relative to the sequence size.  Exons will be represented as a rectangle overlapped on the line and motifs as solid colored areas.  This program also returns a text list of motif locations on the genes given, labelled Motifs_text.txt
Each sequence is labelled with the entire fasta header line, including chromosome, location and such.

 To start the program in an Ubuntu shell:
 Make sure that you are in the directory where your files are at. Ex: cd  /mnt/c/Users/user/Documents/files_for_motif_marking
 Use conda install -c conda-forge pycairo
Start program, including entering arg parse for fasta file and motifs.text file as follows:
./motif_mark.py -s -s <directory path>/<sequence_file>.fasta -m <directory path>/<motif_file.text

Your motif text file should look something like the following:

AACTGYat

YYYSYYN

AAaaggcR

ccgtgtca

Your resulting image will look something like this.  In this case, one of the requested motifs is not found in the sequences.
![Example Motif Marker Output](https://github.com/devarts5/motif-mark/blob/master/Motif_marker_Results.svg)
