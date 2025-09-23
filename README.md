# EcoWatt : Power-Aware Extensions for Microwatt CPU

****Project Overview****

This project integrates RTL-PowerLens, a lightweight AI-assisted framework for real-time power estimation and optimization, into the Microwatt OpenPOWER CPU core. 
Our goal is to enhance the Microwatt ecosystem by enabling designers and researchers to observe and optimize power consumption at the RTL level — without relying on closed-source EDA tools.

By combining Microwatt’s open CPU architecture with PowerLens’s predictive modeling, we provide a unique, open-source platform for teaching, research, and early design exploration in low-power processor design.

Unlike traditional design flows, RTL-PowerLens does not merely facilitate building an SoC — it empowers designers to create power-aware SoCs with improved efficiency and insight.

**Motivation** 

- Traditional RTL power analysis requires expensive, closed EDA tools.
- Designers need early feedback on power impact when adding instructions, caches, or accelerators.
- Our integration lowers the barrier for open-source chip design and makes power-aware architecture exploration accessible to all.

**Key Features**

- Microwatt + RTL-PowerLens Integration — seamless connection between Microwatt’s RTL simulation and PowerLens analysis.
- Open-Source Toolchain — built entirely with Docker, GHDL, Yosys, LibreLane/OpenLane.
- Power-Aware Debugging — visualize how code and microarchitectural changes affect power in real time.
- Custom Instruction Support — demonstrate how adding a new instruction changes both functionality and power footprint.
- Educational Value — provides an open lab for students to learn RTL-to-GDS flows with power awareness built in.

**Technical Approach**

1. Baseline Setup
   - Clone and build Microwatt using GHDL + Yosys.
   - Validate by running Micropython on the CPU in simulation.

2. Integration
   - Extend Microwatt’s RTL with RTL-PowerLens hooks for activity capture.
   - Develop interfaces to feed switching data into ML-based power prediction models.

3. Verification
   - Use unit-level and system-level testbenches to measure power changes.
   - Coverage includes baseline core, custom instruction extensions, and benchmark workloads.

4. Synthesis & P&R
   - Convert VHDL → Verilog with GHDL.
   - Run synthesis and physical design using LibreLane/OpenLane.
   - Collect post-layout switching activity to validate predictions.

**Expected Outcomes**

- Working Microwatt CPU extended with real-time RTL power reporting.
- Case studies:
   * Impact of enabling/disabling FPU.
   * Adding a simple custom instruction and measuring power.
- Documentation + tutorials for open-source power-aware chip design.

**Tools & Resources**

- Simulation & Verification: Docker, GHDL, Yosys, GTKWave
- Synthesis & P&R: LibreLane / OpenLane (SKY130 PDK)
- Baseline Core: Microwatt (VHDL 2008)
- SRAM Blocks: ChipFoundry Commercial SRAMs
  
**Why This Project Stands Out**

- Unique Contribution: Open-source power-aware CPU design framework.
- High Educational Value: Useful for universities and open hardware training.
- Scalable Impact: Can extend beyond Microwatt to other open cores (RISC-V, etc.).
- Aligned with Goals: Strengthens open hardware ecosystem, lowers design barriers, empowers others to create.


**Team**

- Inchara Vittal Shetty
- Graduate Student, NYU Tandon School of Engineering
- Focus: ASIC design, low-power architectures, AI-assisted chip design

**Closing**

This project will make Microwatt not just an open CPU — but a open-source _power-aware_ CPU platform.
