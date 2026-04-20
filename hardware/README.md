# Hardware Design Files

This folder contains the hardware design sources for the FPGA implementation of the FFT accelerator on Xilinx Zynq-7000.

## Files

### `zynq_fft_design.bd`

Vivado Block Design containing:

* ZYNQ7 Processing System
* AXI DMA
* FFT IP Core
* AXI Interconnect
* Reset / Clocking logic
* Integrated Logic Analyzer (ILA)

### `hardware.xsa`

Xilinx hardware handoff file exported from Vivado. Used for software development in Vitis / SDK.

### `project.xpr`

Vivado project file used to reopen the complete hardware project.

---

## Hardware Architecture

ARM Processor (PS) sends FFT input samples through AXI DMA to the FFT IP implemented in Programmable Logic (PL). FFT output is returned through DMA to memory for verification and benchmarking.

---

## Target Board

* Digilent Arty Z7-20
* Xilinx Zynq-7000 SoC

---

## Tool Version

* Vivado 2021.2
