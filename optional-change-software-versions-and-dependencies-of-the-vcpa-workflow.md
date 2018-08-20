# Optional: Change software versions and dependencies of the VCPA workflow

**VCPA is functional equivalent to the CCDG/TOPMed protocol. VCPA is built upon the following default software versions and dependency files for variant call. We strongly recommend users to use these default versions.**

Users can still change the default software versions using the JSON file if needed - see example shown at the bottom of the page.

### **Software**

[BWA](https://github.com/lh3/bwa/releases/tag/v0.7.15) \(version 0.7.15\)

[SAMTOOLS](https://github.com/samtools/samtools/releases/tag/1.3.1) \(version: 1.3.1-42-g0a15035\(using htslib 1.3.2-135-g50db54b\)\)

[GATK](https://software.broadinstitute.org/gatk/download/) \(version 3.7\)

[PICARD](https://github.com/broadinstitute/picard/releases/tag/2.8.1) \(version 2.8.1\)

[SAMBABA](https://github.com/broadinstitute/picard/releases/tag/2.8.1) \(version v0.6.5\)

[SAMBLASTER](https://github.com/GregoryFaust/samblaster/releases/tag/v.0.1.24) \(version 0.1.12b\)

[VCFTOOLS](https://sourceforge.net/projects/vcftools/files/) \(version 0.1.12b\)

[BAMUTIL](https://github.com/statgen/bamUtil/tree/NonPrimaryDedup) \(version v1.0.13\)

[BCFTOOLS](https://github.com/samtools/bcftools/releases/tag/1.3.1) \(version: 1.3.1-1\)

### Dependency files

> **Hg38 Reference genome version GRCh38DH**

* 1000 Genomes Project [version](ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/technical/reference/GRCh38_reference_genome/GRCh38_full_analysis_set_plus_decoy_hla.fa) \(3366 contigs\)
* md5sum: _64b32de2fc934679c16e83a2bc072064_

> **GATK variant call hg38 dependency files**

* **dbSNP annotation**

  [dbSNP 138 lifted SNV file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Homo_sapiens_assembly38.dbsnp138.vcf) \[ [Corresponding index file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Homo_sapiens_assembly38.dbsnp138.vcf.idx) \]

* **Indels annotation**

  [dbSNP 138 lifted Indel file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Homo_sapiens_assembly38.known_indels.vcf.gz) \[ [Corresponding index file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Homo_sapiens_assembly38.known_indels.vcf.gz.tbi) \]

  [Mills and 1000G gold standard indels file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Mills_and_1000G_gold_standard.indels.hg38.vcf.gz) \[ [Corresponding index file](https://storage.googleapis.com/genomics-public-data/resources/broad/hg38/v0/Mills_and_1000G_gold_standard.indels.hg38.vcf.gz.tbi) \]

The example of JSON file: 

```text
Tutorial_vcpa_steps.ref_alt : ## Path of the FASTA.alt alignment file
Tutorial_vcpa_steps.ref_amb : ## Path of the FASTA.amb alignment file
Tutorial_vcpa_steps.ref_ann : ## Path of the FASTA.ann alignment file
Tutorial_vcpa_steps.ref_bwt : ## Path of the FASTA.bwt alignment file
Tutorial_vcpa_steps.ref_pac : ## Path of the FASTA.pac alignment file
Tutorial_vcpa_steps.ref_sa :  ## Path of the FASTA.sa alignment file
Tutorial_vcpa_steps.ref_fai : ## Path of the FASTA.fai alignment file
Tutorial_vcpa_steps.ref_dict :  ## Path of the FASTA.dict alignment file
Tutorial_vcpa_steps.input_bam :  ## Path of the BAM/CRAM file 
Tutorial_vcpa_steps_steps.fastq_directory_path :  ## Path for the FASTQ file 
Tutorial_vcpa_steps.ref_fasta :  ## Path of the reference genome FASTA file 
Tutorial_vcpa_steps.TARGET : ## Path of the WES capture kit / target region file 
Tutorial_vcpa_steps.KNOWN : ## Path of the dbSNP 138 lifted Indel file 
Tutorial_vcpa_steps.KNOWN_index : ## Path of the dbSNP 138 lifted Indel index file
Tutorial_vcpa_steps.DBSNP : ## Path of the dbSNP 138 lifted SNV file
Tutorial_vcpa_steps.DBSNP_index :  ## Path of the dbSNP 138 lifted SNV index file
Tutorial_vcpa_steps.GOLD : ## Path of the Mills and 1000G gold standard indels file
Tutorial_vcpa_steps.GOLD_index : ## Path of the Mills and 1000G gold standard indels index file
Tutorial_vcpa_steps.BWA : ## Location of the BWA software
Tutorial_vcpa_steps.SAMBAMBA : ## Location of the SAMBAMBA software
Tutorial_vcpa_steps.SAMBLASTER : ## Location of the SAMBLASTER software
Tutorial_vcpa_steps.SAMTOOLS : ## Location of the SAMTOOLS software
Tutorial_vcpa_steps.PICARD : ## Location of the PICARD software
Tutorial_vcpa_steps.bamUtil : ## Location of the bamUtil software
Tutorial_vcpa_steps.GATK : ## Location of the GATK software
Tutorial_vcpa_steps.tmp : ## Location of the template
Tutorial_vcpa_steps.log : ## Location of the logs
```

