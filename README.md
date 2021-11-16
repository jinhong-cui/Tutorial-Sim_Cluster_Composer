
<!-- README.md is generated from README.Rmd. Please edit that file -->

# R Simulation Study Automation

<!-- badges: start -->
<!-- badges: end -->

The goal of this repository is to provide
[`R`](https://www.r-project.org/) users an example of how to **automate
simulation studies on high-performance computing platforms (a.k.a. the
cluster)**. The pipeline was initially written for
[`Slurm`](https://slurm.schedmd.com/documentation.html) scheduling
system, but can be easily modified for other systems.

The main idea of this pipeline is to use R to compose jobs via system
call, where each job corresponds to a batch of replications under the
same simulation setting. These replications are implemented via the
Slurm *job array* feature using the flag
[`--array`](https://slurm.schedmd.com/job_array.html).

## Toy Example: Central Limit Theorem

### Getting Started

1.  Copy three code files (including `start_sim.R`,
    `slurm_job_config.job`, `main.R`) in the folder `Code-copy_me` to
    your working directory on the cluster.
2.  Replace the code section \[TODO: insert permanent link here\] in the
    `main.R` file with you simulation code
3.  Replace the directory path with

-   Search *TODO: Replace path here*
-   We recommend to use [absolute path instead of relative
    path](https://www.linux.com/training-tutorials/absolute-path-vs-relative-path-linuxunix/)
    in your files

1.  Source the `start_sim.R` in an R console or run
    `R CMD BATCH start_sim.R` in the command line in the head node of
    the cluster

## Techinical Explaination

## Questions/Discussion Board

## Strategies

-   Modulelize your code
-   Test out your code before deployment on the cluster
-   Choose the correct partition
-   Raw Data Vs Simulation Results

## Remarks

-   Technique
-   Simulation strategies
-   Alternatives
    -   Use `Targets`
-   Advancement
    -   Change parameters of the jobs
