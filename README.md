# Week4_-Using-git
# LLM used for this task
ChatGPT 4o mini.  
I used ChatGPT to address specific questions while developing a basic script. Initially, I created a simple version; then, I asked ChatGPT to improve it or make it more efficient to ensure the output was correct. This process helped refine the code and enhance its functionality.


# Step 1. 

## Install Biopython 
pip install biopython  
> Successfully installed biopython-1.84 numpy-2.0.2

# Step 2. 

## Initialize git repository 
mkdir Week_4    
cd Week_4    
git remote add origin  ANADIR LINK   
git init  
git branch -m master main  
git status # check point  



# Question 2.
touch Gene_finder_adapted2.py    
nano Gene_finder_adapted2.py    

touch example1.fasta   
nano example1.fasta   

git add 
git commit -m 

```bash
python Gene_finder_adapted2.py example1.fasta Output2.txt
``` 
Translating ORFs: 100%| ██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 6/6 [00:00<00:00, 23899.17it/s]  
>ORF_27_93  
ATGATGCTAGCTAACGTAGCTAGCTATACGATCGATGACGTAGCTGATGCTGGTACGATATCGTAG  
>ORF_19_31  
ATGCGTAAATGA  
>ORF_73_97  
ATGCTGGTACGATATCGTAGCTAG  
>ORF_61_70  
ATGACGTAG   
>ORF_30_93  
ATGCTAGCTAACGTAGCTAGCTATACGATCGATGACGTAGCTGATGCTGGTACGATATCGTAG  
>ORF_0_12  
ATGCGTACGTAG  
Job for file example1.fasta finished  

>OUTPUT: Output2.txt  

git add Output2.txt  
git commit -m "Output2.txt"  

# Question 4. 
### Find all Open Reading Frames in the 14 genomes you downloaded  

touch Gene_finder_adapted2.py  
nano Gene_finder_adapted2.py

git add Gene_finder_adapted2.py ALL_ORFS.txt 
git commit -m "Update Gene_finder_adapted2.py ALL_ORFS.txt"

```bash
find /home/chuyascm/ncbi_dataset/data -type f -name "*GCF*.fna" -exec python Gene_finder_adapted2.py {} ALL_ORFS.txt \;  
```
#Checkpoint  
[chuyascm@login509-02-r Week4_-Using-git]$ ls -lh ALL_ORFS.txt  
-rw-r--r-- 1 chuyascm g-chuyascm 60M Oct  2 16:25 ALL_ORFS.txt  

> OUTPUT: ALL_ORFS.txt

# Question 5. 
### Find all Open Reading Frames in the 14 genomes and discard short ORFs that are unlikely to be functional genes - Filtration (-l 100)


git add Gene_finder_filtered.py FILTERED_output1.txt  
git commit -m "Gene_finder_filtered.py FILTERED_output1.txt"  
