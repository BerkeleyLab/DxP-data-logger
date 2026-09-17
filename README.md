# DxP Data Logger Hardware (LoRa + Distributed Sensor Probes Interface)

This repository only contains the hardware for the DxP (Distributed sensor Profiling) data logger (i.e., the “logger / base station” main board that connects to a DxP sensor probe via a connector.

The sensor probe / sensor-array board designs for DxP probes are released in a separate repository: **[DxP Sensor Probes](https://github.com/BerkeleyLab/DxP-sensor-probes)**.

The firmware for the nRF52832 is released in a separate repository: **[DxP Firmware](https://github.com/BerkeleyLab/DxP-firmware)**.


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
- **Micro SD card slot with load switch** for extra storage (e.g., large sensor datasets) and/or for base-station workflows to store data from multiple devices in the network.

---

## Repository contents

### KiCad design files (schematic / PCB)
- `loggerhw_v5.0.sch`
- `loggerhw_v5.0.kicad_pcb`
- `loggerhw_v5.0.kicad_pro`
- `loggerhw_v5.0.kicad_prl`
- `loggerhw_v5.0.pro`

### KiCad libraries
- `symbol/`
- `footprints/`
- `fp-lib-table`
- `fp-info-cache/`
- `sym-lib-table`
- `loggerhw_v5.0-cache.lib`

### Production / fabrication exports
- `fab/`

### Documentation
- `README.md`
- `LICENSE.md`
- `users.md`
