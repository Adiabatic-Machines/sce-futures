# SCE Futures

SCE Futures builds a working vocabulary for superconducting electronics and
then asks you to use it: explain the mechanism, read the evidence, perform the
calculation, and identify what a device result does—or does not—say about a
complete system.

## Lectures

0. [Why Superconducting Electronics?](notebooks/00_executive_overview.ipynb) - Executive overview

### Part I: Foundations
1. [Introduction to Superconductivity](notebooks/01_introduction_superconductivity.ipynb) - Fundamentals of superconductivity
2. [Materials & Properties](notebooks/02_materials_properties.ipynb) - Superconducting materials and their characteristics
3. [Josephson Junctions](notebooks/03_josephson_junctions.ipynb) - The building blocks of superconducting circuits

### Part II: Devices & Circuits
4. [Analog Devices](notebooks/04_analog_devices.ipynb) - SQUIDs, amplifiers, and sensors
5. [Digital Logic](notebooks/05_digital_logic.ipynb) - AQFP logic and standard cells
6. [Memory & Storage](notebooks/06_memory_storage.ipynb) - Superconducting memory technologies
7. [Circuit Design & Integration](notebooks/07_circuit_design_integration.ipynb) - Design flows and integration
8. [Fabrication](notebooks/08_fabrication.ipynb) - Manufacturing superconducting circuits

### Part III: Systems Integration
9. [Packaging & I/O](notebooks/09_packaging_io.ipynb) - Chip carriers, bonding, wiring, interconnects
10. [Cryogenic Systems](notebooks/10_cryogenic_systems.ipynb) - Cryostats, helium management, and safety
11A. [Testing](notebooks/11_testing.ipynb) - Test methodology, margins, grounding, and measurement practice
11B. [Test Equipment & Vendor Guide](notebooks/11b_test_equipment_vendor_guide.ipynb) - Requirement-driven equipment selection and examples

### Part IV: Applications
12. [Classical Applications](notebooks/12_classical_applications.ipynb) - High-performance computing and beyond
13. [AI Workloads & Dataflow](notebooks/13_ai_workloads_dataflow.ipynb) - Understanding modern ML workloads
14. [SCE Accelerator Architecture](notebooks/14_sce_accelerator_architecture.ipynb) - Hardware architecture for AI acceleration

## Getting Started

To run the notebooks locally, clone the repository and install the dependencies:

```bash
git clone https://github.com/Adiabatic-Machines/sce-futures.git
cd sce-futures
python -m pip install -r notebooks/requirements.txt
jupyter lab
```

Start with Lecture 0 and follow the in-lecture previous/next links. To render
the published course without executing notebook code, install
`requirements-docs.txt` and run `python -m mkdocs serve`.
