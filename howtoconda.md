# Why using conda ? 
It can be useful when you want to use specific packages that cannot be loaded on the SIT platform

How to use conda ?
Here is an example on how to do it.

1. Go on the SIT Portal
2. Open Clusters, then select Osiris Shell Access
3. Enter your IARC password
4. Enter this in the Shell (this is an example, feel free to adapt it to your needs) :
srun --cpus-per-task=2 --ntasks=1 --partition=high_p --mem=8G --pty bash -i
After a while, you will get this kind of information : “srun: job 15841977 has been allocated resources”
5. Enter this in the Shell (make sure you have miniconda3 on your system before) : 
source ~/miniconda3/bin/activate
6. List all existing environments (in case you already created some) :
conda env list
7. Otherwise, create a new working environment (let's call it "myenv" here): 
conda create --name myenv
8. Activate your working environment :
conda activate myenv
9. Launch R in the Shell (for this, just type R in the shell)
R
10. Now you can copy paste your R code here
11. Do not forget to kill your job when you are done
For example : 
scancel 15841977

For step 10, you can also run a R script in bash like this : 
Rscript /home/aixm/discern_kidney/1_data_analysis/040225_test_file.R

  



