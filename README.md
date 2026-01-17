# BINF-6110_Assignment-1
## Assignment 1 Part 1: Introduction and Proposed Methods
## Introduction  
 
  **Goals**:  
  - to learn how to assemble a bacterial genome, align it with a reference genome and visualize the outcome\
  - in real world scenario, the goal of this process could be to determine if the raw data exhibits any mutations, or to determine if the observed species is what it is being compared to as opposed to a new or different species                                                       
  **Challenges**:\
    - long reads can be more error prone than short reads and therefore require more QC steps
  - lack of general knowledge in the area
  - needing to qc the raw data
  - find a reference genome\
  - proposed workflow:
     - convert raw read file to FASTQ
     - run through FASTQC to trim the data
     - run through Flye to assemble the data into a FASTA file
     - the FASTA file can be aligned with the reference genome using 
  **Pros and Cons of Approach/Parameters**:
 Sequencing the genome of an organism can be done to achieve a variety of goals. Depeding on the situation, one might need to determine the abundance of species from an eDNA sample, build a reference genome for a new species, or compare the genome of their organism to a reference genome to determine mutations or the effects of functional regions of the genome (https://www.mdpi.com/2076-3417/14/11/4837). In this circumstance, the genome of _Salmonella enterica_ has been sequenced into long reads which will be trimmed, assembled, and aligned with a reference genome. Given that we know the species that has been sequenced  



 References:  
 https://www.mdpi.com/2076-3417/14/11/4837 
