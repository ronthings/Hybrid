# Hybrid

My transfer command is:
```
scp oye@147.188.173.240:/home/oye/unicyclernano/assembly.fasta .
```
Check no phiX in assembly.fasta
```
blastn -query FASTA/AF176034.fasta -subject assembly.fasta -out blast.txt
```
Web Blast (NCBI) each nodes for identity with phiX 174. Nodes can easily be selected by installing Bangdage at http://rrwick.github.io/Bandage/

