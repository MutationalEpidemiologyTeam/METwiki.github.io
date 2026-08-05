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
### Start a Run with sbatch or srun

For runs that require a considerable time, it is preferable to use **sbatch** instead of **srun**. 

That happens because `srun` starts an interactive job directly in the terminal, and the output is written as it is running. But if the interactive is terminated for any reasons, the job may also be interrupted. 
Instead, `sbatch` submits the job to the cluster independently of the terminal session. 

Therefore, it is preferred to use `sbatch` in order to avoid this issue.

### Extras
```{r}
# Resume ongoing job using job ID:
sattach <job ID>.0

# Stop a job:
scancel <job ID>

# Checking queue
You can use the `squeue` command to check the status of your submitted Slurm jobs, including its position in the queue and the elapsed run time.

To display only jobs that were submitted under your account, use the -a option:

squeue -a <your account>

# Submitting batches of samples

If you want to submit mutiple samples or tasks to a pipeline, you can use the `—array` option:

#SBATCH --array=0-100%20

In this example, 100 samples will run in the pipeline, with 20 samples running simultaneously.
```
