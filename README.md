# Crater Geometry and Volume Analysis Using OVITO Python API

## Overview
This repository contains a Python script designed to analyze particle-based simulation data and extract detailed geometric and volumetric properties of craters formed during high-velocity impact events. The code leverages the **OVITO Python API** to process and analyze data, providing insights into crater depth, pileup height, crater axes, and volumetric ratios. 

The script is well-suited for scientific research in material science, condensed matter physics, and impact mechanics.

---

## Features
- **Surface Analysis**:
  - Determines surface atom position using statistical methods (most frequent z-coordinate).
  - Calculates crater depth and pileup height using particle position data.
  
- **Geometric Analysis**:
  - Computes the major and minor axes of the crater using interatomic distances.
  
- **Volumetric Analysis**:
  - Calculates the crater's volume and compares it to the projectile's volume.
  - Computes key ratios such as:
    - Crater-to-Projectile Diameter Ratio.
    - Crater Depth-to-Projectile Diameter Ratio.
    - Crater Volume-to-Projectile Volume Ratio.

- **Results Output**:
  - Results are presented in a JSON format for easy integration with external analysis tools.

---

## How It Works
The script is executed as a Python modifier within the OVITO framework. The workflow is divided into three sequential steps:

1. **Surface Geometry Analysis**:
   - Extracts the surface atom position, crater depth, and pileup height from particle data.
   
2. **Crater Axis Calculation**:
   - Determines the major and minor axes of the crater based on interatomic distances of top-layer atoms.
   
3. **Volume and Ratio Calculations**:
   - Computes the projectile and crater volumes and calculates their ratios along with other geometric metrics.

Each step builds on the results of the previous one, ensuring a logical and cohesive flow of analysis.

## Citation

If you use this script in your research, please cite the following articles:

- [DOI: 10.1016/j.jnucmat.2024.155289](https://doi.org/10.1016/j.jnucmat.2024.155289)
- [DOI: 10.1016/j.jnucmat.2024.155042](https://doi.org/10.1016/j.jnucmat.2024.155042)

## Dependencies
- Python 3.x
- **OVITO Python API** (Available with OVITO Pro or open-source versions)
- NumPy (for numerical computations)
- JSON (for structured results output)

---

## Usage

1. **Setup OVITO**:
   - Install OVITO on your machine ([Download OVITO](https://www.ovito.org/)).
   - Ensure the OVITO Python API is configured in your Python environment.

2. **Run the Script**:
   - Load the script into OVITO's Python Scripting Modifier.
   - Load a particle-based simulation dataset into OVITO.
   - Apply the Python modifier to the dataset.

3. **View Results**:
   - Results such as crater depth, major/minor axes, and volume ratios are printed in the console.
   - JSON-formatted results are displayed for easy integration with other tools.
