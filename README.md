# assembly_compare_ref_query
Assess the QV of an assembly

This pipeline finds differences between assemblies using bwa, then uses freebayes calls to identify heterozygous differences. Remaining differences are used to calculate quality scores.

# Quick Start
Clone recursively
```
git clone https://github.com/EichlerLab/assembly_compare_ref_query --recursive
cd assembly_compare_ref_query
```

Setup (compile module, set PYTHONPATH):

`bash setup.sh`

Configure variables in config.yaml

Run

```
export PYTHONPATH=`pwd`/python-Levenshtein:$PYTHONPATH
snakesub -j 10 -w 60 -kT
```
