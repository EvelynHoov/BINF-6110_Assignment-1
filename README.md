# BINF-6110_Assignment-1: Assembling and alignment of the _Salmonella enterica_ genome using long read data sequenced from an Oxford Nanopore Sequencer
### Evelyn Hoover
## Assignment 1 Part 1: Introduction and Proposed Methods
## Introduction  
 ### Biological Context  
  Bacteria are a phylum of prokaryotic microorganisms that are abundant worldwide. Most species within this phylum are harmless or even beneficial to humans and pose no threat to our health or wellbeing. However, there are some species that can enter or otherwise come into contact with a human and cause a wide range of harmful symptoms. _Salmonella spp._ are generally well-known for this, commonly in conjunction with raw chicken products. _Salmonella enterica_ specifically can cause gastroenteritis, bacteremia, or enteric fever depending on how the bacteria enters the body and the severity of infection (https://www.canada.ca/en/public-health/services/laboratory-biosafety-biosecurity/pathogen-safety-data-sheets-risk-assessment/salmonella-enterica.html). _S. enterica_ is a gram-negative faculatative anaerobe and spread of infection is facilitated by contact with infected animals or humans, their feces, or consumption of infected food or water. Infections can become fatal if left untreated, especially those of the population that are more vulnerable, such as children and the elderly. For this reason, it is important to monitor spread of infections. 
  Antibiotics are commonly used to treat _S. enterica_ infections. For this reason, populations expressing antibiotic resistance are often of concern because of their genetic ability to resist treatment and pass this resistant ability to more cells in the population (https://www.who.int/news-room/fact-sheets/detail/antimicrobial-resistance). If left unchecked this can render antibiotic treatments ineffective and reduce the ability to treat infections, leading to more severe cases of infection (https://www.who.int/news-room/fact-sheets/detail/antimicrobial-resistance). Therefore, sequencing samples of _S. enterica_ and aligning them to reference genomes to monitor for mutations that could give rise to antibiotic resistance is essential for minimising this threat.
 ### Goals  
  The goal of this assignment is to assemble the long read sequences of  _S. enterica_ produced from a Nanopore sequencer and align the assembled genome to a reference genome from the literature. In a real-world scenario this technique would often be used to compare the genetics of a sample to recorded literature to determine mutations or the effects of knockouts of genes within the population. In this circumstance, the goal is to successfully clean the data, assemble it, align it, and visualise it.
 ### Challenges and Limitations  
  Considering the sequences to be used are long reads there may be more errors than if short read sequencing were used. For this reason steps may need to be repeated to ensure the sequences are the highest quality possible before moving onto the next step. However, long read sequencing is necessary when looking for mutations and comparing the genome to a reference. Additionally, as someone with very little experience in bioinformatics as a whole, the progression of this project will not be nearly as linear as it could be with someone with more experience. However, that is simply what happens when learning a new skill.
## Proposed Methods  
 ### Data Description  
  The data used in this assignment is a long read sequence from an Oxford Nanopore Sequencer. The sequence was generated using R10 chemistry and the reads have an expected accuracy of Q20+ and a read length distribution of N50:5-15kb. The data is provided as a FASTQ file.
 ### Quality Control
  The FASTQ file is initially run through FASTQC which is generally used for short read sequences but can also be used to run long read sequences in Linux (https://www.sciencedirect.com/science/article/pii/S2001037025000182). This process works to trim the data of any errors so that it can be assembled properly. While FASTQC can be used on long read sequences, it does have some pitfalls in that it does not provide metrics important for long reads nor read and base QC mapping (https://www.sciencedirect.com/science/article/pii/S2001037025000182). However, FASTQC is simple to use for new users and can provide results sufficient for this project.
 ### Assembly
  To perform de novo assembly on the reads to form a consensus genome, Flye will be used. Flye is optimal for this process as it constructs an assembly graph using disjointed segments which allows it to improve assembly at long and repetetive regions (https://www.nature.com/articles/s41587-021-01108-x). This process does not require manual intervention, however if a polishing step is required after assembly than Medaka and Homopolish are recommended (https://www.nature.com/articles/s41598-025-90127-8). Following assembly, the consensus genome will be converted to a FASTA file.
 ### Alignment  
  After assembly, the consensus genome will be aligned to a reference genome. The reference genome will be obtained from NCBI (https://www.ncbi.nlm.nih.gov/nuccore/NC_003197.2). 
 ### Visualisation
## Conclusion
## References
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
