FireGuard: A Generalized Microarchitecture for Fine-Grained Security Analysis on OoO Superscalar Cores
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
Building simulation platform, RISC-V toolchain, Chisel toolchain, and other dependencies: 

```
git clone https://github.com/ucb-bar/chipyard.git
cd chipyard
git checkout 1.7.0
./scripts/init-submodules-no-riscv-tools.sh
./scripts/build-toolchains.sh riscv-tools # for a normal risc-v toolchain 
```

FireGuard Hardware
========================
Setting environments

```
export FIREGUARD=$(dirname $(pwd))
export PLATFORM=$(pwd)
. ./env.sh
```

Updating source code
```
$FIREGUARD/Scripts/update_src.sh
```

Building Hardware 
```
cd $PLATFORM/sims/verilator
make config=RocketConfig
```

FireGuard Software
========================