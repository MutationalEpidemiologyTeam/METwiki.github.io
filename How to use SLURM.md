# How to run SLURM (SRUN and SBATCH)
SLURM is a cluster management system where jobs can be created and scheduled.
The following codes are for creating jobs, allocating resources.
The SIT help pages on this are located at https://readthedocs.sit.iarc.fr/hpc/slurm.html#slurm

### Getting started on the cluster
```{r}
# Login to cluster (command line):
ssh username@osiris.iarc.lan

# Create new window:
screen
```

### SRUN for interactive sessions
```{r}
# Start an interactive srun session:
srun --pty bash -i

# Start an interactive srun session with resources:
srun --cpus-per-task=4 --ntasks=1 --pty bash -i
```

### SBATCH for queuing jobs
```{r}
# Start an sbatch session with resources:
#!/bin/bash
#SBATCH --job-name=METTY
#SBATCH --account=gcs
#SBATCH --ntasks=1 
#SBATCH --cpus-per-task=4
#SBATCH --mem=25gb                   
#SBATCH --time=5:00:00

# Run sbatch via a bash (.sh) file:
sbatch <filename.sh>
```

### Extras
```{r}
# Resume ongoing job using job ID:
sattach <job ID>.0

# Stop a job:
scancel <job ID>
```
