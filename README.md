# Hybrid assembly


# Hybrid assembly for Oxford Nanopore Reads - Bacteria genome 

Requirements:

Python v3.6.4

Albacore v2.1.10

Conda

Porechop

Blast

Unicycler

All work done on Virtual Machine (CLIMB) Birmingham 
Log in address: 147.188.173.240

Albacore is an ONT's official command-line basecaller, an account is required to log in.
Albacore basecalling command is:
```
read_fast5_basecaller.exe --flowcell FLO-MIN106 --kit SQK-LSK108 --barcoding --output_format 
fast5,fastq --input c:\data\reads\20180308_2115_ 
--save_path d:\Albacore_Output\JCT_Nanopore_Run1_080318c --worker_threads 8 --recursive
```
Porechop is a tool from Oxford Nanopore for finding and removing adapters.
Porechop can be install from conda but need to create an environment first
```
conda create -n pore
conda install porechop racon
```
Make sure on right PATH and run Porechop
Porechop command is:
```
porechop -i /media/deepdata/barcode08/FASTQ -b nanochoped/
```

My transfer command is:
```
scp oye@147.188.173.240:/home/oye/unicyclernano/assembly.fasta 
```
Check no phi X174 in assembly.fasta
```
blastn -query FASTA/AF176034.fasta -subject assembly.fasta -out blast.txt
```
Web-Blast (NCBI) each nodes/contigs for identity with phi X174. Contigs can easily be selected by installing Bangdage at http://rrwick.github.io/Bandage/

