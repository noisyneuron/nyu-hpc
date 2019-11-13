# Contents

[Introduction (this page)](/)

[Account setup](/account.md)

[Data storage and file systems](/storage.md)

[Data transfer](/transfer.md)

[Modules, packages and virtual environments](/modules.md)

[Useful commands and troubleshooting](/useful.md)

[Running Jupyter notebooks](/jupyter.md)



*This documentation relies heavily on the notes shared by [Cristobal Valenzuela](https://github.com/cvalenzuela/hpc) and [Dan Oved](https://github.com/oveddan/itp_presentations/blob/master/hpc/getting_started.md) - big thanks to them*

<br><br>

---





# HPC Introduction

* What is HPC?
  * HPC stands for *High Performance Computing*. Essentially, a lot of big computers to run tasks that are too intensive for your computer, or that your computer simply can't do because of compatibility issues or limited hardware. If you come from 3D world, it's similar to the concept of render farms.
  
  * There are computers sitting in some physical location owned by NYU, without monitors and mouses and keyboards, but they are connected to the internet. You can get on the NYU network and access them on the command line (terminal). 
  
    
* Why would I want to use it? 
  * As an ITP student, machine learning is probably one of the main reasons HPC would be useful to you. While there's a lot of models out there that you can use, its sometime more interesting / fun / useful to train your own models. The relationship between input data and output can become a lot clearer when you train your own models, helping one to understand the workings and limitations of the algorithms, how they can be harnessed as *tools*, and how they can be exploited  and misused. 
  
  * While there might be rhetoric around Machine Learning being a science, it is really more of an art of tuning and tweaking models to get them to do what you want them to do. Developing this intuition will not only help you use ML as a tool for your own work, but will also help you ask questions of how ML is being used in the world.  
  
  * It's free, *while you are at NYU*. Access to powerful machines like this could easily add up to hundreds or thousands of dollars otherwise. 
  
    
* What do I need to know before using HPC?
  
  * Familarity / comfort with the command line (terminal) is a must. There's no point-and-click interface for HPC, so its easy to get lost without some basic command line understanding. 
  
    
* What are the broad steps I need to do?
  * Make an account and set up SSH access
  
  * Transfer training data to servers 
  
  * Setting up the repo you want to use and all the requirements / modules
  
  * Figuring out the appropriate amount of resources you need
  
  * Queuing a job! (Or running a quick job in 'interactive' mode )
  
  * Transferring your model / data back 
  
     
