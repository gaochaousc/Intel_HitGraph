# What is this repository for?
Find the paper on https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8685122

FPGA baseline is "ForeGraph: Exploring Large-scale Graph Processing on Multi-FPGA Architecture (https://web.cs.ucla.edu/~chiyuze/pub/fpga17.pdf) 

"GraphOps: A dataflow library for
graph analytics acceleration" (https://dl.acm.org/doi/pdf/10.1145/2847263.2847337)

# Definition of inputs and outputs
![hit](https://user-images.githubusercontent.com/58924633/85347795-8a8c9680-b4ae-11ea-9f91-51bd60abe20e.PNG)

The hitgraph_2018_processing core contains algorithm implementations which is shown in the yellow part above.
An assumption here is that input and output data are stored in the internal memory before being loaded into algorithm core. 

# Directory Structure
  Algorithm Processing Core Demo: include 4 algorithm processing cores for Sparse Matrix-Vector Multiplication (SpMV), PageRank (PR), Weakly Connected Component (WCC), Single Source Shortest Path (SSSP)
IP core template generate by intel quartus 20.1 for reference

module with testbench: It contains several crucial modules and their testbench, which aims at prove the functions of the design

Algorithm_pipeline: pipelines which is able to served as IP core, they are able to handle the two phases mentioned in paper

# IP core setting:
  IP catalog => basic function => floating point function => named this function add => in Functionality choose Generate Enable and generate HDL;
  
  IP catalog =>  basic function => choose arithmetic => floating point function=> named this function mult => in Functionality choose Generate Enable and generate HDL
  # testbench
  you can just download the testbench and create a project in Modelsim for testing.
