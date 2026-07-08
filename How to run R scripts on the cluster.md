---
  title: How to run R scripts on the cluster
nav_order: 7
parent: Computing Resources
---
  
  # How to run R scripts on the cluster
  R can be run on the cluster to use its resources and can be run interactively or as a job via SLURM.
  
  ### Interactive RStudio (Server)
  ```{r}
# Go to address and login with IARC credentials:
  http://rstudio.iarc.fr/

# Or access via SIT portal:
  https://portal.sit.iarc.fr/pun/sys/dashboard/
```
  
### SRUN for interactive sessions
```{r}
# Start an interactive srun session:
srun --pty bash -i
# Start an interactive srun session with resources:
srun --cpus-per-task=4 --ntasks=1 --partition=low_p --pty bash -i

# Run RStudio script
Rscript CodeToRun.R -o /outputdir/ -m Renvironment.RData
```

### SBATCH for submitting jobs
```{r}
#!/bin/bash
#SBATCH --job-name=METTY
#SBATCH --account=gcs
#SBATCH --ntasks=1 
#SBATCH --cpus-per-task=4
#SBATCH --mem=25gb                   
#SBATCH --time=10:00:00

cd /MET/
  
# Run RStudio script
Rscript CodeToRun.R -o /outputdir/ -m Renvironment.RData
```
