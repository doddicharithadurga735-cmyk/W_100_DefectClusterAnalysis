# W_100_DefectClusterAnalysis

**Data and Analysis for <100> Defect Cluster Stability in Tungsten**

This repository contains the data, analysis scripts, and LAMMPS input files used to investigate the transition kinetics of seventeen <100> defect clusters in tungsten.

## Repository Structure

```text
W_100_DefectClusterAnalysis/
│
├── Data/
│   └── extracted_essential_data.json
│
├── Code/
│   └── FindEms-100.ipynb
│
└── LAMMPS/
    │
    ├── [100]/
    │   └── Trans.in
    │
    └── [Potential]/
        └── [Cluster type]/
            └── [Name]/
                ├── cluster.dat
                └── eq/
                    └── equilibrate.in
```

## Data

```text
Data/
└── extracted_essential_data.json
```

* **`extracted_essential_data.json`**: Combined dataset containing the transition-time data obtained from the isothermal molecular dynamics simulations, including the extended simulation data.

## Code

```text
Code/
└── FindEms-100.ipynb
```

* **`FindEms-100.ipynb`**: Python notebook used to obtain the Arrhenius and Eyring parameters for the investigated <100> defect clusters.

## LAMMPS

The `LAMMPS` directory contains the input files and atomic configuration files required for the molecular dynamics simulations.

### Simulation Input Files

* **`Trans.in`**: LAMMPS input file used to perform isothermal transition simulations for the seventeen <100> defect cluster configurations.

* **`cluster.dat`**: Atomic configuration file representing the embedded <100> defect structures used as input for the NPT molecular dynamics simulations.

* **`equilibrate.in`**: LAMMPS input file used for equilibration of the seventeen <100> defect cluster configurations before the transition simulations.

## Interatomic Potentials

The interatomic potential files used in this study are not redistributed in this repository because we do not hold the copyright or redistribution rights for these potential files. The corresponding sources and references are provided below.

### DND-BN Potential

The DND-BN potential is based on the Derlet--Nguyen-Manh--Dudarev tungsten potential. The original potential is available through OpenKIM:

https://openkim.org/id/EAM_MagneticCubic_DerletNguyenDudarev_2007_W__MO_195478838873_002

The modification of the Derlet potential used for radiation-damage simulations is described by Björkas et al.:

https://www.sciencedirect.com/science/article/abs/pii/S0168583X09007575

### JW Potential

The JW potential used in this study is based on the Ackland--Thetford tungsten potential modified by Juslin and Wirth for radiation-damage simulations. The corresponding publication is available at:

https://doi.org/10.1080/14786435.2010.492248

### M--S Potential

The M--S potential used in this study is the EAM4 tungsten potential developed by Marinica et al. The potential and associated files are available through the NIST Interatomic Potentials Repository:

https://www.ctcms.nist.gov/potentials/entry/2013--Marinica-M-C-Ventelon-L-Gilbert-M-R-et-al--W-4/

The corresponding publication is available at:

https://doi.org/10.1088/0953-8984/25/39/395502
