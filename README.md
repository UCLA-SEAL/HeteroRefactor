# HeteroRefactor
HeteroRefactor: Refactoring for Heterogeneous Computing with FPGA (ICSE 2020)

## Summary 
Heterogeneous computing with field-programmable gate-arrays (FPGAs) has demonstrated orders of magnitude improvement in computing efficiency for many applications. However, the use of such platforms so far is limited to a small subset of programmers with specialized hardware knowledge. High-level synthesis (HLS) tools made significant progress in raising the level of programming abstraction from hardware programming languages to C/C++, but they usually cannot compile and generate accelerators for kernel programs with pointers, memory management, and recursion, and require manual refactoring to make them HLS-compatible. Besides, experts also need to provide heavily handcrafted optimizations to improve resource efficiency, which affects the maximum operating frequency, parallelization, and power efficiency. 

We propose a new dynamic invariant analysis and automated refactoring technique, called HeteroRefactor. First, HeteroRefactor monitors FPGA-specific dynamic invariants—the required bitwidth of integer and floating-point variables, and the size of recursive data structures and stacks. Second, using this knowledge of dynamic invariants, it refactors the kernel to make traditionally HLS-incompatible programs synthesizable and to optimize the accelerator’s resource usage and frequency further. Third, to guarantee correctness, it selectively offloads the computation from CPU to FPGA, only if an input falls within the dynamic invariant.
On average, for a recursive program of size 175 LOC, an expert FPGA programmer would need to write 185 more LOC to implement an HLS compatible version, while HeteroRefactor automates such transformation. Our results on Xilinx FPGA show that HeteroRefactor minimizes BRAM by 83% and increases frequency by 42% for recursive programs; reduces BRAM by 41% through integer bitwidth reduction; and reduces DSP by 50% through floating-point precision tuning.

## Team 
This project is done in collaboration with Professor [Jason Cong](https://vast.cs.ucla.edu/people/faculty/jason-cong)'s group at UCLA. Please visit the [HeteroRefactor project](https://github.com/heterorefactor/heterorefactor).


## How to cite 
Please refer to our ICSE'20 paper, [Refactoring for Heterogeneous Computing with FPGA](https://web.cs.ucla.edu/~miryung/Publications/icse2020-heterorefactor.pdf) for more details. 
### Bibtex  
@inproceedings{10.1145/3377811.3380340,
author = {Lau, Jason and Sivaraman, Aishwarya and Zhang, Qian and Gulzar, Muhammad Ali and Cong, Jason and Kim, Miryung},
title = {HeteroRefactor: Refactoring for Heterogeneous Computing with FPGA},
year = {2020},
isbn = {9781450371216},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3377811.3380340},
doi = {10.1145/3377811.3380340},
booktitle = {Proceedings of the ACM/IEEE 42nd International Conference on Software Engineering},
pages = {493–505},
numpages = {13},
keywords = {high-level synthesis, automated refactoring, FPGA, dynamic analysis, heterogeneous computing},
location = {Seoul, South Korea},
series = {ICSE '20}
}
[DOI Link](https://dl.acm.org/doi/10.1145/3377811.3380340)

## Video
You can watch an ICSE'20 presentation video [here](https://www.youtube.com/watch?v=FCLYIpPHHls)
 
