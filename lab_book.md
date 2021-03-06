# Kaitlyn's Lab Book
## Gloor Lab
----
#### **Wednesday, May 2nd, 2018** (Total: 8 hours)
----
*9:00 - 11:20 am*

- Searched through metagenomic, transcriptomic and metatranscriptomic datasets for a potential research focus.
- Read  [Metatranscriptome of human faecal microbiol communities in a cohort of adult men](https://doi.org/10.1038/s41564-017-0084-4 and browsed through https://www.ebi.ac.uk/metagenomics/projects. "Abu-Ali et al, 2017")
- Downloaded Xcode and Bioconductor to prepare for DADA2 download.

*11:30 am - 1:00 pm*
Biochemistry orientation session

*1:00 - 1:30 pm*
4483E meeting with Dr. Ball.

*1:30 pm - 5:10 pm*
- continued searching for a research dataset
- created a GitHub account (user: @khobbs3)
- discussed "The Big Reproducibility Problems" with Dr. Gloor and received two articles (below)
- read background information on microbiome research methods and current knowledge on influence of microbiome on the brain

I've found 3 articles relating gut microbiota to autism:
- [Pyrosequencing study of fecal microflora of autistic and control children](https://www.sciencedirect.com/science/article/pii/S1075996410001010?via%3Dihub, https://onlinelibrary.wiley.com/doi/epdf/10.1002/aur.1253 "Finegold et al, 2010"),
- [Molecular Characterisation of Gastrointestinal Microbiota of ChildrenWith Autism (With and Without Gastrointestinal Dysfunction) andTheir Neurotypical Siblings](https://onlinelibrary.wiley.com/doi/epdf/10.1002/aur.1253 "Gondalia et al, 2012"),
- [Fecal Microbiota and Metabolome of Children with Autism and Pervasive Developmental Disorder Not Otherwise Specified](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3793965/ "Angelis et al, 2013"))

all using bacterial tag encoded FLX amplicon pyrosequencing with a sample size of 40, 104, and 30, respectively; however, I noticed that each study had it's own restrictions on individuals included and am wondering if this would influence pooled results. Additionally, I'm unsure how to acquire the datasets from these studies.

Alternatively, a microbiome study on obese and lean twins has a population size of 154 but the EMBL-EBI database only has samples from 16 patients.

##### **Background Information:**
- 16S rRNA sequencing of hyper variable regions helps deduce taxonomy. Usually followed by OTU analysis.
- Brain-gut axis - describes the relationship between gut microbiota and cognitive function and neurodegeneration.

##### **"The Big Reproducibility Problems":**
1. [The fickle P value generates irreproducible results](https://www.nature.com/articles/nmeth.3288 "Halsey et al, 2015")
2. [An investigation of the false discovery rate and the misinterpretation of *p*-values](http://rsos.royalsocietypublishing.org/content/1/3/140216 "Colquhoun, 2014")

----

#### Thursday, May 3rd, 2018 (Total: 6.5 hours)
----
*9:30 am - 12:00 pm*
- downloaded atom, watched tutorials on valid syntax, and updated yesterdays entry accordingly
- found and received approval from Dr. Gloor for research dataset with a sample size of 103 and both illumina MiSeq and 454 GS FLX+ sequencing methods: [Alterations of the human gut microbiome in multiple sclerosis](https://www.nature.com/articles/ncomms12015 "Jangi et al, 2015")
- Read *The fickle P value generates irreproducible results*

>*The fickle P value generates irreproducible results*
- "Statistical Power" - sufficient statistical capacity to find an effect
    - more often than not is too low in studies
    - only considered when results have false negatives, not when results give positives
    - unless there is high statistical power, the p-value varies along with different samples and thus does not strongly support or reject the null hypothesis. As a result, null hypothesis testing should be used infrequently.
- Concept does not apply to type II errors (accepting a *false* null hypothesis)
- Statistical power + p-value = estimate of frequency of finding a statistically significant result *IFF null hypothesis is rejected*
  - **rejecting the null is a continuous function of the magnitude of p - not a binary evaluation method**
  - unlikely to give repeatable results due to variability with samples and common misinterpretation of threshold as an index
- larger sample sizes estimate effect size more precisely
- To mediate p-problem:
  - plan for precision by calculating sample size required for a defined degree of precision
  - use confidence intervals to determine size and precision of estimate* - **why?**

*1:00 pm - 5:00 pm*
- Read and took notes on *Alterations of the human gut microbiome in multiple sclerosis*
- Continued background research on microbiota-gut-brain axis
- Researched background information on softwares that process sequenced DNA (mothur, Dada2, SeqPrep)
- Started introductory powerpoint for lab meeting on Monday, May 7th.

>*Alterations of the human gut microbiome in multiple sclerosis*
- 16S rDNA sequencing of human gut microbiome in MS (n=60) and healthy patients (n=43) using Illumina MiSeq and Roche 454 FLX sequencing methods

>**Methods:**
- groups separated into MS treated (copaxone and interferon), MS untreated, and healthy patients
- Examined:
    - Fecal DNA - 16S rDNA for microbe taxonomy using the mothur software package to determine OTUs
      - alpha diversity - determines diversity in a population within a sample
      - beta diversity - determines diversity in a population between samples
    - Sera and mononuclear cells for gene expression profiling
    - Breath - methane concentration to measure presence of *Methanobrevibacter*

>**Results:**
- increases in *Methanobrevibacter* and *Akkermansia* and decreases in *Butyricimonas* in MS patients relative to healthy individuals
  - *Methanobrevibacter* and *Akkermansia* have pro-inflammatory properties - consistent with upregulation of MAPK in monocytes and T-cells
  - *Butyricimonas* has negative correlation with MS-related genes, therefore reduction could promote pro-inflammation
- correlate with variations in the expression of genes involved in dendritic cell maturation, interferon signalling and NF-kB signalling pathways in circulating T cells and monocytes
- For treated patients, *Prevotella* and *Sutterella*, and decreased *Sarcina*, compared with untreated patients

>**Conclusions:**
- microbial differences in MS patients at both phylum and genus levels confirmed by two sequencing techniques though only one pipeline used

##### **Background Information: Microbiota-gut-brain axis**
From [The role of microbiome in central nervous system disorders](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4062078/#R36)
**Afferent nerves** - stretch-sensitive mechanosensor
*The microbiota-gut-brain axis titles the communication between intestinal microbes and the CNS.*

###### Brain-to-Gut:
- Hormones – dictate the microbe niche environment
- Signal molecules/cytokines and anti-microbial peptides (AMTPs) influence microbiota composition
- Autonomic nervous system + hypothalamus pituitary adrenal (HPA) modulate the CNS and ultimately gut physiology (motility, secretion, permeability – microbiota environment).
- Enteric nervous system governs GI function

###### Gut-to-Brain:
- Microbiome is thought to influence CNS maturation
- *VAN* conveys sensory information from viscera to CNS
  - necessary for microbiome-brain communication
  - receptors sense peptides/dietary composition
- *Enteroendocrine* cells in gut epithelium can secrete neurotransmitters and signal peptides in response to stimuli
  - Transduce gut signal to brain
  - For example, satiary peptides sent to blood then brain to signal fullness
- *Metabolism:* microbial - host metabolism, microbial, or microbial assisted
  - dysregulation of serotonergic or kynurenin routes of Trp metabolism affect brain
    - ameliorated by probiotics promoting paths
-*Immunologic:* microbiome known to shape host immune system
  - effects auto-reactivity of peripheral immune cells

###### MS and Microbiome:
**[MS:](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3351877/)** demyelination of neurons by auto-reactive immune attack in CNS
- chronic autoimmune, inflammatory neurological disease of CNS
- no diagnostic test, diagnosis made on evidence of...
  - *space dissemination criterion:* presence of at least two different lesions (plaques or scars) in white matter of CNS
  - *time dissemination criterion:* at least two episodes in disease course
  - __*inflammatory criterion:*__ chronic inflammation of CNS
**EAE:** spontaneous auto-immune encephalomyelitis
  - an animal model for MS used in studies
  - induced by CNS-restrictive antigens
  - commensal microbiota essential for spontaneous and induced EAE
  1. Antibody modulation of gut microbiota controls EAE progression
    - was tested for in patients and saw response relative to control (though did not specify positive or negative response - must purchase book to find out)
  2. Dietary patterns influence EAE development
  3. Polysaccharide of *Bacteroides fragilis* can protect against CNS demyelination [(Ochoa-Reparaz et al., 2010)](https://www.ncbi.nlm.nih.gov/pubmed/20817872)

##### **Background Information: mothur, Dada2, and SeqPrep pipelines**
assign taxonomies and species.
") OTU based
[Dada2:](http://benjjneb.github.io/dada2/) ASV based
  - greater resolution (1-2 nucleotides)
  - processes larger datasets
  - more "exact" than cluster based approach of OTUs

----
#### Friday, May 4th, 2018 (Total: 7 hours)
----
_10:00 am - 12:00 pm_
- Read [Microbiome Datasets Are Compositional: And This Is Not Optional](https://www.frontiersin.org/articles/10.3389/fmicb.2017.02224/full)
- Read [An investigation of the false discovery rate and the misinterpretation of _p_-values](http://rsos.royalsocietypublishing.org/content/royopensci/1/3/140216.full.pdf)
- Read [An Introduction to Proportionality](https://cran.r-project.org/web/packages/propr/vignettes/a_introduction.html)

>*An investigation of the false discovery rate and the misinterpretation of _p_-values*
- **Power:** probability that a test will give correct results when there isa  real effect
  - depends on sample size
  - usually set to 80
- Three things to know to compute false discovery rate:
  1. specificity: percentage of effect correctly assigned
  2. sensitivity of screening: power of significance test
  3. prevalence of effect (or disease ) in a population to be screened
- **False positive rate** (opposite of PPV): # FPs/(#FPs + #TPs)
- **True effect:** difference between simulations
- Use R script to test simulations and estimate inflations
- Recall the first "Big Reproducibility Problem" that p-values will vary with different samples

  >*An Introduction to Proportionality*
  - Correlation-based  analysis is less valid when applied to relative data

*12:30 pm - 5:30 pm*
- 2018 Canada Gairdner Global Health Lecture Series - “Planetary health through food and microbes"


### Weekly hours: 21.5
---

#### Monday, May 7th, 2018 (Total: 7 hours)
----
*9:00 am - 11:20 am*
Lab meeting at St. Joseph's
- presented introductory powerpoint

*12:00 am - 5:00 pm*
- tried to set up dada2 server
- made account directory on agrajag
  - user name: khobbs3
- downloaded FTP fastQ files and transferred to agrajag via USB
  - *difficulties in transferring files via linux terminal led to transferring data files from KT's Macbook-->USB-->cJelli-->agrajag*
- Started creating Linux coding cheat sheet
- discussed using a control using dataset with known relative abundance of microbiota to analyze with Dada2. Will receive dataset at a later date.
- unsuccessfully attempted to import files into R

ssh khobbs3@agrajag.biochem.fmd.uwo.ca

**METHODS**
Find published dataset --> download fastQ files-->transfer to agrajag-->run Dada2 script on R
-->record output-->compare to OTU processed results

  ----
  #### Tuesday, May 8, 2018 (Total: 5 hours)
  ----
  *9:30 am - 11:30 am*
  - worked through [Dada2 workflow](https://github.com/ggloor/miseq_bin/blob/master/dada2_workflow_1.6.R)
    - cannot connect to agrajag through finder (control K), so had to transfer saved files from agrajag to KT's Macbook using scp
  1. **Filter and trimming:** may have to change truncation length if reads are shorter or E (error profile), q30 is the standard for a good position
    -  check plot, possibly set E to 1
    - may need a sample filter, if average quality score drops below threshold discard it...

  *12:00 pm - 1:30 pm*
  2. created filtered files in khobbs3 directory on agrajag in which reads were moved (filtRs then filtFs)
  3. filtered reads but removed
  >truncLen=c(183,174)
    to allow all reads to be filtered (since reads do not surpass length of 150 nucleotides according to plot)
  4. Ran script to learn error rates

  >('''errF <- learnErrors(filtFs, multithread=TRUE, randomize=TRUE))

    - **results filtR:**
      - not all lengths were the same
      - samples 1-13 have unique sequences
    - **results filtF:**
      - not all lengths were the same
      - samples 1-14 have unique sequences
      - Warning messages: 1: Transformation introduced infinite values in continuous y-axis

  *2:15 pm - 4:30 pm*
  5. error rates were plotted (filtFs is the first plot) ![err rate plot](/Users/kait/Documents/4/Summer\ 4483E/err.pdf)
    - **Note:** learnErrors function only uses a subset of the data (first 100M bases)
  6. dereplicated filtFs reads then filtRs reads
    - **dereplication:** combines identical sequence reads to unique reads
  7. inferred sequence variants in each sample for dadaFs and dadaRs (dereplicated filtFs and filtRs reads, respectively)
  8. merged forward and reverse primers
  9. made sequence table where rows = samples
  10. summarized output sequencing lengths
    - **Results:** table(nchar(getSequences(seqtab)))

 169 | 203 | 221 | 251 | 252 | 253 | 254 | 255 | 260
   1  |  1  |  2  | 11 | 1520 | 7704 |  75 |   6  |  1

  11. removed chimera
    - **Results:**
      - Identified 7058 bimeras out of 9321 input sequences
      - table dimensions: 105 x 2263
  12. **checked how many reads made it through the pipeline**
    - **Results:** ![reads in pipeline](/Users/kait/Documents/4/Summer\ 4483E/readsout.txt)
  13. Assigned *approximate* taxonomy, added to table, and transposed table (columns = samples)
    - **Note:** there are multiple ways to assign taxonomy*, in this I used whatever is filed into agrajag (script: taxpath<-"/Volumes/data/annotationDB/dada2/silva_nr_v123_train_set.fa.gz")
    - sv sequences and table with taxonomy exported to KT's Macbook as sv_seq.txt and dada2_nochim_tax.txt, respectively.
      - to be used for further analysis

  - updated Coding Language Cheat Sheet
  - downloaded OTUs, reads and taxonomic assignments from publicated dataset (/Users/kait/Documents/4/Summer\ 4483E/SRR3501917_MERGED_FASTQ_otu.tsv)

###### **Notes:**
  - Due to variation in taxonomy assignments comparing taxonomic names can lead to misinterpretation, it is better to compare sequence variants (sv_seq.txt)
  - Dada2 is designed to considered two errors in PCR sequencing techniques: (1) errors from DNA polymerase in generating the PCR product and (2) errors in the amplification procedure
  - [CoDaSeq Workshop](https://github.com/ggloor/CoDa_microbiome_tutorial/wiki) will be explored and used next day to visually summarize sequence variants
    - installed ALDEx2 in preparation
    - To Read:
      [] [The data we have: multivariate compositional data](https://github.com/ggloor/CoDa_microbiome_tutorial/blob/master/multi_comp.pdf)
      [] [CoDa and Sequencing](https://github.com/ggloor/CoDa_microbiome_tutorial/blob/master/coda_seq.pdf)
 
----
#### Wednesday, May 9, 2018 (Total: 6 hours)
----
*9:40 am - 12:00 pm*
- Read:
  - [x] The data we have: multivariate compositional data
  - [x] CoDa and Sequencing
- worked through CoDa set up in R but had to download a newer version of R (3.5.0
 to install packages made on version 3.3.2

###### **Notes:**
> **The data we have: multivariate compositional data**
- *multivariate:* involved two or more variable quantities per sample
  - independent variables can be treated as univariate
  - high-throughput sequencing (HTPS) is multivariate and dependent (as a result of sequencing technique) and is corrected by considering the *relative abundance*
- for compositional data, relative abundances are considered as opposed to absolute abundance to accurately assess and compare relationships
- data points are log-transformed
  - b in the y = mx + b formula becomes non-linear
  - *problem:* a non-zero intercept will yield a curved relationship in log space (x and y are not correlated when they are in normal space)
- **Geometry:**
  - unconstrained data: uniformly dispersed (uncorrelated)
    - linear distance suggests movement from one data point to another is *additive*
  - constrained data: data forms a "simplex" plane (correlated)
    - movement from one data point to another is *multiplicative* ie. taxon abundance is multiplicative of original abundance


   ---

>**CoDa and Sequencing**
- results from random sampling are more consistent for high abundance OTU but are not as definitive for rare OTUs
- for HTPS, constrained data results are the same before and after sequencing while unconstrained data is distorted
  - due to instrument capacity, HTPS constrains data (total number of reads accepted)
  - random sampling performed by sequencing can select a constant sum and therefore constrain the data
- constrained dataset = constant sum (total count) = increase or decrease in one sample is compensated accordingly by increase or decrease in another
- 16S rRNA sequencing is unconstrained (total count is variable depending on bacterial load in environment); as a result, the sample dataset must be analyzed by relative abundance

*1:00 pm - 4:45 pm*
- updated version of R still had issues installing packages, Dan took a look and noticed I am missing compilers so to correct the error a precompiled binary was installed (install.packages("Rcpparmadillo"))
  - ERROR: compilation failed for package ‘RcppArmadillo’
- [Created exploratory compositional PCA plot:](https://github.com/ggloor/CoDa_microbiome_tutorial/wiki/Part-1:-Exploratory-Compositional-PCA-biplot)
  - **NOTE:** did not create a smaller table to take random samples from, counted zeros of entire table (dada2_nochim_tax.txt)
  - number of zeros in table = 221697
  - created new data table excluding the taxonomy column so all row entries are numerical (dd<-d[,1:ncol(d)-1])
  - "PC1:  0.078"
  - "PC2:  0.048"
  - filtered reads so that count > 10  (cutoff of <= 10)
  - generated biplot using scale = 0 to plot based on samples
  - downloaded summary of metadata from published article (mg_project_summary_20180509.csv) as reference for biplot labels according to data subsets
  - subsetted samples in R using *subsetName* <- c("*sampleName1*", "*sampleName2*"... etc.):
    - controls, untreated, copaxone, interferon

    > controls <- c("SRR3501908", "SRR3501909", "SRR3501910", "SRR3501911", "SRR3501912", "SRR3501913", "SRR3501914", "SRR3501915", "SRR3501916", "SRR3501925", "SRR3501936", "SRR3501945", "SRR3501946", "SRR3501947", "SRR3501948", "SRR3501949", "SRR3501950", "SRR3501951", "SRR3501952", "SRR3501953", "SRR3501954", "SRR3501955", "SRR3501956", "SRR3501957", "SRR3501958", "SRR3501959", "SRR3501969", "SRR3501973", "SRR3501974", "SRR3501975", "SRR3501976", "SRR3501977", "SRR3501978", "SRR3501979", "SRR3501980", "SRR3501981", "SRR3501982", "SRR3501983", "SRR3501984", "SRR3501985", "SRR3501986", "SRR3501987", "SRR3501991", "SRR3502002")
    > untreated <- c("SRR3501917", "SRR3501918", "SRR3501921", "SRR3501923", "SRR3501924", "SRR3501932", "SRR3501933", "SRR3501944", "SRR3501960", "SRR3501961", "SRR3501962", "SRR3501963", "SRR3501964", "SRR3501965", "SRR3501966", "SRR3501967", "SRR3501988", "SRR3501989", "SRR3501990", "SRR3501992", "SRR3501993", "SRR3501994", "SRR3501995", "SRR3501996", "SRR3501997", "SRR3501998", "SRR3501999", "SRR3502000", "SRR3502010")
    > copaxone <- c("SRR3501919", "SRR3501927", "SRR3501930", "SRR3501931", "SRR3501935", "SRR3501940", "SRR3501942", "SRR3501943", "SRR3501970", "SRR3501971", "SRR3502001", "SRR3502003", "SRR3502005", "SRR3502007")
    > interferon <- c("SRR3501920", "SRR3501922", "SRR3501926", "SRR3501928", "SRR3501929", "SRR3501934", "SRR3501937", "SRR3501938", "SRR3501939", "SRR3501941", "SRR3501968", "SRR3501972", "SRR3502004", "SRR3502006", "SRR3502008", "SRR3502009", "SRR3502011", "SRR3502012")
 > df<-dd[,c(controls, untreated, copaxone, interferon)]
- [PCA Plot Background:](http://research.med.helsinki.fi/corefacilities/proteinchem/pca_introduction_basics.pdf)
  - transforms coordinates to "principal components" starting at the center of the original data points
  - PC1 points in direction of highest variance, PC2 = second highest... etc.
  - coordinates are perpendicular
  - variance plots shows how much variance is explained by each PC - remove those that contribute little variance
  - values in PC-coordinates = "scores"
  - **Overall:** reduce multidimensional data to lower dimension while retaining information

----
#### Thursday, May 10, 2018 (Total: 5 hours)
----
*9:40 am - 1:15 pm*
- relabelled subsets:
  - controls = "C"
  - untreated = "U"
  - interferon = "I"
  - copaxone = "N"
-relabelled subsets did not show on biplot, Dan came up with an alternative method:
  *Summary: create excel sheet with RunID (downloaded from [Jangi et al, 2015](https://www.ebi.ac.uk/metagenomics/projects/SRP075039) metadata) and add a new column named "identifier". Identifier will contain the associated label ("U", "I", "C", "N")*
    - RunIDs must be sorted into numerical order to match Dada2 output table column "RunID"(dada2_nochim_tax)
    - A new column must be added to the dada2 table called Identifiers
    - import xls into R and overlap RunIDs column to apply Identifier
    - write biplot function with xlabs=names$identifier
-*Result:*
  - difficulty in importing excel into R - tried different lines of code to ultimately determine the excel file was corrupted.
  - attempted to create and save a new excel file and computer lagged severely
  - both excel and terminal R session crashed
  - updated RStudio for attempt the same method on a simpler interface
  - repeated entire procedure from "Before We Start" to "Part 1: Exploratory Compositional PCA Biplot"
  - successfully imported excel file

*2:30 - 4:00 pm*
  - successfully generated biplot with subset labels, saved as "Subset Biplot Dada2.pdf" in ~/Documents/4/Summer\ 4483E/CoDa-Output
  - starting writing CoDa Methods with code annotations to better understand the functions used as well as add in variations I made to achieve output

----
#### Friday, May 11, 2018
----
  *9:45 am - 2:00 pm* (Total: 4.25 hours)
- Wrote point form background file in preparation for introductory thesis presentation (/Users/kait/Documents/4/Summer\ 4483E/Lab Book/Background)
    - Read [Exact sequence variants should replace operational taxonomic units in marker-gene data analysis](www.nature.com/ismej)
- Created powerpoint for presentation (~/undergrad/4/Summer\ 4483E/Presentations/KHobbs\ Introduction\ to\ Thesis)


### Weekly hours: 27.25

----
#### Sunday, May 13, 2018
----
*8:00 pm - 10:00 pm* (Total: 2 hours)
- Reviewed and edited powerpoint
- Wrote script for presentation (on khobbs3@uwo.ca OneDrive)

----
#### Monday, May 14, 2018
----
*9:00 am - 12:00 pm* (Total: 5 hours)
R Workshop Beginner

*8:00 pm - 11:00 pm*
- Edited powerpoint and script
- Added a summary of Dada2 workflow to Background methods and powerpoint

----
#### Tuesday, May 15, 2018 (Total: 1 hour)
----
*9:45 am - 11:00 am*
- added more detail to Illumina Background and powerpoint - why reads are multiplexed
- received control dataset from Ben
  - Control set: [PRJNA324163](https://www.ebi.ac.uk/ena/data/view/PRJNA324163)
    - **Note:** only grab 33 samples (2 runs from the each sample to compare runs)
- computer was excruciatingly slow, left early to go to the Genius Bar

----
#### Wednesday, May 16, 2018 (Total: 4.5 Hours)
----
*9:30 am - 10:20 am*
- Helped Toby with the Dada2 workflow, explained to him the premise of my research

*10:20 am - 12:30 pm*
- Read published article on control dataset and added to background
  [Synthetic spike-in standards for high-throughput 16S rRNA gene amplicon sequencing](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5389483/)
- Finished powerpoint presentation
  - added information about control dataset
  - fixed visuals for Illumina protocol

*12:45 pm - 2:15 pm*
- Finished script for powerpoint presentation (see KHobbs Thesis Script)

*3:00 pm - 5:00 pm*
Ethics presentations with Dr. Ball

----
#### Thursday, May 17, 2018 (Total: 6.5 hours)
----
*9:30 am - 12:00 pm*
- emailed project title to Lindsay Ralph
- worked through CoDa from the beginning
  <!--- backed up and wiped computer yesterday in attempt to increase speed but lost CoDa Methods --->
- Answered Toby's questions about the Dada2 workflow steps
- Analyzed ![err.pdf](/Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/Dada2-Output/err.pdf)
  1. probability that base substitution will occur
  2. observed (points) vs machine-learning-derived expected (line) occurrences

##### Results:
  - Forward Reads:
    - error rates drop with increased consensus quality scores
    - relatively good fits of observed to expected
      - EXCEPT: G2T, C2T

  - Reverse Reads:
    - error rates drop with increase in Q
      - EXCEPT: A2T, A2G
    - relatively good fits of observed to expected
      - EXCEPT: G2T, A2T, G2C

*1:00 pm - 5:00 pm*
R Workshop Intermediate

---

#### Friday, May 18, 2018 (Total: 5 hours)
*9:30 am - 12:00 pm*
- worked on generating PCA biplot in CoDa work flow that will represent subsets that were assigned to MS data (C, I, U, O)
    - attempted to create biplot from df (with assigned subsets) instead of dd
      - unsuccessful

*2:30 pm - 4:15 pm*
- updated CoDa Methods to include successful biplot generation
- generated and recorded observations for ![screeplot](/Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/CoDa-Output/Dada2 PC Analysis):
  - PC1 is somewhat more informative (high density in boxplot than other components)
  - No PC is very informative (PC1: 0.07 and the rest are lower... PC >50% shows stronger relationship)
- generated and recorded observations for ![Dada2 MS Biplots](/Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/CoDa-Output/Dada2 MS Biplots)
##### Results:
    - samples do not show clear difference between each other. Supported by:
        - low PC value
        - large overlap of ellipses in compositional Space
        - no clear driver shown in loadings (mass is centered around origin (0,0)
        indicating symmetry in data and no presence of OTUs/features
        driving sample variation)
##### Notes on interpreting biplots:
      - loadings are OTUs/features
      - position of samples depends on position of loadings -- loadings will drive sample variation
      - distance between loadings is informative:
        - overlapping of points implies a relationship
      - distance between samples is NOT informative:
        - because PCAs are multi-dimensional, overlapping points may appear to be similar
        in the plotted 2 dimensions but upon looking from a 3rd dimension may not show correlation
            - pairwise analysis will reveal where samples differ*
            **NOTE**
            - MS study researchers performed DMD/AMOVA to compare OTU distributions between samples

*4:15 pm - 5:15 pm*
- Reviewed MS article and added to Notes on MS Study
- Started on CoDa Methods Part Two: ALDEx2 for Differential Expression Analysis
- Helped Toby work through error in Dada2 workflow

Next steps:
  - univariate analysis - ALDEx.glm function
  - multivariate analysis - ALDEx.clr function
    - on transformed data (dd.clr) for change between subsets/groupings

----
#### Saturday, May 19, 2018 (Total: 2 hours)
----
- practiced presentation and edited slides

### Weekly hours: 26

----
#### Sunday, May 20, 2018 (Total: 2 hours)
----
- practiced presentation and revised slides

----
#### Tuesday, May 22, 2018 (Total: 7 hours)
----
*9:30 am - 11:00 am*
- Presented slides to Ben and Dan and received feedback
- Revised slides (objectives, OTU and ASV approach in detail, methods, and expected results)
- Annotated slides and e-mailed presentation to Dr. Gloor

*11:00 am - 11:30 am*
- Resumed CoDaSeq: Part 2: ALDEx2 for Differential Expression Analysis

*12:15 pm - 5:00 pm*
- Got stuck on aldex.clr line of code
  - ERROR: mismatch between number of samples and condition vector
  - The 'grps' list is not ordered according to the dd.clr rows
    - Resolution:
      - used df vector and transposed to have samples = rows ('df.t')
  - ERROR: undefined columns selected
    - Resolution:
      - must order dd.czm by groups where each group = 1 col
      ** have yet to figure out the code to perform this
- Took notes answering the questions on the CoDa workflow Part 2 (see CoDa Methods Summary)
- Reread "Exact sequence variants should replace operational taxonomic units in marker-gene data analysis"
to review OTUs vs ASVs
- Practiced presentation

----
#### Wednesday, May 23, 2018 (Total: 9.5 hours )
----
*9:30 am - 4:00 pm*
- continued search for a way to sort data frame by metadata for CoDa Part 2:
  - referenced [mmaklai Github] (https://github.com/mmacklai/example-scripts/blob/master/aldex2/aldex2example.R)
- Since aldex.ttest only supports 2 conditions and my dataset contains 4 (controls, untreated, copaxone, interferon),
I modified the code to filter the data and perform the tests/functions on all possible pairs:
  1. control - untreated ('cvu')
  2. control - copaxone ('cvcop')
  3. control - interferon ('cvint')
  4. untreated - copaxone ('uvcop')
  5. untreated - interferon ('uvint')
  6. copaxone - interferon ('copvint')

- completed CoDa Part 2: ALDEx workflow - results exported to "~/Summer 4483E/Test Dataset/CoDa-Output/Part 2 - ALDEx"
- practiced presentation to an audience and received feedback
- received Latex tutorial in preparation for writing up my background, objectives and methods
- revised presentation to include corrections:
  - added page numbers
  - added citations
  - added overview slide
  - corrected errors in text
  - added supplementary slides on Illumina protocol and gut-brain axis to prepare for answering questions
- read [From reads to operational taxonomic units: an ensemble processing pipeline for MiSeq amplicon sequencing data](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5466709/)
and added notes on error rates to Background.
- showed slides to Jean and Dan and incorporated edits:
  - changed sequencing errors to include environmental contaminants and software processing errors
  - changed shapes to nucleotides
  - changed order of datasets and methods to introduce controls first
  - removed gut-brain axis slide

- e-mailed Dr. Gloor updated slideshow

*6:30 pm - 9:30 pm*
- edited powerpoint and script and practiced presenting

----
#### Thursday, May 24, 2018 (Total: 2 hours)
----
*9:45 am - 12:00 pm*
- presented powerpoint to lab group and made edits:
  - slide: "Introduced Error"
    - emphasize the magnitude of error introduced by PCR
  - slide: "Processing and Analyzing Reads"
    - discuss the issue of including sequences from other species into a cluster (leads to misassignment)
  - added new slide to tie project together
    - "How is profiling the gut microbiome of MS patients informative?"

*2:45 pm - 4:45 pm*
Presentations

----
#### Friday, May 25, 2018  (Total: 2 hours)
----
*9:30 am - 12:00 pm*
- read [Compositional analysis: a valid approach to analyze microbiome high-throughput sequencing data](http://www.nrcresearchpress.com/doi/pdf/10.1139/cjm-2015-0821)
- downloaded LaTeX
- completed pairwise comparison for
  1. untreated - copaxone ('uvcop')
  2. untreated - interferon ('uvint')
  3. copaxone - interferon ('copvint')
- exported pdfs to /Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/CoDa-Output/Part 2 - ALDEx

##### Results:
-ALDEx Plots: Log2(condition difference) versus Log2(relative abundance)
  - all grey dots with the exception of controls_copaxone.pdf, which shows 2 red dots

- Within/Between plots:
  - small scale differences between samples and more variation within (relative to between)
  - clusters around zero on y-axis (between samples)

- Questions about results:
  - what do the ablines represent?
    - line of equivalence
  - what do the red dots represent in the controls_copaxone.pdf showing an ALDEx plot
  - is the significance level (0.05) too large?
  - what are monte carlo instances?


### Weekly hours: 22.5

----
#### Monday, May 29, 2018 (Total: 7 hours)
----
*9:00 am - 11:30 am*
Lab meeting at St. Joseph's Hospital

*12:00 pm - 4:30 pm*
- interpreted results for pairwise t-tests

Within/Between Plots:

cvu               | cvcop               | cvint              | uvcop             | uvint            | copvint
----------------- |-------------------- |------------------- |------------------ |----------------- |---------------
poor separation  | poor separation      | poor separation     | poor separation  | poor separation  | poor separation
no sig. outliers    | 2 red dots indicating greater than significance level   | no sig. outliers   | no sig. outliers | no sig. outliers |no sig. outliers


Overall no differences between samples

Possible explanations for differences in analysis compared to published article:
- published article performed pairwise tests between specific phyla and genera whereas I compared pairwise tests on an entire population

- More questions about results:
  - what does the blue dot represent in the controls_copaxone btw-win.pdf represent?
    - nothing... plot using aldex.plot instead of plot function

- Looked at SVs that were removed by filtering by checking rowSum == 0
- Noted which samples were removed in each subset by comparing SVs included in the controls and untreated group (aldex.cvu)
to those excluded by the copaxone and interferon groups (copvint)
  > Results:
    - 98 SVs listed in 'common1' variable indicating SVs present in the treated subsets that were removed from the untreated and controls
    - 458 SVs listed in 'common2' variable indicating SVs present in the control/untreated subsets that were removed from the treated subsets.

  Discussion:
    - *These results indicate the presence of a different SV composition in treated individuals compared to untreated/controls;
    however, the control SVs should be contrasted to those found in the untreated MS patients.

- Constructed chart to compare and contrast methods of processing reads and performing differential analysis:

Method component | my methods | methods in publication
-----------------|------------|------------------------
Processing reads |        |
data transformation |  |
multiple test correction ||
test type | welches/wilcoxon rank-sum |

----
#### Tuesday, May 30, 2018 (Total: 6.5 hours)
----
*9:30 am - 12:00 pm*

- reviewed how reads were filtered (dd.czm and dd.clr have different applied functions)

dd <- data.frame(dd[which(apply(dd, 1, function(x){sum(x)}) > ncol(dd)), ], check.names=F)
  - this removes SVs with too many zeros?
    - ( rms SVs with less counts across samples than there are samples?)
    - the number '1' indicates filtering is done by row (therefore by features)

- compared the SVs that were:
    1. removed in control subset but included in untreated MS ('common3')
    2. removed in untreated subset but included in controls ('common4')
    3. removed in control subset but included in treated MS ('common5')
    4. removed in treated MS subset but included in controls ('common6')

> Results:
  1. 287 SVs
  2. 383 SVs
  3. 287 SVs
  4. 458 SVs

  *Note:*
  Total number of samples and SVs (samples, SVs) in each subset after filtering:
    - controls = 44, 1281
    - untreated = 29, 1281
    - treated = 32, 1281
      - copaxone = 15, interferon = 17

    Total number of samples and SVs in each subset BEFORE filtering:
    - controls = 44, 2263
    - untreated = 29, 2263
    - treated = 32, 2263
      - copaxone = 15, interferon = 17

- Labeled the common SVs that were removed/included in subsets in cvu effect plot
  - on effect plot: added text representing the SVs present in untreated but filtered out of controls (in blue text) as well as those present in controls but filtered out of untreated (red text)
  - result = no SVs were positively significant (none were greater than the mean of the samples) and the resulting plot with labels on all common SVs was not informative
  ![CVU effect plot with all common SVs labeled](/Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/CoDa-Output/Part 2 - ALDEx/with text-control_untreated btw-win.pdf)
  ![CVU effect plot with common positive significant labels](/Users/kt/Documents/Documents/Undergrad/4/Summer 4483E/Test Dataset/CoDa-Output/Part 2 - ALDEx/with sig points - control_untreated btw-win.pdf)

*12:45 pm - 4:00 pm*
- Computer froze for 45 minutes leading to forced restart
- Worked on generating strip charts for taxonomic level comparisons following github workflow (https://github.com/ggloor/CoDa_microbiome_tutorial/wiki/Part-4:-Visual-Data-Exploration)
  - stuck on generating xlimits
    - "Error in .subset(x, j) : only 0's may be mixed with negative subscripts"
    - need to generate a second table from dada2 counts table to separate the taxonomic classes
- completed 'compare and contrast chart' for my methods and published methods:

Method component | My methods | Methods in publication
-----------------|------------|------------------------
Processing reads | ASV       | OTU
data transformation | clr | unifrac for overall community differences, DESeq2 for individual taxa -[no transformation](http://bioconductor.org/packages/devel/bioc/vignettes/DESeq2/inst/doc/DESeq2.html#why-un-normalized-counts)
multiple test correction | Benjamini-Hochberg 0.1 | Benjamini-Hochberg 0.1
test type | welches/wilcoxon rank-sum | Wilcoxon rank-sum or Walds?!

----
#### Wednesday, May 30, 2018 (Total: 3.5 hours)
----
*9:45 am -  12:00 pm*

- created separate table for taxonomy labels from dada2_nochim_tax using str_split_fixed function in R
- unsuccessfully attempted to filter dataset by genus name and transform filtered SVs for biplots

*4:30 pm - 6:00 pm*
- successfully filtered sequence variants to those corresponding to Akkermansia or Methanobrevibacter genera and generated aldex plots and biplots
- Issues:
  1. biplot colours representing subsets are not displayed
  2. SV numbers generated using the grep function do not correspond to those in the dada2_nochim_tax table assigned Akkermansia or Methanobrevibacter genera
- attempted to download processed reads from [EBI](https://www.ebi.ac.uk/ena/browse/sequence-download) but could not login to [FTP server](ftp://ftp.ebi.ac.uk/pub/databases/ena/sequence)
using khobbs3 user and password

----
#### Thursday, May 31, 2018 (Total: 7 hours)
----
*10:15 am - 5:00 pm *
- Solved issues in generating biplots and filtering data (review code used to achieve this)
  - modified filter code in CoDa Part 1 to remove internal loop and generate new dataframe ('ddf')
  - re-ran ALDEx2 code using 'ddf' instead of 'dd' to ensure consistency in output
  - cut and pasted tax col to rownames so that filtering in CoDa part 1 and removal of zeros by ALDEx clr transformation still corresponded with taxonomic assignments of rows
- Unsuccessful attempts at generating effect tables for Akkermansia SVs in controls, untreated, copaxone, and interferon-treated individuals
- Generated individual tables for
  - control and untreated ('cvu'),
  - control and copaxone treated patients ('cvcop') and,
  - control and interferon treated patients ('cvint')
 where SVs were classified as Akkermansia or Methanobrevibacter. Tables include SVs and their corresponding effect size ('Akk-effects-X.txt' and 'Methanobrevibacter-effects-X.txt' where X = subsets used).
- Started Thesis Intro Outline

Total number of SVs left after filtering and removing zeros:
  - 1179


----
### Friday, June 1, 2018 (Total: 1 hour)
----
* 2:20 pm - 3:20 pm*
- completed tables for Butyricimonas and renamed rownames to reflect SV numbers
- searched for any SVs with 1 < effect size < -1
  - Result: none exist

### Weekly hours: 25

----
### Monday, June 4, 2018  (Total: 6.5 hours)
----
*9:30 am - 4:00 pm*
- worked with ben's rho analysis workflow on MS study
  - Result: using a rho value of 0.7 and 0.6 no mean differences in clrs were detected
    - using a rho value of 0.5 detected 6 SV pairs; however, no clr mean differences were significant (>|2|)

- downloaded processed reads from publication (counts data) from EBI ("Analysis summary") and generated screeplot as well as coloured biplot for output
    - controlled for differences in data transformation by performing clr transformation on mothur output
**Results:**
    - still small PC1 and PC2 values for mothur output (0.1 and 0.073, respectively)
    - lots of overlap between subgroups in biplot
    - presence of uncoloured points in biplot - does this mean there are extra samples that were not subsetted?
      - yes, 105 samples that had SVs generated from 454 sequencing were removed so that only Illumina-generated SVs remained

- repeated rho analysis of mothur output:
**Results:**
    - rho value of 0.7 generated 18 OTU pairs
      - clr differences range from +/- 0.6 to +/- 4.5, indicating presence of technical errors
      - no tax assignments of technical errors corresponded to those with claimed significant difference by published article;
      therefore, false positive assignments by articles are not due to technical sequencing error. Since data transformation was controlled for in the rho analysis of mothur output, the absence of transforming data by Jangi et al
      may have caused the misinterpretation.
      - does table have to be transformed for propr analysis? If not - can validate by performing rho analysis on non-transformed mothur output.

- repeated rho analysis removing 454 samples:
**Results:**
  - rho value of 0.7 generated 17 OTU pairs with maximum clr difference of 6.6

- began writing introduction and background for 4483E submission


----
#### Wednesday, June 6, 2018 (Total: 5.5 hours)
----
*10:30 am - 12:30 pm*
- Unsuccessful attempt at generating strip charts for MS dataset
   - group table must be comprised of only two subsets to have the same number of rows as the aldex.out table; however, the subsetted groups are by sample names and the group table contains SV names instead.
- Watched tutorials and set up latex and texmaker
- Continued writing introduction and backgrounds

*1:30 pm - 4:00 pm *
- read and annotated articles:
  - *Wrinkles in the rare biosphere: pyrosequencing errors can lead to artificial inflation of diversity estimates*
  - *Rapid and comprehensive identification of prokaryotic organisms by metagenomic analysis. U.S. Pat. No. 8,532,934.*
  - *Microbiome Profiling by Illumina Sequencing of Combinatorial Sequence-Tagged PCR Products*

----
#### Thursday, June 7, 2018 (Total: 4 hours)
----
*10:30 am - 2:30 pm*
- Continued writing introduction

----
#### Friday, June 8, 2018 (Total: 5 hours)
----
*10:30 am - 3:30 pm*
- Read:
  - Schloss, P. D. (2010). The effects of alignment quality, distance calculation method, sequence filtering, and region on the analysis of 16S rRNA gene-based studies. PLoS computational biology, 6(7), e1000844.
  - Hansen KD, Wu Z, Irizarry RA, Leek JT (2011) Sequencing technology does not eliminate biological variability. Nat Biotechnol 29(7):572–573.
- Began formatting thesis introduction, backgrounds, methods, and hypothesis in TexMaker
- read aldex2 propr rho [github](https://github.com/cran/propr/blob/master/R/aldex2propr.R)

> propr
ALDEx2 adds 0.5 to all counts. Otherwise logratio = transformed counts as averaged across monte carlo instances.
Matrix = proportionality as averaged across Monte Carlo instances


### Weekly hours: 21

----
### Monday, June 11, 2018 (Total: 4 hours)
----
*10:00 am - 11:30 am*
- continued writing and editing Introduction
  - To add:
     - a brief description on the sequencing data type (compositional) and how sequencing influences this

*1:00 pm - 3:30 pm*
- read pages 1-23, 53 of *Compositional analysis of high throughput sequencing data (Gloor, 2018)*
- added references to EndNote and attempted to automate citations in Latex.

----
#### Tuesday, June 12, 2018 (Total 4 hours)
----
*10:30 am - 2:30 pm*
- formatted latex thesis document to include references and figures.
- reviewed readings
- sent rough draft to Dr. Gloor

----
#### Wednesday, June 13, 2018 (Total: 2 hours)
----
*12:00 am - 2:00 pm*
- edited thesis writing

----
#### Friday, June 15, 2018 (Total: 1 hour)
----
- made corrections for thesis write up and fixed latex citations and pdf output

### Weekly hours: 11

----
#### Wednesday, June 20, 2018 (Total: 7 hours)
----
*10:00 am - 5:00 pm*
- reread [Synthetic spike-in standards for high-throughput 16S rRNA amplicon sequencing](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5389483/#sup1)
- identified samples to download:
    - [x] even spike-in mix and even mock DNA (Sample ID: E)
        total = 21 samples

These samples were chosen because they contain consistent concentrations of spike-ins and mock DNA and therefore can serve as both positive and negative control samples.

- downloaded samples:
    - downloaded .csv file project summary from EBI
    - cross-referenced sample name from supplementary data to .csv to identify run accession ID
    - downloaded sample FASTQ FTP by run accession ID from ENA

- began working through dada2 workflow ("~/methods/control_dada2")
  (*computer froze for 2 hours*)
- completed dada2 workflow:
  - quality profiles show some reads are shorter than others with a max length of 200
    - ends of reverse reads are of poorer quality as expected
  - error profiles have relatively good fits to the estimated error line
  - all reads made it through pipeline as shown by readsout.txt
- received error when assigning taxonomy: ">" expected at beginning of line 1, likely indicates improper format of fastQ files; however, the FTP downloads seem to be acceptable.
May need to re-download or save as plain text.

----
#### Thursday, June 21, 2018 (Total: 5.5 hours)
----
*10:00 am - 3:30 pm *
- reran dada2 workflow in R in attempt to correct yesterday's error. Computer froze for two hours.
- discussed project progress with Dr. Gloor:
  - Why might ALDEx output differ from DESeq (assuming there are no differences in dada2 and mothur)?

... | ALDEx | DESeq
-----|-------|------
transformation | clr (log ratio) | linear proportion
dealing w zeros| probability distribution | point estimations
mean abundance/var* | no assumptions | assumes mean < var, subject to shrinkage
  * most influential

  - to better understand why there are differences in results between dada2->ALDEx2 and mothur->DESeq2 protocols the mothur output should be interpreted
  with ALDEx and the dada2 output should be interpreted with DESeq2.

- started following [DESeq2 tutorial](https://bioc.ism.ac.jp/packages/2.14/bioc/vignettes/DESeq2/inst/doc/beginner.pdf) starting from 2.4.2 using the count matrix input from dada2
  - requires additional columns with sample information ("condition" and "type")
  - generated sampleInfo.csv containing two cols: "run" and "condition"
  - imported and split cols in RStudio
  - *note: in workflow se = counts, and seIDx = cts *

----
#### Friday, June 22, 2018 (Total: 6 hours)
----
*10:00 am - 1:00 pm*
*Bcc summer seminars:*
  - transition from academia to industry
  - concise writing with Dr. Brandl

*1:00 pm - 4:00 pm*
- continued on running dada2 output through DESeq2
  - slow step in lines:
      >pkgs <- rownames(installed.packages())
      biocLite(pkgs, type="source")
  - got stuck on:
    > head( cbind( colData(counts)[ , 1:3 ], sampleInfo[ cts, ] ) )
    - class of 'counts' is not accepted (SummarizedExperiment)
    - possibly because count table uploaded in .csv format appears as one col?

- moved on to analyze mothur --> ALDEx2 [x]
Results:
  - effect plots do not show any SVs that are different


### Weekly hours: 18.5

----
#### Monday, June 25, 2018 (Total: 6 hours)
----
*10:00 am - 3:15 pm*
- [x] ran dada2 --> DESeq2
  - did not need code from previous day, instead followed 2.4.3 and 3.2 from [Beginner's guide to using the DESeq2 package](https://bioc.ism.ac.jp/packages/2.14/bioc/vignettes/DESeq2/inst/doc/beginner.pdf)
  - accurately generated colData ('sampleInfo2') with rownames and dim = colnames and dim of counts matrix
  - generated SummarizedExperiment table
  - ran DESeq2 pipeline contrasted controls and untreated individuals
  - exported tables with taxonomic assignments as extra cols
- [x] gathered and began interpreting DESeq2 results for dada2 output
  - added general guidelines for interpreting DESeq2 results to "Interpreting Results" file
  - found the number of significant results for each comparison before and after the benj-hoch adjustment
      adjustment|cvu | cvcop | cvint
      ----------|----|-------|------
      before | 26 | 50 | 36
      after | 20 | 48 | 32

  - generated plots
    - MA:
      - plots look VERY different from those generated by ALDEx2...
      DESeq2 | ALDEx2
      -------|-------
      red points at y lims, no clustering, dispersion as x -> 1e03 | points cluster around zero, disperse as x -> lim
    xlim: (1e-03, 1e03)  | xlim: (0, 12)
    ylim: (-1, 1)  | ylim: (-3, 3)
      - smaller range of log-fold change in DESeq2 than ALDEx2 although points still appear significant
      - larger range of means for DESeq2 results suggest greater variation within data subsets(?)

    - Dispersion:
      - no observable dispersion outliers, all points appear to have been fitted to the mean-dispersion fit
      and none exist outside of the "cloud"

  - generated lists of SVs deemed significant by DESEq2 and their assigned taxonomies from dada2
    - [] to contrast dada2 SVs to those found by mothur and to reproduce the published results, I began to run mothur with DESeq2
      - *side note:* mothur found 704 SVs for 210 samples whereas dada2 found 2263 for 105 samples
      - stopped at generating tables

*3:15 pm - 4:00 pm*
    - tested out Ben's R package ['filtR'](https://github.com/bjoris33/filtR/blob/master/R/filtR_function.R)
    RESULTS:
      dada2 output:
        - rho = 0.5, clr cutoff = 5
          - no results generated in 'final5' table (no technical errors)
            > some OTU pairs in 'final1' table (after filtering by rho but before filtering by clr) indicates that some OTU's associate with each other but are not likely to be technical errors (could be result of natural variation)
        - rho = 0.5, clr cutoff = 4
          - no results for 'final5' but some for 'final1'

      mothur output:
        - rho = 0.7, clr cutoff = 5
          - no result generated with clr cutoff of 5
        - rho = 0.7, clr cutoff = 4
          - 8 OTU pairs with clr differences up to +\- 5 indicating presence of technical errors
        - rho = 0.5, clr cutoff = 4
          - 288 OTU pairs with clr differences up to +\- 5 indicating presence of technical errors

    - updated dada2proprworkflow.R so that output is readable (used 'write.table' insteald of 'pdf()')

----
#### Tuesday, June 26, 2018 (Total: 7 hours)
----
* 9:45 am - 5:00 pm*
- [x] update mothurproprworkflow.R so that output is readable (use 'write.table' instead of 'pdf()') ** be mindful of which cols are being removed (tax = rownames)
    - redownloaded .tsv file from EBI and cut out tax col
- [x] ran filtR on mothur output
    - rho value was kept at default (0.7) but clr cutoff was changed to 3 as 5 was too stringent and produced no results
- [x] since no results were generated from filtR for dada2 using rho = 0.5 and clr cutoff = 5, the workflow was repeated with rho = 0.5 and clr cutoff = 3
    - still no results generated with new clr cutoff
- [x] began compiling results for future reference and interpretation and added filtR background to 'Interpreting Results' file
- [x] ran mothur --> DESeq2
    - found the number of significant results for each comparison before and after the benj-hoch adjustment
        adjustment|cvu | cvcop | cvint
        ----------|----|-------|------
          before | 14 | 8 | 26
          after | 3 | 0 | 19

    - DESeq2 MA plots for mothur:
        - cvint/cvcop: similar shape to dada2, different centre (not centered around zero) and more dense
        - cvu: different shape, high density at ylim = 1
        - both dada2 and mothur have log2fold changes that range from (-1, 1)

    - Created volcano plots for both dada2 and mothur output and added guidelines for interpreting results to 'Interpreting Results'
      mothur:
        - two significant variants: disulphobrivios and pseudomonas

      dada2:
        - many significant variants

    - MA plots don't look normal - could be consequence of method of normalizing data...

----
#### Wednesday, June 27, 2018 (Total: 7 hours)
----
* 10:00 am - 4:30 pm *
- attempted to deduce why the DESeq2-generated MA plots look irregular
  - tried dropping levels of ddsFullCountTable$condition before running pipeline - *plots still irregular*
  - watch [StatQuest tutorial on DESeq2 library normalization](https://www.youtube.com/watch?v=UFB993xufUU)
    - average of log values is not easily swayed by outliers
    - log averages = 'geometric averages'
    - normalization
        1. log2
        2. average each row
        3. filter out genes with infinity (for differential expression analysis) to remove house keeping genes with infinity expression levels
        4. subtract avg log from log(counts) = log(counts) - average log for a gene = log(reads for gene X/average for gene X)
              - used to find genes that are higher, lower, or equal to the average
        5. calculation median of ratios for each sample
              - to avoid influence of outliers or genes with large differences in abundance
              - genes with large differences will be rare; therefore, any effect observed is likely due to small changes
        6. convert medians to "normal numbers" to get final scaling factors for each sample
              - raise log base ^ median value (e.g. 2^med)
        7. divide original read counts by scaling factors
              - can be scaled up or down (?)
  - filtered genes with counts that are less than 5 - *plots still irregular*
        **Note:** this is a different filtering method than ALDEx2
      >  se <- se[ rowSums(assay(se)) >= 5, ]

      The normalization applied by DESeq2 is unsuitable for the inputted datasets (both mothur and dada2 derived count tables) and the published article by Jiang et al did not disclose the parameters used to obtain their results.
      Additionally, the normalization step is incorporated into the 'DESeq' function making manipulation complicated and suggests a likelihood that the researchers used the default parameters.
      As a result, no further attempts to normalize the data will be pursued and instead I will create a phylogenetic tree using pplacer then run and contrast results from Unifrac's PCoA plots used by Jiang et al to CoDa's biplots.
      Note: researchers wrote that they used custom R scripts for Unifrac but did not include them in their publication.

- must make tree before running Unifrac. pplacer was used by researchers but this requires a reference package to reference a tree, alignments, and taxonomic information, which is unnamed.
- unsuccessfully attempted pplacer. Instead, I will run mothur using the raw reads in order to obtain all files that are generated by mothur (including a tree) and then run Unifrac weighted and unweighted analysis.
    - caveat: no straight-forward alternative methods for dada2 output for a parallel analysis.

- [] mothur pipeline (in terminal):
    - downloaded [mothur](https://github.com/mothur/mothur/releases)
    - since mothur does not read paths where folder names have white spaces, folders were renamed:
        - summer 4483E --> 4483E
        - 16S rRNA Reads --> miseq
        - Test Dataset --> test
    - processing reads is a lengthy step (~105 minutes)
        - It took 658 secs to screen 11498168 sequences, removed 4877029.

- [x] updated methods to reflect changes in pathnames
- [x] reran ben's filtR script with bug fixes and updated results

*7:30 pm - 8:00 pm*
- summary:

Start |	End |	NBases |	Ambigs |	Polymer |	NumSeqs
------|-----|--------|---------|----------|--------
Minimum: |	1 |	151 |	151	| 0	 | 3	| 1
2.5%-tile:	| 1 |	252 |	252 |	0 |	4 |	165529
25%-tile: |	1 |	253	| 253 |	0 |	4	| 1655285
Median: |	1 |	253 |	253	| 0 |	4 |	3310570
75%-tile: |	1 |	253 |	253 |	0	| 5	| 4965855
97.5%-tile: |	1	| 253 |	253 |	0 |	5 |	6455611
Maximum: |	1 |	275 |	275 |	0 |	151 |	6621139
Mean:	| 1 |	252 |	252 |	0 |	4

# of unique seqs:	1468617
total # of seqs:	6621139

----
#### Thursday, June 28, 2018 (Total: 1.5 hours)
----
* 4:00 pm - 5:30 pm *
- [] mothur pipeline (in terminal):
  - [] download [arp](http://bugs.arb-home.de/wiki/ArbOSX)
  - [x] downloaded Silva ref database [NR99](https://www.arb-silva.de/download/arb-files/)
      If you are using SILVA please cite:
      Quast C, Pruesse E, Yilmaz P, Gerken J, Schweer T, Yarza P, Peplies J,
      Glockner FO (2013) The SILVA ribosomal RNA gene database project: improved
      data processing and web-based tools. Nucleic Acids Research 41:D590-D596

      Yilmaz P, Parfrey LW, Yarza P, Gerken J, Pruesse E, Quast C, Schweer T,
      Peplies J, Ludwig W, Glockner FO (2014) The SILVA and "All-species Living
      Tree Project (LTP)" taxonomic frameworks. Nucleic Acid Res. 42:D643-D648


- [] Unifrac weighted -> AMOVA
- [] Unifrac unweighted -> AMOVA
- [] PCoA plots

----
#### Friday, June 29, 2018 (Total: 3 hours)
----
* 9:30 am - 12:00 pm *
- in order to download Arb, a certain amount of RAM is required...
- [] repeat DESeq analysis using Wilcoxon rank sum test
    - 'DESeq' function only runs Wald's or likelihood ratio test (LRT) but not Wilcoxon rank sum... Jiang et al must have performed separate Wilcoxon analysis
- [x] transferred control files (even spikes and mock communities) to agrajag via finder (control + K)
    - ~ 30 min to transfer
- [] began running dada2 on control set through terminal
    - paused at referencing Silva for taxonomy

* 8:00 pm - 9:00 pm *
- [x] completed dada2 for control dataset and transferred files to KT's Macbook
    RESULTS:
      - err profiles: C2G appears error prone (deviates from trendline) but the remaining transitions/transversions appear to occur as expected


### Weekly hours: 24.5

----
#### Tuesday, July 3, 2018 (Total: 7 hours)
----
* 9:30 am - 4:30 pm*
- [x] reviewed positive control results:
  - quality scores:
    - reads are ~ 250 bp in length
    - forward: consistent q score between 30-40
    - reverse: consistent q score between 30-40 for 150 bp then q dips to ~25 afterwards
  - tax results:
          ... | dada2 | QIIME --> USEARCH
          ----|-------|-------
        No. Samples | 24 | 24
        No. SVs (before rmving 0s) | 988 | 2038
        No. SVs (after)  | 988 | 286
        Ref DB | Silva | UCHIME pipeline -> Broad Microbiome Utilities’ 16S Gold

  > **NOTE: the positive control contains spike-in standards. 0 count SVs were removed from QIIME output in 'control_filtered.R'
  by removing rows where sum of counts == 0 in order to only include SVs that correspond to the 24 samples used **
    ** to eliminate biases, QIIME pipeline could be repeated with referencing Silva DB **

- [] to reference Silva DB through agrajag, the silva_nr_v123_train_set.fa.gz file was transfered from agrajag to KT's Macbook (direct reference from mothur via agrajag was denied permission)
  - error: requires start and end of sequences against ref db (see summary.seqs)
      - [solution:](https://github.com/mothur/mothur/issues/235)
        1. download e.coli fasta from https://www.ncbi.nlm.nih.gov/nuccore/174375?report=fasta
        and pcrTest.oligos from https://www.mothur.org/wiki/Oligos_File
        2. mothur > pcr.seqs(fasta=ecoli.16srrna.fasta, oligos=pcrTest.oligos)
        3. mothur > align.seqs(fasta=ecoli.16srrna.pcr.fasta, reference=silva.bacteria.fasta)
        4. mothur > summary.seqs(fasta=ecoli.16srrna.pcr.align)
  - disrupted file outputs from previous run lead to restarting mothur pipeline**

- [x] Ran filtR on control dada2 count table
      - Results:
      
        rho CO | clr CO | dada2 result
        -------|--------|-------------
        0.7    | 5      | clr too high (NA)
        0.7    | 4      | clr too high (NA)
        0.7    | 3      | clr too high (NA)
        0.7    | 2      | clr too high (NA)
        0.5    | 1      | clr too high (NA)
        0.3    | 1      | clr too high (NA)

- [x] ran filtR on control QIIME count table
    - Results:
    
      rho CO | clr CO | QIIME result
      -------|--------|-------------
      0.7    | 5      | clr too high (NA)
      0.7    | 4      | clr too high (NA)
      0.7    | 3      | clr too high (NA)
      0.7    | 2      | clr too high (NA)
      0.7    | 1      | clr too high (NA)
      0.5    | 1      | clr too high (NA)
      0.3    | 1      | clr too high (NA)

> Possible conclusions:
  - Since both QIIME and dada2 count tables did not generate technical errors (according to filtR), it is possible that dada2 found more SVs than QIIME due to its higher resolution.
  - The additional SVs may represent biological variation that was falsely clustered using the OTU based approach to processing reads employed by QIIME.

- mothur output files still could not be opened after second run... reran mothur from beginning and changed output directory to ~/test/mothur/mothur-output
- stuck at referencing silva db - how do I ensure primers are aligned to db? start and end from summary.seq() do not align.
    - changed start and end to match the minimum start/end from summary.seq() and got the same result

----
### Wednesday, July 4, 2018 (Total: 6 hours)
----
*10:30 am - 4:30 pm *
- [x] summarized count tables for test dada2 and mothur
- computer froze for 1.5 hours, then I backed it up on a hard drive
-  primers used: V4 region for Illumina MiSeq
- caveats in pursuing mothur analysis:
  - Jiang et al used custom python scripts to filter
  - exact primer sequences used are unknown
  - Silva reference db file may be different
- discussed problem of aligning V4 region of primers to E. coli with Dr. Gloor...
> conclusions:
  - since the exact mothur SOP modified and used by Jiang et al is unknown, it is improbable that the exact count table will be reproduced.
  Additionally, deviations in the processed results will accumulate in downstream analysis, generating vastly different and incomparable results.
  Consequently, the attempts to reproduce the paper's results will be aborted.

----
### Friday, July 6, 2018 (Total: 6 hours)
----
* 9:30 am - 1:30 pm *
- [x] wrote up conclusions about test results
- [x] created powerpoint for next lab meeting ("Khobbs - Jul 9")
    - summarized positive control results
    - summarized filtR results
    - contrasted DESeq2 and ALDEx2 MA plots
    - contrasted protocol between myself and the MS article
- [x] ran filtR for mothur with rho CO = 0.5 and clr CO = 3 so that conditions are the same for both dada2 and mothur interpretations
- [] looked for a way to isolate spike in standards for negative control testing
  - according to the supplmentary data, all available samples that include the spike-in standards also include a bacterial community
  - count from positive control has many NA's introduced... these may be the spike-ins but unsure of how to confirm..
    - reference sv_seqs.txt to sequences of the SVs generated from article (if possible)

* 3:00 pm - 5:00 pm *
- searched for sequences of sequence variants from published article and began trying to isolate all the SVs with NA for taxonomy using R.

----
### Saturday, July 7, 2018 (Total: 1 hour)
----
*1:00 - 2:00 pm*
- finished up powerpoint presentation for lab meeting


### Weekly hours: 20

----
### Sunday, July 8, 2018 (Total: 2 hours )
----
* 11:30 am - 1:30 pm *
- wrote a summary to explain PCA biplot results for dada2 and mothur and added to powerpoint presentation, 'Compiled Results', and 'Interpreting Results'
- edited powerpoint
    - removed effect plots in effort to save time and simplify presentation
    - added script
    - referenced Ben's filtR and added more filtR results
- rehrearsed presentation

----
#### Monday, July 9, 2018 (Total: 7 hours)
----
*9:00 am - 12:00 pm*
Lab meeting

*12:00 pm - 4:00 pm*
- [x] continued working in R to identify and count the number of spike-ins
- [x] summarized control results
  - spike-ins are identified by a taxonomic classification "NA:NA..." in 'dada2_nochim_tax.txt'
    > Note: there are also numerous taxonomic assignments of "Bacteria:NA:NA:NA:NA:NA" - could these also be spike ins?

  dada2 results:
  
... | "Bacteria:NA:NA:NA:NA:NA" | "NA:NA..."
----|---------------------------|----------
 No. of SVs| 187 | 66

  Total SVs for dada2 control set: 988


  QIIME results:
    - for the QIIME sample set ('control_24_samples_tax') the col containing taxonomic assignments was renamed "tax.vector"
    - must identify how QIIME labels reads without tax assignment
      - all SVs have some classification... why?
  Total SVs for mothur control set: 1752

- discovered that the supplementary information pdf includes the spike-in sequences. These will be cross-referenced to 'sv_seqs.txt' to identify the spike-ins and ensure there was no false classifications.
  - [x] all 12 spike-in sequences were downloaded from GenBank in fasta format using accession numbers listed in Supplementary Table S1. (all 12 are included in the mixed samples)
      - file path <- "/Users/kt/Documents/Documents/Undergrad/4/4483E/control/spike-in_seqs"
  - sv_seqs.txt was modified such that the second column was named 'sequence' and the first was left unnamed (so the first column would become the row names when imported into R)
  - [x] compiled the 12 sequences into one variable and merged with sv_seq.txt
  - [] cross referenced dada2 output to sequences of spikes using 'merge' function
    - result: no common sequences... saved table of compiled sequences and opened in excel to see the column names are offset. Changed in excel, imported new table and ran 'merge' function again to achieve results.
    - still no common sequences...
        - *Possible explanation could be that dada2 filter out the spike-in sequences since they had a low abundance. This principle could
        also justify why QIIME had successfully assigned taxonomies to all OTUs.*
        - to find out if dada2 removed the spike-in sequences, a table should be generated after fwd and rvs reads are sorted (before filtering).
         R is not running on agrajag today so this task will be performed tomorrow.
- supplementary information also states that 'centroid' sequences were referenced to Greengenes database (release 13_5)

----
#### Tuesday, July 10, 2018 (Total: 5.5 hours)
----
*9:45 am - 3:15 pm*
- reran script for negative control
  - no results. if both dada2 and QIIME removed synthetic variable sequences then how did the researchers use them as spike-in standards?
- read about [R loops](https://nicercode.github.io/guides/repeating-things/) to simplify negative control script
- ran dada2 via agrajag to try to create table with sequences before filtering
    - tried using 'getSequence' dada2 function for 'fnF', 'filtF' and 'out' variables but it returns sample names only
    - using control+F to find a synthetic variable sequence in sv_seq.txt (opened in excel) returns no matches
- continued working on simplifying negative control code with loops as a new .R script called 'control-negative.R'
    - importing multiple files adapted from [Johannes Schielein](https://blogazonia.wordpress.com/2014/05/08/import-multiple-files-to-r/)
    - tried to concatenate the sequence using 'unite_' or 'paste' and was unsuccessful
- updated spikes_seq.txt table to include proper labels
- backed up computer and pushed github updates

End of day summary:
  - Unsuccessful attempts to confirm that the synthetic variable regions were filtered by dada2. This hypothesis is left unconfirmed.
  - Both dada2 and QIIME count tables do not include the synthetic variable regions possibly because they are filtered out due to
      - low abundances (most likely)
      - errors? (unlikely)
      - dada2 could have identified them as potential technical errors

----
#### Wednesday, July 11, 2018 (Total: 6 hours)
----
*10:00 am - 4:00 pm*
- [x] attempted to generate table of sequences before filtering again for dada2 by changing the class of input for 'getSequences' function
    - class must be "derep-class" or "dada-class" which both require a list with specific entities. class may also be a dataframe with $abundance and $sequence columns which are not included in 'fnFs'
'fnRs', 'filtFs', or 'filtRs'.
- [x] continued learning how to include loops in order to simplify 'control-identifyingSpikeIns.R' script (in new file: 'control-negative.R')
  - Ben wrote a nested for-loop to concatenate the sequences
- [x] wrote a blurb for the Gloor lab website and e-mailed to Dan
- [x] select scripts from "Methods" folder that were used and copied into folder "4483_methods"
- [x] made a list and rough outline of significant results/discussion/tentative conclusions to include in write up ("write-up_outline")
- [x] read and highlighted Dr. Gloor's "A reproducible effect size is more useful than an irreproducible hypothesis test to analyze high-throughput sequencing datasets"

----
#### Thursday, July 12, 2018 (Total: 5.5 hrs)
----
*10:30 am - 4:00 pm*
- [x] made sure all methods scripts are reproducible and understandable
    - [x] **mothur-biplots.R:**
        - dada2 biplot for mothur-generated count table looks slightly different and PCs are slightly higher but overall same general interpretation (no difference between groups)
    - [x] **mothur-ALDEx.R:**
        - cut out 454 sequencing results (this was NOT done previously or not recorded in script) to verify results
          *located in "repeat" folder*
        - no differences found in plots
    - [x] created "mothur-InterSubsetComparison.R" script to contrast sequence variants between subgroups
      - creates summary tables "svs_b4_and_after_filtering.txt" and "common_SVs.txt"
      - [x] **mothur-DESeq2.R:**
      - changed line of code that removes the 454 sequences to include the first sample (original excluded it)
      - MA plots look slightly different but still significantly abnormal
      - updated plots and tables exported to "/Users/kt/Documents/Documents/Undergrad/4/4483E/test/mothuranalysis/DESeq2/corrected"
    - [x] **filt.R:**
      - mothur: repeated with removing 454 sequences and got no pairs... with added samples also got no pairs. out of curiousity downloaded a new counts table from EBI and repeated to get the same result.
    - [x] **dada2-biplots.R:**
      - repeat biplots are identical to originals
    - [x] **dada2-ALDEx2.R:**
      - repeated plots are identical to originals
    - [x] repeated inter-subset comparisons for dada2 in "dada2-InterSubsetComparison.R"

- [x] cleaned up github
    - new repo "4483"

- [x] updated "Compiled Results"
- [x] started writing results summaries for controls (in notebook) and created to-do list for tomorrow


----
#### Friday, July 13, 2018 (Total: 3 hrs)
----
*11:30 am - 2:30 pm*
[x] controls: write summaries
    - positive
    - negative
[x] attempt to find out whats happening to spike-ins through pipelines
  - ran through "control-negative.R" and corrected errors
  - ran through "control_dada2.R" and attempted to get SV sequences before filtering
      - created "control-negative-b4-filt.R" to summarize steps taken


### Weekly hours: 29

----
#### Monday, July 16, 2018 (Total: 6 hrs)
----
*10:30 am - 4:30 pm *
[x] ran dada2 through agrajag for negative control
  - slow step = naming dereplicated reverse reads
  - time consuming - kept losing connection to R session
  - had to force quit and restart RStudio
  - freezes at "seqtab <- makeSequenceTable(derepF, derepR)" line of code
    - unsuccessfully, changed working directory to exit agrajag since connection to R is lost
    - to improve this protocol a different function should be used to extract sequences since 'makeSequenceTable' is causing time-consuming errors

[x] wrote detailed summaries for results: (see "Compiled Results")
- test:
  - [x] pca Biplots
  - [x] quality profiles
  - [x] effect Plots
  - [x] MA Plots
    - [x] ALDEx2
    - [x] DESeq2
  - [x] filtR
  - [x] DESEq2 tables
    - number of significant OTUs/ASvs for dada2 and mothur generated by DESeq2 (Tables 4A,B)

[x] found more sources discussing read-processing pipelines
- [err profiles:](https://www.ncbi.nlm.nih.gov/pubmed/18660515)
- [quality profiles](https://ieeexplore.ieee.org/xpls/icp.jsp?arnumber=6609580)

----
#### Tuesday, July 17, 2018 (Total: 5.5 hrs)
----
* 9:30 am - 3:00 pm *
[x] fixed code for negative control before filtering
  - separated 'makeSequenceTable' code to make table for forward and reverse reads distinctively generating "dada2_before_filt_fwd.txt" and "dada2_before_filt_rvs.txt"
  - transferred files to "~/4483/control/"
  - results: no spike-in sequences are found in datasets before filtering... why?***
    - for my sanity, I validated the absence of spike-in sequences using ctrl+F in excel
    - confirmed that samples used contain spike-ins by referencing samples used to supplementary information and EBI project summary
    - cannot confirm whether they are present in QIIME table because sequence table is not published on EBI

[x] Expanded "Compiled Results" into full sentences to include in write-up and began interpreting results for conclusions
  > POTENTIAL CONCLUSIONS:
    - it appears as though the discrepancy in the published results lies in the analytical tool DESeq2 as opposed to in the OTU-based mothur pipeline, which, according to filtR, produces no technical variants.
    - dada2 consistently detected more SVs than the OTU-based pipelines used in the test and control with no technical variants. This seems to suggest that dada2's higher resolution permits for a more thorough and robust distinction of true biological variants.
    This also suggests that biological variants are likely to be falsely clustered in OTU generation thus generating results with false negatives.

[x] made list of limitations:
  - caveats in mothur analysis:
    - Jiang et al used custom python scripts to filter
    - exact primer sequences used are unknown
    - Silva reference db file may be different (not disclosed)
  - negative control - what is happening with the spike-ins?
  - processing pipelines are designed to detect true biological variants but there is currently no way to prove or disprove the validity of the claims
  - comparing bacterial names is not ideal as there is so much discrepancy among databases when it comes to assigning taxonomies to sequence variants
      - using the same db can mediate this; however, Jiang et al did not disclose the version of Silva used
  - Jiang et al subgrouped their cohorts further by age, gender, BMI, dietary history and demographics but did not disclose which samples belonged to which subgroup
  - lack of significant difference could be result of low power of study

[x] made list of questions to answer:
  - for the negative control, why weren't the spike-in sequences present in the sequence table before filtering?
  - could clustering of true biological variants (generating FNs) lead to false POSITIVE differences between subgroups?
  - is there a tool to identify basis for true biological variants?
      - consider rho and clr cutoff for filtR and the graphs that may associate with it
          - see chinese elderly paper
  - is there a way to find number of dada2 ASVs before filtering?

[] find number of significantly more and less abundant ASUs using ALDEx2 for dada2 and mothur
    - computer froze for 1 hr

- technical difficulties with R made today slow.

----
#### Wednesday, July 18, 2018 (Total: 4 hrs)
----
* 9:30 am - 1:30 pm *
[x] read Gut microbiota of elderly (gloor) paper

[x] began answering list of questions
* what are other confounding factors to be considered when comparing subgroups? *
- age: diversity of gut microbiota declines with age (Lynch SV, Pedersen O. 2016. The human intestinal microbiome in health and disease. N Engl J Med 375:2369–2379. doi:10.1056/NEJMra1600266)
  - limitations: survivor biases
- gender
- ethnicity
- lifestyle

*could clustering of true biological variants (generating FNs) lead to false POSITIVE differences between subgroups?*
- yes, inclusion of biological variants adds diversity into a cluster thus extending its differentiation
- https://stats.stackexchange.com/questions/15158/precision-and-recall-for-clustering

*is there a tool to identify basis for true biological variants?*
    - consider rho and clr cutoff parameters for filtR and the graphs that may associate with it
    - use filtR updated graph to evaluate discarded sequences

* what are the biological roles of the bacteria found to be different in the published article? *
Genera:
- Akkermansia: some species known to partake in immune modulation and contribute to healthy microbiome in gut (Derrien, M.  et al. Modulation of mucosal immune response, tolerance, and proliferation in mice colonized by the mucin-degrader Akkermansia muciniphila. Front. Microbiol. 2, 166 (2011);van Passel, M. W. J.  et al. The genome of Akkermansia muciniphila, a dedicated intestinal mucin degrader, and its use in exploring intestinal metagenomes. PLoS ONE 6, e16876 (2011).)

- Methanobrevibacter smithii is most abundant (there is another Methanobrevibacter less abundant)
  - have synotrophic relationship with other gut microbiota and are thought to play role in immune response (High prevalence of Methanobrevibacter smithii and Methanosphaera stadtmanae detected in the human gut using an improved DNA detection protocol)
    *NOTE* that most claims for roles in immune response are by studies with focus on autoimmune diseases (IBS, Crohn's) and thus may hold a small scope
  -produce short-chain fatty acids (SCFAs) from carbohydrate, which constitutes about 10% of the host̕ s daily energy  (Microbial ecology of methanogens and methanotrophs)[https://www.sciencedirect.com/science/article/pii/S0065211307960058]

- Butyricimonas: (study)[https://www.nature.com/articles/s41398-017-0031-4.pdf?origin=ppub] shows potential role in gut-brain axis

- Prevotella: known to contain a set of bacterial genes for cellulose and xylan hydrolysis ("Impact of diet in shaping gut microbiota...")[https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2930426/]


[x] found number of significantly more and less abundant ASUs using ALDEx2 we.eBH and wi.eBH for dada2 and mothur (see "Compiled Results" Tables 4C, D, E, F)

[x] added onto list of limitations:
  - caveats in mothur analysis:
    - Jiang et al used custom python scripts to filter
    - exact primer sequences used are unknown
    - Silva reference db file may be different (not disclosed)
  - negative control - what is happening with the spike-ins?
  - processing pipelines are designed to detect true biological variants but there is currently no way to prove or disprove the validity of the claims
  - comparing bacterial names is not ideal as there is so much discrepancy among databases when it comes to assigning taxonomies to sequence variants
      - using the same db can mediate this; however, Jiang et al did not disclose the version of Silva used
  - Jiang et al subgrouped their cohorts further by age, gender, BMI, dietary history and demographics but did not disclose which samples belonged to which subgroup
  - lack of significant difference could be result of low power of study
  - research paper also used 454 roche sequencing, which cannot be analyzed with dada2 and may be the source of discrepancy between my and their results

controls (healthy) | untreated | interferon | glutamirate acetate (copaxone)
-------------------|-----------|------------|-------------------------------
44 | 29 | 18 | 14

  total = 105 samples from 103 individuals

----
#### Thursday, July 19, 2018 (Total: 4 hrs)
----
* 10:30 am - 2:30 pm *

[x] read (Benchmarking of RNA-sequencing analysis workflows using whole- transcriptome RT-qPCR expression data)[https://www.nature.com/articles/s41598-017-01617-3.pdf]
  - should use in discussion as example of similar research pursuits
  - is there a way to do what the paper did to contrast the methods?

[x] continued writing results in full sentences and added list of discussion points for the discussion/conclusion

[x] finished attempting to answer questions:
*could clustering of true biological variants (which generates FNs) lead to false POSITIVE differences between subgroups?*
- https://stats.stackexchange.com/questions/15158/precision-and-recall-for-clustering

*is there a way to find number of dada2 ASVs before filtering?*
- compile files from "control-negative-b4-filt.R"
- reran R script and computer froze

*for the negative control, why weren't the spike-in sequences present in the sequence table before filtering?*
- could there be something wrong with the spike-in sequences downloaded?
    - possible errors when stitching together the sequences in the fasta file

----
#### Friday, July 20, 2018 (Total: 5.5 hrs)
----
* 9:30 am - 12:00 pm*
[x] ran updated filtR and looked at graph to evaluate discarded sequences (slow)
  - test:
    - **dada2:** no plot generated
    - **mothur:** plot shown comparing 1 out of 2 OTU pairs removed
      - saved as "mothur_filtR.pdf" in ~/4483/test/mothuranalysis/
    - talked with Ben about plots made and added plot information to "Interpreting Results"
    - added results to "Compiled Results"

*mothur filtR Results:*
  - rho = 0.7, clr cutoff = 5
    - 4 OTU pairs removed

  plots:
    - 3 out of 4 pairs fit well to either both the linear model + expected results line or the linear model alone
    - 1 pair has, confusingly, lots of dispersion (high residuals) and a high rho value as well as a low clr mean difference
      - the high rho value is whats driving the pair to be filtered although it is unclear what is driving the high rho values
      - possible driver is the intercept of the clr mean difference


  - control:
    - **dada2:** no plots generated
    - **QIIME:** must temporarily remove "tax.vector" column name in excel in order to read table into R with taxonomy as rownames
      - 1 OTU pair removed (contrary to previous results...)
      - save plot as "qiime_filtR.pdf" in ~/4483/control/
      - updated "Compiled Results" (Table 9B.)

*QIIME filtR Results:*

rho CO | clr CO | QIIME result
-------|--------|-------------
0.7    | 5      | 1 pair rmvd
    
**Table 9B.** filtR results for a counts table generated by QIIME.

plot:
- linear model and expected line overlap
- large clr difference between OTUs
- low residuals but moderate rho value (0.75)

therefore, this OTU pair was correctly removed by filtR and this shows technical variants are present in QIIME output


[x] tested to see if errors were incorporated when stitching together the sequences in the fasta file
  - opened "LC140942.txt" files in excel and manually merged rows to form one sequence as one entry
  - created and ran "b4_filt_check.R" (slow) and used the manually merged LC140942.txt only to compare sequences before filtering
    - excessive freezing at line 3 lead to force-quitting RStudio multiple times


*12:00 pm - 1:30 pm*
**Biochemistry pizza lunch**

*1:30 pm - 3:00 pm*

[x] continued testing the manually merged spike-in by running the first portion of "control-negative-b4-filt.R" first through agrajag to avoid freezing
- intersected 'spike and 'seqtabR'/'seqtabF'
- still no results shown

[x] reread control article to find any over-looked details that may help deduce why the spike-ins are not present in chosen samples
  - researches used USEARCH to compare sequences to references
  - downloaded USEARCH 32 gb from https://www.drive5.com/cgi-bin/download_form.py?accept=yes&version=10.0.240&linux=yes&win32=yes&email=khobbs3%40uwo.ca&B1=Submit


### Weekly hours: 25

----
#### Monday, July 23, 2018 (Total: 4.5)
----
*9:00 am - 11:30 am*
Lab meeting

*11:30 am - 1:30 pm*
[x] continued writing results in formal copy
[x] searched for and downloaded new samples for negative control to repeat
    - according to supplementary data, some 'Q' samples contain a higher concentration of the spike-in sequences, which would combat any low-abundance filtering done by dada2
    - cross-referenced to the 'mg_project_summary_20180620', sample Run IDs used are:

    SRR3832216
    SRR3985724
    SRR3985757
    SRR3985763

    - fastQ (FTP) files were downloaded from ENA and saved into "/Users/kt/Documents/Documents/Undergrad/4/4483E/control/ftp_files/negative_control_Q"
    - transferred to agrajag under ~/control/negative_control_Q
    - started running dada2 on the 4 samples

----
#### Tuesday, July 24, 2018 (Total: 6)
----
*10:30 am - 4:30 pm*
- finished running dada2 on negative control samples
- ran samples through "control-negative-b4-filt.R" and found that the spike-ins, again, were not present in the sample before dada2 filtering
- repeated negative control with samples

SRR3985779
SRR3985780
SRR3985781

SRR3985784
SRR3985785
SRR3985786 * only one file available for download on ENA so it was removed in order to keep the dada2 run simple

SRR3985774
SRR3985775
SRR3985776

which were included in three different runs and spike-ins were added prior to use. Output saved to ~/control/dada2-output/negative.
  - still returns a list of zero reads before and after filtering

- sent ben summarized filtR results from control and test projects for his write-up
- made powerpoint following "write-up_outline" format
  - positive control tables
  - negative control summary of attempts
  - test plots:
    - biplots
    - Effect
    - MA

- updated github 

### Weekly hours: 10.5



[Mothur:](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2786419/pdf/1541-09.pdf "Introducing mothur: Open-Source, Platform-Independent, Community-Supported Software for Describing and Comparing Microbial Communities
