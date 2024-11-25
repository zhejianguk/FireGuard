Artefact Evaluation for "FireGuard: A Generalized Microarchitecture for Fine-Grained Security Analysis on OoO Superscalar Cores", Submitted to DAC 2025. 
==================================================

This repository contains artefacts and workflows to reproduce experiments from the DAC 2025 submission 1436

"FireGuard: A Generalized Microarchitecture for Fine-Grained Security Analysis on OoO Superscalar Cores"

Platform pre-requisities
========================
* An x86-64 system (for Verilator simulation, more cores will improve simulation time).
* An AMD U280 FPGA (for FPGA simulation)
* Linux operating system (We used Ubuntu 20.04 and Ubuntu 22.04)
* A SPEC CPU2006 iso, placed in the root directory of the repository (we used v1.0), for the full workflow.

Installation of Toolchain
========================
Building RISC-V toolchain and other dependcies: 

```
git clone https://github.com/ucb-bar/chipyard.git
cd chipyard
# checkout latest official chipyard release
# note: this may not be the latest release if the documentation version != "stable"
git checkout 1.7.0
./scripts/init-submodules-no-riscv-tools.sh
./scripts/build-toolchains.sh riscv-tools # for a normal risc-v toolchain 
```
