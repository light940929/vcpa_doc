# Step 7: Review quality metrics of processed data

**After the sample get processed by VCPA, users can review the sample level stage-by-stage quality metrics of the VCPA pipeline via the tracking database.**

**The tracking database can be accessed using the below endpoints \(where IP is the public IP address of the tracking database\)**

1\) To view the list of projects: [`http://IP/v1/projects`](http://ip/v1/projects)

2\) To view the samples information with each of the projects:

[`http://IP/v1/sample/details?project_id=*`](http://ip/v1/sample/details?project_id=*)

\(where \* is the project\_id\)

VCPA is divided into 4 stages at the per sample level \(see overview figure in the Introduction session for details\). For each stage of VCPA, the quality metrics can be accessed respectively as follows:

3\) **Stage0** - [http://IP/v1/stats/stage0/project\_id](http://ip/v1/stats/stage0/project_id)=\*

4\) **Stage1** - [http://IP/v1/stats/stage1/project\_id](http://ip/v1/stats/stage1/project_id)=\*

5\) **Stage2a** - [http://IP/v1/stats/stage2a/project\_id](http://ip/v1/stats/stage2a/project_id)=\*

6\) **Stage2b** - [http://IP/v1/stats/stage2b/project\_id=\*](http://ip/v1/stats/stage2b/project_id=*)

\(where \* is the project\_id\)



**Notable metrics:**

**Sequencing coverage** – Sequencing coverage describes the average number of reads that ‘align’ or ‘cover’ known reference bases. This coverage level helps determine whether variant discovery can be made with a certain degree of confidence at a specific base location. Coverage metrics are captured at **stage1** of VCPA.

**Average coverage equation -** The WGS depth of coverage calculation is performed using sambamba. We extract the read count and coverage across several percentages.  
The average depth of coverage for WGS is calculated as: the average chromosome read count \* read size summed, divided by number of non-N nucleotides.

**Transition to Transversion \(Ti/Tv\) Ratio** – Ratio of the number of transitions \(changes from A &lt;-&gt; G and C &lt;-&gt; T\) to the number of transversions \(changes from A &lt;-&gt; C, A &lt;-&gt; T, G &lt;-&gt; C or G &lt;-&gt; T\) for a pair of sequences. It is one of the metrics to evaluate the quality for the callset. Ti/Tv ratio are captured at **stage2b** of VCPA.

GATK VariantEval is used to calculate the Ti/Tv ratio. Database also capture number of known and novel Ti and Tv SNPs.  


