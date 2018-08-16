# Step 8: Generating Project-level VCF via joint genotyping

**After generating the gVCFs, users can follow the steps provided below for joint genotype call for sample level gVCF into a project level VCF. VCPA implements these steps by referencing to the best practices of GATK. Refer to stage 3 of the VCPA pipeline for details.** [**https://bitbucket.org/NIAGADS/vcpa-pipeline/src/master/VCPA/stage3/**](https://bitbucket.org/NIAGADS/vcpa-pipeline/src/master/VCPA/stage3/)

**To summarize: We used TileDB from Intel to combine all the gVCFs then run the GenotypeGVCF from GATK to do the joint genotype calling. After that, we recalibrate the variant quality scores \(VQSR\) and apply the desired level of recalibration to the SNPs and INDELs in the call set, also from GATK. Last, we separate biallelic and multiallelic variants by bcftools.**

1\) **Combine multiple gVCFs** \([TileDB](https://tiledb.io/) from intel/MIT\) - combine all the sample level gVCFs using the combinegVCFs function.

2\) **GenotypedGVCF** \(GATK3.7\) - joint genotype calling on the output from previous step.

3\) **Variant Quality Score Recalibration \(**VQSR\) on both SNPs and indels \(GATK3.7\) - this is to recalibrate the SNPs and indels via VQSR scores

4\) **ApplyRecalibration** \(GATK3.7\) - this is for applying the desired level of recalibration to the SNPs and indels in the call set

5\) **Separate the Biallelic and Multiallelic variants** \(bcftools\) - QC will handle biallelic and multiallelic variants separately.

