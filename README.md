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
