---
sidebar_position: 1
---

# High Performance Computing

Let's discover **High Performance Computing in less than 10 minutes**.

## Getting Started

**High Performance Computing (HPC)** refers to the use of advanced computing technologies to solve complex problems that require significant computational power. HPC systems typically consist of large clusters of computers, each with multiple processors or cores, interconnected by high-speed networks. These systems are designed to perform calculations and data analysis tasks at a much faster rate than traditional computing systems.

HPC is used in a wide range of fields, including scientific research, engineering, finance, and healthcare. It allows researchers and analysts to run simulations, model complex systems, and analyze large amounts of data quickly and efficiently. HPC is particularly important for applications that require large-scale data analysis, such as weather forecasting, gene sequencing, and drug discovery.

To take advantage of HPC systems, applications must be designed to run in parallel, meaning that they can be divided into smaller tasks that can be processed simultaneously on different processors. HPC systems also require specialized software, including programming languages and libraries that are optimized for high-performance computing..

**Learn more** on **[HPC](https://en.wikipedia.org/wiki/High-performance_computing)**.

### [LIGER](https://supercomputing.ec-nantes.fr/liger) - An x86 Superscalar Water-cooled Cluster

LIGER is the largest and most capable computational resource available in the western French region, Pays de la Loire, for industrial and academic collaborators. A BULL’s superscalar x86 supercomputer performs a max performance (Rmax) of almost 200 Teraflop/s.

With its Direct Liquid Cooling System (DLC), Liger is the only cluster known in the region water-cooled and showed significantly more energy efficiency than comparable systems, which is essential to control operating costs.

Partners access Liger, whether for open, publishable science or business-sensitive and proprietary research, through the High-Performance Computing Institute of Centrale Nantes (ICI). Partners gain access to one of the fastest Tier-2 regional class high-level HPC infrastructures available, including subject-matter experts, network access, file systems, archive storage, and training/help-line support.

The 10-rack Atos/BULL DLC system is based on the INTEL Xeon x86 architecture configured in a cube topology with a cold aisle confined.

### What you'll need

- [SLURM](https://slurm.schedmd.com/documentation.html) is an open source, fault-tolerant, and highly scalable cluster management and job scheduling system for large and small Linux clusters. Slurm requires no kernel modifications for its operation and is relatively self-contained. As a cluster workload manager, Slurm has three key functions. First, it allocates exclusive and/or non-exclusive access to resources (compute nodes) to users for some duration of time so they can perform work. Second, it provides a framework for starting, executing, and monitoring work (normally a parallel job) on the set of allocated nodes. Finally, it arbitrates contention for resources by managing a queue of pending work.

  - SLURM Tutorial

  On all of the cluster system, users run programs by submitting scripts to the Slurm job scheduler. A slurm script must do three things:
  1. prescribe the resource requirements for the job
  2. set the environment
  3. specify the work to be carried out in the form of shell commands.

  Below is a sample Slurm script for running a Python code using a Conda environment:

  ```bash
#!/bin/bash
#SBATCH --job-name=myjob         # create a short name for your job
#SBATCH --nodes=1                # node count
#SBATCH --ntasks=1               # total number of tasks across all nodes
#SBATCH --cpus-per-task=1        # cpu-cores per task (>1 if multi-threaded tasks)
#SBATCH --mem-per-cpu=2G         # memory per cpu-core (4G is default)
#SBATCH --time=00:01:00          # total run time limit (HH:MM:SS)
#SBATCH --mail-type=begin        # send email when job begins
#SBATCH --mail-type=end          # send email when job ends
#SBATCH --mail-user=<YourNetID>@princeton.edu
module purge
module load anaconda3/2022.5
conda activate pytools-env
python myscript.py

```


- [Singularity](https://docs.sylabs.io/guides/latest/user-guide/) is a container platform. It allows you to create and run containers that package up pieces of software in a way that is portable and reproducible. You can build a container using SingularityCE on your laptop, and then run it on many of the largest HPC clusters in the world, local university or company clusters, a single server, in the cloud, or on a workstation down the hall. Your container is a single file, and you don’t have to worry about how to install all the software you need on each different operating system.

## Generate a new site

Generate a new Docusaurus site using the **classic template**.

The classic template will automatically be added to your project after you run the command:

```bash
npm init docusaurus@latest my-website classic
```

You can type this command into Command Prompt, Powershell, Terminal, or any other integrated terminal of your code editor.

The command also installs all necessary dependencies you need to run Docusaurus.

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.
