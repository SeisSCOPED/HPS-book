
## HPC
HPC (High Performance Computing) typically refers to a system of tightly connected nodes that enables computing large-scale jobs. The software carpentries have tutorials on how to use clusters. See the [Introduction to HPC lessons](https://epcced.github.io/hpc-intro/). These computing architectures enable "Vertical Scaling", meaning adding larger CPU / memory, or I/O resource. 

HPC systems have 1) a compute cluster, 2) a scratch file system (temporary), and 3) a home file systems. Codes are usually in the home, big data is on the scratch file system. Jobs get run on the compute cluster. HPC requires scheduling jobs in a queue, when the resource is available, the jobs get run. It is typical to run big codes on 500-2,000 nodes. 

Institutions may have their own HPC systems. At UW, the system is called [Hyak](https://hyak.uw.edu/).

National HPC resources require specific request for allocation. Requests are typically done using [ACCESS](https://allocations.access-ci.org/) or [TACC](https://www.tacc.utexas.edu/).


HPC can deploy virtual cloud systems to allow horizontal scaling and cloudstore-like file systems.

One typically 1) chooses the HPC resource, and then 2) moves the data there for the computing workflow.
