
## Local environment

To work locally using python and Jupyter notebooks.

:::{note}
This content only concerns Linux and macOS, please reach out to contribute to windows environments.
:::

We recommend using [Visual Studio Code](https://code.visualstudio.com/) for code and notebook editing, running codes and notebooks, interacting with GitHub. It is how we wrote this book!

Either through your OS or VS Code, open a terminal. The terminal is used to pass commands to the computer. The programming language to send codes to the computer is Shell. BASH (Bourne Again SHell) is one of the implementations of Shell and is used to efficiently perform tasks. Great tutorials on how to get started with Shell are in the [Software Carpentries Lessons](https://swcarpentry.github.io/shell-novice/).

Get to know your hardware. Find out what CPU, GPU, what memory is on your local environment. One that allows to monitor the resources in real time is ``top`` (or a more human-readable ``htop``). Install it on your local environment (e.g., use ``brew install htop`` on macOS). 

Machine Learning research requires parallelization. Typically, CPUs (Central Processing Units) are plenty sufficient for most ML applications. They are the basics and default hardware of most computers and are particularly practical when handling large data sets for the In/Out operations. 

However, Deep Learning applications are mostly enabled by the much expansive parallelization of GPUs (Graphic Processing Units). GPUs were developed mostly for gaming, and it is why they have become affordable. The advantages of the GPU is the parallelization capabilities. The arrival of a programming language CUDA (Compute Unified Device Architecture) in 2007 enabled dramatic growth in porting heavy computations on GPUs. CPUs and GPUs are composed of multiple **cores**. CPUs typically have between 8 and 96 cores. GPUs typically have between 5,000-10,000 cores.

To watch how the GPU resources are used, use the following command (if installed on your resource):
```bash
    watch nvidia-smi
```

Individual CPUs can compose a **node**. Multiple **nodes** can compose a **cluster**. Clusters can be accessed locally (if you are lucky!) and most often remotely. There are three typical clusters: your local resource (research group), the institutional resource (e.g., Hyak at UW), the HPC center (e.g., Texas Advanced Computing Center), or the Cloud service provider. In Cloud computing, a node is an **instance**.

