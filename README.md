# MuTect2 Target Chunking

Demo pipeline for testing different data chunking methods for MuTect2.

[MuTect2](https://software.broadinstitute.org/gatk/documentation/tooldocs/3.8-0/org_broadinstitute_gatk_tools_walkers_cancer_m2_MuTect2.php) is a common tool used for variant calling of tumor-normal pairs. However, it is limited to running only in single-threaded mode, which can lead to extremely long execution times. 

This demo pipeline uses different techniques to chunk the included list of target regions (`targets.bed`) into smaller segments to run in parallel, then aggregate all results for comparison to ensure that variant calls are the same across all chunking methods.

# Usage

This pipeline comes pre-configured for usage on NYULMC's Big Purple HPC cluster using pre-built Singularity containers and pre-downloaded reference files. 

In order to use this pipeline on your system you will need to update the file paths saved in `nextflow.config` for your system. 

Singularity and Docker container recipes are included in the `containers` directory.

Once correctly configured, the pipeline can be run with:

```
make run
```


