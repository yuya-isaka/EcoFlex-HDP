# EcoFlex-HDP: High-Speed and Low-Power and Programmable Hyperdimensional-Computing Platform with CPU Co-processing

## Overview

Hyperdimensional computing (HDC) offers an efficient way to perform various cognitive tasks by mapping data to hyperdimensional vectors with thousands to tens of thousands of dimensions. EcoFlex-HDP is a novel computational platform dedicated to HDC. It exploits the parallelism and high memory access efficiency of HDC operations to reduce computation time and energy consumption, outperforming commercial CPUs. Additionally, EcoFlex-HDP can work collaboratively with a CPU, enabling integration with existing software and providing the flexibility to apply new algorithms, thereby contributing to the development of an HDC ecosystem. Experimental evaluations with the Cortex-A9 processor show that HDC operations can be accelerated by up to 169 times, and the energy-delay product can be improved up to 13,469 times in training an image recognition task.

## Directory Structure

The project is organized as follows:

```
EcoFlex-HDP/
|-- src/
|   |-- [SystemVerilog files for HPU on FPGA]
|   |-- [Verilog files for HPU on FPGA]
|   |-- [Test codes]
|
|-- test/
|   |-- application/
|   |   |-- Image/
|   |   |-- Language/
|   |   |-- Voice/
|   |
|   |-- micro-benchmark/
|       |-- benchmark-CPU/
|       |-- benchmark-HDP/
```

### `src` Directory

This directory contains the SystemVerilog and Verilog files for implementing the HDC processing unit (HPU) on FPGA. It also contains test codes for these implementations.

### `test` Directory

This directory contains test codes used in our experiments and is divided into two sub-directories:

- `application`: Contains C code for various recognition tasks such as image, language, and voice recognition.
  - `Image`: C code for image recognition tasks.
  - `Language`: C code for language recognition tasks.
  - `Voice`: C code for voice recognition tasks.

- `micro-benchmark`: Contains benchmarking code to evaluate the performance of EcoFlex-HDP and is divided into:
  - `benchmark-CPU`: C code for benchmarking HDC operations on a CPU.
  - `benchmark-HDP`: C code for benchmarking HDC operations on EcoFlex-HDP.
