# Malaria Drug Resistance Variant Annotation

This project focuses on **Plasmodium falciparum**, the deadly parasite responsible for causing malaria. It analyzes malaria drug resistance using variant annotation techniques. The project utilizes tools like **biopython**, **VCFpy**, **snpEff**, and others to pull data, align sequences, call variants, and visualize results. The primary goal is to map and annotate variants related to resistance in transporters such as **CRT** and **MDR1**, focusing on malaria drug resistance.

## Project Overview

This project aims to develop a bioinformatics pipeline for variant calling and annotation, providing key insights into Plasmodium falciparum (Pf) drug resistance. By studying known genetic markers associated with drug resistance, the pipeline helps uncover critical mutations that contribute to resistance, advancing our understanding of the genetic factors involved in malaria treatment."

### Key Steps:

1. **Install Required Tools and Libraries**:
    - Install bioinformatics tools for data analysis, alignment, and variant calling.
    - Prepare the environment with **Biopython**, **VCFpy**, **snpEff**, and other necessary tools.

2. **Pull Data from NCBI**:
    - Retrieve **NGS** data for **CRT** and **MDR1** transporters from the **NCBI** database.
   
3. **Align Data with Reference Genome**:
    - Align the sequences with the **Pf3D7** reference genome using **BWA** and **Samtools**.
    
4. **Variant Calling**:
    - Use tools like **bcftools**, **samtools**, and **vcftools** to call and filter variants.

5. **Annotate Variants**:
    - Build a **Pf3D7** custom database for **snpEff** to annotate the variants and understand their role in drug resistance.

6. **Visualize Data in IGV**:
    - Use **IGV** to visualize the alignment map and **VCF** files.

## Setup

To run this project you need to install the necessary dependencies and tools. Here are the steps:

### 1. Install Python Libraries

```bash
!pip install biopython
!pip install pybedtools
!pip install igv-jupyter
!pip install igv-notebook
!pip install vcfpy
!pip install malariagen_data
```

### 2. Install Bioinformatics Tools

These dependencies can be installed on your system using `apt-get`:

```bash
# Install samtools, bwa, blast
!apt-get install ncbi-blast+ bwa samtools

# Install bcftools
!apt-get install bcftools

# Install gffread
!apt-get install -y gffread

# Install snpEff
!wget https://snpeff.blob.core.windows.net/versions/snpEff_latest_core.zip
!unzip snpEff_latest_core.zip

# Install Java (required for snpEff)
!sudo apt-get install openjdk-21-jdk

# Install VCF tools
!apt-get install vcftools

# Install tabix
!apt-get install tabix

```

### 3. Data Retrieval and Alignment

- **Pull Data from NCBI**: Retrieve **CRT** and **MDR1** sequences.
- **Align Sequences**: Use **BWA** to align sequences with the **Pf3D7** reference genome.

### 4. Variant Calling and Annotation

- Use **samtools** and **bcftools** for variant calling.
- Annotate variants using **snpEff** with a **Pf3D7** database.

### 5. Visualization

- Visualize the **VCF** files and alignment maps in **IGV** for in-depth analysis.


### Future Directions

The project can be expanded by integrating data from **MalariaGEN**, which provides real-world, annotated samples with known resistance profiles(acess to this data isdemonstrated in the notebook). This would help identify key mutations linked to drug resistance, improve variant prediction models, and validate the findings with actual clinical data.

### Contributions

Contributions are welcome! If you have suggestions, improvements, or bug fixes, feel free to submit a pull request or open an issue.






