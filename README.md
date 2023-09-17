# EcoFlex-HDP: High-Speed and Low-Power and Programmable Hyperdimensional-Computing Platform with CPU Co-processing

## Overview

Hyperdimensional computing (HDC) can efficiently perform various cognitive tasks efficiently by mapping data to hyperdimensional vectors with thousands to tens of thousands of dimensions. However, the primary operations of HDC—Bind, Permutation, and Bound—need to be executed more efficiently on a standard CPU platform. This study introduces a novel computational platform, EcoFlex-HDP, specifically designed for HDC. EcoFlex-HDP exploits the parallelism and high memory access efficiency of HDC operations to achieve low computation time and energy consumption, outperforming the CPU. Furthermore, it can work cooperatively with a CPU, enabling integration with existing software, providing flexibility to apply new algorithms, and contributing to the development of an HDC ecosystem. Through experimental evaluations with a Cortex-A9 processor, HDC operations were shown to be accelerated by a maximum of 169 times. Furthermore, EcoFlex- HDP was confirmed to improve the energy–delay product by up to 13,469 times when training an image recognition task. All source codes for our platform and experiments are available at https://anonymous.4open.science/r/EcoFlex-HDP/README.md.

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
