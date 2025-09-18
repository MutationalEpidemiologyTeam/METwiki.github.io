# Why using conda ? 
It can be useful when you want to use specific packages that cannot be loaded on the SIT platform

How to use conda ?
Here is an example on how to do it.

1. Go on the [SIT Portal](https://portal.sit.iarc.fr/pun/sys/dashboard/)
2. Open "Clusters" in the top menu, then select "Osiris Shell Access"
3. Enter your IARC password
4. Type this in the Shell (this is an example, feel free to adapt it to your needs) :
<pre>srun --cpus-per-task=2 --ntasks=1 --partition=high_p --mem=8G --pty bash -i</pre>
After a while, you will get this kind of information : “srun: job 15841977 has been allocated resources”

6. Enter this in the Shell (make sure you have miniconda3 on your system before) : 
<pre>source ~/miniconda3/bin/activate</pre>
7. List all existing environments (in case you already created some) :
<pre>conda env list</pre>
8. Otherwise, create a new working environment (let's call it "myenv" here): 
<pre>conda create --name myenv</pre>
9. Activate your working environment :
<pre>conda activate myenv</pre>
10. Launch R in the Shell (for this, just type R in the shell)
<pre>R</pre>
11. Now you can copy paste your R code here
12. Do not forget to kill your job when you are done.
For example : 
<pre>scancel 15841977</pre>

For step 10, you can also run a R script in bash like this : 
<pre>Rscript /home/aixm/discern_kidney/1_data_analysis/040225_test_file.R</pre>

  





  



