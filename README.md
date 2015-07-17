### Introduction

**MView** is a command line utility that extracts and reformats the results of
a sequence database search or a multiple alignment, optionally adding HTML
markup for web page layout. It can also be used as a filter to extract and
convert searches or alignments to common formats.

Inputs:

- Sequence database search: BLAST, WashU-BLAST, UVic FASTA families;
- Multiple sequence alignment: CLUSTAL, HSSP, MSF, FASTA, PIR, MAF.

Outputs:

- HTML markup, FASTA, CLUSTAL, MSF, PIR, RDB (tab-separated values).

Full documentation can be found in the on-line
[manual](https://desmid.github.io/mview/ "MView manual").


### Requirements

MView is implemented in Perl, version 5 as a self-contained command line
program that should run cross-platform. 


### Download

The [latest version](https://github.com/desmid/mview "MView site") of the
software can be downloaded from the GitHub MView project repository as a
gzipped tar archive.


### Installation

1. Save the archive to your software area, e.g., `/usr/local`, then uncompress
   and extract it:
```
     tar xvzf mview-v1.59.tar.gz
```
   or
```
     gunzip < mview-v1.59.tar.gz | tar xvf -
```
This would create a directory called `mview-v1.59` and place all the files
under there.

2. Change to this directory and load `bin/mview` into an editor.

3. Set a valid path for the Perl interpreter on your machine after the ``#!``
   at the top of the file, for example:
```
     #!/usr/bin/perl
```

4. Find the `use lib '/path/to/mview/lib';` line and change it, in our
   example, to:
```
     use lib '/usr/local/mview-v1.59/lib';
```
   and save the file.

5. Finally, make sure that the directory containing the mview script (that you
   just edited) is on your `PATH` and rehash or login again.


### Found a bug?

Please send an email to `biomview _at_ gmail.com`.

If MView isn't able to parse your input file or produces a warning message, it
would be very helpful if you can include/attach the data file in your email so
that I can (1) quickly reproduce the error, and (2) add the example to the
test suite.


### Citation

If you use MView in your work, please cite:

> Brown, N.P., Leroy C., Sander C. (1998). MView: A Web compatible database
> search or multiple alignment viewer. *Bioinformatics*. **14** (4):380-381
> [PubMed](http://www.ncbi.nlm.nih.gov/pubmed/9632837 "PubMed link").


### Copyright and licence

MView and associated libraries are Open Source Software with copyright
protected under the GNU General Public License, version 2.


### Acknowledgements

People who contributed early code or suggestions include C. Leroy and other
members of the former Sander group at EBI. Useful suggestions relating to the
EBI sequence database search services have come from R. Lopez, W. Li and
H. McWilliam at EBI. Many other people have suggested new features and
reported bugs; I hope I have acknowledged them in the change log and apologise
if I have missed anyone out.