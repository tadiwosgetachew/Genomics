# Malaria Drug Resistance Variant Annotation

This project focuses on Plasmodium falciparum, the parasite responsible for malaria, a disease that remains widespread globally. As drug-resistant strains become increasingly prevalent, understanding the genetic markers of resistance is crucial. This project aims to analyze malaria drug resistance by identifying and annotating key genetic variants, particularly in transporters like CRT and MDR1, which are known to contribute to resistance against antimalarial drugs.

## Project Overview

This project aims to develop a bioinformatics pipeline for variant calling and annotation, providing key insights into Plasmodium falciparum (Pf) drug resistance. By studying known genetic markers associated with drug resistance, the pipeline helps uncover critical mutations that contribute to resistance, advancing our understanding of the genetic factors involved in malaria treatment.

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

### Future Directions

The project can be expanded by integrating data from **MalariaGEN**, which provides real-world, annotated samples with known clinical  resistance profiles(acess to this data is demonstrated in the notebook). This would help identify key mutations linked to drug resistance, improve variant prediction models, and validate the findings with actual clinical data.

### Contributions

Contributions are welcome! If you have suggestions, improvements, or bug fixes, feel free to submit a pull request or open an issue.

## Acknowledgments

We would like to express our gratitude to the following:

- **MalariaGEN**: For providing access to a comprehensive database of malaria drug resistance data.
- **NCBI**: For providing access to high-quality genomic data and tools like `snpEff`, `samtools`, and `bcftools` that were critical for variant calling and annotation.
- **IGV**: For providing a robust platform to visualize sequencing data and variant calls.
- **The Open Source Community**: For creating and maintaining the tools and libraries (such as `Biopython`, `pybedtools`, `vcfpy`, and `tabix`) that were integral to building this pipeline.
- **The Malaria Research Community**: For their ongoing efforts in studying malaria and drug resistance, providing valuable data and insights for the development of anti-malarial strategies.











