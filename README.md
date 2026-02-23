# SCE Futures: Superconductor Electronics

An introduction to superconductor electronics for new AM team members.

## What You'll Learn

This course covers the fundamentals of superconducting devices, from basic physics to circuit design and fabrication:

| Module | Topics |
|--------|--------|
| **Fundamentals** | Superconductivity basics, BCS theory, Cooper pairs |
| **Materials** | Nb, NbN, NbTiN, high-Tc materials, selection criteria |
| **Josephson Junctions** | Physics, I-V characteristics, types and fabrication |
| **Analog Devices** | SQUIDs, parametric amplifiers, kinetic inductance devices |
| **Digital Logic** | SFQ, RSFQ, ERSFQ, AQFP, circuit design |
| **Fabrication** | Thin films, lithography, process flows |
| **Applications** | Quantum computing, sensors, HPC |

## Repository Structure

```
sce-futures/
├── notebooks/          # Course content (Jupyter notebooks)
│   ├── 01_introduction_superconductivity.ipynb
│   ├── 02_materials_properties.ipynb
│   ├── 03_josephson_junctions.ipynb
│   ├── 04_analog_devices.ipynb
│   ├── 05_digital_logic.ipynb
│   ├── 06_fabrication.ipynb
│   └── 07_applications.ipynb
├── examples/           # Example designs and simulations
└── designs/            # Your work goes here
```

## Getting Started

1. Clone this repository
2. Set up your Python environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -r notebooks/requirements.txt
   ```
3. Launch Jupyter:
   ```bash
   jupyter lab notebooks/
   ```
4. Start with `01_introduction_superconductivity.ipynb`

## Course Overview

| Week | Topics |
|------|--------|
| **1** | Superconductivity fundamentals, materials, Josephson junctions |
| **2** | Analog devices — SQUIDs, amplifiers, sensors |
| **3** | Digital logic — SFQ families, circuit design, simulation |
| **4** | Fabrication, applications, project work |

## Contributing

Internal contributions welcome. Please follow the established notebook format when adding new content.
