# DxP Data Logger Hardware (LoRa + Distributed Sensor Probes Interface)

This repository only contains the hardware for the DxP (Distributed sensor Profiling) data logger (i.e., the “logger / base station” main board that connects to a DxP sensor probe via a connector.

The sensor probe / sensor-array board designs for DxP probes are released in a separate repository.

> **No SD card slot** is included in this revision (on-device buffering uses the 4 MB on-board flash chip).



---

## Hardware overview
Designed for low-power, distributed environmental sensing deployments using the system concept from:
- *Wielandt et al., “TDD LoRa and Delta Encoding in Low-Power Networks of Environmental Sensor Arrays for Temperature and Deformation Monitoring”* (2023)

**Main logger board capabilities:**
- **LoRa modem:** RFM95W (single-channel LoRa)
- **Wireless SoC:** Nordic **nRF52832** (BLE capable)
- **Timekeeping:** **PCF2129AT** RTC
- **On-board storage:** **4 MB SPI flash** (data buffering)
- **Power:** designed for **2× AA** operation (1.8 V – 3.6 V range); includes **load switching** (e.g., TPS22919) to reduce sleep power
- **Sensor/probe interface:** **I2C** to connect to distributed sensor probes (supports long arrays through an address bit shift register on the sensor probe).

---

## Repository contents
- **KiCad design files (schematic/PCB):**
  - `loggerhw_v4.2.sch`
  - `loggerhw_v4.2.kicad_pcb`
  - `loggerhw_v4.2.kicad_pro`
  - `loggerhw_v4.2.kicad_prl`
  - `loggerhw_v4.2_BOM.csv`
- **KiCad libraries:**
  - `symbol/`
  - `footprints/`
  - `fp-lib-table`
  - `sym-lib-table`
- **Production / fabrication exports:**
  - `fab/` (production outputs generated from the KiCad design—e.g., fabrication-ready exports)
- **This repo documentation:**
  - `README.md`
  - `Users.md`

--------------------------

*** Copyright Notice ***

Wireless data logger with distributed sensors Copyright (c) 2026, The
Regents of the University of California, through Lawrence Berkeley National
Laboratory (subject to receipt of any required approvals from the U.S. Department
of Energy). All rights reserved.

If you have any questions or would like to license this tool for commercial purposes,
please contact the Berkeley Lab's Intellectual Property Office at ipo@lbl.gov.

NOTICE. This tool was developed under funding from the U.S. Department
of Energy and the U.S. Government consequently retains certain rights. As
such, the U.S. Government has been granted for itself and others acting on 
its behalf a paid-up, nonexclusive, irrevocable, worldwide license in the tool
to reproduce, distribute copies to the public, prepare derivative works, and
perform publicly and display publicly, and to permit others to do so.

-----------------------------
*** License Agreement ***

Wireless data logger with distributed sensors Copyright (c) 2026, The
Regents of the University of California, through Lawrence Berkeley National
Laboratory (subject to receipt of any required approvals from the U.S. Department
of Energy). All rights reserved.

This tool is licensed under the CC BY-NC 4.0 International License at 
https://creativecommons.org/licenses/by-nc/4.0/.

Under this CC BY-NC 4.0 International Public License, the following summarized
terms/rights apply to the licensee when using this tool:
- may share (copy and redistribute the material in any medium or format for non-commercial use
  only - NOT for commercial purposes) 
- may adapt (remix, transform, and build upon the material for non-commercial use only - NOT for
  commercial purposes)
- must attribute the original work and author (You must give [appropriate credit](https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1#ref-appropriate-credit) , provide a link
  to the license, and [indicate if changes were made](https://creativecommons.org/licenses/by/4.0/?ref=chooser-v1#ref-indicate-changes) . You may do so in any reasonable manner,
  but not in any way that suggests the licensor endorses you or your use.)

For the complete license, please go to the above-mentioned link. 