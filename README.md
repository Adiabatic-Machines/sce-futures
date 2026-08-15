# SCE Futures: Superconductor Electronics

An instructor-led path from superconductivity fundamentals to devices,
fabrication, cryogenic integration, testing, and accelerator architecture. Each
lecture states its learning objectives, ends with a summary and self-check, and
links directly to the next part of the course.

## What You'll Learn

The course moves from physical principles to complete-system reasoning:

| Module | Topics |
|--------|--------|
| **Fundamentals** | Superconductivity basics, BCS theory, Cooper pairs |
| **Materials** | Nb, NbN, NbTiN, high-Tc materials, selection criteria |
| **Josephson Junctions** | Physics, I-V characteristics, types and fabrication |
| **Analog Devices** | SQUIDs, parametric amplifiers, kinetic inductance devices |
| **Digital Logic** | AQFP design (primary), *SFQ for I/O interfaces |
| **Fabrication** | Thin films, lithography, process flows |
| **Systems** | Packaging, cryogenics, test methodology, equipment selection |
| **Applications** | Sensors, metrology, quantum control, AI workloads and accelerator architecture |

## Repository Structure

```
sce-futures/
├── notebooks/          # Course content (Jupyter notebooks)
│   ├── 00_executive_overview.ipynb
│   ├── 01_introduction_superconductivity.ipynb
│   ├── ...
│   ├── 11_testing.ipynb
│   ├── 11b_test_equipment_vendor_guide.ipynb
│   └── 14_sce_accelerator_architecture.ipynb
├── docs/               # MkDocs home and published assets
├── mkdocs.yml          # Published navigation
└── requirements-docs.txt
```

## Getting Started

1. Clone this repository.
2. Set up your Python environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   python -m pip install -r notebooks/requirements.txt
   ```
3. Launch Jupyter for executable notebooks:
   ```bash
   jupyter lab notebooks/
   ```
4. Start with `00_executive_overview.ipynb`, then follow the previous/next
   links in each lecture.

To preview the published course instead, install `requirements-docs.txt` and
run `python -m mkdocs serve`. MkDocs renders stored notebook outputs; it does
not execute the code cells.

## Course Overview

| Week | Topics |
|------|--------|
| **1** | Superconductivity fundamentals, materials, Josephson junctions |
| **2** | Analog devices — SQUIDs, amplifiers, sensors |
| **3** | Digital logic — AQFP design, *SFQ for I/O (PTL, async FIFOs) |
| **4** | Fabrication, AI accelerator architecture, project work |

## Contributing

Open an issue before changing technical claims, equations, or system-level
comparisons. Contributions should preserve the established objective, summary,
self-check, and navigation pattern. Vendor examples and fast-moving system
numbers must carry their source, date, and evidence state.
