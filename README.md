## Genome comparisons of crAss-like phages

<img src="https://user-images.githubusercontent.com/63568880/206448659-1f3f8143-0632-48cc-8a4b-a30e25b6dbb5.svg" width="700">


## About

This repo contains the HMMs for hallmarks genes (MCP, Portal, and TerL) used for the detection of crAss-like phages. This also has basic bash script (crAss.sh) that allows users to search through metagenomes/contigs for putative crAssphages using these profiles. The script will be updated on a regular basis and will soon be provided in the form of a nextflow pipeline.

## Usage

For the script to run successfully users need to install both [Prodigal](https://github.com/hyattpd/Prodigal) and [HMMER](http://hmmer.org/) beforehand.

To test if all dependencies are installed and executable, users may run the crAss.sh script using these [HMM profiles](https://github.com/SAmicrobiomes/crAssZA/tree/main/HMM%20profiles), as well as this [contig file] (with .fasta extension)(https://github.com/SAmicrobiomes/crAssZA/tree/main/example%20files). Please make sure that all these files are in the same directory. Note that the HMM profiles require to get converted to binary compressed datafiles using hmmpress, using the following command:

```
hmmpress *.HMM
```

This will create a set of files with extensions: <hmmfile>.h3m <hmmfile>.h3i <hmmfile>.h3f and <hmmfile>.h3p



Once done users may execute the crAssZA.sh script as follows: 

```
(crAss)[user@machine007]$ ./crAss.sh
```


Once executed, the script will run for a few seconds and set of output files will be generated. These will have extentions *faa and *hmmout that may require further manual inspection.


