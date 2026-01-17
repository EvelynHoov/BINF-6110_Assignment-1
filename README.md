# BINF-6110_Assignment-1
## Assignment 1 Part 1: Introduction and Proposed Methods
## Introduction\
  **Goals**:\
  - to learn how to assemble a bacterial genome, align it with a reference genome and visualize the outcome\
  - in real world scenario, the goal of this process could be to determine if the raw data exhibits any mutations, or to determine if the observed species is what it is being compared to as opposed to a new or different species                                                       
  **Challenges**:\
  - lack of general knowledge in the area
  - needing to qc the raw data
  - find a reference genome\
  - proposed workflow:
     - convert raw read file to FASTQ
     - run through FASTQC to trim the data
     - run through Flye to assemble the data into a FASTA file
     - the FASTA file can be aligned with the reference genome using 
  **Pros and Cons of Approach/Parameters**:
