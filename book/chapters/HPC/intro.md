
# HPC
HPC (High Performance Computing) typically refers to a system of tightly connected nodes that enables computing large-scale jobs. The software carpentries have tutorials on how to use clusters. See the [Introduction to HPC lessons](https://epcced.github.io/hpc-intro/). These computing architectures enable "Vertical Scaling", meaning adding larger CPU / memory, or I/O resource. 

HPC systems have 1) a compute cluster, 2) a scratch file system (temporary), and 3) a home file systems. Codes are usually in the home, big data is on the scratch file system. Jobs get run on the compute cluster. HPC requires scheduling jobs in a queue, when the resource is available, the jobs get run. It is typical to run big codes on 500-2,000 nodes. 

Institutions may have their own HPC systems. At UW, the system is called [Hyak](https://hyak.uw.edu/).

National HPC resources require specific request for allocation. Requests are typically done using [ACCESS](https://allocations.access-ci.org/) or [TACC](https://www.tacc.utexas.edu/).


HPC can deploy virtual cloud systems to allow horizontal scaling and cloudstore-like file systems.

One typically 1) chooses the HPC resource, and then 2) moves the data there for the computing workflow.

# Access HPC systems at TACC (Frontera as an example)
First create your account following the instructions on the [getting started page](https://tacc.utexas.edu/use-tacc/getting-started/).
Then, following the detailed instructions [here](https://docs.tacc.utexas.edu/basics/mfa/) to setup multi-factor authentication.
Note that after these two steps, you still need to have an active allocation to be able to access the systems.
You will need to request for an allocation or ask to be added to one from your PI.
If you had an account before but have not been using it for a long time, your account may be deactivated. 
In that case, please submit a ticket through [this link](https://tacc.utexas.edu/about/help/) to have your account manually activated.

Note that it takes a few minutes for the system to sync up with your account, so there will be noticeable delays from setting up multi-factor authentication or assigning your account to an allocation.
You will not be able to proceed to the next steps before the sync finished.

## Login to Frontera
Open any terminal app from your laptop to use the ssh command `ssh username@frontera.tacc.utexas.edu` to login to the system:
```
my_laptop:~$ ssh username@frontera.tacc.utexas.edu
To access the system:

1) If not using ssh-keys, please enter your TACC password at the password prompt
2) At the TACC Token prompt, enter your 6-digit code followed by <return>.

Password:
TACC Token Code:
```
You will need to type in your password and the MFA tokens you setup in the previous section.
Note that there may be some delays for you to be able to login, and it may seems you had wrong credentials put in when it is not synced.

## User Environment
The default login shell for your user account is bash (csh/tcsh & zsh available).
This is sourced from "~/.bashrc" via your .profile by default put all your customizations in ".bashrc" (you will need to log out and back in to activate it ) 
Key environment variables:
1.	$PATH (where your env looks for commands)
1.	$LD_LIBRARY_PATH (where compilers find libs, like MKL, etc.)

Please don't run anything computational intensive on the login node!
The login node is shared across all users.

## Use idev to get an interactive session on a compute node
```
$ idev –m 30 –N 1 –n 2 –p development
```
This will give you access to a compute node in the development queue for 30 minutes (set up to run MPI jobs with 2 tasks on 1 node).



