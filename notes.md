###

----

Things to note

- Files deleted every so often
- Different file systems have different limits, in terms of *number of files* and *storage space*
- Can check with `myquota`
- Accessing out of NYU network
- Upload download from google drive
- Figuring out cuda versions
- Custom python modules
- Figuring out what resources you need
- Low gpu warnings 
- Using Jupiter notebooks??
- Figuring out when your job is estimated to start
- Setting up an environment .. 
- Installing pip packages to user account 
- OOM errors
- 





----

Handy commands:

`squeue --start --job 2353612` view estimated start time

`myquota` to see how much space you're using. Storage and filesize limits on drives. 

[this](https://www.tensorflow.org/install/source#tested_build_configurations) lists the coda version required for different versions of tensor flow. The trick to remember is the `cudnn` versions always reference the `cuda` version first.. ie in the link, `cuda 10.0` works with `cudnn 7.4`. on hpc. You will find the module `cudnn/10.0v7.4.2.24` -- its the part after the `v` that you're matching up 

Always figure out resources you need in interactive mode first.. for each cpu max of 2 opus [TEST]. Common errors :'OOM'

When you queue the job, you can ask to receive an email for everything. Things to watch out for - low GPU usage -- it will kill your job after 2 hours.. also will tell u when job is started / ended

If something fails, look at the output file .. 

Some GitHub repos you find will have a bunch of packages that need to be installed. but you might have another package that needs similar packages, just different versions .. setting up 'virtual environments' lets you do this 