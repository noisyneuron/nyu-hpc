# HPC

* What is HPC?
  * High Performance Computing. Lots of big computers to run tasks that are too intensive for your machine, or that your computer simply can't do. If you come from 3D world, it's similar to the concept of render farms.
  * They are computers sitting in some physical location owned by NYU, without monitors and mouses and keyboards, but they are connected to the internet. You can get on the NYU network and access them on the command line (terminal). 
* Why would I want to use it? 
  * Machine learning tasks where you want to train on big data set, longer training time. While there's a lot of models out there that you can use, the relationship between input data and output can become a lot clearer when you train your own models -- understanding the limitations of the algorithms, trying on different datasets and observing first hand, tweaking parameters etc -- and you can use these *ML tools* 
  *  It's free, *while you are at NYU*. Access to powerful machines like this could easily add up to hundreds or thousands of dollars otherwise
* What do I need to know before using HPC?
  * Familarity / comfort with the command line (terminal) is a must. There's no point-and-click interface for HPC, so its easy to get lost without some basic command line understanding. 
* What are the broad steps I need to do?
  * Make an account and set up SSH access
  * Transfer training data to servers 
  * Getting the repo you want and getting all the requirements / modules
  * Figuring out the appropriate amount of resources you need
  * Queuing a job! (Or running a quick job in 'interactive' mode )
  * Transferring your model / data back 
* Things to note and useful commands

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